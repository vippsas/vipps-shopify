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
- Sign up to use Vipps på Nett [vipps.no/shopify](https://api.vippsbedrift.no/v1/partial/signup/vippspanett/shopify?utm_source=produktsideShopify&utm_medium=crude&utm_campaign=VippspanettShopify).
- After 1-2 days you will get an email with login details to Vipps Developer Portal, where you can get the API credentials
- Download and configure

# How to get Vipps account keys from Vipps Developer Portal

1. Sign in to the Vipps Portal at https://portal.vipps.no/ using Bank ID
2. Select the "Utvikler" ("Developer") tab and choose Production Keys. Here you can find the merchant serial number (6 figures)
3. Click on "Show keys" under the API keys column to see “Client ID”, “Client Secret” and “Vipps Subscription Key”

See: [Getting Started](https://github.com/vippsas/vipps-developers/blob/master/vipps-developer-portal-getting-started.md) with the Vipps Portal, and the Vipps eCommerce [FAQ](https://github.com/vippsas/vipps-ecom-api/blob/master/vipps-ecom-api-faq.md).

# Installation

1. Install the app here: https://vipps-for-shopify.herokuapp.com/shopify/installapp
2. Configure the Vipps app by filling in your API keys (API keys is available in the Vipps Developer Portal).
3. Then install the payment method, by following the instructions inside the app.

# How does it look like in Shopify?

Step 1
![Step 1](https://github.com/vippsas/vipps-shopify/raw/master/VippsforShopify-Github1.jpg?raw=true "Step 1.")
Step 2
![Step 2](https://github.com/vippsas/vipps-shopify/raw/master/VippsForShopify-Github4.jpg?raw=true "Step 2.")
Payment capture
![Payment capture](https://github.com/vippsas/vipps-shopify/raw/master/VippsforShopify-Github3.jpg?raw=true "Payment capture.")

# What does the different order statuses in Shopify actually mean together with Vipps?

See [Shopify Order statuses with Vipps](https://github.com/vippsas/vipps-shopify/blob/master/order-statuses.md) for information regarding order statuses.

# How can I get help if I have any issues?
For issues with your Vipps for Shopify installation contact us via our [support system here](https://vipps-shopify.atlassian.net/servicedesk/customer/portal/3). For other issues you should contact [Vipps](https://github.com/vippsas/vipps-developers/blob/master/contact.md).

# Shopify FAQ (mainly Vipps for Shopify app)
See the [Shopify FAQ](https://github.com/vippsas/vipps-shopify/blob/master/shopify-faq.md) we have created for more help with Shopify

# Vipps FAQ
See the [Vipps eCom API FAQ](https://github.com/vippsas/vipps-ecom-api/blob/master/vipps-ecom-api-faq.md) for more help with Vipps eCommerce.
