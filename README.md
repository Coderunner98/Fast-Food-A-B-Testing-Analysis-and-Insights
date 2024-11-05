# Fast-Food-A-B-Testing-Analysis-and-Insights

## Project Overview

## Motivation

Fascinated by the Google “41 Shades of Blue” experiment, which aimed to test how different blue shades affected click-through rates on Google’s ads. This project is inspired by that experiment and explores how I would have analyzed the data as a data analyst at Google. This is a different dataset I used to see The study that delves into the complexities of marketing effectiveness using A/B testing, aiming to pinpoint the most successful promotional strategy by uncovering the specific influences of each promotion on sales, market size, and store age.

## Dataset

A fast food chain is considering adding three different promotions to its menu, but they are undecided about which campaign to choose. These promotions have been tested in selected markets in various locations to determine which one was more effective in driving sales.

## The Columns in the dataset includes:

MarketID: unique identifier for market
MarketSize: size of market area by sales
LocationID: unique identifier for store location
AgeOfStore: age of store in years
Promotion: one of three promotions that were tested
week: one of four weeks when the promotions were run
SalesInThousands: sales amount for a specific LocationID, Promotion, and week


## What is A/B Testing

A/B testing is a method used to compare two versions of a variable to determine which performs better. In this process, two variants, A and B, are tested simultaneously among different user groups. The goal is to identify which version yields better results, such as higher conversion rates or increased user engagement. By isolating one variable at a time, A/B testing provides clear, data-driven insights into what changes lead to improved outcomes. This approach helps businesses optimize their strategies and make informed decisions based on empirical evidence rather than assumptions.



## Goal

Review the A/B testing results to decide on the most effective marketing strategy

 ## Shape:

The dataset contains 548 rows and 7 columns. Data Types: MarketID, LocationID, AgeOfStore, Promotion, week: Integer (int64) MarketSize: Object (categorical) SalesInThousands: Float (float64) Null Values: There are no missing values in the dataset. 


![Unknown](https://github.com/user-attachments/assets/582de6c4-94e2-4d42-a027-2e0862ca0a39)

Quantiles: MarketID: Values range from 1 to 10. LocationID: Ranges from 1 to 920, with a median of 504. AgeOfStore: Ranges from 1 to 28


![Unknown](https://github.com/user-attachments/assets/759f9922-217f-41fa-8e57-81f6942befd2)

Looking at the box plot we can see there are outliers so removing them so main advantage is Enhanced Accuracy of the Model: By eliminating outliers, which have the potential to distort results, models may become more accurate. More Focus on Typical Patterns and Trends: Prevents the study from being distorted by extreme numbers, allowing for clearer insights. Superior Statistical Tests: Outliers can cause disruptions to the normalcy that many statistical tests presume. Adverse effects Information Loss: Significant variances or unusual occurrences may be represented by outliers. Bias: If outliers are a natural aspect of variability, eliminating them could generate bias. Results can be misinterpreted if outliers are removed without properly documenting the process.

To remove outliers from your data using the Interquartile Range (IQR) method, follow these steps: First, calculate the IQR by identifying the first quartile (Q1) and the third quartile (Q3), and then subtract Q1 from Q3. Next, determine the lower bound by subtracting 1.5 times the IQR from Q1, and the upper bound by adding 1.5 times the IQR to Q3. Finally, filter the data by removing any data points that fall outside these calculated bounds.


Calculate the IQR as IQR = Q3 − Q1

Determine the Bounds:

Lower bound = Q1 − 1.5 × IQR Upper bound = Q3 + 1.5 × IQR



![Unknown-5](https://github.com/user-attachments/assets/b370a811-9d23-4c78-8f75-1b5d90c846a5)
![Unknown-6](https://github.com/user-attachments/assets/7fef51de-b25e-4f84-a7eb-de482f8166b8)
![Unknown-7](https://github.com/user-attachments/assets/db2a8927-0a4c-46bd-9a2b-8f0416b5fcbc)

