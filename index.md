# Project Overview & The Data Set

For this project, we chose to use the Dataset of [Kaggle Datasets](https://www.kaggle.com/morriswongch/kaggle-datasets). Kaggle is a valuable tool for data scientists, however it can be difficult to navigate especially for beginners. By categorizing the data sets the goal is to help students, hobbyists, and researchers more efficiently find data sets useful to them.

# How to Pick a Quality Data Set
Through the project, we chose to give each dataset a quality score, a point value based on the attributes of the dataset. The higher the point value, the more good qualities a dataset has. 

## Assigning Point Values
The following table shows the different attributes used to give points to a dataset with their corresponding point allocation. 

| Variable      | Description | Value Assigned|
| ------------- | ------------- | ------------- |
| File Type     | The type of downloadable file |Easier Type, more points (i.e. CSV = +3 points)  |
| Dataset Size  | The size of the dataset | Bigger size gives more points (0-3 points)  | 
| is Featured | Is the dataset featured| Yes= +1|
|is Super Featured | Has the dataset been featured for a long period of time| Yes = +1|
|Competition Count|The number of competitions the set has been in| If the set has been in a competition = +1|
|Description| Description of the dataset values and origin| If the set has a description = +1|
|Category| Category classification of the dataset| If the set has a category = +1|
|Vote Button|The number of "upvotes" by users| More upvotes gives more points (0-3 points)|
|License Type| The type of usage license | Free license  = +1 |

From these attributes, different point categories were created to determine the different "areas" from where the points were coming. 

| Category | Meaning | Attributes|
| ------------- | ------------- |------------- |
| Popularity | The usage and interaction with the dataset on Kaggle | isFeatured, isSuperFeatured, Ratio, voteButton|
|Quality|The quality of the dataset itself | File Type, Dataset Size, Competition Count|
|Information| The avalible information about the dataset| Description, Category, License Type|

In total a dataset can get 18 quality points, 7 total in popularity, 8 in quality, and 3 in information. Using the total points of a dataset of interest, a user can determine whether or not it fits their needs. 

Users can look into their datasets quality points here. 

## Determining Clusters of Dataset Types
After determining these quality points, we questioned what kind of clusters we could find between the dataset's attributes and their total number of points. Out of all of the clustering there were two main types of outcomes of clustering.

### 1. Vertical Striped Cluster

categories
votes
dataset size (1&2)
categories

### 2. Horiztonal Striped Clusters
ratio
normalized dataset size










