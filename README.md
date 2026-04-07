# big-data-mining-clustering-lab
# Clustering Lab: Hierarchical and DBSCAN on Wine Dataset

## Purpose of the Lab
The goal of this lab was to get hands-on experience with clustering techniques using the Wine dataset from sklearn. I applied both Hierarchical Clustering and DBSCAN to see how each method groups data without using labels. This helped me better understand how clustering works, how parameter choices affect results, and how to evaluate the quality of clusters.

---

##  Key Insights

### Hierarchical Clustering
Hierarchical clustering worked really well on this dataset. The clusters it produced were fairly clean and seemed to match the actual wine classes pretty closely. The dendrogram was especially helpful because it showed how the data points were grouped step by step, which made it easier to decide that around 3 clusters was a good choice.

### DBSCAN Clustering
DBSCAN was interesting because it doesn’t require setting the number of clusters ahead of time. Instead, it groups points based on how dense they are. One thing I noticed right away is that the results changed a lot depending on the `eps` value. Smaller values created more noise points, while larger values grouped more data together. It was also useful to see how DBSCAN can detect outliers, which hierarchical clustering doesn’t really do.

### Evaluation Metrics
The evaluation scores helped show how well the clustering matched the actual labels. Hierarchical clustering generally gave more consistent results. DBSCAN’s scores depended heavily on the parameter settings, especially when too many points were labeled as noise.

---

## Challenges and Decisions

One of the biggest challenges was choosing the right parameters. For hierarchical clustering, picking the number of clusters required interpreting the dendrogram, which isn’t always straightforward. For DBSCAN, finding the right `eps` and `min_samples` took some trial and error.

Another challenge was visualization. Since the dataset has many features, plotting only two of them doesn’t always give a complete picture of how the clusters are actually separated. Sometimes the clusters looked more mixed in the plots than they really were.

Handling noise in DBSCAN was also something I had to think about. Since some points were labeled as noise, it affected certain evaluation metrics, and I had to decide how to interpret those results.

---

## Conclusion
Overall, hierarchical clustering worked better for this dataset because the data has clear groupings. DBSCAN was still useful, especially for understanding density-based clustering and identifying outliers. This lab showed me how important parameter tuning and visualization are when working with clustering algorithms.
