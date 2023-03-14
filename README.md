# Market-Basket-Analysis-in-Python-using-Apriori-Algorithm
In this project, I used Python and Jupyter Notebook to perform market basket analysis on a grocery transaction dataset using the Apriori algorithm. First, I imported the necessary libraries, including pandas for data manipulation, TransactionEncoder for one-hot encoding the transaction data, and apriori and association_rules from mlxtend for performing the Apriori algorithm and generating association rules.

Next, I read in the dataset using pandas and inspected its information and shape using dataset.info() and dataset.shape, respectively. Since some columns had many null values, I decided to drop them using dataset.drop(), along with the "Item(s)" column that would not be useful for generating frequent itemsets.

After cleaning the data, I created a list of lists to contain each transaction, except for null values. Then, I used TransactionEncoder to convert the transaction data to a one-hot encoded format and passed it to the apriori function to generate frequent itemsets with a minimum support of 0.03. Finally, I used association_rules to generate association rules with a minimum lift of 1 and sorted them by support.
