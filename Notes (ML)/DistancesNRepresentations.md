# Distances and Representations

## Representation
Consider a table of data, with rows and columns. Each row of data can be represented as a **Vector** in a matrix form, these differing vectors are called **Samples/Datapoints**, and the numerical values from each 'column' are the **Features/Dimensions**.

There are different kinds of feature types:
* **Numerical (Continuous)**
* **Categorical (Nominal)**
* **Categorical (Ordinal)**
* **Binary**

## Distances
Unsupervised learning looks for the structure in the data, and measures similarity by the distance between datapoints are plotted in the feature space. There are a few ways to measure the 'closeness' of datapoints:
* **Euclidean Distance**, the distance of a straight line between two points. Given by $d(x,y) = \sqrt{\sum_i(x_i-y_i)^2}$. Preferable for low-dimensional data.
* **Manhattan Distance**, the distance from moving between two points, one dimension at a time. Given by $d(x,y) = \sum_i|x_i-y_i|$. Preferable for high-dimensional or sparse data.
* **Cosine Similarity**, measures the alignment between two vectors of datapoints from the origin. Given by $similarity(x,y) = \frac{x . y}{||x||y||} = cos\theta$. Preferable for when the scale of a feature doesn't matter, and only the orientation metters.
* **Hamming Distance**, counts the amount of mismatching bits in two bit strings.
* **Mahalanobis Distance**, the distance used in high-dimensional Gaussian distributions, which accounts for correlation across different dimensions. Given by $d_{\sum}(x,y) = \sqrt{(x-y)^T\sum^{-1}(x-y)}$.
* **Jaccard Index**, measures the intersection over the union, typically between sets. Given by $J(x,y) = \frac{|x \cap y|}{|x \cup y|}$

## Feature Scaling
...

## Categorical and Mixed Data
Consider data that instead of being numerical, has values of words representing various categories. It has been previously mentioned that for categorical feature types, it can be either done as **Nominal** or **Ordinal**.

**Ordinal** categorical representation assigns each word/category with a numerical value. So for ***example***, $Size = \{Small,Medium,Large\}$, would instead be represented by $Size = \{1,2,3\}$ where $1 = Small$, $2 = Medium$ and $3 = Large$.

**Nominal** categorical representation encoded to **One-Hot Notation**, where each word/category is considered a separate feature, and can only have binary values 1s or 0s to represent whether a datapoint contains that feature. So for ***example***, $Small = \{1,0,0\}$, $Medium = \{0,1,0\}$ and $Large = \{0,0,1\}$; where each 'column' represents each feature. However this may be a problem considering high-dimentional data with more categories.

It is important to **Standardise** the data, to keep all the data in similar scale. It may be required to convert all features to a nominal categorical representation if a feature is using this representation. As to not cause scaling problems.

## Non-Linear Representation
...