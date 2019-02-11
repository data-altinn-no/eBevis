# Introduction 
This is the Postman collection for running acceptance tests against eBevis Web API.

In order to run this, you will need a (test) Enterprise Certificate and a valid API-key from the [eBevis Developer Portal](https://ebevis.no). The certificate along with its private key needs to be in PEM-format.

For more information, see https://altinn.github.io/docs/guides/ebevis/

# Getting Started
1. Get and install Postman from https://www.getpostman.com/
2. Clone this repo to a local directory
3. Start Postman, and import the collection by clicking the "Import" button in the upper left and selecting `collection.json`
4. Import the environments (`*_postman_environments.json`) by clicking "Manage environments" (the cogwheel in the upper right). You usually only want the "staging"-environment.
5. Edit the environment and enter your API-key as the value for the variable `SubscriptionKey`. The other variables can be left as-is.
5. Set up client certificates
    1. Convert your Enterprise Certificate to a cert/key-pair in PEM-format. [See this site](https://www.sslshopper.com/article-most-common-openssl-commands.html) for tips on how to do this with OpenSSL.
    1. Click Settings (the wrench icon in the top right)
    2. Select the Certificates tab
    3. Hit Add Certificate
    4. Supply `api.ebevis.no` as host, and point CRT/KEY file to the certificate file and private key you made in step 1.
    5. Add a passphrase if applicable
    5. Click Add
