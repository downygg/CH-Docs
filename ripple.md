# Ripple (XRP)

## Generate New Address

```
  POST /xrp/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet / testnet**|

## Check Balance Address

```
  POST /xrp/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet / testnet**                                           | Chain Network         |
| `from_address` | `string` | **rMUJftHNRdqiRECJFvYJPCTZL292CG8Nei**                          | Your Address          |

## Transfer Coin
```
  POST /xrp/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet / testnet**                                         | Chain Network        |
| `from_address`  | `string` | **rMUJftHNRdqiRECJFvYJPCTZL292CG8Nei**                        | Your Address         |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `seed`          | `string` | -                                                             | Secret Seed Key      |
| `tag`           | `number` | -                                                             | Destination Tag      |
