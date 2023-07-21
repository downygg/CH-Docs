# Tron

## Generate New Address

```
  POST /tron/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet**          |

## Check Balance Address

```
  POST /tron/balance
```

| Parameter | Type     | Value                                   | Description           |
| :-------- | :------- | :---------------------------------------|:----------------------|
| `network` | `string` | **mainnet**                             |-                      |
| `address` | `string` | **TAWE8B9DXDgTmfr3bhFsjZ4U8Jx4nFTTTT**  | Your Address          |

## Transfer Coin
```
  POST /tron/transfer
```

| Parameter       | Type     | Value                                 | Description          |
| :--------       | :------- | :-------------------------------------|:---------------------|
| `network`       | `string` | **mainnet**                           |-                     |
| `from_address`  | `string` | **TAWE8B9DXDgTmfr3bhFsjZ4U8Jx4nFTTTT**| Your Address         |
| `amount`        | `double` | **5**                                 | Amount Transfer      |
| `to_address`    | `string` | -                                     | Destination Address  |
| `private_key`   | `string` | -                                     | Address Private Key  |



