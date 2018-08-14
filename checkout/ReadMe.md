
*****************************************************************************************

# Getting Started

Download the php folder from the above repository.You can refer [here](https://stackoverflow.com/questions/7106012/download-a-single-folder-or-directory-from-a-github-repo) to download a single folder from the repository.

## Pre-requisites

```
1)Apache web server
2)Ruby on Rails
```

## How to start

Below we describe the Ruby integration for Cashfree PG. You'll need Cashfree credentials for this setup to work. You can access the credentials from the merchant dashboard (API access > credentials) [here](https://test.gocashfree.com/merchant/pg#api-key).

**Step 1**

  -Open the project(pgsim) in terminal and type the below commands

    ```
    rails server
    ```

  - Open the file *request.php*, and update the value of the variable *$mode* to "TEST"(for testing) or "PROD"(for production) depending on your environment.

  - Update the variable *$secretKey* with the correct value for the mode you have selected in *request.php* and *response.php* files.

**Step 2**

  - Visit *localhost/php/start.php* in the browser, fill in the details as required, set the returnUrl as *localhost/php/response.php* and click Submit.

  - Once the payment page loads, enter the following card details for testing purpose. 
  
  ```
  Card Number : 4111 1111 1111 1111
  CVV : 123
  ```
  You can enter any name, month and year for card expiration. For more details around test cards, see [Test Data](https://docs.cashfree.com/docs/resources/#test-data).

**Step 3**

  - Once you've entered the details you will be redirected to the Cashfree PG Simulator page. Here you can simulate either a failed or a successful transaction. You will then be redirected to the *returnUrl*(given in step 2) with the transaction details.

**NOTE :** 

- In the file request.php, please make sure that you are using the correct integration mode. 
- Give a valid returnUrl, since all the transaction details will be sent to it.
- It is imperative that you process the response correctly to prevent any fraud on your website. 

## Support

For further queries reach us at [techsupport@gocashfree.com](techsupport@gocashfree.com). 

*****************************************************************************************
