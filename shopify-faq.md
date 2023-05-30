# Frequently asked questions

## Table of contents

- [In which countries can I use Vipps?](#in-which-countries-can-i-use-vipps)
- [The order that comes from Vipps is labelled authorized, what does that mean?](#the-order-that-comes-from-vipps-is-labelled-authorized-what-does-that-mean)
- [Customers are getting error messages when they are trying to check out with Vipps?](#customers-are-getting-error-messages-when-they-are-trying-to-check-out-with-vipps)
- [I do not receive any Vipps orders?](#i-do-not-receive-any-vipps-orders)
- [Can we use Vipps Express Checkout with Shopify?](#can-we-use-vipps-express-checkout-with-shopify)
- [How can I get the Vipps payment logo in the footer?](#how-can-i-get-the-vipps-payment-logo-in-the-footer)
- [What do the different order statuses in Shopify mean when combined with Vipps](#what-do-the-different-order-statuses-in-shopify-mean-when-combined-with-vipps)

## In which countries can I use Vipps?

You can only get paid by users who have Vipps. At the moment, Vipps is only available i Norway.

## The order that comes from Vipps is labelled authorized, what does that mean?

The order's status is *reserved* in Vipps. The amount is only reserved and not
captured from the customers account. When the order is completed, you can capture
the payment. You can either do this inside each order by clicking the button
*capture*, or by marking more orders and choose the *actions* dropdown, and then click *capture payments*.

According to Norwegian regulations you should not capture a payment until the
product or service is provided to the customer. For more information,
please see the Norwegian Consumer Authority's
[Guidelines for the standard sales conditions for consumer purchases of goods over the internet](https://www.forbrukertilsynet.no/english/guidelines/guidelines-the-standard-sales-conditions-consumer-purchases-of-goods-the-internet).

## Customers are getting error messages when they are trying to check out with Vipps

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://developer.vippsmobilepay.com/docs/vipps-developers/).

## I do not receive any Vipps orders?

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://developer.vippsmobilepay.com/docs/vipps-developers/).

## I get `Error 2734583247: Order is not reserved in Vipps`

This is often caused by having "Direct capture" enabled in your Vipps account. Please change to "Reserve capture" and the issue should be resolved. Direct capture is not supported by the Shopify payment gateway.

See:
[Reserve and capture](https://developer.vippsmobilepay.com/docs/vipps-developers/common-topics/reserve-and-capture).

## Can we use Vipps Express Checkout with Shopify?

The Shopify module is currently not supporting express checkout. We try to use default platform features for our official modules and due to some limitations with the platform it is not possible to use express checkout with the default shipping alternatives available from the module. We are constantly working on improvements on the module and will add support as soon as it is flexible enough to implement. 

## How can I get the Vipps payment logo in the footer?

Unfortunately the new Payments App API from Shopify does not currently support adding payment method logos in the footer, as previously. To add the Vipps logo in the footer, you'll have to edit the theme files, by adding/editing a line of code in your footer or where you'll want the logos to appear. An example would be, but needs testing in your shop before using:

```liquid
{% assign enabled_payment_types = 'vipps,payment_2,payment_3' | remove: ' ' | split: ',' %}
```

## What do the different order statuses in Shopify mean when combined with Vipps?

In Shopify, you have two main statuses:

1. Financial status (is the order paid, refunded, cancelled, etc.?)
2. Fulfillment status (is the order sent, or not?)

### Financial status

There are multiple types available here, but the most common ones you might see is:

#### Authorized

With Vipps, this means that the order is reserved, but no money have changed hands yet. The funds are reserved on the customers account, until you capture the order, and the funds will be deducted from the customers account and you will receive it (minus fees).

All orders in authorized state should not be there for too long, because the reservations might expire if you don't capture them, typically within 7-14 days.

#### Pending

With Vipps this is a rare status, and often indicate that something is wrong with your account in Vipps. Very often this is related to your Vipps account are set to do "Direct Capture", which is not supported by the Vipps gateway in Shopify. You should double-check your account if you get a lot of orders in "Pending" state.

#### Paid

When a order is successfully captured in Vipps, it will be changed to the "Paid" state. This indicates that you will get the funds from the customer very soon. The order is "OK" and ready to be shipped.

#### Refunded / partially refunded

The title tells most of it, but when an order gets the "refunded" status, you have successfully refunded the order in Vipps, either fully or partially. Remember that all orders that is captured, are refunded, not cancelled.

#### Cancelled

Orders that are not captured yet, will be cancelled if you choose to cancel them in Shopify Admin. If the order is captured (hence in "Paid" state), it will be refunded instead.

### Fulfillment status

These types are the most common:

1. Unfulfilled
2. Partially fulfilled
3. Fulfilled

These indicate whether you have shipped the order or not. Vipps does not take part in these statuses other than the default mechanisms in Shopify Admin. These can be used as usual, and do not indicate any status of the Vipps payment. Only the Financial status tells the status of the Vipps order.


## Other frequently asked questions

See:
[Vipps API: Frequently Asked Questions](https://developer.vippsmobilepay.com/docs/vipps-developers/faqs/reserve-and-capture-faq/#what-is-the-difference-between-reserve-capture-and-direct-capture)
