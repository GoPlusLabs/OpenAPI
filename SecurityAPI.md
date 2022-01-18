## 1. Get supported blockchains

>URL: https://api.gopluslabs.io/api/v1/supported_chains

>Method：GET

>Parameters: No Parameters

>Response:

Parameter|Description
---|---
code|`1` means success
message|`OK` for success, `Error message` for failure
result| supported blockchain list, in which `id` is the path for token security information API


```json
{
  "code": 1,
  "message": "OK",
  "result": [
    {
      "id": "1",
      "name": "ethereum"
    },
    {
      "id": "56",
      "name": "bsc"
    },
    {
      "id": "42161",
      "name": "arbitrum"
    },
    {
      "id": "137",
      "name": "polygon"
    },
    {
      "id": "128",
      "name": "heco"
    },
    {
      "id": "43114",
      "name": "avalanche"
    }
  ]
}
```

## 2. Get current security information of any tokens

>URL: https://api.gopluslabs.io/api/v1/token_security/{id}?contract_addresses=

>Method：GET

>Parameters:

Parameter|Description|Required
---|---|---
id|The `id` of the blockchain|Yes
contract_addresses|The contract address of tokens, comma separated and lowercased|Yes


>Response:

Parameter|Description
---|---
code|`1` means success
message|`OK` for success, `Error message` for failure

sample response for `https://api.gopluslabs.io/api/v1/token_security/56?contract_addresses=0x547a1d47be3890af07dbe2d641d36e2984dbf5da`:
```json
{
  "code": 1,
  "message": "OK",
  "result": {
    "0x547a1d47be3890af07dbe2d641d36e2984dbf5da": {
        "is_open_source": 1,
        "is_proxy": 0,
        "owner_address": "0x744aF9cBb7606BB040f6FBf1c0a0B0dcBA6385E5",
        "is_mintable": 1,
        "slippage_modifiable": 1,
        "is_blacklisted": 1,
        "is_whitelisted": 0,
        "can_take_back_ownership": 0,
        "transfer_pausable": 1,
        "is_honeypot": 0,
        "is_anti_whale": 0,
        "is_in_dex": 1,
        "dexs": [
            {
                "name": "PancakeV2",
                "liquidity": 1.350085492413504,
                "pair": "0x714876f7cc6978a44967aBaF89B5a947a3B4906d"
            }
        ],
        "buy_tax": -1,
        "sell_tax": -1,
        "holder_count": 115,
        "total_supply": "9829073597816940",
        "holders": [
            {
                "address": "0x4c46c1487114caedb6b687cc280a3843a13a5749",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "9000000000000000",
                "percent": "0.915651"
            },
            {
                "address": "0x8157789f5a5710ea73fb513745467c91c080a6a1",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "544495675406708.031895221640068061",
                "percent": "0.055396"
            },
            {
                "address": "0x94e5efa12063945e8420bad953957cf1a38b4266",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "207388633622433.650262684701488034",
                "percent": "0.021100"
            },
            {
                "address": "0xa180fe01b906a1be37be6c534a3300785b20d947",
                "is_locked": 0,
                "tag": "Binance: Hot Wallet 16",
                "is_contract": 0,
                "balance": "72565140320087.617773419248969361",
                "percent": "0.007383"
            },
            {
                "address": "0x714876f7cc6978a44967abaf89b5a947a3b4906d",
                "is_locked": 0,
                "tag": "PancakeSwap V2: Bossy Dog-BSC-USD",
                "is_contract": 0,
                "balance": "2193490344020.496645383595828923",
                "percent": "0.000223"
            },
            {
                "address": "0x64899def3e65ea4f3eb9317af332470796174098",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "1598397511519.545430580835518453",
                "percent": "0.000163"
            },
            {
                "address": "0xa693618f14f5cedbccc2bed086afabd2a61f3899",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "830086593532.244134097340162959",
                "percent": "0.000084"
            },
            {
                "address": "0x838b12f13ce59bb9ec8f3a737463b7c2e0fcf28c",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "300000000",
                "percent": "0.000000"
            },
            {
                "address": "0xfd48417ced58a470b4b46c4d6ec907320626c5d5",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "230000000",
                "percent": "0.000000"
            },
            {
                "address": "0x8e8670b89a9cef34c6b912c4bd5dd3bcf36192db",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "212296574.442954725762054946",
                "percent": "0.000000"
            }
        ],
        "lp_total_supply": "1704693.102131",
        "lp_holder_count": 3,
        "lp_holders": [
            {
                "address": "0x8157789f5a5710ea73fb513745467c91c080a6a1",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "1680371.847121530760972273",
                "percent": "0.985733"
            },
            {
                "address": "0xb1b9b4bbe8a92d535f5df2368e7fd2ecfb3a1950",
                "is_locked": 0,
                "tag": "",
                "is_contract": 0,
                "balance": "24321.255009529292961923",
                "percent": "0.014267"
            },
            {
                "address": "0x0000000000000000000000000000000000000000",
                "is_locked": 0,
                "tag": "Null Address: 0x000...000",
                "is_contract": 1,
                "balance": "0.000000000000001",
                "percent": "0.000000"
            }
        ]
    }
  }
}
```
