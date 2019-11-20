# Clustering using auto-encoding neural networks and classical k-means
Neural Network that clusters input data.

The objective is to identify structures in the overall client population in order to help the human operator distinct between possible frauds and legit transactions. When the client plays with a sum that surpasses a certain treshold, the transaction is tempararily blocked, pending for supervision. The algorithm will help either by classifying the client in a known cluster or recognizing it as an anomaly in the overall dataset, the human operator can then decide if blocking the transaction completely or letting it through.

In order to achieve the objective, the algorithm will be composed of multiple elements: the raw data has high feature cardinality and comprises millions of data-points, so in order to reduce the dimensinality for better and faster analisys, we will implement the encoder part of an auto-encoder neural network (trained on the whole dataset) for automatic PCA, and then the features extracted this way will be fed into a k-means clustering algorithm to segment the client data into subgroups.
