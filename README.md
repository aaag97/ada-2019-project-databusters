# How to Survive Eating Out in Chicago


## Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, hospitals, day care facilities, shelters, schools and more, all of which are subject to recurring inspections by The Food Protection Division of the Chicago Department of Public Health.

Our goal for this project is to promote public health in areas of food safety and sanitation and prevent food-borne illness by providing a reliable recommendation system for eating out in Chicago, based on a "safety score" that we will compute using the information from inspections of food establishments in Chicago.

We will also try to link high/low risk areas of contracting food-borne illnesses with the socioeconomic indicators of the different community areas of the city of Chicago to see if there are any patterns, our end goal being to showcase an example of the use of "data science for social good”.

## Research questions

### I. Do facility attributes influence food inspection outcomes for establishments in Chicago?

Our main dataset as well as our secondary datasets give us many attributes for each establishment such as facility type, risk, location and whether it is a chain or not [1](https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html). Which of these attributes contributes the most to food inspection outcomes in Chicago?

### II. Chicago Food Deserts: an indicator of social segreggation?

Many articles seem to point to the fact that different areas in Chicago do not have equal access to healthy food [2](https://chicago.eater.com/2018/12/13/18138387/chicago-magazine-john-kessler-food-scene-racism-immigration-food) [3](https://www.chicagoreporter.com/food-deserts-persist-in-chicago-despite-more-supermarkets/). These articles claim that this is due to the persistence of racial segreggation. Our aim is to inspect this further and see whether our dataset could help in seeing if this is true.

### III. The survival guide: a personalized guide for eating out safely

This represent the conclusion to our findings. The aim is to design an interactive interface where the user can enter some data about themself such as allergies and they could get the safest establishments for them to eat at.

## Datasets

#### Chicago Food Inspections Dataset
We chose the _Chicago Food Inspections_ dataset from the given datasets. It contains information about food inspections of different establishments in Chicago from January 1, 2010 to the present. We will use it as our main dataset for the project and it can be downloaded either as a JSON file _socrata\_metadata.json (9.14 KB)_  or a CSV file _food-inspections.csv (219.71 MB)_ from [4](https://www.kaggle.com/chicago/chicago-food-inspections) (In addition to that source, you can check for the main source dataset on Chicago Data Portal [5](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb)). More information about the attributes in the Chicago Food Inspections' dataset can be found on [6](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF).

#### Socioeconomic Indicator Dataset 
As we mentioned in our last research question, we need a Socioeconomic Indicator Dataset in order to make an inference about the influence of the location of a facility on its food inspection outcomes in Chicago. To that end, we will be using _census-data-selected-socioeconomic-indicators-in-chicago-2008-2012.csv (364 KB)_ [7](https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2). It contains six socioeconomic indicators of public health quality and a hardship index, for each Chicago community area, for the years 2008-2012.

## APIs

#### Yelp Fusion
Yelp is a business directory service and crowd-sourced review forum. 
Alongside our main dataset, we will be using the Yelp Fusion API, [8](https://www.yelp.com/developers/documentation/v3). This is a collection of endpoints developers can reach to get information on establishment. It has been made available to use for personal, educational, and academic purposes. To support our research questions, we will be using:

- **Business Match Endpoint**: Lets us match business data from other sources against businesses on Yelp, based on provided business information. 
- **Business Details**: Given the id of any establishment obtained from the Business Match Endpoint, this returns details like price range, rating, and cuisine. 


## A list of internal milestones up until project milestone 2

#### Clean primary dataset (November 10th)

* Explore features
* Drop features which are irrelevant to our research questions
* Clean each column in the dataset
    * Try to reduce the number of unique values for each column through clustering
    * Find ways to fill missing values

#### Come up with a data story (November 20th)

* Plot different features and examine their distribution and correlations
* Cluster thematically close questions together and modify README to reflect evolution of ideas
* Finalize list of secondary datasets to use to answer research questions
* Divide secondary dataset management among group members
* Conduct cleaning process on secondary datasets

## A list of internal milestones up until project milestone 3

#### Answer research questions on primary dataset (December 3rd)

* Divide questions among group members
* Answer the research questions using all resulting datasets and analysis from milestone 2
* Come up with insightful responses to questions
* Peer review after all the group members have finished writing their responses

#### Putting it all together (December 13th)

* Finalize structure of data story after gathering all responses found
* Divide tasks for data story construction among group members
* Put together data story
* Final peer review regarding the different parts each group member was responsible for
* Test data story to detect bugs and errors
* Fix errors and bugs
* Test and finalize data story
    
## Resources
[1] https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html <br/>
[2] https://chicago.eater.com/2018/12/13/18138387/chicago-magazine-john-kessler-food-scene-racism-immigration-food <br/>
[3] https://www.chicagoreporter.com/food-deserts-persist-in-chicago-despite-more-supermarkets/ <br/>
[4] https://www.kaggle.com/chicago/chicago-food-inspections <br/>
[5] https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb <br/>
[6] https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF <br/>
[7] https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2 <br/>
[8] https://www.yelp.com/developers/documentation/v3 <br/>