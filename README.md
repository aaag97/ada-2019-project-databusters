# How to Survive Eating Out in Chicago


## Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, hospitals, day care facilities, shelters, schools and more, all of which are subject to recurring inspections by The Food Protection Division of the Chicago Department of Public Health.

Our goal for this project is to promote public health in areas of food safety and sanitation and prevent food-borne illness by providing a reliable recommendation system for eating out in Chicago, based on a "safety score" that we will compute using the information from inspections of food establishments in Chicago.

We will also try to link high/low risk areas of contracting food-borne illnesses with the socioeconomic indicators of the different community areas of the city of Chicago to see if there are any patterns, our end goal being to showcase an example of the use of "data science for social good”.

## Research questions

#### How does the performance of establishments evolve through time as a function of its inspections results?

#### Does the type of a given facility influence the outcome of its inspection?
>Moreover, how homogenous is the sanitary status of facilities which belong to a given type? Also, what are the most common violations? Are there violations which typically happen in most facilities which fail inspections? Or do they depend on another factor such as establishment type or location?

#### Is the food safety of an establishment related to its popularity?
>With the increasing popularity of social media, customers are very keen to comment on their experiences at those establishments. Would it be possible to infer the safety status of those facilities from the customers’ reviews? That question leads us hence to investigate whether an inspection failure is more likely to occur for an establishment which has below-average reviews. Moreover, we could ask whether an inspection caused by a customer complaint is more likely to result in a failure than a regular inspection. Finally, in terms of restaurants, chains (e.g. McDonald's) are often considered more popular than local restaurants. We encountered some news about the _McDonald's Cyclospora Outbreak_ [1](https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html). This lead us to think about whether chains might be riskier to eat at compared to local facilities? Or are they more likely to get complaints which increases the frequency and the severity of their inspections?

#### Does the cuisine of a restaurant influence the inspection outcome?

#### Is there a relationship between the inspection outcome of a facility and its location?
>Does the area of a given facility influence its inspection results? For example, typically, big cities are comprised of "bad" neighborhoods. If a restaurant is in such a neighborhood, is it more likely to fail its inspection? Another way to evaluate this is to compare the latest inspection outcomes on a map of Chicago with a map specifying the food safety levels in the city.

#### What customers say about a restaurant is also the same for an inspection result?
>By using Yelp dataset, we will investigate if there exists a correlation between the reviews (in terms of sentiment analysis) and inspection results. 

## Datasets

#### Chicago Food Inspections Dataset
We chose the _Chicago Food Inspections_ dataset from the given datasets. It contains information about food inspections of different establishments in Chicago from January 1, 2010 to the present. We will use it as our main dataset for the project and it can be downloaded either as a JSON file _socrata\_metadata.json (9.14 KB)_  or a CSV file _food-inspections.csv (219.71 MB)_ from [2](https://www.kaggle.com/chicago/chicago-food-inspections) (In addition to that source, you can check for the main source dataset on Chicago Data Portal [3](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb)). More information about the attributes in the Chicago Food Inspections' dataset can be found on [4](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF).

#### Socioeconomic Indicator Dataset 
As we mentioned in our last research question, we need a Socioeconomic Indicator Dataset in order to make an inference about the influence of the location of a facility on its food inspection outcomes in Chicago. To that end, we will be using _census-data-selected-socioeconomic-indicators-in-chicago-2008-2012.csv (364 KB)_ [6](https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2). It contains six socioeconomic indicators of public health quality and a hardship index, for each Chicago community area, for the years 2008-2012.

#### Foodborne Illnesses Dataset
To enrich our resources, we will additionally be doing some webscraping on [Yelp](https://www.yelp.com) and [iwaspoisoned.com](iwaspoisoned.com) to prepare a dataset for food related illnesses by searching for users' complaints.

## APIs

#### Yelp Fusion
Yelp is a business directory service and crowd-sourced review forum. 
Alongside our main dataset, we will be using the Yelp Fusion API, [5](https://www.yelp.com/developers/documentation/v3). This is a collection of endpoints developers can reach to get information on establishment. It has been made available to use for personal, educational, and academic purposes. To support our research questions, we will be using:

- **Business Match Endpoint**: Lets us match business data from other sources against businesses on Yelp, based on provided business information. 
- **Business Details**: Given the id of any establishment obtained from the Business Match Endpoint, this returns details like price range, rating, and cuisine. 


## A list of internal milestones up until project milestone 2
#### Clean primary dataset (November 7th)
 
* Explore features
* Do webscraping to gather reviews on foodborne illnesses
* Drop features which are irrelevant to our research questions
* Plot different features at year level and at facility name level
* Detect and drop outliers through plotted figures

#### Come up with a data story (November 7th)

* Cluster thematically close questions together
* Organize the structure of the data story from the different cluster of questions obtained, making sure it starts with questions regarding the primary dataset

#### Answer research questions on primary dataset (November 14th)

* Divide questions among group members
* Conduct the primary dataset analysis to answer the research questions which don't involve secondary datasets
* Come up with insightful responses to questions
* Peer review after all the group members have finished writing their responses

#### Combine primary dataset with secondary datasets (November 21st)

* Finalize list of secondary datasets to use to answer research questions
* Divide secondary dataset management among group members
* Conduct cleaning process on secondary datasets
* Divide remaining research questions
* Conduct further data analysis to answer remaining research questions
* Peer review after all group members have finished writing responses.

#### Putting it all together (December 10th)

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
* Although we searched thoroughly for a dataset containing food-borne illnesses in Chicago, we could not find such a dataset. We have only managed to find [this](https://wwwn.cdc.gov/norsdashboard/) dataset which contains information regarding food-borne illnesses by state on the scale of the USA. If you have such a dataset or if you have suggestions regarding where we could find it, would it possible to let us know?
    
## Resources
[1] https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html <br/>
[2] https://www.kaggle.com/chicago/chicago-food-inspections <br/>
[3] https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb <br/>
[4] https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF <br/>
[5] https://www.yelp.com/developers/documentation/v3 <br/>
[6] https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2
