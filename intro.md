# CHainshub Documentation

## Endpoint
- Merchant Transaction Endpoint (https://adelaide.chainshub.id/api/transaction/create)
- Coin Transaction Endpoint (https://adelaide.chainshub.id/api/{coin_code}/{method})

## Available Coin Code 
- Tron -> `tron`
- Binance Smartchain -> `bsc`
- Avalance C-Chain -> `avax`
- Dogecoin -> `doge`
- Litecoin -> `ltc`
- Fantom -> `ftm`
- Usdt BEP20 -> `usdt`

## Available Method 
- `generate` for Generating Address
- `balance` for check coin balance
- `transfer` for transfer coin

## Authorization
Pass `Authorization` key on your request header with Api Key.

### Merchant Transaction Authorization 
- `Api Key` Find at Merchant > Merchant List

### Coin Transaction Authorization
- `Api Key` Find at Api Key Menu
