# How to survive eating out in Chicago

# Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, hospitals, day care facilities, shelters, schools and more.
All of which are subject to recurring inspections by The Food Protection Division of the Chicago Department of Public Health.

Our goal for this project is to promote public health in areas of food safety and sanitation and prevent food-borne illness by providing a reliable recommendation system for eating out in Chicago, based on a "safety score" that we will compute using the informations from inspections of food establishments in Chicago.

We will also try to link high/ low risk areas of contracting food-borne illnesses with the socioeconomic indicators of the different community areas of the city of Chicago to see if there are any patterns, our end goal being to use “Data science for social good”.

# Research questions
A list of research questions you would like to address during the project. 

# Dataset
List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant.

(Je mets juste ces sources qui peuvent etre interessantes)
- https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF
- Note about 7/1/2018 change to food inspection procedures that affects the data in this dataset: http://bit.ly/2yWd2JB

# A list of internal milestones up until project milestone 2
1. Clean primary dataset 
 
    * Explore features
    * Drop features which are irrelevant to our research questions
    * Plot different features at year level and at facility name level
    * Detect and drop outliers through plotted figures

1. Come up with a data story

    * Cluster thematically close questions together
    * Organize the structure of the data story from the different cluster of questions obtained, making sure it starts with questions regarding the primary dataset

1. Answer research questions on primary dataset

    * Divide questions among group members
    * Conduct the primary dataset analysis to answer the research questions which don't involve secondary datasets
    * Come up with insightful responses to questions
    * Peer review after all the group members have finished writing their responses

1. Combine primary dataset with secondary datasets

    * Finalize list of secondary datasets to use to answer research questions
    * Divide secondary dataset management among group members
    * Conduct cleaning process on secondary datasets
    * Divide remaining research questions
    * Conduct further data analysis to answer remaining research questions
    * Peer review after all group members have finished writing responses.

1. Putting it all together

    * Finalize structure of data story after gathering all responses found
    * Divide tasks for data story construction among group members
    * Put together data story
    * Final peer review regarding the different parts each group member was responsible for
    * Test data story to detect bugs and errors
    * Fix errors and bugs
    * Test and finalize data story


# Questions for TAa
* How flexible is the project? Would it be possible to change the research questions later on if we find more interesting questions or if we encounter a dead end when trying to answer one of the questions?
* Will we have TA support when it comes to constructing the data story (e.g. front end etc)?
* Is there any resource for datasets or API you could recommend for the following? We have found some datasets for them but were wondering if you would like to suggest something better/more reliable.
    * Healthcare data (in particular food poisoning data in the USA)
    * Popularity of restaurants in the USA
    * Cost of restaurants in the USA
