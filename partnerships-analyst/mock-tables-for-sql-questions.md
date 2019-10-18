**orders**

| order_id | inventory_item_id | buyer_user_id | order_date | order_item_price | category_id | status    |
|----------|-------------------|---------------|------------|------------------|-------------|-----------|
| 127947   | 123456            | 798           | 1/3/19     | $134             | 8           | ordered   |
| 127948   | 123457            | 467           | 1/4/19     | $56              | 5           | fulfilled |
| 127949   | 123458            | 467           | 1/4/19     | $79              | 1           | fulfilled |
| 127950   | 123459            | 467           | 1/4/19     | $67              | 4           | fulfilled |
| 127951   | 123460            | 158           | 1/6/19     | $349             | 6           | fulfilled |
| 127952   | 123461            | 158           | 1/6/19     | $79              | 5           | refunded  |
| 127953   | 123462            | 798           | 1/6/19     | $83              | 4           | ordered   |

Primary Key: order_id
Foreign Keys
- buyer_user_id (joins to users)
- inventory_item_id (joins to tradeins)
- category_id (to categories)
&nbsp;
&nbsp;

**tradeins**

| tradein_id | inventory_item_id | supplier_user_id | tradein_date | tradein_price | category_id |
|------------|-------------------|------------------|--------------|---------------|-------------|
| 123910     | 123457            | 158              | 4/16/18      | $25           | 5           |
| 124014     | 123561            | 765              | 8/4/18       | $18           | 9           |
| 123912     | 123459            | 951              | 6/1/18       | $39           | 7           |
| 124856     | 124403            | 732              | 6/15/18      | $71           | 5           |

Primary Key: tradein_id
Foreign Keys
- supplier_user_id (joins to users)
- inventory_item_id (joins to orders)
- category_id (to categories)


**users**

| user_id | created_at | name              |
|---------|------------|-------------------|
| 158     | 6/4/17     | Mark Bittman      |
| 765     | 9/1/17     | Paula Wolfert     |
| 643     | 6/1/17     | Julia Child       |
| 732     | 6/15/18    | Yottam Ottolenghi |
| 467     | 1/4/19     | Deb Perelman      |

Primary Key: user_id


**categories**

| category_id | name   |
|-------------|--------|
| 1           | Spoons |
| 2           | Forks  |
| 3           | Knives |
| 4           | Plates |
| 5           | Bowls  |

Primary Key: category_id
