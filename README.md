# DataVisualization Class Project

## Data

The data I propose to visualize for my project is a sample of 200 Defensive Asylum Cases as they progress through the immigration court system.	

[Department of Justice: EOIR CASE Dataset](https://www.justice.gov/eoir/foia-library-0) (EOIR CASE-- Warning if you download its large!)	

Here is the [Key code for the full dataset, marked with what data I used in this dataset](https://drive.google.com/file/d/19RFlM9sRa9uE3c7HBLK_lRiWs6eF9c7U/view?usp=sharing)	

Data Description:	
This dataset is a sample of 200 cases that have processed through the United States immigration court system seeking defensive asylum in the last ~ 10 years (2010-2019). This dataset covers information about the case and their time in different parts of the immigration court process through data about their case proceedings, scheduled hearings and the judges that have heard their cases. Some variables that are of particular interested may be the DEC_CODE which represents the outcome of the case. 	

## Prototypes

I’ve created a proof of concept visualization of this data. It's a scatterplot and it shows the count of unique cases based on the date the asylum applications was received. The color corresponds with the decision of the application. Hovering over each dot will show the total count of the cases. 

[![image](https://user-images.githubusercontent.com/12132049/94341688-5c50b280-ffd9-11ea-8ab6-680e1043de53.png)
](https://vizhub.com/trueicesk8ter/98b317412ae745c1b19209fdd5c254bc?file=README.md)


## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * What is the relationship between case decision and how long they spend in the system? Is there a correlation with decision type and length it takes for a case to be processed?
 * How long do cases take to complete the entire legal process?
 * What is the split in the Nationality?
 * Is there any relationship between Nationality and how long cases take to complete the entire legal process?
 * What is the number of workload/cases per judge?	
 * Is there a relationship between custody of the individual and their time in the system? (Do detained cases take less time?)
 * What is the relationship between the overall case decision code and the asylum application code?

## Sketches
For this project I have envisioned some different directions as seen below in my sketches.

#### Applications for Asylum Cases Scatter Plot: Examining the relationship between the date asylum applications were received and the total number of cases and decision of the cases( * This sketch is realized and show above*)
  * The data is visualized by creating a scatterplot where it shows the count of unique cases based on the date the asylum applications was received. This requires(ed) the used of aggregation function to count the total cases with the same application date. The categorical variable of "case decision" is depicted using color. The interactive part is demonstrated by hovering over each dot will show the total count of the cases. This helps to answer the question "What is the relationship between the overall case decision code and the asylum application code?".

#### Varying Year Scatter Plot: Examining the relationship between date of entry to system, wait-time and decision of the case
  * The data in this sketch requires the use of a basic scatterplot to show the date of entrance to the system and the time it takes to exit the system (wait time) and the decision of the case. In order to realize this sketch the variable "wait-time" must be calculated which is the difference in days between the date a case exited the system to when they entered the system. The basic outline of this sketch has a similar basic structure to the one already realized above for the application date and number of cases, however, the difficulty in producing this sketch will come in creating a drop-down menu that selects the specific year of the date of entry and the x-axis changes to show the 12 months in that year plotted. This sketch once realized would help to answer the questions around how the time in the system relates to when they entered the system. In addition, there is possibility to add another drop down menu to selected other variables to compare in a similar manner such as looking at the nationality and how long a case took to complete and what the decision of that code was. 


## Open Questions

  * Some fears and uncertainty I have in realizing the sketch above is the incorporation of the drop down menu. Not only do I need to create a drop down menu, but I need to make the option for the drop down menu based on a created variable "year" and then making the axis to display in months. I am unsure how I will incorporate the drop-down menu. I have tried a few times, already without luck so the question for me really is what is the best way to do this? Should I use react and d3 or try to use VegaLite?
