# Merchant Transaction

## Create Invoice

```
  POST /transaction/create
```

| Parameter        | Type     | Example Value                              | Description    |
| :--------        | :------- | :------------------------------------------|:----------------|
| `currency`       |`string`  | **bsc**                                    | Available Value: `bsc`,`ftm`,`matic`,`solana`,`trx`,`doge`,`ltc`
| `merchant_ref`   |`string`  | **INVOICE-001**                           | Merchant Identifier 
| `customer_email` |`string`  | **customer@gmail.com**                     | Customer Email
| `customer_name`  |`string`  |**James Bond**                              | Customer Name
| `pair`           |`string`  |**idr**                                     | Available Pair: `idr`,`crypto`
| `redirect_url`   |`string`  |**https://yourwebsite.com/callback=success**|Redirect page when payment completed|
| `cancel_turl`    |`string`  |**https://yourwebsite.com/callback=failed** |Redirect page when payment expired|
| `amount`         |`string`  |**10000**                                   |Amount Base on Pair
| `signature`      |`string`  |**-**                                       |The signature is made from 4 pieces of data which are combined, namely `merchant_ref`, `currency`, `pair` and `amount` with the HMAC-SHA256 algorithm which is locked with the merchant's private key so that it becomes a hash

## Example Generating Signature
   - PHP
       ```
       <?php

          $privateKey   = 'your_merchant_private_key';
          $merchant_ref = 'INVOICE-001';
          $currency     = 'bsc';
          $pair         = 'idr';
          $amount       = '10000';
          
          $signature = hash_hmac('sha256', $merchant_ref.$currency.$pair.$amount, $privateKey);
        ?>
       ```
   - Python
       ```
          import hmac
          import hashlib
          
          privateKey   = 'your_merchant_private_key';
          merchant_ref = 'INVOICE-001';
          currency     = 'bsc';
          pair         = 'idr';
          amount       = '10000';
          
          signStr   = "{}{}{}{}".format(merchant_ref, currency, pair, amount)
          signature = hmac.new(bytes(privateKey,'latin-1'), bytes(signStr,'latin-1'), hashlib.sha256).hexdigest()
       ```
   - NodeJs
       ```
          const crypto = require('crypto')
          
          var privateKey   = 'your_merchant_private_key';
          var merchant_ref = 'INVOICE-001';
          var currency     = 'bsc';
          var pair         = 'idr';
          var amount       = '10000';
          
          var signature = crypto.createHmac('sha256', privateKey)
              .update(merchant_ref + currency + pair + amount)
              .digest('hex');
       ```
    
## Callback Handle
   Callback Data will be send base on URL at Merchant Setting.

   - PHP Example
     ```
     <?php
        // Get POST Data
        $post_data = file_get_contents('php://input');

        // Get All Header Request
        $header = apache_request_headers();

        // Get CH Event Data
        $event = (isset($header['CH-EVENT']) ? $header['CH-EVENT'] : null);

        // Get Incomming Signature
        $incoming_signature = (isset($header['CH-CALLBACK-SIGNATURE']) ? $header['CH-CALLBACK-SIGNATURE'] : 'null');

        // Define Your Private key
        $private_key = 'YOUR MERCHANT PRIVATE KEY';

        // Rebuild Your Signature
        $signature = hash_hmac('sha256', $post_data, $private_key);

        // Compare Incoming Signature between Local Signature
        if(!hash_equals($incoming_signature,$signature)) {
            die('Signature Invalid');
        }

        // Decode Post Data
        $data = json_decode($post_data,true);

        // Define Your Pass Key
        // Available Key : Completed , Amount Received
        $success_mark = array("Completed");
    
        if(in_array($data['transaction_status'],$success_mark)) {
            $merchant_ref = $data['merchant_ref'];
            // Do Action Base On Merchant Ref to process success payment
        } elseif($pl['transaction_status'] == 'Transaction Expired') {
            $merchant_ref = $data['merchant_ref'];
           // Do Action Base On Merchant Ref to process expired payment
        } else {
           // Do Anything
        }
     ```
     
