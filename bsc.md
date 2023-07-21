# Binance Smartchain

## Generate New Address

```
  POST /bsc/generate
```

| Parameter | Type     | Value                      |
| :-------- | :------- | :--------------------------|
| `network` | `string` | **mainnet** / **testnet**  |

## Check Balance Address

```
  POST /bsc/balance
```

| Parameter      | Type     | Value                                           | Description           |
| :------------- | :------- | :-----------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet** / **testnet**                       |-                      |
| `from_address` | `string` | **0x57848181Fdd07EF34BC33a3e3Ac799D88C93f4D6**  | Your Address          |

## Transfer Coin
```
  POST /bsc/transfer
```

| Parameter       | Type     | Value                                            | Description          |
| :--------       | :------- | :------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet** / **testnet**                        |-                     |
| `from_address`  | `string` | **0x57848181Fdd07EF34BC33a3e3Ac799D88C93f4D6**   | Your Address         |
| `amount`        | `double` | **0.005**                                        | Amount Transfer      |
| `to_address`    | `string` | -                                                | Destination Address  |
| `private_key`   | `string` | -                                                | Address Private Key  |
| `gas`           | `string` | **21000**                                        | Gas Limit            |
| `gasprice`      | `string` | **10**                                           | Gas Price in Gwei    |
