# Vipps for Shopify

The Vipps product page is here: https://www.vipps.no/produkter-og-tjenester/bedrift/ta-betalt-paa-nett/ta-betalt-paa-nett/shopify/

See the main GitHub page for Vipps contact information, etc: https://github.com/vippsas 

# Description

Official Vipps Payment for Shopify. More than 3.6 million Norwegians use Vipps. Give them a fast and familiar shopping experience.

This is the official Vipps plugin that provides a direct integration with Shopify. Now you can let your customers choose Vipps directly in the checkout.

You can also do important back office tasks such as capture and refund directly from Shopify. Easy for your customer and easy for you.

Read [information from Vipps](https://www.vipps.no/produkter-og-tjenester/bedrift/ta-betalt-paa-nett/ta-betalt-paa-nett/shopify/) about the plugin.

# Vipps Express Checkout

Vipps does not yet have a solution for express checkout in Shopify

# Vipps Payment
When you enable this plugin, your customers will be able to choose Vipps as a payment method directly in the checkout. There is no need to go via a third party payment method. If your customer choose Vipps, the customer fills in their contact information and is then asked to enter their phone number in the Vipps dialogue. Then the customer confirms the payment in the Vipps app. The order is now completed and are now stored in your Shopify store.

# How to get started
- Sign up to use Vipps på Nett [vipps.no/shopify](https://www.vipps.no/produkter-og-tjenester/bedrift/ta-betalt-paa-nett/ta-betalt-paa-nett/shopify/).
- After 1-2 days you will get an email with login details to Vipps Developer Portal, where you can get the API credentials
- Download and configure

# Installation
1. Install the app here.
2. Configure the Vipps app by filling in your API keys (API keys is available in the Vipps Developer Portal, info in the section below).
3. Then install the payment method, by following the instructions inside the app.

# How to get Vipps account keys from Vipps Developer Portal

1. Sign in to the Vipps Portal at https://portal.vipps.no/ using Bank ID
2. Select the "Utvikler" ("Developer") tab and choose Production Keys. Here you can find the merchant serial number (6 figures)
3. Click on "Show keys" under the API keys column to see “Client ID”, “Client Secret” and “Vipps Subscription Key”

See: [Getting Started](https://github.com/vippsas/vipps-developers/blob/master/vipps-developer-portal-getting-started.md) with the Vipps Portal, and the Vipps eCommerce [FAQ](https://github.com/vippsas/vipps-ecom-api/blob/master/vipps-ecom-api-faq.md).

# Frequently asked questions

**_In which countries can I use Vipps?_**

You can only get paid by users who have Vipps. At the moment Vipps is only available i Norway.

**_The orders who comes from Vipps is labeled “authorized”, what does that mean?_**

The orders status is “reserved” in Vipps. The amount is only reserved and not captured from the customers account. When the order is completed, you can capture the payment. You can either do this inside each order by clicking the button “capture”, or by marking more orders and choose the “actions” dropdown, and then click “capture payments”.

**_Customers are getting error messages when they are trying to check out with Vipps._**

Your API keys are most likely wrong. Double check that all of your keys (also merchant serial number) is correct and that it is production keys and not test keys.

Remember that you have your own merchant serial number for your production keys and another merchant serial number from your test keys. This is easy to miss.

**_I do not receive any Vipps orders?_**

Your API keys are most likely wrong. Double check that all of your keys (also merchant serial number) is correct and that it is production keys and not test keys.

Remember that you have your own merchant serial number for your production keys and another merchant serial number from your test keys. This is easy to miss.

# How can I get help if I have any issues?
For issues with your Vipps for Shopify installation contact us via our [support system here](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3). For other issues you should contact [Vipps](https://github.com/vippsas/vipps-developers/blob/master/contact.md).

# Vipps FAQ
See the [Vipps eCom API FAQ](https://github.com/vippsas/vipps-ecom-api/blob/master/vipps-ecom-api-faq.md) for more help with Vipps eCommerce.
