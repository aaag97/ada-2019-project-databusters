# How to survive eating out in Chicago

## Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, hospitals, day care facilities, shelters, schools and more, all of which are subject to recurring inspections by The Food Protection Division of the Chicago Department of Public Health.

Our goal for this project is to promote public health in areas of food safety and sanitation and prevent food-borne illness by providing a reliable recommendation system for eating out in Chicago, based on a "safety score" that we will compute using the information from inspections of food establishments in Chicago.

We will also try to link high/ low risk areas of contracting food-borne illnesses with the socioeconomic indicators of the different community areas of the city of Chicago to see if there are any patterns, our  end goal being to showcase an example of the use of "data science for social good”.

## Research questions

- **Is the food safety of an establishment related to its popularity?** With an increasing effect of social media, customers are very keen to comment on their experiences at those establishments. Would it be true to infer the safety of those places from the customers’ reviews? That question would lead us to also investigate whether an inspection failure occurs after a negative review is given to an establishment and whether an inspection caused by a customer complaint is more likely to result in a failure over a regular inspection?

- **Does the cuisine influence the inspection outcome?** There are different types of establishments that are placed in the city of Chicago like elsewhere in the world. Is their unique cuisine affecting their sanitary check/inspection result? Are their failures resulted from the same causes or not? We encountered with a news about _mcdonalds-cyclospora-outbreak_ [1](https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html), and we ask that would food chains be riskier to eat at compared to local facilities? 

- **How does the performance of establishments evolve through time as a function of its inspections results?** Facilities are subject to inspection on a regular basis in terms of some health and sanitary criteria. We will examine how the inspection results vary depending on previous results. As many other triggers, socioeconomic factors might also be a reason of failure on an inspection. In that sense, we will examine the highly risky facilities by observing a map showcasing the food safety levels in Chicago and analyzing assessing a possible relationship between those levels and the previously states factors.

## Datasets
List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant.

#### Chicago Food Inspections Dataset
We chose the `Chicago Food Inspections` dataset from given datasets which contains information from inspections of restaurants and other food establishments in Chicago from January 1, 2010 to the present. We will use it as our main dataset for our project and it can be downloaded either as _socrata_metadata.json (9.14 KB)_ or _food-inspections.csv (219.71 MB)_ from [2](https://www.kaggle.com/chicago/chicago-food-inspections) (In addition to that source, you can check for the main source dataset on Chicago Data Portal [3](https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb)). In order to have more information about the attributes in the Chicago Food Inspections' dataset please visit [4](https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF).


#### Yelp Open Dataset
First of all, for whom does not know what is Yelp, it is a business directory service and crowd-sourced review forum. 
As well as our main dataset, we will also use `Yelp Open` dataset, [5](https://www.yelp.com/dataset), which is a subset of its businesses, reviews, and user data for use in personal, educational, and academic purposes so as to support our research questions based on clients' satisfaction in different food establishments in Chicago.  
It consists as of:
- `business.json`: Contains business data including location data, attributes, and categories.
- `review.json`: Contains full review text data including the user_id that wrote the review and the business_id the review is written for.
- `user.json`: User data including the user's friend mapping and all the metadata associated with the user.
- `checkin.json`: Checkins on a business.
- `tip.json`: Tips written by a user on a business. Tips are shorter than reviews and tend to convey quick suggestions.
- `photo.json`: Contains photo data including the caption and classification (one of "food", "drink", "menu", "inside" or "outside").


#### Socioeconomic indicators Dataset 
As we precised in the last item of our research questions above, we need a socioeconomic indicators dataset to make an inference about its influence on food inspections in Chicago. For that reason, we will use _census-data-selected-socioeconomic-indicators-in-chicago-2008-2012.csv (364 KB)_ [6](https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2) which contains a selection of six socioeconomic indicators of public health significance and a hardship index, by Chicago community area, for the years 2008-2012.  


#### Foodborne illnesses Dataset
For enriching our resources, we will additionally do webscraping on `yelp.com` and `iwaspoisoned.com` to prepare a dataset for food related outbreaks by searching for users' reviews on those websites. 


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
[1] https://www.chicagotribune.com/business/ct-biz-mcdonalds-cyclospora-outbreak-20180719-story.html
[2] https://www.kaggle.com/chicago/chicago-food-inspections
[3] https://data.cityofchicago.org/Health-Human-Services/Food-Inspections-Dashboard/2bnm-jnvb
[4] https://data.cityofchicago.org/api/assets/BAD5301B-681A-4202-9D25-51B2CAE672FF
[5] https://www.yelp.com/dataset
[6] https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2