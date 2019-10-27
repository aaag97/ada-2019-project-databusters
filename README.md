# How to survive eating out in Chicago

## Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, hospitals, day care facilities, shelters, schools and more, all of which are subject to recurring inspections by The Food Protection Division of the Chicago Department of Public Health.

Our goal for this project is to promote public health in areas of food safety and sanitation and prevent food-borne illness by providing a reliable recommendation system for eating out in Chicago, based on a "safety score" that we will compute using the information from inspections of food establishments in Chicago.

We will also try to link high/ low risk areas of contracting food-borne illnesses with the socioeconomic indicators of the different community areas of the city of Chicago to see if there are any patterns, our  end goal being to showcase an example of the use of "data science for social good”.

## Research questions

- **Is the food safety of an establishment related to its popularity?** With an increasing effect of social media, customers are very keen to comment on their experiences at those establishments. Would it be true to infer the safety of those places from the customers’ reviews? That question would lead us to also investigate whether an inspection failure occurs after a negative review is given to an establishment and whether an inspection caused by a customer complaint is more likely to result in a failure over a regular inspection?

- **Does the cuisine influence the inspection outcome?** There are different types of establishments that are placed in the city of Chicago like elsewhere in the world. Is their unique cuisine affecting their sanitary check/inspection result? Are their failures resulted from the same causes or not? Would food chains be riskier to eat at compared to local facilities?

- **How does the performance of establishments evolve through time as a function of inspections results?** Facilities are subject to inspection on a regular basis in terms of some health and sanitary criteria. We will examine how the inspection results vary depending on previous results. As many other triggers, socioeconomic factors might also influence the outcome of an inspection. In that sense, we will examine the highly risky facilities by observing a map showcasing the food safety levels in Chicago and analyzing assessing a possible relationship between those levels and the previously stated factors.

## Datasets

#### **Main dataset of Inspections of restaurants and other food establishments in Chicago**
We chose the `Chicago Food Inspections` dataset from the sugested datasets which contains information from inspections of restaurants and other food establishments in Chicago from January 1, 2010 to the present. We will use it as our main dataset for our project and it can be downloaded either as _socrata_metadata.json (9.14 KB)_ or _food-inspections.csv (219.71 MB)_ from [1](https://www.kaggle.com/chicago/chicago-food-inspections) (Also check for the main source dataset on Chicago Data Portal [2] 
[![Visit the website](https://github.com/aaag97/ada-2019-project-databusters/blob/master/chicagodp.png)](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb).

We will also enrich this dataset with some other datasets:  


(Je mets juste ces sources qui peuvent etre interessantes)
- https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF
- Note about 7/1/2018 change to food inspection procedures that affects the data in this dataset: http://bit.ly/2yWd2JB

## A list of internal milestones up until project milestone 2
1. Clean primary dataset (November 7th)
 
    * Explore features
    * Drop features which are irrelevant to our research questions
    * Plot different features at year level and at facility name level
    * Detect and drop outliers through plotted figures

2. Come up with a data story (November 7th)

    * Cluster thematically close questions together
    * Organize the structure of the data story from the different cluster of questions obtained, making sure it starts with questions regarding the primary dataset

3. Answer research questions on primary dataset (November 14th)

    * Divide questions among group members
    * Conduct the primary dataset analysis to answer the research questions which don't involve secondary datasets
    * Come up with insightful responses to questions
    * Peer review after all the group members have finished writing their responses

4. Combine primary dataset with secondary datasets (November 21st)

    * Finalize list of secondary datasets to use to answer research questions
    * Divide secondary dataset management among group members
    * Conduct cleaning process on secondary datasets
    * Divide remaining research questions
    * Conduct further data analysis to answer remaining research questions
    * Peer review after all group members have finished writing responses.

5. Putting it all together (December 10th)

    * Finalize structure of data story after gathering all responses found
    * Divide tasks for data story construction among group members
    * Put together data story
    * Final peer review regarding the different parts each group member was responsible for
    * Test data story to detect bugs and errors
    * Fix errors and bugs
    * Test and finalize data story


## Questions for TAs
* Will we have TA support when it comes to constructing the data story (e.g. front-end etc)?
* Is there any resource for datasets or API you could recommend for the following? We have found some datasets for them but were wondering if you would like to suggest something better/more reliable.
    * Healthcare data (in particular food poisoning data in the USA)
    * Popularity and cost of restaurants in Chicago (more generally in the USA)
    
## Resources
[1] https://www.kaggle.com/chicago/chicago-food-inspections
[2] https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb
