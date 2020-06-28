# Classification-of-leaves-images-using-DBSCAN-algorithm
Density-based spatial clustering of applications with noise (DBSCAN) is a well-known data clustering algorithm that is commonly used in data mining and machine learning.
Based on a set of points (let’s think in a bidimensional space as exemplified in the figure), DBSCAN groups together points that are close to each other based on a distance measurement (usually Euclidean distance) and a minimum number of points. It also marks as outliers the points that are in low-density regions.
Parameters:
The DBSCAN algorithm basically requires 2 parameters:
eps: specifies how close points should be to each other to be considered a part of a cluster. It means that if the distance between two points is lower or equal to this value (eps), these points are considered neighbors.
minPoints: the minimum number of points to form a dense region. For example, if we set the minPoints parameter as 5, then we need at least 5 points to form a dense region.
Parameter estimation:
The parameter estimation is a problem for every data mining task. To choose good parameters we need to understand how they are used and have at least a basic previous knowledge about the data set that will be used.
eps: if the eps value chosen is too small, a large part of the data will not be clustered. It will be considered outliers because don’t satisfy the number of points to create a dense region. On the other hand, if the value that was chosen is too high, clusters will merge and the majority of objects will be in the same cluster. The eps should be chosen based on the distance of the dataset (we can use a k-distance graph to find it), but in general small eps values are preferable.
minPoints: As a general rule, a minimum minPoints can be derived from a number of dimensions (D) in the data set, as minPoints ≥ D + 1. Larger values are usually better for data sets with noise and will form more significant clusters. The minimum value for the minPoints must be 3, but the larger the data set, the larger the minPoints value that should be chosen.

•	In our project, we’ve taken a data set of 1600 images of leave. We converted the images into black and white format, so that colours distinction is reduced to two. Conversion to black and white is done by converting the colour values to binary: black and white.
•	We used two approaches to proceed with DB Scan: Image approach and CSV file approach.
Image approach: In this approach, we utilized every pixel of the every image and assigned an intensity value to it between 0 and 1. Since images are black and white, intensity values will
 
be binary (either 0 or 1). Once the intensity value of every single pixel of every single image is assigned, a normalized value is given to every image according to their pixel-intensity value.


The normalized values are then plotted on a graph and allowed to form clusters with neighbouring plotted points. The epoch is calculated by applying repeated iteration on these points and after 10 epochs, accuracy came out to be ~40%. Hence the clusters are formed and these clusters can be scanned through.
