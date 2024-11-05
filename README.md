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



## Boxplot

![Unknown](https://github.com/user-attachments/assets/759f9922-217f-41fa-8e57-81f6942befd2)

Looking at the box plot we can see there are outliers so removing them so main advantage is Enhanced Accuracy of the Model: By eliminating outliers, which have the potential to distort results, models may become more accurate. More Focus on Typical Patterns and Trends: Prevents the study from being distorted by extreme numbers, allowing for clearer insights. Superior Statistical Tests: Outliers can cause disruptions to the normalcy that many statistical tests presume. Adverse effects Information Loss: Significant variances or unusual occurrences may be represented by outliers. Bias: If outliers are a natural aspect of variability, eliminating them could generate bias. Results can be misinterpreted if outliers are removed without properly documenting the process.

To remove outliers from your data using the Interquartile Range (IQR) method, follow these steps: First, calculate the IQR by identifying the first quartile (Q1) and the third quartile (Q3), and then subtract Q1 from Q3. Next, determine the lower bound by subtracting 1.5 times the IQR from Q1, and the upper bound by adding 1.5 times the IQR to Q3. Finally, filter the data by removing any data points that fall outside these calculated bounds.


Calculate the IQR as IQR = Q3 − Q1

Determine the Bounds:

Lower bound = Q1 − 1.5 × IQR Upper bound = Q3 + 1.5 × IQR








![Unknown-5](https://github.com/user-attachments/assets/b370a811-9d23-4c78-8f75-1b5d90c846a5)
![Unknown-6](https://github.com/user-attachments/assets/7fef51de-b25e-4f84-a7eb-de482f8166b8)
![Unknown-7](https://github.com/user-attachments/assets/db2a8927-0a4c-46bd-9a2b-8f0416b5fcbc)

The Q-Q plots generated for SalesInThousands across different Promotion types and MarketSize categories allow us to assess the normality of the sales data distribution. If the data points align closely with the reference line, the distribution is likely normal.

This analysis helps compare the effectiveness of promotions across market sizes and identify any deviations from normality, indicating variability or inconsistencies in sales performance.

Using df.groupby("Promotion").agg({"SalesInThousands": ["count", "mean", "median", "std"]}) helps in evaluating the effectiveness of different promotions by aggregating key statistics for SalesInThousands. By grouping the data by Promotion and calculating the count, mean, median, and standard deviation of sales:

Count provides the number of observations for each promotion, which helps in understanding the sample size. Mean shows the average sales amount, offering insight into the overall effectiveness of each promotion.

Median provides the middle value of sales, which is useful for understanding the central tendency, especially if the data is skewed. Standard Deviation (std) measures the variability of sales, indicating how spread out the sales figures are around the mean.

These metrics collectively offer a comprehensive view of how each promotion performs and how sales data is distributed, aiding in informed decision-making about which promotion strategies are more effective.

Based on the Q-Q Plot by Sales & Promotion Types we can see that data is not distributed normally.

## Model Accuracy & Comparison

![Unknown-8](https://github.com/user-attachments/assets/37f5d29d-a201-466f-95b0-3251a1414a58)



## Model Performance Analysis of Regression Techniques

The following analysis presents the accuracy of various regression models used to predict sales:

Gradient Boosting: 76.44%

This model demonstrates the highest accuracy, indicating its effectiveness in capturing complex relationships within the data.

K-Nearest Neighbors: 71.17%

With solid performance, KNN is effective in scenarios where local patterns are significant, making it a useful model for regression tasks.

Random Forest: 70.78%

As an ensemble method, Random Forest performs well by averaging multiple decision trees, thus reducing overfitting and handling various data distributions effectively.

Decision Tree: 58.45%

While easy to interpret, the decision tree's lower accuracy suggests it may be too simplistic for this dataset, capturing some trends but failing to generalize well.

Linear Regression: 27.53%

This model shows the lowest accuracy, indicating that a simple linear approach is insufficient for capturing the underlying patterns in the data.

## Conclusion

The analysis of model performance across several regression techniques highlights the strengths and limitations of each model in predicting sales. Gradient Boosting stands out as the most suitable model, achieving an accuracy of 76.44%. Its ability to capture complex, nonlinear relationships within the data makes it well-suited for predicting sales, particularly in dynamic, high-dimensional datasets.

The K-Nearest Neighbors (KNN) model, with an accuracy of 71.17%, performs respectably, especially in contexts where local patterns are crucial. Its accuracy suggests it may be beneficial for tasks where sales are influenced by similar data points, though it lacks the robustness of ensemble-based models. The Random Forest model, achieving 70.78%, also shows strong performance. Its ensemble approach helps mitigate overfitting by averaging multiple decision trees, making it adept at managing diverse data distributions and enhancing model stability.


## Recommendations

1. Prioritize Gradient Boosting for Sales Predictions

Use Gradient Boosting as the primary model for predicting sales, given its ability to handle complex data relationships effectively. This model should be the first choice for any future sales forecasting tasks in this dataset or similar ones.

 2. Consider K-Nearest Neighbors and Random Forest for Supplementary Analysis

While Gradient Boosting is recommended as the primary model, K-Nearest Neighbors and Random Forest can be useful for supplementary analyses. KNN may offer insights in contexts where local data similarities matter, and Random Forest provides a stable, ensemble-based alternative that can handle varied data distributions.

 3. Avoid Simple Models like Linear Regression and Decision Tree for Complex Datasets
    
Refrain from using simpler models such as Linear Regression and Decision Tree for complex datasets, as they lack the predictive accuracy needed for nuanced patterns. These models may be more suitable for straightforward, linear datasets where interpretability is prioritized over accuracy.

On the other hand, the Decision Tree model, with an accuracy of 58.45%, offers interpretability but falls short in predictive power, indicating that it is likely too simplistic for this dataset's complexity. Linear Regression, with an accuracy of only 27.53%, is the least suitable model for this task, demonstrating that a linear approach fails to capture the nuanced patterns within the data.

Overall, this analysis recommends Gradient Boosting as the optimal choice for accurate sales predictions, given its ability to capture intricate patterns. The hierarchy of model effectiveness—from Gradient Boosting to Linear Regression—provides clear guidance for model selection, highlighting the need for advanced, ensemble-based techniques for improved forecasting accuracy in similar datasets. This ranking can guide model deployment for ongoing and future predictive analytics efforts.


