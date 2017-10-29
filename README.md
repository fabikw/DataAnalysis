# Analizing shopping trends in Instacart

Instacart 2017 data set on orders is pretty extensive (713MB across 6 tables), including information about the products ordered, time of day and day of the week as well as categories for the different items.

The data can be downloaded from [Instacart dataset](https://www.instacart.com/datasets/grocery-shopping-2017) and includes training data of the orders made on 2017 as well as prior data about orders from the same (anonymized) users. The dataset includes approximately 3 million individual orders and approximately 33 million individual products ordered. There are close to 50,000 distinct products spanning 20 different departments.

The data contains individual information of each order:
  * Products ordered,
  * User ID,
  * Time of day (with resolution of one hour),
  * Day of the week,
  * Index of the order for the given user,
  * Days since last order.

It also contains, for each product, the following information:
  * Department (broad category)
  * Aisle (Fine category)
  * Has this item been ordered before by this user?
  
Information about the variables can be found in [jeremystand's Gist](https://gist.github.com/jeremystan/c3b39d947d9b88b3ccff3147dbcf6c6b). Note that some variable names are incorrect, like `days_since_prior` should be `days_since_prior_order`.

Analizing this information and deriving meaningful conclussions can lead to a better use of Instacart resources or benefit for their customers. For example, knowing when a product is more or less likely to be ordered can lead to sales and offers to customers to incentivize their purchase or drive it even higher.

We derive two results from our analysis, that can be used to drive offers:
  * We observe that the weekly trend of orders is similar for products in different categories, with the exception of alcoholic products which follow their own trend.
  * The users of Instacart concentrate on two modes: those who include organic items in most of their orders and those who have no organic items in most of their orders. Users with intermediate percentage of orders with organic items are uniform in distribution. Additionally, the number of users with high percentage of orders with organic items is high, with more than half the users ordering organic items in more than 84% of their orders.
