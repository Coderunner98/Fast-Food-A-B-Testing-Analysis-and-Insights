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

The dataset contains 548 rows and 7 columns. Data Types: MarketID, LocationID, AgeOfStore, Promotion, week: Integer (int64) MarketSize: Object (categorical) SalesInThousands: Float (float64) Null Values: There are no missing values in the dataset. Quantiles: MarketID: Values range from 1 to 10. LocationID: Ranges from 1 to 920, with a median of 504. AgeOfStore: Ranges from 1 to 28



