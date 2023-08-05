  # Algorand

## Generate New Address

```
  POST /algorand/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet / testnet**|

## Check Balance Address

```
  POST /algorand/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet / testnet**                                           | Chain Network         |
| `from_address` | `string` | **E2RR5JRUBII5LD6OVRL2KYJKVHCKN37SHHHBBNUEWKE6PJWYILDH5YIZJI**  | Your Address          |

## Transfer Coin
```
  POST /algorand/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet / testnet**                                         |-                     |
| `from_address`  | `string` | **E2RR5JRUBII5LD6OVRL2KYJKVHCKN37SHHHBBNUEWKE6PJWYILDH5YIZJI**| Your Address         |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `secret`        | `string` | -                                                             | Secret Key           |
