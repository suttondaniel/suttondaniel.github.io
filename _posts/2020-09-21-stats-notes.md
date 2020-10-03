---
title: "Current projects"
date: 2020-09-21
tags: [data science, statistics]
---

## Measures of Variability on an interval or ratio scale

1. The max of an array minus the min of an array
2. Find the average distance from the mean
3. Find the mean **absolute** distance from the mean 
   - otherwise known as the mean absolute deviation, or average absolute deviation
4. Square each distance, then find the mean of these distances
    - otherwise known as the mean squared distance, or mean squared deviation
      - this is more commonly known as **variance**
5. Finding the variance, then taking the root of that.  Here we find the **standard deviation**
    - remember that deviation is synonymous with distance.  so standard deviation is the standard distance.  in code form: 
        ```
        def standard_deviation(array):
            reference_point = sum(array) / len(array)
    
            distances = []
            for value in array:
                squared_distance = (value - reference_point)**2
                distances.append(squared_distance)
        
            variance = sum(distances) / len(distances)
    
            return sqrt(variance)
        ```

    - Most statisticians agree that applying **Bessel's Correction**, i.e. using len(distances) - 1 in order to reduce the denominator, is the best choice for taking the standard deviation of a sample
    - sigma = standard deviation
    - sigma squared = variance
    - s = sample standard deviation
    - s squared = sample variance
    - remember, a statistic is an **unbiased estimator** when that statistic is equal on average to the parameter it estimates
      - the sample mean, for instance, is an unbiased estimator for the population mean whether we sample with or without replacement
      - the sample variance is an unbiased estimator for the population variance, only when we sample with replacement

## Z-scores - how far a value is away from the mean in terms of number of stdevs
 - z = (val - mean) / standard deviation
 - i.e. the number of standard deviations away from the mean a value is
 - A z-score is negative if the value is below a mean
   - So the formula you wrote while trying to be fancy with the absolute value calculation was actually wrong
   - See dicts.txt in your Notes folder for info on how to find the minimum absolute value in a dict
 - Z scores overlay perfectly over a distribution of values: 
   - if you were to take the z score of each value in a distribution, the distribution of those values would look identical to the original values themselves
   - This is why a distribution of z-scores is often called a **standard distribution**
   - 




