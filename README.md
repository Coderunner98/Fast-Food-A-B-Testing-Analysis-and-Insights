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


 ## Shape:

The dataset contains 548 rows and 7 columns. Data Types: MarketID, LocationID, AgeOfStore, Promotion, week: Integer (int64) MarketSize: Object (categorical) SalesInThousands: Float (float64) Null Values: There are no missing values in the dataset. Quantiles: MarketID: Values range from 1 to 10. LocationID: Ranges from 1 to 920, with a median of 504. AgeOfStore: Ranges from 1 to 28
## What is A/B Testing

A/B testing is a method used to compare two versions of a variable to determine which performs better. In this process, two variants, A and B, are tested simultaneously among different user groups. The goal is to identify which version yields better results, such as higher conversion rates or increased user engagement. By isolating one variable at a time, A/B testing provides clear, data-driven insights into what changes lead to improved outcomes. This approach helps businesses optimize their strategies and make informed decisions based on empirical evidence rather than assumptions.
data:image/png;base64,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6nmTmJioTZs26f/+7/905MgRvfrqq3r77bf1+OOPV3jOuoJwi3Jr0KCBPvnkE50/f15dunTRgw8+qL59++r111+v8nlHjRqlyMhIde7cWY0bN9bu3buLzdO0aVNt2LBBn3/+uaKiojR27FiNGDFCL7300g3Vd+bMGXXs2FEdO3ZUenq65syZo44dO2rkyJE3NC/qjrp67ixcuFD5+fl68MEHFRISYn/MmTPnhuZF3VBXz5vc3Fw988wzatu2re68807985//1DvvvMP/OWVgM7++jg4AAADUYly5BQAAgGUQbgEAAGAZhFsAAABYBuEWAAAAlkG4BQAAgGUQbgEAAGAZhFsAAABYBuEWAAAAlkG4BQCLOHHihGw2m1JSUpxdCgA4DeEWACQNGzZMNptNNptNbm5uat26tWbMmKErV644u7QSDRs2TIMGDXJoCwsLU3p6utq1a1dlzxsREWE/TiU9hg0bVmXPDQBlUc/ZBQBATdG/f38tXbpUeXl52rBhg8aNG6f69esrISGh2Nj8/Hy5ubk5ocrSubq6Kjg4uEqfY9++fSosLJQkffbZZxo8eLBSU1Pl4+MjSfL09KzS5weA6+HKLQD8f+7u7goODlZ4eLiefvpp9evXT+vWrZP07yulf/nLXxQaGqrIyEhJ0tdff6277rpLnp6eCgwM1OjRo5WTk2Of8+p+f/3rXxUUFCQ/Pz/7FeHnn39eAQEBatasmZYuXepQy7XmnTZtmpYvX661a9far5hu3769xGUJO3bsUNeuXeXu7q6QkBD9+c9/drgaHR0drWeffVaTJk1SQECAgoODNW3atFKPUePGjRUcHKzg4GAFBARIkpo0aaKgoCD16NFDf//73x3Gp6SkyGazKS0tTZJks9m0cOFCDRgwQJ6enmrZsqU++OADh31Onjyphx9+WH5+fgoICND999+vEydOlOFvEAAItwBQKk9PT+Xn59u3t2zZotTUVG3atEnr169Xbm6uYmJi5O/vr3379mn16tXavHmzxo8f7zDP1q1bdebMGe3cuVNz587V1KlTde+998rf31979+7V2LFjNWbMGJ06dUqSrjvvxIkT9fDDD6t///5KT09Xenq67rjjjmL1nz59WgMHDlSXLl104MABLVy4UIsXL9Yrr7ziMG758uXy8vLS3r17NWvWLM2YMUObNm0q17Gy2Wx66qmnioX0pUuXqlevXmrdurW9bcqUKRo8eLAOHDigoUOHasiQITpy5IgkqaCgQDExMfL29tauXbu0e/duNWzYUP3793f4uwCAUhkAgImNjTX333+/McaYoqIis2nTJuPu7m4mTpxo7w8KCjJ5eXn2fRYtWmT8/f1NTk6Ove3jjz82Li4uJiMjw75feHi4KSwstI+JjIw0PXv2tG9fuXLFeHl5mffee69c816t96rjx48bSearr74yxhjzwgsvmMjISFNUVGQfk5SUZBo2bGivp3fv3qZHjx4O83Tp0sVMnjz5usds27ZtRpL56aefjDHGnD592ri6upq9e/caY4zJz883jRo1MsuWLbPvI8mMHTvWYZ5u3bqZp59+2hhjzNtvv12s5ry8POPp6Wk++eST69YEAFy5BYD/b/369WrYsKE8PDw0YMAAPfLIIw4f0bdv395hne2RI0cUFRUlLy8ve9udd96poqIipaam2tvatm0rF5d//3MbFBSk9u3b27ddXV0VGBios2fPlmve6zly5Ii6d+8um83mME9OTo79KrEkdejQwWG/kJAQey3lERoaqnvuuUdLliyRJP3rX/9SXl6eHnroIYdx3bt3L7Z99crtgQMHlJaWJm9vbzVs2FANGzZUQECALl++rGPHjpW7JgB1D79QBgD/X58+fbRw4UK5ubkpNDRU9eo5/hP567BZHvXr13fYttlsJbYVFRVVaP4bVZm1jBw5Uk888YTmzZunpUuX6pFHHlGDBg3KvH9OTo46deqkd999t1hf48aNK1QTgLqFK7cA8P95eXmpdevWat68ebFgW5I2bdrowIEDys3Ntbft3r1bLi4u9l84q4iyzOvm5ma/a8G15klOTpYxxmEeb29vNWvWrML1XcvAgQPl5eWlhQsXauPGjXrqqaeKjdmzZ0+x7TZt2kiSbr/9dn377bdq0qSJWrdu7fDw9fWtkpoBWAvhFgAqaOjQofLw8FBsbKwOHTqkbdu2KS4uTk888YSCgoKqdN6IiAgdPHhQqampOnfunAoKCorN88wzz+jkyZOKi4vT0aNHtXbtWk2dOlXx8fEOyyQqk6urq4YNG6aEhATddNNNxZYgSNLq1au1ZMkSffPNN5o6dao+//xz+y/LDR06VI0aNdL999+vXbt26fjx49q+fbueffZZh6UUAFAawi0AVFCDBg30ySef6Pz58+rSpYsefPBB9e3bV6+//nqVzztq1ChFRkaqc+fOaty4sXbv3l1snqZNm2rDhg36/PPPFRUVpbFjx2rEiBF66aWXbqi+6xkxYoTy8/M1fPjwEvunT5+uVatWqUOHDlqxYoXee+893XrrrZJ+ee07d+5U8+bN9cADD6hNmzYaMWKELl++bL+XLgBci838+vMqAABu0K5du9S3b1+dPHmy2BVsm82mjz76qNi3qwFAZeEXygAAlSIvL08//PCDpk2bpoceeuiGlmYAQEWxLAEAUCnee+89hYeHKysrS7NmzXJ2OQDqKJYlAAAAwDK4cgsAAADLINwCAADAMgi3AAAAsAzCLQAAACyDcAsAAADLINwCAADAMgi3AAAAsAzCLQAAACzj/wF2gIiuH/CPUwAAAABJRU5ErkJggg==![image](https://github.com/user-attachments/assets/4699fcc1-19a9-451e-8db5-f78efa0c43e8)


Goal
Review the A/B testing results to decide on the most effective marketing strategy

