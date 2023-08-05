# Bitcoin Cash

## Generate New Address

```
  POST /bch/generate
```

| Parameter | Type     | Value                |
| :-------- | :------- | :--------------------|
| `network` | `string` | **mainnet**          |

## Check Balance Address

```
  POST /bch/balance
```

| Parameter      | Type     | Value                                                           | Description           |
| :------------- | :------- | :---------------------------------------------------------------|:----------------------|
| `network`      | `string` | **mainnet**                                                     | Chain Network         |
| `from_address` | `string` | **bitcoincash:qzfsgpklwrkm5hxhqur82jpjmq2uuvxf45paxwt8nd**      | Your Address          |

## Transfer Coin
```
  POST /bch/transfer
```

| Parameter       | Type     | Value                                                         | Description          |
| :--------       | :------- | :-------------------------------------------------------------|:---------------------|
| `network`       | `string` | **mainnet**                                                   | Chain Network        |
| `amount`        | `string` | **5**                                                         | Amount Transfer      |
| `to_address`    | `string` | -                                                             | Destination Address  |
| `wif`           | `string` | -                                                             | Wif Key              |
