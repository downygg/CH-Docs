# The Open Network (TON)

## Generate New Address

```
  POST /ton/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet / testnet**|

## Check Balance Address

```
  POST /ton/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet / testnet**                                           | Chain Network         |
| `from_address` | `string` | **EQBh6rIjQE42tIXuwSjaLMnbHOdOHsL9yC_M78ySzIO6HZI5**            | Your Address          |

## Transfer Coin
```
  POST /ton/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet / testnet**                                         | Chain Network        |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `memo`          | `string` | -                                                             | Memo Transaction     |
| `mnemonic`      | `json`   | -                                                             | Mnemonic Address     |
