# Amazon Vine Analysis

## Overview of the analysis:

The purpose of this project consist in choosing a dataset from a different variety of products to analyze. In this case, **Video Games** was choosen as our dataset, then we use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Afterwards Pandas was used to determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Results:
From all the dataset some considerations were made.
 1. Only consider products with equal or greater than 20 total votes
 2. From the previous filtering only consider those who have a helpful votes/total votes ratio equal or greater than 50%.
 
Afterwards an analysis was made using Pandas, the following results were obtained for Paid (Vine) reviews and Unpaid (non-Vine) reviews:

![image](https://user-images.githubusercontent.com/83261520/135560142-f070ebd0-f148-4282-9c55-8c6743af8d69.png)

- There were a total of 94 Vine reviews and a total of 40,471 non-Vine reviews. 
- From the total of reviews, 48 Vine reviews were 5 stars and 15,663 non-Vine reviews were 5 stars. 
- The percentage of 5 star Vine reviews is 51.06% and the percentage of 5 star non-Vine reviews is 38.70%.

## Summary:

Based on the results shown, it does not seems to be any positivity bias for reviews caused by the Vine program, as there are only 94 reviews this only represents the 0.2% of the total amount of considered reviews for this analysis, also 5 star Vine review percentage is not that high to have some significance in the reviews.

Another way to analyze this is by taking a look at the following summary statistics.

![image](https://user-images.githubusercontent.com/83261520/135565538-4d87b2fd-75db-472d-9c67-4899ca22525e.png)

***Vine review statistics***

![image](https://user-images.githubusercontent.com/83261520/135564144-0a91fba9-b2d5-48a8-ba69-6cdd4d6a2589.png)

***non-Vine review statistics***

![image](https://user-images.githubusercontent.com/83261520/135564184-05f2be7e-e777-43cb-83ff-d8de509875ab.png)

***Vine and non-Vine review statistics***

The average star rating from Vine reviews is 4.2, meanwhile from non-Vine reviews is 3.34 and overall the average star rating is also 3.34, altough it does seems that most of the Vine reviews are among 4 and 5 stars this is not enough to provoke any positivity bias as the number of Vias reviews is really small compared to the total number of reviews.
