# Machine-Learning_tasks
4 tasks for Machine Learning and Statistics 2020


## Task 1: Write a Python function called sqrt2 that calculates and prints to the screen the square root of 2 to 100 decimal places.

In order to complete the task I will do the following:

1. Research the topic by repeated watching the lecture video and find more information online.
2. Based on information that I find I will write a python function that calculates square root of 2 and use Pyhton to set the output to 100 decimal places without using any libraries.
3. Test my function using Python library.
4. Write conclusion and references.


The square root of 2 or root 2 is represented using the square root symbol √ and written as √2 whose value is 1.414. I will use Newton's method to find the root of 2. 

The method comprises of 4 steps: 

1. Take a reasonable guess (approximate root) for the square root.
2. Add the approximate root with the original number divided by the approximate root and divide by 2.
x_i := (x_i + n / x_i) / 2
3. Continue step 2 until the difference in the approximate root along the iterations is less than the desired value (or precision value).
4. The approximate root is the square root we want.



## Task 2: Use scipy.stats to verify given value and calculate the associated p value of Chi squared test.

Completion of the task:

1. Research chi squared test online.
2. Based on information that I find I will write a chi square python function in scipy.stats to verify given Chi square value and calculate p value.
3. Write analysis and conclusion
4. Write references.

The aim of this task is to verify Chi sqared value using scipy.stats and calculate p-value. Data that I have got shows the same Chi sqared value as the one that is shown in the given example on wikipedia page. In both cases Chi square is 24.6. To be more precise I got the result of 24.57120 with p-value of 0.00041. P-value tells us if we need to reject null hypothesis or not. Null hypothesis is an assumption that there is no relationship between variables. In this case four different neighbourhoods (A, B, C, D) were tested to see if there is any connection between neighbourhoods and person's occupational profession (white collar, blue collar, no collar). As p-value is 0.00041 it tells us that we need to reject null hypothesis (H0) which means that there is significant relationship between the neighbourhood and the occupation of people who live there. In order to show significant difference between the variables p-value should be less than 0.05 if probability is defined in 95%.


## Task 3: The standard deviation

The aim of this task is to discuss two Microsoft Excel functions STDEV.P and STDEV.S that are used to calculate standard deviation. I will research these Excel functions and write about the difference between them. Then I will use numpy to perform a simulation demonstrating that the STDEV.S calculation is a better estimate for the standard deviation of a population when performed on a sample. 


- Standard deviation

The standard deviation is the average amount of variability in a dataset. It tells us how far each value lies from the mean.

A high standard deviation means that values are generally far from the mean, while a low standard deviation indicates that values are clustered close to the mean. Standard deviation is a useful measure of spread for normal distributions.

In normal distributions, data is symmetrically distributed with no skew. Most values cluster around a central region, with values tapering off as they go further away from the center. The standard deviation tells us how spread out from the center of the distribution data is on average.

Many scientific variables follow normal distributions, including height, standardized test scores, or job satisfaction ratings. When there is the standard deviations of different samples, their distributions can be compared using statistical tests to make inferences about the larger populations they came from.

- Findings

As I mentioned in my jupyter notebook, high standard deviation means that values are generally far from the mean, while a low standard deviation indicates that values are clustered close to the mean. The aim of this task was to demonstrate that the STDEV.S calculation is a better estimate for the standard deviation of a population when performed on a sample. I have created 500 points of data using random normal distribution which represented population, and from those data points I extracted every 10th data point to make a sample. Calculations based on that sample showed that STDEV.S formula that was used on that sample had lower standard deviaton which indicated that values are clustered closer to the mean. STDEV.S standard deviation is 4.1581 while STDEV.P standard deviation is 4.2767. This result is not surprising as I used different formula. As previously stated STDEV.S formula uses N-1 which means that in calculation of standard deviation, standard deviation is alaways lower than in STDEV.P that uses only N. In this simulataion, I set st. deviation to 4, and STDEV.S function was closer to the set mean than STDEV.P. As this was a small sample I used Bassel's correction N-1 that appears to produce less biased standard deviation.


## Task 4: The iris dataset

The purpose of this task is to apply k-means clustering to Fisher’s famous Iris data set using scikit-learn and explain how this model could be used to make predictions of species of iris.

Scikit-learn (Sklearn) is the most useful and robust library for machine learning in Python. It provides a selection of efficient tools for machine learning and statistical modeling including classification, regression, clustering and dimensionality reduction via a consistence interface in Python.

- K-means is often referred to as Lloyd’s algorithm. In basic terms, the algorithm has three steps:

The first step chooses the initial centroids, with the most basic method being to choose samples from the dataset.
After initialization, K-means consists of looping between the two other steps. The first step assigns each sample to its nearest centroid. The second step creates new centroids by taking the mean value of all of the samples assigned to each previous centroid.
The difference between the old and the new centroids are computed and the algorithm repeats these last two steps until this value is less than a threshold. In other words, it repeats until the centroids do not move significantly.

- Findings

Kmeans clustering is one of the most popular clustering algorithms and usually the first thing analysts do in order to get an idea of the structure of the dataset. It gives us very good overview of how far data is from the center of a cluster, that's why the aim of kmeans is to group data points into non-overlapping subgroups. That is exactly what we have got in a case of setosa iris flower. There was no overlapping with other two clusters. Kmeans does a very good job when the clusters have a kind of spherical shapes. But on the other hand, it suffers if there are any deviations from shperical shapes. That is the case with other two clusters virginica and versicolor iris flower. Moreover, another disadvantage of KMeans is that the number of clusters from the data need to be pre-defined which was not an issue in this case as we had sorted data in 3 clusters. But if the data was unsorted, Kmeans method might not be an ideal algorithm to use and we should look for an alternative approach.