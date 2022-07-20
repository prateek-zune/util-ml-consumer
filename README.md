# Utils
A spring boot application for miscellaneous requirements like asset_provider lookup, etc

This project contains 1 major application currently:
1. Asset Provider Lookup
=> This application helps customers search for assets across different providers (not limited to PCT).

For example -> There is one customer NETS, who wants an Asset Provider Lookup Page, on which there will be different proviers which the customer has access to.
The assets can be of any of the providers which belong to customer.

For this to happen, there's a single page web app in folder "asset-provider-lookup" which looks for the customer name in the URL. And based on the customer name found in URL, it would go and check for that customer's provider in the DB.

For example -> NETS URL - nets.trackmytrailer.net -> from this URL, "nets" will be fetched in angular and based on this customer name, providers will be fecthed from DB via spring boot backend code.

This was done to make sure that we don't keep creating a new page for every customer, instead we create a single page and redirect all the customers via sub-domain through Route53 or some other redirection server.

Glimpse of the NETS website in production:

![image](https://user-images.githubusercontent.com/63440956/146963052-f1d45e3b-9bc8-4c85-8b11-7d27a5916e13.png)
