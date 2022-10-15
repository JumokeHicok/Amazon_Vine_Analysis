# Amazon_Vine_Analysis

## Project Overview
The purpose of this project is to perform ETL on Amazon product reviews of books using S3, AWS RDS, Postgres, and PySpark and analyze the vine vs non-vine review results. 

1. Connect to the AWS RDS server and create the tables in pgAdmin.  
2. Using PySpark, transform the dataset into four separate DataFrames and load into the tables in pgAdmin.
3. Using PySpark, calculate the total reviews, number of 5-star reviews, and percentage of 5-star reviews for the paid and unpaid reviews.
4. Provide a written analysis of any positivity bias in the Vine program.

## Results
- There were 5,012 Vine
- There were 109,297 non-Vine reviews
- There were 2,031 5-star Vine reviews
- There were 49,967 5-star non-Vine reviews
- 40.5% of the Vine reviews were 5-star
- 45.7% of the non_Vine review were 5-star

![DataFrame](/Resources/vine_dataframe.png)

## Challenge Summary
There does not appear to be any positivity bias for reviews in the Vine program.  Based on the calculations shown above, the percentages of 5-star reviews for Vine and non-Vine reviewers is pretty similar.  The percentage is actually slighly higher for non-Vine reviewers.  One analysis that could be done to further prove out that there is no bias is to add 8 additional columns to our dataframe to calculate the count and percentage for each star rating (4, 3, 2, 1).
