<!-- START_METADATA
---
title: Payments for Shopify
sidebar_position: 1
description: Enable fast, secure Nordic mobile payments with Vipps/MobilePay for Shopify checkout.
pagination_next: null
pagination_prev: null
section: Plugins
---
END_METADATA -->

# Payments for Shopify

![Support and development by Crude ](./docs/images/crude.svg#gh-light-mode-only)![Support and development by Crude](./docs/images/crude_dark.svg#gh-dark-mode-only)

*This plugin is built and maintained by [Crude](https://crude.no/)
and can be downloaded from the [Shopify App Store](https://apps.shopify.com/vipps).
For support, contact [Vipps/MobilePay for Shopify support](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3).*

<!-- START_COMMENT -->
💥 Please use the plugin pages on [https://developer.vippsmobilepay.com](https://developer.vippsmobilepay.com/docs/plugins-ext/shopify/). 💥
<!-- END_COMMENT -->

Enable customers to choose Vipps or MobilePay as a payment method directly in the checkout.

<div className="text-center my-8">
<a
href="https://apps.shopify.com/vipps"
target="_blank"
rel="noopener noreferrer"
className="inline-block bg-orange-500 hover:bg-orange-600 text-white font-bold text-base px-6  py-6 rounded-lg no-underline shadow-md transition-colors duration-200"
><span aria-hidden="true">📱</span> Download from Shopify App Store</a>
</div>

## Description

This is the official *Vipps/MobilePay Payment* plugin for Shopify. Let your customers choose Vipps/MobilePay directly in the checkout.

Branded locally as MobilePay in Denmark and Finland, and as Vipps in Norway. One platform gathering more than 11 million users and more than 400,000 merchants across the Nordics. Give your users an easy, fast and familiar shopping experience.

Increase your conversion rate by letting your customers pay with a fast, secure and convenient payment method. Vipps MobilePay allows users to make quick and easy payments using their mobile phone, without the need for entering credit card details or other sensitive information.

You can also do important back office tasks such as capture and refund directly from Shopify. Easy for your customer and easy for you.

:::tip Configure your online payment solution
This plugin can be used to configure either:

- **Online payments** - Accept Vipps/MobilePay payments on your existing checkout flow
- **Complete checkout solution** - Use Vipps/MobilePay as your primary checkout method

Both solutions provide seamless integration with Shopify's payment processing and order management.
:::

To add branding and order information, install the [Companion app](companion.md).

## Payment

When you enable this plugin, your customers will be able to choose Vipps or MobilePay as a payment method directly in the checkout. There is no need to go via a third party payment method. If your customer chooses Vipps or MobilePay, the customer fills in the contact information and is then asked to enter the phone number in the Vipps/MobilePay app. Then the customer confirms the payment in the Vipps/MobilePay app. The order is now completed and are now stored in your Shopify store.

**Please note:** We don't have a solution for *Express Checkout* in Shopify.
This is due to limitations on Shopify's side, and if Shopify makes changes that
make *Express Checkout* possible, we will add this functionality.

## How to get started

- Sign up to use [*Payment Integration*](https://vippsmobilepay.com/online/payment-integration) or [*Checkout*](https://vippsmobilepay.com/online/checkout).
- After 1–2 days, you will get an email with login details to the business portal, [portal.vippsmobilepay.com](https://portal.vippsmobilepay.com/), where you can get the API credentials.
- Download and configure.

## How to get account keys

1. Sign in to [portal.vippsmobilepay.com](https://portal.vippsmobilepay.com/).
2. In the *Developer* section, choose *Production Keys*. Here, you can find the merchant serial number (6 figures).
3. Click on *Show keys* under the *API keys* column to see *Client ID*, *Client Secret*, and *Ocp-Apim-Subscription-Key*.

See:

- [Logging in to the portal](https://developer.vippsmobilepay.com/docs/knowledge-base/portal#log-in)
- [How to find the API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/portal#how-to-find-the-api-keys)

## Installation

Make sure you have easy access to the API keys, by logging in to [portal.vippsmobilepay.com](https://portal.vippsmobilepay.com/) and find the correct API keys.

### Step 1 - Add the payment method

Go to *Settings* in your Shopify store, then click *Payments*. Click *Add payment method*.

![Step 1](docs/images/1InstallVippsMobilePay.png)

### Step 2 - Manage the account

![Step 2](docs/images/2InstallVippsMobilePay.png)

### Step 3 - Configure your account and select payment product

![Step 3](docs/images/3InstallVippsMobilePay.png)

### Step 4 - Fill in the API key information

You can find your keys, as described in
[API keys](https://developer.vippsmobilepay.com/docs/knowledge-base/api-keys/).

![Step 4](docs/images/4InstallVippsMobilePay.png)

### Step 5 - Activate Vipps MobilePay payment

![Step 5](docs/images/5InstallVippsMobilePay.png)

### Step 6 - Test

Do a few test orders against the production API keys to confirm that the integration is working without errors.

## Add branding to your store

To add Vipps or MobilePay logos and icons to your store, get the [Companion app](companion.md).

## What do the different order statuses mean?

See [Shopify Order statuses with Vipps MobilePay](shopify-faq.md#what-do-the-different-order-statuses-in-shopify-mean-when-combined-with-vipps-mobilepay) for information regarding order statuses.

## How can I get help if I have any issues?

For issues with your *Vipps/MobilePay for Shopify* installation, [contact us](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3).

For business-related issues, such as a deactivated sales unit, contact [Vipps MobilePay business support](https://help.vippsmobilepay.com/).

## FAQ

- [Shopify FAQ](shopify-faq.md)
- [Knowledge base](https://developer.vippsmobilepay.com/docs/knowledge-base)

## Support

For issues with the plugin, contact [Vipps/MobilePay for Shopify support](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3).
