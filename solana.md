# Solana

## Generate New Address

```
  POST /solana/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet / testnet**|

## Check Balance Address

```
  POST /solana/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet / testnet**                                           | Chain Network         |
| `from_address` | `string` | **HiLfaP2J1mZLJFMVtLoHktui5ds3RjL8mUKcWMVkQnub**                | Your Address          |

## Transfer Coin
```
  POST /solana/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet / testnet**                                         | Chain Network        |
| `from_address`  | `string` | **HiLfaP2J1mZLJFMVtLoHktui5ds3RjL8mUKcWMVkQnub**              | Your Address         |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `secret`        | `string` | -                                                             | Secret Key           |
