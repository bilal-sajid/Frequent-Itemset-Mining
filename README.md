# Frequent Item Mining Algorithms

## Introduction

Welcome to the Frequent Item Mining Algorithms implementation! This repository contains two Jupyter Notebooks: `apriori.ipynb` and `fp_growth.ipynb`, allowing you to explore association rule mining using your own datasets. The Apriori and FP-Growth algorithms are popular data mining techniques used to uncover interesting relationships between items in large datasets, commonly known as market basket analysis.

## What are the Apriori and FP-Growth Algorithms?

### Apriori Algorithm

The Apriori algorithm identifies frequent itemsets in transactional data and derives association rules from these itemsets. An association rule is an implication of the form \(A ⇒ B\), which means that if an item (or set of items) \(A\) is purchased, then item \(B\) is likely to be purchased as well.

### FP-Growth Algorithm

The FP-Growth (Frequent Pattern Growth) algorithm is an alternative to the Apriori algorithm. Instead of generating all possible itemsets, FP-Growth builds a compact data structure called the FP-tree. It then explores the tree to extract frequent itemsets directly, making it more efficient, especially for larger datasets.

### Key Terms

- **Support**: The support of an itemset is the proportion of transactions in the dataset that contain the itemset. It helps in determining the frequency of occurrence.
  
- **Confidence**: The confidence of an association rule \(A ⇒ B\) is the proportion of the transactions containing \(A\) that also contain \(B\). It measures the reliability of the inference made by the rule.

- **Lift**: The lift of a rule \(A ⇒ B\) is the ratio of the observed support to that expected if \(A\) and \(B\) were independent. A lift greater than 1 indicates a positive correlation between the items.

## Why Use the Apriori and FP-Growth Algorithms?

Understanding customer behavior is crucial for businesses looking to enhance sales and improve marketing strategies. Here’s how both algorithms can be beneficial:

- **Market Basket Analysis**: Identify which products are frequently bought together. This information can help in product placement and cross-selling strategies.
  
- **Recommendation Systems**: Enhance customer experience by recommending products based on previous purchases.
  
- **Inventory Management**: Optimize stock levels by understanding product relationships and customer buying patterns.

## Inputting Thresholds

When using the applications, you will enter support and confidence thresholds for both algorithms:

- **Support Threshold**: Filters out itemsets that are not common (e.g., only consider itemsets appearing in at least 20% of transactions).

- **Confidence Threshold**: Filters out weak rules (e.g., only consider rules where the second item appears at least 70% of the time when the first item is present).

Adjusting these thresholds helps you find the most relevant patterns in your data.

## Getting Started

### Requirements

- Python 3.x
- Jupyter Notebook
- Required libraries:
  - `pandas`
  - `mlxtend`

### How to Use

1. **Prepare Your Dataset**: 
   - Your dataset should be in CSV format, structured in a single column. Each row should represent a transaction with items separated by commas.
   - Example format:
     ```
      spaghetti,antioxydant juice
      chocolate,milk,almonds,eggs,strawberries,white wine
      french fries,strawberries
      mineral water
     ```

2. **Load the Jupyter Notebooks**: 
   - Open `apriori.ipynb` or `fp_growth.ipynb` in Jupyter Notebook.

3. **Run the Preprocessing Step**: 
   - The notebooks will preprocess the data to convert it into a suitable format for the respective algorithms.

4. **Input Support and Confidence**: 
   - You will be prompted to input the desired support and confidence values. These parameters will guide the algorithms in generating association rules.

5. **View Results**: 
   - The resulting DataFrame will display the association rules derived from your data, along with their support, confidence, and lift values.

## Example Output

The output will include a DataFrame containing the following columns:
- **Antecedents**: The item(s) in the rule.
- **Consequents**: The item(s) that are likely to be purchased when the antecedents are bought.
- **Support**: The support of the rule.
- **Confidence**: The confidence of the rule.
- **Lift**: A measure of how much more likely the antecedent is to occur with the consequent than without it.

## When to Use Each Algorithm

- **Apriori Algorithm**: Best suited for smaller datasets with fewer transactions. It generates all possible itemsets and can become computationally expensive with larger datasets.
  
- **FP-Growth Algorithm**: More efficient for larger datasets as it compresses the dataset into a frequent pattern tree (FP-tree) and only explores the frequent itemsets. Use this algorithm when dealing with larger datasets or when performance is a concern.
r

Feel free to reach out with questions or contributions!
