# What does the different order statuses in Shopify actually mean together with Vipps?

In Shopify, you have two main statuses:

1. Financial status (is the order paid, refunded, cancelled, etc.?)
2. Fulfillment status (is the order sent, or not?)

**_Financial status_**

There are multiple types available here, but the most common ones you might see is:

1. Authorized

With Vipps, this means that the order is reserved, but no money have changed hands yet. The funds are reserved on the customers account, until you capture the order, and the funds will be deducted from the customers account and you will receive it (minus fees).

All orders in authorized state should not be there for too long, because the reservations might expire if you don't capture them, typically within 7-14 days.

2. Pending

With Vipps this is a rare status, and often indicate that something is wrong with your account in Vipps. Very often this is related to your Vipps account are set to do "Direct Capture", which is not supported by the Vipps gateway in Shopify. You should double-check your account if you get a lot of orders in "Pending" state.

3. Paid

When a order is successfully captured in Vipps, it will be changed to the "Paid" state. This indicates that you will get the funds from the customer very soon. The order is "OK" and ready to be shipped.

4. Refunded / partially refunded

The title tells most of it, but when an order gets the "refunded" status, you have successfully refunded the order in Vipps, either fully or partially. Remember that all orders that is captured, are refunded, not cancelled.

5. Cancelled

Orders that is not captured yet, will be cancelled if you choose to cancel them in Shopify Admin. If the order is captured (hence in "Paid" state), it will be refunded instead.

**_Fulfillment status_**

These types are the most common:

1. Unfulfilled
2. Partially fulfilled
3. Fulfilled

These indicate whether you have shipped the order or not. Vipps does not take part in these statuses other than the default mechanisms in Shopify Admin. These can be used as usual, and do not indicate any status of the Vipps payment. Only the Financial status tells the status of the Vipps order.
