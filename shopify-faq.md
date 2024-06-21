<!-- START_METADATA
---
title: Vipps/MobilePay Shopify Plugins FAQ
description: Frequently asked questions for the Shopify plugins.
pagination_next: null
pagination_prev: null
---
END_METADATA -->

# Frequently asked questions

<!-- START_COMMENT -->
## Table of contents

- [In which countries can I use Vipps MobilePay?](#in-which-countries-can-i-use-vipps-mobilepay)
- [The order that comes from Vipps MobilePay is labelled authorized, what does that mean?](#the-order-that-comes-from-vipps-mobilepay-is-labelled-authorized-what-does-that-mean)
- [Customers are getting error messages when they are trying to check out](#customers-are-getting-error-messages-when-they-are-trying-to-check-out)
- [I do not receive any Vipps or MobilePay orders?](#i-do-not-receive-any-vipps-or-mobilepay-orders)
- [Can we use Express Checkout with Shopify?](#can-we-use-express-checkout-with-shopify)
- [How can I get the Vipps or MobilePay payment logo in the footer?](#how-can-i-get-the-vipps-or-mobilepay-payment-logo-in-the-footer)
- [What do the different order statuses in Shopify mean when combined with Vipps MobilePay](#what-do-the-different-order-statuses-in-shopify-mean-when-combined-with-vipps-mobilepay)
<!-- END_COMMENT -->

## In which countries can I use Vipps MobilePay?

You can get paid by users who have Vipps in Norway, or who have MobilePay in Denmark or Finland.

## For how long is an order reserved?

:::note
Payments initiated in Finland and Denmark have only 14 days to be captured; while
payments in Norway have 180 days.
If the payments aren't captured within this time, they will be automatically cancelled.

Payments can only be captured up to 14 days (MobilePay) or 180 days (Vipps) after reservation.
See [Reserve and capture](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture/).
:::

When a payment is completed with Vipps MobilePay, the money will be reserved, but only transferred to the merchant when the order is set to “Complete” or the money is captured manually. For MobilePay, this reservation period is 14 days, so you will need to ship and fulfill orders before this; or to make an agreement with the customer to capture the money before this period is over. For Vipps, the period is 180 days. For payments made by credit card in Vipps/MobilePay Checkout, the period can again be as short as 7 days.


## How can I get the Vipps or MobilePay payment logo in the footer?

Because of a limitation with Shopify's Payments App API, which doesn't currently support adding payment method logos in the footer,
you need the [Vipps/MobilePay Shopify Companion plugin](https://developer.vippsmobilepay.com/docs/plugins-ext/shopify-companion/) to add the logos and icons.

This also lets you add more payment information into the app.

The companion app can be used in combination with both the
[Checkout app for Shopify](https://developer.vippsmobilepay.com/docs/plugins-ext/checkout-shopify/)
or [Payment app for Shopify](https://developer.vippsmobilepay.com/docs/plugins-ext/shopify/).


<details>
<summary>Deprecated method</summary>
<div>
Alternatively, to add the Vipps or MobilePay logo in the footer, you'll can the theme files by adding/editing a line of code in your footer or where you'll want the logos to appear. An example would be, but needs testing in your shop before using:

```liquid
{% assign enabled_payment_types = 'vipps,payment_2,payment_3' | remove: ' ' | split: ',' %}
```
</div>
</details>





## The order that comes from Vipps MobilePay is labelled authorized, what does that mean?

The order's status is *reserved* in Vipps. The amount is only reserved and not
captured from the customers account. When the order is completed, you can capture
the payment. You can either do this inside each order by clicking the button
*capture*, or by marking more orders and choose the *Actions* dropdown, and then click *Capture payments*.

According to Norwegian regulations you should not capture a payment until the
product or service is provided to the customer. For more information,
please see the Norwegian Consumer Authority's
[Guidelines for the standard sales conditions for consumer purchases of goods over the internet](https://www.forbrukertilsynet.no/english/guidelines/guidelines-the-standard-sales-conditions-consumer-purchases-of-goods-the-internet).

## Customers are getting error messages when they are trying to check out

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/api-keys/).

## I do not receive any Vipps or MobilePay orders

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/api-keys/).

## I get `Error 2734583247: Order is not reserved`

This is often caused by having "Direct capture" enabled in your Vipps or MobilePay account. Please change to "Reserve capture" and the issue should be resolved. Direct capture is not supported by the Shopify payment gateway.

See:
[Reserve and capture](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture).

## Can we use Express Checkout with Shopify?

The Shopify module is currently not supporting express checkout. We try to use default platform features for our official modules and due to some limitations with the platform it is not possible to use express checkout with the default shipping alternatives available from the module. We are constantly working on improvements on the module and will add support as soon as it is flexible enough to implement.


## What do the different order statuses in Shopify mean when combined with Vipps MobilePay?

In Shopify, you have two main statuses:

1. Financial status (is the order paid, refunded, cancelled, etc.?)
2. Fulfillment status (is the order sent, or not?)

### Financial status

There are multiple types available here, but the most common ones you might see is:

#### Authorized

With Vipps MobilePay, this means that the order is reserved, but no money have changed hands yet. The funds are reserved on the customers account, until you capture the order, and the funds will be deducted from the customers account, and you will receive it (minus fees).

All orders in authorized state should not be there for too long, because the reservations might expire if you don't capture them, typically within 7-14 days.

#### Pending

With Vipps MobilePay, this is a rare status, and often indicate that something is wrong with your account. This may be related to your Vipps MobilePay account being set to do "Direct Capture", which is not supported by the Vipps MobilePay gateway in Shopify. You should double-check your account if you get a lot of orders in "Pending" state.

#### Paid

When an order is successfully captured in Vipps MobilePay, it will be changed to the "Paid" state. This indicates that you will get the funds from the customer very soon. The order is "OK" and ready to be shipped.

#### Refunded / partially refunded

The title tells most of it, but when an order gets the "refunded" status, you have successfully refunded the order in Vipps MobilePay, either fully or partially. Remember that all orders that is captured, are refunded, not cancelled.

#### Cancelled

Orders that are not captured yet, will be cancelled if you choose to cancel them in Shopify Admin. If the order is captured (hence in "Paid" state), it will be refunded instead.

### Fulfillment status

These types are the most common:

1. `Unfulfilled`
2. `Partially fulfilled`
3. `Fulfilled`

These indicate whether you have shipped the order or not. Vipps does not take part in these statuses other than the default mechanisms in Shopify Admin. These can be used as usual, and do not indicate any status of the Vipps payment. Only the Financial status tells the status of the Vipps order.

## Other frequently asked questions

See:
[Knowledge base](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture/#what-is-the-difference-between-reserve-capture-and-direct-capture)
