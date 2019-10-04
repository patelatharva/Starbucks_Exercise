- Explanatory Blog post on Medium: [https://towardsdatascience.com/how-to-target-promotions-with-conversion-prediction-model-to-maximize-net-incremental-revenue-f51dabdb6320?source=friends_link&sk=3707a9a742ad170ac03ffcb9a10aa87b](https://towardsdatascience.com/how-to-target-promotions-with-conversion-prediction-model-to-maximize-net-incremental-revenue-f51dabdb6320?source=friends_link&sk=3707a9a742ad170ac03ffcb9a10aa87b)  
- Project Notebook: [https://nbviewer.jupyter.org/github/patelatharva/Starbucks_Exercise/blob/master/Starbucks.ipynb](https://nbviewer.jupyter.org/github/patelatharva/Starbucks_Exercise/blob/master/Starbucks.ipynb)  

## How to target promotions with conversion prediction model to maximize Net Incremental Revenue?

Every time a company chooses to promote some product through tactics like offering discounts or running a digital ad campaign, there is a certain cost as well as some potential revenue earning opportunity associated with it. If the company is not careful in choosing the right set of customers to be receiving the promotion, it can end up losing a lot of money without earning much in return.

## Dataset

The dataset that I have used in this project was originally used as a take-home assignment provided by Starbucks for their job candidates. The data for this exercise consists of about 120,000 data points split in a 2:1 ratio among training and test files. In the experiment simulated by the data, an advertising promotion was tested to see if it would bring more customers to purchase a specific product priced at $10. Since it costs the company 0.15 to send out each promotion, it would be best to limit that promotion only to those that are most receptive to the promotion. Each data point includes one column indicating whether or not an individual was sent a promotion for the product, and one column indicating whether or not that individual eventually purchased that product. Each individual also has seven additional features associated with them, which are provided abstractly as V1-V7.

## Goal

Our goal is to maximize the following metrics:

* **Incremental Response Rate (IRR)** 

IRR depicts how many more customers purchased the product with the promotion, as compared to if they didn't receive the promotion. Mathematically, it's the ratio of the number of purchasers in the promotion group to the total number of customers in the purchasers group (_treatment_) minus the ratio of the number of purchasers in the non-promotional group to the total number of customers in the non-promotional group (_control_).

* **Net Incremental Revenue (NIR)**

NIR depicts how much is made (or lost) by sending out the promotion. Mathematically, this is 10 times the total number of purchasers that received the promotion minus 0.15 times the number of promotions sent out, minus 10 times the number of purchasers who were not given the promotion.

Here, I have applied different approaches for modeling this problem and used Regularized Gradient Boosting algorithm (XGBoost) to predict whether the person is likely to purchase product after receiving promotion.

Based on this prediction, the algorithm recommends whether to send promotion to the person or not.

You can learn more from [the project notebook available here.](https://patelatharva.github.io/Starbucks_Exercise/Starbucks.html)
