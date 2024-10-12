### Understanding Support and Confidence

- **Support**: Support is the proportion of transactions in the dataset that contain a particular itemset. It helps to measure how frequently an itemset appears in the dataset. A higher support value means that the itemset occurs more frequently.
  
  For example, if you set `support = 0.3`, it means that you are only interested in itemsets that appear in at least 30% of the transactions.

- **Confidence**: Confidence measures the likelihood that when an item (or itemset) A is present in a transaction, item (or itemset) B will also be present. It indicates the strength of the association rule.

  For example, if you set `confidence = 0.7`, it means that you are only interested in rules where the consequent occurs in 70% of the transactions that contain the antecedent.

### Example:
If you have a dataset of supermarket transactions and you're using Apriori to find associations, you might set:

- **Support**: 0.2 (to find itemsets that appear in at least 20% of the transactions)
- **Confidence**: 0.6 (to find rules where 60% of the time when one item appears, the associated item appears as well)
