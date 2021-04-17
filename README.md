# Starbucks_project

![image](https://user-images.githubusercontent.com/72763736/115127278-ae741800-9fab-11eb-967f-67bb3f26855f.png)

# Background Information
The dataset you will be provided in this portfolio exercise was originally used as a take-home assignment provided by Starbucks for their job candidates. The data for this exercise consists of about 120,000 data points split in a 2:1 ratio among training and test files. In the experiment simulated by the data, an advertising promotion was tested to see if it would bring more customers to purchase a specific product priced at $10. Since it costs the company 0.15 to send out each promotion, it would be best to limit that promotion only to those that are most receptive to the promotion. Each data point includes one column indicating whether or not an individual was sent a promotion for the product, and one column indicating whether or not that individual eventually purchased that product. Each individual also has seven additional features associated with them, which are provided abstractly as V1-V7.

# Optimization Strategy

The task is to use the training data to understand what patterns in V1-V7 to indicate that a promotion should be provided to a user. Specifically, the goal is to maximize the following metrics:

* **Incremental Response Rate (IRR)** 

IRR depicts how many more customers purchased the product with the promotion, as compared to if they didn't receive the promotion. Mathematically, it's the ratio of the number of purchasers in the promotion group to the total number of customers in the purchasers group (_treatment_) minus the ratio of the number of purchasers in the non-promotional group to the total number of customers in the non-promotional group (_control_).

$$ IRR = \frac{purch_{treat}}{cust_{treat}} - \frac{purch_{ctrl}}{cust_{ctrl}} $$


* **Net Incremental Revenue (NIR)**

NIR depicts how much is made (or lost) by sending out the promotion. Mathematically, this is 10 times the total number of purchasers that received the promotion minus 0.15 times the number of promotions sent out, minus 10 times the number of purchasers who were not given the promotion.

$$ NIR = (10\cdot purch_{treat} - 0.15 \cdot cust_{treat}) - 10 \cdot purch_{ctrl}$$
# Files
`training.csv` - A file with all the training data

`Test.csv` - Test data for the model 

`Starbucks.ipynb` - A notebook with all the steps to get the solution

`test_results.py` - A module to check the results of the model and the solution find by Udacity

`requirementes.txt` - All libraries need to run the notebook

# Requirements

seaborn==0.8.1

scipy==1.2.1

scikit-learn==0.24.1

pandas==1.1.5

numpy==1.19.5

matplotlib==2.1.0

imblearn==0.0

catboost==0.25.1

# Solution
The results are shown here:

IRR with this strategy is 0.0183.

NIR with this strategy is 319.00.

Udacity came up with a model with an IRR of 0.0188 and a NIR of 189.45 on the test set.

The model get a better NIR and pratically the same IRR compared to Udacity results.
# Acknowledgment 

To Starbucks and Udacity for provide those datasets.
