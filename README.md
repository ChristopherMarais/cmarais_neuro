# Mouse Neuro data cleaning


Christopher Marais

gmarais@ufl.edu

University of Florida

PhD Forest Resources and Conservation


### Mouse Neuro Electrophysiology Data Clustering
The main aim of this project was to take sparse binary timeseries data and cluster it. The Objective was to reducethe amount of data compression/manipulation in an attempt to preserve the integrity of the data and get and understanding of the level of noise in the data. The resulting clusters were then loosely compared to experimental variables to see if there was any relationship between the clusters and the experimental variables.

![Framework](neuro_data_flow.png)

1. **Data Compression:** The Data was compressed by reducing the number of 0s in the sparse binaryu timeseries by a scaling factor. This way the ratio oif the distances between the 1s was preserved and the data was compressed. Some local structure of the data is lost ian this way, but the global structure of the timeseries is maintained.
2. **Pairwise Distance Calcualtions:** The pairwise distance between all the timeseries was calculated using the Dynamic TIme Warping distance. This distance is a measure of the similarity between two timeseries. The distance is calculated by finding the optimal alignment between the two timeseries. The distance is then the sum of the distances between the aligned points. This distance was the foundation for the clustering.
3. **Clustering:** The clustering was done using heirarchical clustering. The heirarchical clustering was done using the weighted linkage method. This method is a bottom up approach where the two closest clusters are merged at each step. The distance between the clusters is the average distance between the points in the two clusters. This method was chosen because it is a simple method that is easy to implement and understand. The heirarchical clustering was done using the scipy library in python.
4. **Evaluation:** The clustering was evaluated using the Adjusted Rand Index. This index is a measure of the similarity between two clusterings. The index is a value between -1 and 1. A value of 1 indicates that the two clusterings are identical. A value of 0 indicates that the two clusterings are random. A value of -1 indicates that the two clusterings are as different as possible. Additionally, we used the Normalized Mutual Information to evaluate the clustering. This index is a measure of the mutual information between two clusterings. The index is a value between 0 and 1. A value of 1 indicates that the two clusterings are identical. A value of 0 indicates that the two clusterings are random. These metrics were used to compare the clustering to the experimental variables.

* Although other methods exist to do this sort of analysis that are very effective, the aim of this analysis was to minimise hte amount of data manipulation and compression. This will form as a baseline for future analysis. The xpectation was to see a lot of nopise as the data was not filtered and the expectation was to see the strongest relationship between units and the clusters that were made. This is exaclty waht has occured. (Further methods will be explored in future analysis to narrow down a balnce between clustering effectiveness and data manipulation.)

To repeat this analysis yourself, follow the instructions in each of the folders in the order at which they are numbered.
