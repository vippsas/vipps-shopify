<!-- START_METADATA
---
title: Vipps for Shopify
sidebar_position: 1
description: Provide Vipps payments for Shopify.
pagination_next: null
pagination_prev: null
---
END_METADATA -->

# Vipps for Shopify

![Support and development by Crude ](./docs/images/crude.svg#gh-light-mode-only)![Support and development by Crude](./docs/images/crude_dark.svg#gh-dark-mode-only)

![Vipps](./docs/images/vipps.png) *Available for Vipps.*

For a MobilePay payment plugin, please refer to [Vipps/MobilePay Checkout for Spotify](https://developer.vippsmobilepay.com/docs/plugins-ext/checkout-shopify/).

*This plugin is built and maintained by [Crude](https://crude.no/).*

<!-- START_COMMENT -->
💥 Please use the plugin pages on [https://developer.vippsmobilepay.com](https://developer.vippsmobilepay.com/docs/plugins-ext/shopify/). 💥
<!-- END_COMMENT -->

The plugin is available from the [Shopify app store](https://apps.shopify.com/vipps?locale=nb).

## Description

Official Vipps Payment for Shopify. More than 4.3 million Norwegians use Vipps. Give them a fast and familiar shopping experience.

This is the official Vipps plugin that provides a direct integration with Shopify. Now you can let your customers choose Vipps directly in the checkout.

You can also do important back office tasks such as capture and refund directly from Shopify. Easy for your customer and easy for you.

## Express Checkout

Vipps does not have a solution for Express Checkout in Shopify.
This is due to limitations on Shopify's side, and if Shopify makes changes that
make Express Checkout possible, we will add this functionality.

## Vipps Payment

When you enable this plugin, your customers will be able to choose Vipps as a payment method directly in the checkout. There is no need to go via a third party payment method. If your customer chooses Vipps, the customer fills in the contact information and is then asked to enter the phone number in the Vipps dialogue. Then the customer confirms the payment in the Vipps app. The order is now completed and are now stored in your Shopify store.

## How to get started

- Sign up to use [*Payment Integration*](https://vippsmobilepay.com/online/payment-integration).
- After 1-2 days, you will get an email with login details to the Merchant Portal, [portal.vippsmobilepay.com](https://portal.vippsmobilepay.com/), where you can get the API credentials.
- Download and configure.

For more details, see [Applying for services](https://developer.vippsmobilepay.com/docs/knowledge-base/applying-for-services/).

## How to get account keys from the merchant portal

1. Sign in to [portal.vippsmobilepay.com](https://portal.vippsmobilepay.com/).
2. In the *Developer* section, choose *Production Keys*. Here, you can find the merchant serial number (6 figures).
3. Click on *Show keys* under the *API keys* column to see *Client ID*, *Client Secret*, and *Vipps Subscription Key*.

See [How to find the API keys](https://developer.vippsmobilepay.com/docs/developer-resources/portal#how-to-find-the-api-keys).

## Installation

### Step 1 - Add the payment method

Go to *Settings* in your Shopify store, then click *Payments*. Click *Add payment method*.

![Step 1](./docs/images/Vipps2Shopify1.png)

### Step 2 - Connect the account

![Step 2](./docs/images/Vipps2Shopify2.png)

### Step 3 - Install the app

Read the privacy policy and then install the app.

![Step 3](./docs/images/Vipps2Shopify3.png)

### Step 4 - Fill in the Vipps API key information

You can find your keys, as described in
[API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/api-keys/).

![Step 4](./docs/images/Vipps2Shopify4.png)

### Step 5 - Activate Vipps payment

![Step 5](./docs/images/Vipps2Shopify5.png)

## What do the different order statuses mean?

See [Shopify Order statuses with Vipps](shopify-faq.md#what-do-the-different-order-statuses-in-shopify-mean-when-combined-with-vipps) for information regarding order statuses.

## How can I get help if I have any issues?

For issues with your Vipps for Shopify installation, [contact us](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3). For other issues, contact [Vipps](https://developer.vippsmobilepay.com/docs/contact/).

## FAQ

* [Shopify FAQ](shopify-faq.md)
* [Vipps Knowledge base](https://developer.vippsmobilepay.com/docs/knowledge-base)
