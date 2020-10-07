# DataVisualization Class Project

## Data

The data I propose to visualize for my project is a sample of 200 defensive asylum cases as they progress through the immigration court system.	

[Department of Justice: EOIR CASE Dataset](https://www.justice.gov/eoir/foia-library-0) (EOIR CASE-- Warning if you download its large!)	

Here is the [Key code for the full dataset, marked with what data I used in this dataset](https://drive.google.com/file/d/19RFlM9sRa9uE3c7HBLK_lRiWs6eF9c7U/view?usp=sharing)	

Data Description:	
This [dataset](https://gist.github.com/trueicesk8ter/4d284843bed8a1e318eac8fc672b53d4) is a sample of 200 cases that have processed through the United States immigration court system seeking defensive asylum in the last 10 years (2010-2019). This dataset covers information about the case and their time in different parts of the immigration court process. Data includes information about their case proceedings, scheduled hearings and the judges that have heard their cases. One variable that is of particular interest is the DEC_CODE which represents the outcome of the case. 	

## Prototypes

I’ve created a proof of concept visualization for this data in the form of a scatterplot. The scatter plot shows the count of unique cases based on the date the asylum applications was received. The color corresponds with the decision of the application. Hovering over each dot will show the total count of the cases. 
[![image](https://user-images.githubusercontent.com/12132049/94341688-5c50b280-ffd9-11ea-8ab6-680e1043de53.png)
](https://vizhub.com/trueicesk8ter/98b317412ae745c1b19209fdd5c254bc?file=README.md)

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:
* What is the relationship between case decision and how long they spend in the system? Is there a correlation with decision type and length it takes for a case to be processed?
 * How long do cases take to complete the entire legal process?
 * What is the split in nationality for these cases?
 * Is there any relationship between nationality and how long cases take to complete the entire legal process?
 * Is there a relationship between custody of the individual and their time in the system? Do detained cases take less time?
 * What is the relationship between the overall case decision code and the asylum case wait time?

## Sketches
For this project I have envisioned some different directions as seen below in my sketches.
#### Applications for Asylum Cases Scatter Plot: Examining the relationship between the date asylum applications were received and the total number of cases and decision of the cases (*This sketch is realized and shown above*)
![image](https://user-images.githubusercontent.com/12132049/94341953-b488b400-ffdb-11ea-8478-947f481de6d3.png)

  * The data is visualized by creating a scatterplot where it shows the count of unique cases based on the date the asylum applications were received. This requires the use of an aggregation function to count the total cases that have the same application date. The categorical variable of "case decision" is depicted using color. The interactive part is demonstrated by hovering over each dot, which will show the total count of the cases. This helps to answer the question "what is the relationship between the overall case decision code and the asylum application code?".

#### Varying Year Scatter Plot: Examining the relationship between date of entry to system, wait-time and decision of the case
![image](https://user-images.githubusercontent.com/12132049/94341970-daae5400-ffdb-11ea-8f1a-50cd2b2d601c.png)

  * The data in this sketch requires the use of a basic scatterplot to show the date of entrance to the system and the time it takes to exit the system (wait time) and the decision of the case. In order to realize this sketch, the variable "wait-time" must be calculated which is the difference in days between the date a case exited the system to when they entered the system. The basic outline of this sketch has a similar basic structure to the one already realized above for the application date and number of cases. However, the difficulty in producing this sketch will come in creating a drop-down menu that selects the specific year of the date of entry and the x-axis changes to show the 12 months in that year plotted. This sketch once realized would help to answer the questions around how the time in the system relates to when they entered the system. In addition, there is possibility to add another drop down menu to select other variables to compare in a similar manner such as looking at the nationality and how long a case took to complete and what the decision of that code was. 

## Ideas for Interaction
My data is complex. There are many different aspects of a case’s time through the system that would be of interest to the end-user, as seen above in my list of “Questions & Tasks”.  Adding interaction to this visualization would increase the usefulness of my final visualization as one visualization with the use of interaction could end up helping to answer most of these questions. 
One interaction sticks out at as being the best choice in this case: the use of a cross filter. This cross filter would allow the end-user to “brush” over different aspects of the cases such as “wait-times”. If the end-user brushed over a region of “wait-times” that seemed to be large, the rest of the visualization would filter and show the rest of the displayed graphs in relation to this selected filter. The sketch below demonstrates what the final product might look like. 
![image](https://user-images.githubusercontent.com/12132049/95381311-f9eb9200-08b5-11eb-9235-69ff64764e35.png)


## Schedule of Deliverables
### Week of 10/7-10/14
* Create frequency bar plot of wait-times in days, month of entry and nationality (these will eventually be our data displays).

### Week of 10/15-10/21
* Learn how to add a cross filter to data (research).
* Try and implement the brushing effect on our [main plot](https://vizhub.com/trueicesk8ter/98b317412ae745c1b19209fdd5c254bc).

### Week of 10/22-10/28
* Combine main plot with the three other display plots created during week 10/7-10/14 into a single display.
* Start trying to implement the cross filter on the main plot to filter the subplots.
### Week of 10/29-11/04
* Finalize the cross filter and have it working properly.
* Make any adjustment to the display to make it visually pretty.
* Celebrate on a job well done!

## Open Questions
  * Some fears and uncertainty I have in realizing the sketches above is the incorporation of the drop-down menu. Not only do I need to create a drop-down menu, but I need to make the option for the drop-down menu based on a created variable "year" and then make this new axis display in months for the selected year. I am unsure how I will incorporate the drop-down menu. I have tried a few times, already without luck so the question for me really is what is the best way to do this? Should I use react and d3 or try to use VegaLite?
* Another concern is the timeline provided above in the schedule of deliverables. As with learning anything new, sometimes things take longer than expected. I am hopeful I will have as “few” hiccups as possible while trying to produce my final project.



