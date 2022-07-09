# Amazon_Vine_Analysis

- Resources
    - Google Colab
    - PySpark
    - AWS - RDS, S3
    - PostgreSQL, pgAdmin4

## Overview

Analyze Amazon reviews written by members of the paid Amazon Vine program.  RDS instance created on Amazon Web Services with a bucket containing stored data.  Data is extracted from AWS and transformed using PySpark in a Google Colab notebook.  The data is then loaded to a PostgreSQL server that we created and connected with our AWS RDS instance using pgAdmin4.  Lastly, five star review percentages are calculated for both paid and unpaid categories.

![Screen Shot 2022-07-08 at 10 04 04 PM](https://user-images.githubusercontent.com/100544761/178089261-f13402d1-2afb-4094-a5f0-7b7803f47965.png)


## Results

1. How many Vine reviews and non-Vine reviews were there?
    - Total Reviews Paid: 107
    - Total Reviews Unpaid: 39869
2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    - Five Star Reviews Paid: 56
    - Five Star Reviews Unpaid: 21005
3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    - Five Star Reviews Percentage: 52.34%
    - Five Star Reviews Percentage: 52.69%

## Summary

Of the reviews with votes over 20, and with helpful vote percentage more than 50%, both Vine and non-Vine 5 star review percentages were just over 50%.  This indicates of course that half of the transactions led to perfectly satisfied customer experiences.  That there is no significant difference in percentages indicates that regardless of Vine and non-Vine status, reviews were applied evenly resulting in no evidence to suggest positivity bias based on the Vine program. We could of course cluster reviews of other rating values for comparison, however there may be many other variables contributing to ratings. We have limited data categories to provide insight, but I would suggest comparing ratings in the dichotomous category of verified purchases for possible bias. I actually took the liberty to do this and results were as follows:  

    - Five Star Review Percentages for Verified Purchases:  62.92%
    - Five Star Review Percentages for Unverified Purchases:  57.95%

It looks like there are 5% more five star reviews for verified purchases which may suggest a slight bias.  However, these two numbers are within a small percentage of difference resulting in no concrete evidence to accept this as a strong indication.