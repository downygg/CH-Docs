# Stellar (Lumens)

## Generate New Address

```
  POST /stellar/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet / testnet**|

## Check Balance Address

```
  POST /stellar/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet / testnet**                                           | Chain Network         |
| `from_address` | `string` | **GC4XHC2POPSUN4RNVGHZ7KPGWW5NX3GDT4OTW6WQNLDLMVP63KVFNUKV**    | Your Address          |

## Transfer Coin
```
  POST /stellar/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet / testnet**                                         | Chain Network        |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `secret`        | `string` | -                                                             | Secret Key           |
| `memo`          | `string` | -                                                             | Memo Transaction     |
