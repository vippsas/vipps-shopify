# Frequently asked questions

## In which countries can I use Vipps?

You can only get paid by users who have Vipps. At the moment Vipps is only available i Norway.

## The orders who comes from Vipps is labeled “authorized”, what does that mean?

The orders status is “reserved” in Vipps. The amount is only reserved and not
captured from the customers account. When the order is completed, you can capture
the payment. You can either do this inside each order by clicking the button
“capture”, or by marking more orders and choose the “actions” dropdown, and then click “capture payments”.

According to Norwegian regulations you should not capture a payment until the
product or service is provided to the customer. For more information,
please see the The Norwegian Consumer Authority's
[Guidelines for the standard sales conditions for consumer purchases of goods over the internet](https://www.forbrukertilsynet.no/english/guidelines/guidelines-the-standard-sales-conditions-consumer-purchases-of-goods-the-internet).

## Customers are getting error messages when they are trying to check out with Vipps.

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://github.com/vippsas/vipps-developers/blob/master/vipps-getting-started.md#getting-the-api-keys).

## I do not receive any Vipps orders?

Your API keys are most likely wrong. Double check that all of your keys
(also merchant serial number) is correct and that it is production keys
and not test keys.

Remember that you have your own merchant serial number for your production
keys and another merchant serial number from your test keys.
This is easy to miss.

See:
[Getting the API keys](https://github.com/vippsas/vipps-developers/blob/master/vipps-getting-started.md#getting-the-api-keys).

## I get a error saying "Application error" when trying to checkout

This is mostly caused by incorrect Gateway password and Gateway username in the
Vipps payment method in Shopify settings. Ensure that you have input the
correct username and password instructed within the Vipps App in Shopify.
The username and password are generated and shown there.

## I get `ERRORCODE 5473`

This is mostly caused by incorrect Gateway password and Gateway username in the
Vipps payment method in Shopify settings. Ensure that you have input the
correct username and password instructed within the Vipps App in Shopify.
The username and password are generated and shown there.

## Can we use Vipps Express Checkout with Shopify?
The Shopify module is currently not supporting express checkout. We try to use default plattform features for our official modules and due to some limitations with the plattform it is not possible to use express checkout with the default shipping alternatives available from the module. We are constantly working on improvements on the module and will add support as soon as it is flexible enough to implement. 

## Other frequently asked questions

See:
[Vipps eCommerce API: Frequently Asked Questions](https://github.com/vippsas/vipps-ecom-api/blob/master/vipps-ecom-api-faq.md#what-is-the-difference-between-reserve-capture-and-direct-capture)

