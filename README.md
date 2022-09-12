# Formula-One-Analysis
Data analysis is the process of digging through data to discover hidden connections and predict future trends has a long history. Sometimes referred to as "knowledge discovery indatabases," the term "data mining" wasn’t coined until the 1990s. But its foundation comprises three intertwined scientific disciplines: statistics (the numeric study of data relationships), artificial intelligence (human-like intelligence displayed by software and/or machines) and machine learning (algorithms that can learn from data to make predictions). What was old is new again, as data mining technology keeps evolving to keep pace with the limitless potential of big data and affordable computing power.

# A. First descriptive objective: Identify drivers according to their accumulated points
   ## 1. Segmentation :  
   ### 1.1. K-Means :  

k-means clustering is a method of vector quantization, originally from signal processing, that is popular for cluster analysis in data mining. k-means clustering aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean, serving as a prototype of the cluster.
In order to determinate the number of clusters we choose the Elbow method :
 we have to select the closest point of flattening , K = 3

![image](https://user-images.githubusercontent.com/58832576/189641993-08c2b04d-1883-4a0e-881a-a82bfc4a3648.png)
![image](https://user-images.githubusercontent.com/58832576/189642657-89b1f500-4df0-433b-abe0-0ba00a65e229.png)

##### Segmentation of drivers :
The group with the highest number of points and rate is the one that we should select,  so based on the Kmeans segmentation it is the one in yellow.

![image](https://user-images.githubusercontent.com/58832576/189644725-76c2adcb-aea2-4d1d-b49d-9f08a7ffec21.png)
#### --> the classification rate is perfect since each driver belongs to only one cluster.

 ###  1.2	HAC : 
 
 Hierarchical ascending classification (AHC) is a classification method which has the following advantages :
 We work from the dissimilarities between the objects that we want to group together. We can therefore choose a type of dissimilarity adapted to the subject studied
 and the nature of the data.
 
 ![image](https://user-images.githubusercontent.com/58832576/189646137-37ea7ab2-b295-4ab6-af96-7f85515b567e.png)
 
 The specific splitting such that k =3 in order to be able to compare the result obtained by K-Means and CAH the splitting is done at height 470.

# B. Second descriptive objective: number of times a driver is eliminated:
##   1.	Segmentation :
###     1.1	K-Means :

•	we have to select the closest point of flattening, K = 4	

![image](https://user-images.githubusercontent.com/58832576/189648657-a7f1a176-b03f-4d2d-89b7-65944e52e92b.png)

###### Interpretation:

![image](https://user-images.githubusercontent.com/58832576/189648792-15a7dda8-29bc-4f56-a8e3-003f1bf1935e.png)

The majority of the individuals we studied belong to cluster number 1.
![Capturee](https://user-images.githubusercontent.com/58832576/189710041-26f90f03-80eb-457f-ae6a-5dc77dcee2c4.PNG)
After applying the segmentation, we conclude that the classification rate is	perfect since each driver belongs to only one cluster.
The group colored in red is adequate to select ,since the number of laps and the position order value are minimal.


   ### 1.2	CAH
We considered that we have no idea about the number of clusters to work with so we chose to work with the CAH method.

![image](https://user-images.githubusercontent.com/58832576/189718094-a1d943b8-5dfa-468c-b4ba-c27c1f71d1b9.png)

We make the section of the dendrogram, the section is made on moment that we obtained a great interclass inertia.

![image](https://user-images.githubusercontent.com/58832576/189718198-43ee0016-38ba-479a-aef2-d27440a3fa10.png)

The specific splitting such that k = 3 in order to be able to compare the result obtained by k-means and cah the splitting is done at height 300.

# C.	Third descriptive objective :Identifying pit stop duration per driver:	

The object is  to cluster a particular dataset where we have the duration and number of pitstops of drivers.

## 1.	Segmentation :	

 ### 1.1	K-Means	

![image](https://user-images.githubusercontent.com/58832576/189719111-9ce0a661-6ddf-4a43-8978-1d1ead86a3cf.png)

The elbow method  shows the curve below, we chose K=3.

![image](https://user-images.githubusercontent.com/58832576/189719227-61a882be-45b9-45a7-9c0a-81a726495a5b.png)

Using k-means we were able to segment the drivers into 3 clusters, cluster 1 contains	drivers with a duration of pitstops is between 20000 ms and 25000 ms while cluster 0	contains drivers with a  duration of pitstops is greater than 25000.

![Cap](https://user-images.githubusercontent.com/58832576/189719612-98ae1091-a3e3-466f-bfe5-c959ffc41a81.PNG)

### Interpretation :

After the segmentation we obtained this graph, we will choose the group colored in red since it contains individuals whose rank and duration are reduced.This group meets our descriptive objective.

### 1.2	CAH

We considered that we have no idea about the number of clusters to work with. So we chose to work with the CAH method
By applying the algorithm we obtained the dendrogram as the picture shows :

![image](https://user-images.githubusercontent.com/58832576/189720052-5ece2c3d-882f-42f2-b9b3-9a679a5e276f.png)
![image](https://user-images.githubusercontent.com/58832576/189720087-0b0a05a4-a71e-4ff2-a6ed-955c4171e1ff.png)

The specific splitting such that k = 3 in order to be able to compare the result obtained by k-means and cah the splitting is done at height 28.

![image](https://user-images.githubusercontent.com/58832576/189720271-c90fdfde-84ef-44eb-940c-137611cc8920.png)

##### -->  In short, each individual belongs to a  single cluster so the classification rate of CAH is the same as K-Means unlike CAH, does not provide tools to help detect the number of classes.

# D. Fourth descriptive objective: Identify drivers according to their fastest lap speed	
## 1. Segmentation
###   1.1 K-means
In order to determinate the number of clusters we choose the Elbow method :
We have to select the closest point of flattening , K=2.

![garbage](https://user-images.githubusercontent.com/58832576/189721443-00ce970f-6c11-424e-80b6-88e04ccec659.PNG)

We obtained a segmentation of 2 different groups, so that the components of each group have the same behavior. for the first group which has a rank between 4 and 13, and the 2nd group has a rank varies between 14 and 20. concerning the axis fast Lap Speed have the same behavior.

### 1.2 CAH
We considered that we have no idea about the number of clusters to work with.
So we chose to work with the CAH method
![image](https://user-images.githubusercontent.com/58832576/189721708-b70f3b0e-689b-4fd7-9dee-42a7edfaebb5.png)

The specific splitting such that k = 2 in order to be able to compare the result obtained by k-means and CAH the splitting is done at height 6500.

![Captureeeeee](https://user-images.githubusercontent.com/58832576/189722103-c18511f6-890e-4f20-98b0-9b831911e866.PNG)

 The classification rate is perfect since each driver belongs to only one cluster 

# E. Fifth explicative objective: Determine  the most  correlated variables with Driver variable

Segmentation:
Principal component analysis (PCA) is a statistical procedure that uses an orthogonal transformation to convert a set of observation of possibly correlated variables (entities each of which takes on various numerical values) into a set of values of linearly uncorrelated variables called principal components.

 We have to work with quantitative data with this method, so we did the coding of the attributes and qualitative data.

![image](https://user-images.githubusercontent.com/58832576/189722621-c3284cb1-0460-44b0-b470-1821e317f833.png)

 We standardized the data to avoid problems scales.

![image](https://user-images.githubusercontent.com/58832576/189722740-e20e1fc9-d381-48fa-baae-82d39d6d32ee.png)
	Then we applied the ACP method and we obtained the matrix of correlation with the diagonal (the eigenvalues)

Using the Kaiser principle we had 2 relevant columns so we managed to minimize the number of columns.
Last thing we did the correlation circle which gave us the variables most correlated with our objective.
![a](https://user-images.githubusercontent.com/58832576/189723407-7fc40cf1-c339-4bf2-8ba7-74fb681389ad.PNG)

![AAA](https://user-images.githubusercontent.com/58832576/189725811-340f82f8-746f-4aff-879a-2e95efe4e1c7.PNG)
 Conclusion: the ACP method is the most accurate and reliable method for our goal.


# F. Sixth explicative objective: Determine the number of accidents per track/per constractor

We have to work with quantitative data with this method, so we did the coding of the attributes and qualitative data.


![hiii](https://user-images.githubusercontent.com/58832576/189726840-7a076326-0307-4c36-a05c-3080ec68f85e.PNG)


### 	We standardized the data to avoid problems scales.

![image](https://user-images.githubusercontent.com/58832576/189727006-53dbf6de-7809-4426-8155-d6562f4f1d95.png)

### Then we applied the ACP method and we obtained the matrix of correlation with the diagonal (the eigenvalues)

![image](https://user-images.githubusercontent.com/58832576/189727106-33e821c9-4859-4fcd-9a5e-977bd4115bb4.png)

Using the Kaiser principle we had 2 relevant columns , so we managed to minimize the number of columns and the Vizualisation of the Map of individuals.

![image](https://user-images.githubusercontent.com/58832576/189727404-a26abcc3-8379-4f0f-98bc-107cd4470e09.png)
![image](https://user-images.githubusercontent.com/58832576/189727421-296326d6-5c9b-4204-9a7b-9cbb7fe6617c.png)

Vizualisation of the correlation circle
![image](https://user-images.githubusercontent.com/58832576/189727490-d51311cd-66af-4a74-aaa1-0441d90a5303.png)

## Interpretation:
If the PCA is performed on a small number of individuals, the interpretation of the cloud of individuals is then possible.
Whatever the case considered, we interpret, on a given factorial plan, only the individuals who are well represented.
(Fair Park, Adelaide Street..)
To do this, you have to look at their absolute and relative contributions.

# G.	Classification & Prediction:
The K-nearest neighbors (kNN) algorithm is a Machine Learning algorithm that belongs to the class of simple and easy-to-implement supervised learning algorithms that can be used to solve classification problems and regression.

![image](https://user-images.githubusercontent.com/58832576/189728603-8cf7d701-d3e4-477c-82ef-5c95492988ff.png)

In this figure we can have a look on the Classification of racers by podium

![image](https://user-images.githubusercontent.com/58832576/189728686-9fd5664c-078a-4381-94ac-e5c6dd731ae2.png)
This figure shows a code snippet that we used to divide the data into training data and test data.

![image](https://user-images.githubusercontent.com/58832576/189728802-1b322ac6-6985-408c-9486-bb5e295c4120.png)

The best way to find it is to plot the graph of the K value and the corresponding error rate for the data set.

![image](https://user-images.githubusercontent.com/58832576/189728979-a3950c30-04d1-4099-a006-139a751efb35.png)

This figure shows a code snippet that we used to Training phase: Apply the KNN model with the training data.

 However we opted for the grid search method because it gives us a direct result.
 
 ![image](https://user-images.githubusercontent.com/58832576/189729155-4c2bcef2-3a99-43e6-8889-bcbd23b0a560.png)
 Thanks to grid search we got K=19 .
 
 ## Model evaluation:
![image](https://user-images.githubusercontent.com/58832576/189729280-cf8d4909-478e-478e-a9e5-5dbc9622989a.png)

Thanks to the KNN algorithm, we obtain an excellent rate of good classification of racers close to 100%.

![image](https://user-images.githubusercontent.com/58832576/189729399-735e2f97-b18d-46f8-9fbb-d86b9d67ae9a.png)

Using tis classification algorithms we succeeded to predict wether a driver is going to win the race or not based on the features that we chose to introduce to the algorithms.


















