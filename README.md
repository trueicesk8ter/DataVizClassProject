# DataVisualization Class Project

## Data

The data I propose to visualize for my project is a sample of 200 Defensive Asylum Cases as they progress through the immigration court system.	

[Department of Justice: EOIR CASE Dataset](https://www.justice.gov/eoir/foia-library-0) (EOIR CASE-- Warning if you download its large!)	

Here is the [Key code for the full dataset, marked with what data I used in this dataset](https://drive.google.com/file/d/19RFlM9sRa9uE3c7HBLK_lRiWs6eF9c7U/view?usp=sharing)	

Data Description:	
This dataset is a sample of 200 cases that have processed through the United States immigration court system seeking defensive asylum in the last ~ 10 years (2010-2019). This dataset covers information about the case and their time in different parts of the immigration court process through data about their case proceedings, scheudled hearings and the judges that have heard their cases. Some variables that are of particular intrested may be the DEC_CODE which represents the outcome of the case. 	

## Prototypes

I’ve created a proof of concept visualization of this data. It's a scatterplot and it shows the count of unique cases based on the date the asylum applications was recieved. The color corresponds with the decision of the application. Hoevering over each dot will show the total count of the cases. 

[![image](https://user-images.githubusercontent.com/68416/65240758-9ef6c980-daff-11e9-9ffa-e35fc62683d2.png)](https://beta.vizhub.com/curran/eab039ad1765433cb51aad167d9deae4)

(please put a screenshot of one or more visualizations of this dataset you already made, for previous assignments)

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * What is the relationship between case decision and how long they spend in the system? Is there a correlation with decision type and length it takes for a case to be processed?
 * How long do cases take to complete the entire legal process?
 * What is the split in the Nationality?
 * Is there any realtionship between Nationality and how long cases take to complete the entire legal process?
 * What is the number of workload/cases per judge?	
 * Is there a relationship between custody of the individual and their time in the system? (Do detained cases take less time?)
 * What is the realtionship between the overall case decision code and the asylum application code?

## Sketches

(insert one or more hand-drawn sketches of interactive visualizations that you imagine)
(describe each sketch - how is the data visualized, what are the interactions, and how do these relate to the questions/tasks)

## Open Questions

(describe any fear, uncertainty, or doubt you’re having about the feasibility of implementing the sketched system. For example, “I’m not sure where to get the geographic shapes to build a map from this data” or “I don’t know how to resolve the codes to meaningful names” … Feel free to delete this section if you’re confident.)
