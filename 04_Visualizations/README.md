# Visualization

This folder contains the visual outputs of each script. The number with which each file starts corresponds to the script that was used to generate that file. The visualizations are:

- `02_dtw_distance_count_distribution.png` - This is a lineplot displaying the counts of each distance value found in the distance matrix. This is a distribution of how the distances in the distance matrix are alyed out. It also shows where the plot starts to plateau, which is used as a threshold foir distinguishing between entities that are within or outside of the same clusters during clustering.

![02_dtw_distance_count_distribution.png](04_Visualizations/02_dtw_distance_count_distribution.png)


- `03_attribute_ARI_plot.png` - This plot shows the Adjusted Rand Index (ARI) of each attribute. The ARI is a measure of how well the clustering performed if the attribute is assumed to be the true labels. The ARI is a value between -1 and 1 where 1 is a perfect match and 0 is a random match.

![03_attribute_ARI_plot.png](04_Visualizations/03_attribute_ARI_plot.png)


- `03_attribute_NMI_plot.png` - This plot shows the Normalized Mutual Information (NMI) of each attribute. The NMI is a measure of how well the clustering performed if the attribute is assumed to be the true labels. The NMI is a value between 0 and 1 where 1 is a perfect match and 0 is a random match.

![03_attribute_NMI_plot.png](04_Visualizations/03_attribute_NMI_plot.png)