| **Field**                | **Definition**                                                |
|--------------------------|---------------------------------------------------------------|
| item_id                  | Unique ID for the inventory item                              |
| category                 | High level category segment - forms a hierarchy with Category |
| department               | Lower level category segment                                 |
| from_state_name          | Workflow state the item transitioned from (see workflow stages below for values and their definitions)                    |
| to_state_name            | Workflow state the item transitioned into  (see workflow stages below for values and their definitions)                    |
| staff_id                 | ID of the employee who caused the state transition            |
| transition_date_time     | Timestamp when the transition occurred                        |
| transition_order         | For this item, this is the Xth transition in its lifespan     |
| duration_secs            | Time in seconds that the item was in the from_state           |
| cumulative_duration_secs | Time in seconds since the item was created                    |
| price                    | Sale price of the item                                        |






| **Item Workflow Stages**| **Description**                                                                                                    | **Parent Process**|
|-------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------|
| CREATED                 | Item is created - checked into system for the first time                                                           | Receiving         |
| FORSALE_REVIEW          | Item is fully checked in, with all information populated. Ready to be reviewed.                                    | Receiving         |
| FORSALE_APPROVED        | Item has been reviewed, and has been approved to appear on the site. At this time, the item is available for sale. | Receiving         |
| ORDERED                 | Item has been ordered by a customer.                                                                               | Customer Order    |
| PICKING                 | Associate is on the warehouse floor picking items for the order.                                                   | Fulfillment       |
| PICKED                  | Item has been picked from storage shelves and is awaiting being packed.                                            | Fulfillment       |
| PACKING                 | Item is being packed for shipping.                                                                                 | Fulfillment       |
| PACKED                  | Item is packed for shipping and is awaiting shipping label.                                                        | Fulfillment       |
| DROPPED                 | Item has shipping label and has been dropped for carrier pickup.                                                   | Fulfillment       |
| PICKED_UP               | Item has been picked up by shipping carrier and is on its way to a customer.                                       | Fulfillment       |
