# link_prediction_ml

## Network Science
### Challenge Part II

![image](https://user-images.githubusercontent.com/88637523/167493735-db9c5099-94c3-406e-a6a8-8496a67963d3.png)

Link prediction strategy:

• Obtain a sample of existing links (edges);

• Obtain the same size sample of non-existent links (non_edges);

• Obtain the Jaccard Coefficient of the samples;

• Obtain the Preferential Attachment of the samples;

• Obtain the resource allocation index (Resource Allocation Index) of the samples.


 After completing these steps, a dataframe was created with all the data obtained in the previous item to be used as a training set for the classification models. The three parameters obtained are part of a set of functions for predicting links in the Networkx library. Each index by itself can be used for link prediction, so the main idea is to combine these values in links labeled as non_edge = 0 and edge = 1 with balanced samples to evaluate the joint performance in a classification model.
Before training the models, the data were standardized using Sklearn's StandarScaler(), since the data obtained were at different scales, as can be seen in the following figure:

![image](https://user-images.githubusercontent.com/88637523/167490401-c9ea2ab7-f425-4a31-bc99-00c3734f3e5c.png)
 

 It is an important step because the models perform better with data in a standardized range, avoiding giving greater weight to data with larger scales. Standardization scales the data by subtracting the mean and dividing by the standard deviation, which results in a distribution with a standard deviation and a variance of 1.
Finally, six different models were trained and tested to classify links. After testing, considering computational time and metrics, the K-Nearest Neighbors and the Decision Tree Classifier were selected. The metrics applied were accuracy, confusion matrix, mean squared error and F1 score.


Notebooks can be found at this repository!
