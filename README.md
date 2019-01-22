# XRP_Shopify_Payment_Sync

A solution for those who have begun accepting XRP via their Shopify website and utilized the order number
as the destination tag in order to match orders to payments.

This database will match destination tag from the XRP wallet to the order number in Shopify and then update order details.


Quick Overview:

Open the XRP-Shopify Payment Sync Access Database and enter in your API Key, API Password, Shopify Store Name and XRP Wallet Address. 
The USD Issuer Exchange is used during the exchange rate process to identify the proper XRP/USD exchange rate via the Ripple APIs, 
it is currently set to use Bitstamp. Allowable Difference is the USD amount you are willing to accept as a difference between what 
the customer sends to you in XRP and what it converts to in USD. 

If the USD amount received is higher than the total order price, the program will simply mark the order as paid in full. 
(You can either check your wallet or view the processed orders via the Processed Orders button to confirm dollar amounts.)

If the USD amount received is less than the total order price but is within your allowable difference amount 
(which should be set as a negative), then the program will mark the order as paid in full.

If the USD amount received is less than the total order price and is not within the allowable difference amount, then 
the program will mark the order partially paid and update it accordingly in Shopify.



The program will run every 5 minutes once you click Run, and the button will change to Stop upon clicking. 
You can leave it running in the background should you so desire. 

The program will connect to Shopify, obtain any orders that were processed using the gateway name XRP and that are pending payment.

The program then connects to your XRP wallet and downloads the last 50 transactions.

It then obtains the current exchange rates and calculates the difference between USD and XRP.

A query matches any orders from Shopify to your XRP wallet based on the destination tag.

Next based on the matching orders and calculations it will update Shopify accordingly either marking it as paid or partially paid.

Last it will save all the processed orders to a table which can be accessed via the Processed Orders button. 







If this database has helped you and you'd like to donate ( rTocauxk75yWyEhwo5QxHGwytweG7JXYD ) or if you'd like to 
experience some amazing coffee from our tocacoffee.com website, use code XRPChat and save 35% on your purchase!
