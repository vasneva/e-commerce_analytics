# e-commerce analytics

**Project Goals**

- Determine the number of users who made only one purchase and identify their proportion of the total user base.
- Calculate the average monthly number of orders that are not delivered for various reasons, providing a breakdown for each reason.
- Analyze which day of the week each product is purchased most frequently.
- Calculate the average number of weekly purchases for each user by month.
- Conduct a cohort analysis of users to identify the cohort with the highest retention rate by the third month.
- Perform RFM segmentation of users and describe the resulting clusters based on recency, frequency, and monetary metrics. Draw conclusions.

**Data Description**

**Files:**

- `olist_customers_dataset.csv` — table of unique user identifiers
  - `customer_id` — per-order user identifier
  - `customer_unique_id` — unique user identifier (like a passport number)
  - `customer_zip_code_prefix` — user postal code
  - `customer_city` — user delivery city
  - `customer_state` — user delivery state

- `olist_orders_dataset.csv` — orders table
  - `order_id` — unique order identifier (receipt number)
  - `customer_id` — per-order user identifier
  - `order_status` — order status
  - `order_purchase_timestamp` — order creation timestamp
  - `order_approved_at` — order payment confirmation timestamp
  - `order_delivered_carrier_date` — timestamp of order handoff to logistics
  - `order_delivered_customer_date` — order delivery timestamp
  - `order_estimated_delivery_date` — promised delivery date

- `olist_order_items_dataset.csv` — ordered items in each order
  - `order_id` — unique order identifier (receipt number)
  - `order_item_id` — item identifier within an order
  - `product_id` — product ID (like a barcode)
  - `seller_id` — product manufacturer ID
  - `shipping_limit_date` — maximum shipping date by the seller to transfer to the logistics partner
  - `price` — unit price of the product
  - `freight_value` — product weight

**Unique Order Statuses in the `olist_orders_dataset` Table:**

- `created` — created
- `approved` — approved
- `invoiced` — invoiced
- `processing` — order is being prepared
- `shipped` — shipped from warehouse
- `delivered` — delivered to user
- `unavailable` — unavailable
- `canceled` — canceled
