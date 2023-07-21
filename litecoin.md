  # Litecoin

## Generate New Address

```
  POST /ltc/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet**          |

## Check Balance Address

```
  POST /ltc/balance
```

| Parameter      | Type     | Value                                   | Description           |
| :------------- | :------- | :---------------------------------------|:----------------------|
| `network`      | `string` | **mainnet**                             |-                      |
| `from_address` | `string` | **LfmssDyX6iZvbVqHv6t9P6JWXia2JG7mdb**  | Your Address          |

## Transfer Coin
```
  POST /ltc/transfer
```

| Parameter       | Type     | Value                                    | Description          |
| :--------       | :------- | :----------------------------------------|:---------------------|
| `network`       | `string` | **mainnet**                              |-                     |
| `from_address`  | `string` | **LfmssDyX6iZvbVqHv6t9P6JWXia2JG7mdb**   | Your Address         |
| `amount`        | `double` | **0.005**                                | Amount Transfer      |
| `to_address`    | `string` | -                                        | Destination Address  |
| `private_key`   | `string` | -                                        | Address Private Key  |
| `fees`          | `double` | **0.0001**                               | Minner Fee           |
| `public_key`    | `string` | -                                        | Address Public Key   |
