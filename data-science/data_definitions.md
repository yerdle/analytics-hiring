## Data Definitions
This repository includes two datasets you can leverage for your assignment, which include information on individual inventory items from Homebody, our fictional partner whose Yerdle-powered resale program offers used home goods. Definitions for each field are below. 


## [Item Data](https://github.com/yerdle/analytics-hiring/blob/master/data-science/item_data.csv)
| **field**                   | **definition**                                                                                                                                                                                                      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unique_item_id              | Unique identifier for the specific used item from Homebody's inventory.                                                                                                                                             |
| used_list_price             | Price at which the used item is for sale. If the item was ordered, then this is the price at which it sold.                                                                                                         |
| used_condition              | Level of wear on item.                                                                                                                                                                                              |
| department                  | High level segment reflecting the category of the item. Forms a hierarchy with category.                                                                                                                            |
| category                    | Detailed segment reflecting the category of the item.                                                                                                                                                               |
| item_parent_sku             | The parent product for the item. This is the level of granularity you might see on an ecommerce product page - a single style, though there may be multiple sizes, colors, or other configurations available all on the same page. |
| color                       | Color of the item.                                                                                                                                                                                                  |
| size                        | 2 character code for size. Size codes vary substantially across products.                                                                                                                                          |
| msrp_new                    | Manufacturer's suggested retail price when the item was new.                                                                                                                                                        |
| last_known_retail_price_new | The last known discounted price of the item at retail (when it was new). If this value is null, the item was never discounted and was only sold at MSRP.                                                            |
| first_approved_date         | The date this item was first approved for sale (when it first appeared online in Homebody's used goods store).                                                                                                      |
| first_ordered_date          | The date this item was ordered. If this value is null, the item is still in Homebody's inventory.                                                                                                                   |



## [Pageviews](https://github.com/yerdle/analytics-hiring/blob/master/data-science/pageviews.csv)

| **field**           | **definition**                                                                                                                                                                                                                                |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| item_parent_sku | The parent product for the item. This is the level of granularity you might see on an ecommerce product page - a single style, though there may be multiple sizes, colors, or other configurations available all on the same page. Foreign key to item_data. |
| pageviews       | The number of pageviews for the product detail page of the item_parent_sku.                                                                                                                                                                   |
