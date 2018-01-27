# K-Nearest-Neighbours

K-Nearest Neighbours is an example of a Supervised, Non-Parametric Classification method:
+ Supervised because it works with labelled data.
+ Non-Parametric because it doesn't make assumptions about the distribution shape of the underlying data.

The output is an assignment of an item to a class, (Tnew = c), rather than giving a probability of membership to a class, P(Tnew = c|Xnew, x, t), for which you might consider Logistic Regression or Naive Bayes.

Let's take the following scenario, we a number of objects in our training set (N), each of which has attribute Xn and label Tn. To assign a new point to a class, KNN will find the points closest or most similar attributes to that new point. 
Of the 'K' nearest neighbouring objects, where K = 5, the majority class of those 5 objects will determine the identity of the new object.

A requirement of KNN is some notion of distance or similarity.
You could use Euclidean, which is a the default for many packages but if you want to account for closely correlated points, you might consider using the Mahalanobis distance instead.

How do we choose 'K'?
The choice of K is one thing we have control over.
+ When K is too small, KNN is extremely sensitive and is open to the influence of noise.
+ As we increase K, you include neighbours that are further away from your new point and this reduces the risk of over-fitting.
+ If we increasing K by too much , we'll lose underlying pattern of the data.
A popular way to choose K is using Cross-Validation. 

Data set: Iris Species, available from sklean datasets and https://archive.ics.uci.edu/ml/datasets/iris.
Steps are annotated in the corresponding Jupyter notbeook.






