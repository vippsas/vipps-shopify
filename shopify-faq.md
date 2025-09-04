<!-- START_METADATA
---
title: Vipps/MobilePay Shopify Plugins FAQ
description: Frequently asked questions for the Shopify plugins.
pagination_next: null
pagination_prev: null
---
END_METADATA -->

# Frequently asked questions

## In which countries can I use Vipps MobilePay?

You can use Vipps and MobilePay brands in Norway, Denmark, Finland, and Sweden.
For details, see [Offering Vipps MobilePay in the Nordics](https://developer.vippsmobilepay.com/docs/knowledge-base/across-borders/).

## For how long is an order reserved?

When a payment is completed with Vipps MobilePay, the money will be reserved.
You get the money when the order is set to "Complete" or the money is captured manually.

For MobilePay, this reservation period is 14 days, so you will need to ship and fulfill orders before this;
or to make an agreement with the customer to capture the money before this period is over.
For Vipps, the period is 180 days. Payments made by credit card can have a reservation period as short as 7 days.
See [Capture deadlines](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture/#capture-deadlines).

## How can I get the Vipps or MobilePay payment logo in the footer?

There is a limitation with Shopify's Payments App API, which doesn't currently support adding payment method logos in the footer.
So, to get around this for adding logos and icons, you need the [Companion app](companion.md).

This also lets you add more payment information into the app.

<!-- START_HIDDEN_IN_GITHUB
<details>
<summary>Deprecated method</summary>
<div>
END_HIDDEN_IN_GITHUB -->

Alternatively, to add the Vipps or MobilePay logo in the footer, you'll can the theme files by adding/editing a line of code in your footer or where you'll want the logos to appear. An example would be, but needs testing in your shop before using:

```liquid
{% assign enabled_payment_types = 'vipps,payment_2,payment_3' | remove: ' ' | split: ',' %}
```

<!-- START_HIDDEN_IN_GITHUB
</div>
</details>
END_HIDDEN_IN_GITHUB -->

## The order that comes from Vipps MobilePay is labelled authorized, what does that mean?

The order's status is "Reserved" in Vipps MobilePay. The amount is only reserved and not
captured from the customers account. When the order is completed, you can capture
the payment. You can either do this inside each order by clicking the button
*capture*, or by marking more orders and choose the *Actions* dropdown, and then click *Capture payments*.

According to Norwegian regulations you should not capture a payment until the
product or service is provided to the customer. For more information,
please see the Norwegian Consumer Authority's
[Guidelines for the standard sales conditions for consumer purchases of goods over the internet](https://www.forbrukertilsynet.no/english/guidelines/guidelines-the-standard-sales-conditions-consumer-purchases-of-goods-the-internet).

## How to fix problems with authentication

The most common problem is using API keys for the wrong environment.

Double-check that you are using the correct production API keys (not test keys)
and the correct production Merchant Serial Number.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/api-keys/).

## Customers are getting error messages when they are trying to check out

See:
[How to fix problems with authentication](#how-to-fix-problems-with-authentication).

## I do not receive any Vipps or MobilePay orders

See:
[How to fix problems with authentication](#how-to-fix-problems-with-authentication).

## I get `Error 2734583247: Order is not reserved`

This is often caused by having "Direct capture" enabled in your Vipps or MobilePay account. Please change to "Reserve capture" and the issue should be resolved. Direct capture is not supported by the Shopify payment gateway.

See:
[Reserve and capture](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture).

## Can we use Express Checkout with Shopify?

The Shopify module does not currently support express checkout. We try to use default platform features for our official modules and, due to some limitations with the platform, it is not possible to use express checkout with the default shipping alternatives available from the module. We will add support as soon as it is flexible enough to implement.

## What do the different order statuses in Shopify mean when combined with Vipps MobilePay?

In Shopify, you have two main statuses:

1. Financial status (is the order paid, refunded, cancelled, etc.?)
2. Fulfillment status (is the order sent, or not?)

### Financial status

There are multiple types available here, but the most common ones you might see are described here.

#### Authorized

With Vipps MobilePay, the "Authorized" status means that the order is reserved, but no money has changed hands yet. The funds are reserved on the customers account until you capture the order. That is when the funds are deducted from the customers account, and you will receive it (minus fees).

All orders in authorized state should be resolved quickly, because the reservations might expire if you don't capture them, typically within 7–14 days.

#### Pending

With Vipps MobilePay, "Pending" is a rare status, and often indicates that something is wrong with your account. This may be related to your Vipps MobilePay account being set to do "Direct Capture", which is not supported by the Vipps MobilePay gateway in Shopify. You should double-check your account if you often get orders in "Pending" state.

#### Paid

When an order is successfully captured in Vipps MobilePay, the status will be changed to "Paid". This indicates that you will get the funds from the customer very soon. The order is "OK" and ready to be shipped.

#### Refunded / partially refunded

When an order gets the "refunded" status, you have successfully refunded the order in Vipps MobilePay, either fully or partially. Remember that all orders that are captured, can be refunded, not cancelled.

#### Cancelled

Orders with the "Cancelled" state we cancelled before being captured. Orders that are not captured yet, will be cancelled if you choose to cancel them in Shopify Admin. If the order is captured (hence in "Paid" state), it will be refunded instead.

### Fulfillment status

These types are the most common:

1. `Unfulfilled`
2. `Partially fulfilled`
3. `Fulfilled`

These indicate whether you have shipped the order or not. Vipps MobilePay does not take part in these statuses other than the default mechanisms in Shopify Admin. These can be used as usual, and do not indicate any status of the payment. Only the Financial status tells the status of the order.

## Other frequently asked questions

See:
[Knowledge base](https://developer.vippsmobilepay.com/docs/knowledge-base/reserve-and-capture/#what-is-the-difference-between-reserve-capture-and-direct-capture)
