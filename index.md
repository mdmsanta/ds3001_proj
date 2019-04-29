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

### 1. "True" Clusters
The only true clusters, true being that they were not stripes as we will see later, was found in the categories clustering. The categories were preprossed to be integer values. 

![Competition Clustering](mdmsanta/ds3001_project/master/competition%20count.png)

<img src= "https://raw.githubusercontent.com/mdmsanta/ds3001_project/master/competition%20count.png">



### 2. Vertical Striped Clusters
As seen in these graphs, the clusters are vertical stripes of the data and tend to only be based on x-values.

![Categories Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/categories.png)

![Votes Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/votes.png)


Dataset size presented a different type of challenge. The amount of outliers easily created uneven and odd looking clusters due to the skew in the data. The first image shows the orginal full set of points and the second is without the three prominate outliers. 

![Dataset Size (1) Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/kmeans-size1.png)

![Dataset Size (2) Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/kmeans-size2.png)

### 3. Horiztonal Striped Clusters
Lastly, we saw horizontal stripped clusters. This group of clustering algorithms gave the most insight into the data. With these horizontal stripes we can categorize our point values into three main groups: low, medium, and high. On both clustering graphs there are the same cutoffs for each of these categories: 0-6,7-10,11-18.

![Ratio Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/Kmeans-ratio.png)

The following graph shows the dataset size again, but with a normalization to counter act the outliers, of which we still have some. 

![Normalized Data Clustering](https://github.com/mdmsanta/ds3001_project/blob/master/kmeans-size-N.png)

## Decision Trees
After making these different categories, we wanted to then determine the most important or most contributing attributes in determining the category a dataset will fall. To do this, we used a decision tree. (Note: in this tree we left out categories and description since when processed for the tree, it creates a massive amount values to add and unreasonable to add to the tree). The full tree is shown below. 

![Full Tree](https://github.com/mdmsanta/ds3001_project/blob/master/TREEEEEEEE.PNG)

Since this a huge tree, lets restrict the tree to only three splits:

![Final Tree](https://github.com/mdmsanta/ds3001_project/blob/master/finaltree.png)

(Note: For file type, if CSV, file type = 0, if not file type > 0.5)

In these first few splits, we can see that the ratio value, vote button, and file type are the most contributing attributes to classify the datasets. From this we can recommend users to focus on not only their scores, but having a hire ratio of downloads to views, up votes by users, and the type of file of the data set. 




