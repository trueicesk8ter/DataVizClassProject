# DataVisualization Class Project

## Data

The data I used to visualize for my project is a sample of 200 defensive asylum cases as they progress through the immigration court system.	

[Department of Justice: EOIR CASE Dataset](https://www.justice.gov/eoir/foia-library-0) (EOIR CASE-- Warning if you download its large!)	

Here is the [Key code for the full dataset, marked with what data I used in this dataset](https://drive.google.com/file/d/19RFlM9sRa9uE3c7HBLK_lRiWs6eF9c7U/view?usp=sharing)	

Data Description:	
This [dataset](https://gist.github.com/trueicesk8ter/4d284843bed8a1e318eac8fc672b53d4) is a sample of 200 cases that have processed through the United States immigration court system seeking defensive asylum in the last 10 years (2010-2019). This dataset covers information about the case and their time in different parts of the immigration court process. Data includes information about their case proceedings, scheduled hearings and the judges that have heard their cases. One variable that is of particular interest is the DEC_CODE which represents the outcome of the case. 	

## Step 1: Create Drawn Prototypes and Sketches

First I created a proof of concept visualization for this data in the form of a scatterplot. The scatter plot shows the count of unique cases based on the date the asylum applications was received. The color corresponds with the decision of the application. Hovering over each dot will show the total count of the cases. 
[![image](https://user-images.githubusercontent.com/12132049/94341688-5c50b280-ffd9-11ea-8ab6-680e1043de53.png)
](https://vizhub.com/trueicesk8ter/98b317412ae745c1b19209fdd5c254bc?file=README.md)

#### Applications for Asylum Cases Scatter Plot: Examining the relationship between the date asylum applications were received and the total number of cases and decision of the cases (*This sketch is realized and shown above*)
![image](https://user-images.githubusercontent.com/12132049/94341953-b488b400-ffdb-11ea-8478-947f481de6d3.png)

  * The data is visualized by creating a scatterplot where it shows the count of unique cases based on the date the asylum applications were received. This requires the use of an aggregation function to count the total cases that have the same application date. The categorical variable of "case decision" is depicted using color. The interactive part is demonstrated by hovering over each dot, which will show the total count of the cases. This helps to answer the question "what is the relationship between the overall case decision code and the asylum application code?".

#### Varying Year Scatter Plot: Examining the relationship between date of entry to system, wait-time and decision of the case
![image](https://user-images.githubusercontent.com/12132049/94341970-daae5400-ffdb-11ea-8f1a-50cd2b2d601c.png)

  * The data in this sketch required the use of a basic scatterplot to show the date of entrance to the system and the time it took to exit the system (wait time) and the decision of the case. In order to realize this sketch, the variable "wait-time" had to be calculated which is the difference in days between the date a case exited the system to when they entered the system. The basic outline of this sketch had a similar basic structure to the realized above for the application date and number of cases. However, the difficulty in producing this sketch was adding a drop-down menu that selects the specific year of the date of entry and then changing the x-axis changes to show the 12 months in that year plotted. This sketch is realized in the final visualization shown below in step 3. 


## Step 2: Questions & Tasks to answer

The following tasks and questions were what drove the visualization and interaction decisions for this project:
* What is the relationship between case decision and how long they spend in the system? Is there a correlation with decision type and length it takes for a case to be processed?
 * How long do cases take to complete the entire legal process?
 * What is the split in nationality for these cases?
 * Is there any relationship between nationality and how long cases take to complete the entire legal process?
 * What is the relationship between the overall case decision code and the asylum case wait time?



## Step 3: Final Visualization
The final visualization can be found [here](https://vizhub.com/trueicesk8ter/e7f6582ae1f243c1be02bec204523c45)

<img width="719" alt="FinalVisual" src="https://user-images.githubusercontent.com/12132049/97751670-0d5ed700-1ac9-11eb-9340-38613b9d7029.png">


### Highlights of Visualization
 
There are many aspects of this final visualization such as the ability to filter data by year (dropdown menu) or select a subset of the data to get a closer look at in the 3 mini plots (brushing effect). 

* The first highlight is the addition of 3 mini barplots that show more information about the selected data. 
The first plot shows frequency of wait times for cases selected. The second shows the frequency by month the case entered the system. The final shows the frequency of cases by nationality. 
<img width="708" alt="3MiniPlots" src="https://user-images.githubusercontent.com/12132049/97748404-d4703380-1ac3-11eb-83d0-37843ec14741.PNG">



* The second highlight demonstrates what happens when there is no data for either the dropdown menu and or when an area is brushed and there is no data in that region. 
<img width="721" alt="NoData_Brushed_2" src="https://user-images.githubusercontent.com/12132049/97748447-e225b900-1ac3-11eb-9159-26fa3bae400a.png">
<img width="793" alt="NoData_1" src="https://user-images.githubusercontent.com/12132049/97748454-e3ef7c80-1ac3-11eb-81fe-80cc6fd7dd9b.png">

* The third and final highlight demonstrates what is my favorite part of this visualization which highlights in the color corresponding to the decision code that is hovered on the left hand side. Not only is the point in the main scatterplot highlighted, but in addition the bar that corresponds to the hovered data is highlighted in the 3 mini bar plots below. 
<img width="791" alt="Hover_color" src="https://user-images.githubusercontent.com/12132049/97748338-b276b100-1ac3-11eb-89d5-d226f518fdf2.png">

## Future Work
 I was able to complete everything I hoped to, however there are a few things in the future I would like to change/add to make improve this visualization. 
 * Add a 2D brushing effect to be able to brush in both the X and Y direction
 * Potentially add more mini plots to the body that can show more information about the data

