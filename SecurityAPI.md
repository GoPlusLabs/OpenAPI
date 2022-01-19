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
            "name": "eth"
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

sample response for `https://api.gopluslabs.io/api/v1/token_security/1?contract_addresses=0x408e41876cccdc0f92210600ef50372656052a38`:
```json
{
    "code": 1,
    "message": "OK",
    "result": {
        "0x408e41876cccdc0f92210600ef50372656052a38": {
            "is_open_source": "1",
            "is_proxy": "0",
            "is_in_dex": "1",
            "owner_address": "0x0000000000000000000000000000000000000001",
            "is_mintable": "0",
            "slippage_modifiable": "0",
            "is_blacklisted": "0",
            "is_whitelisted": "0",
            "can_take_back_ownership": "0",
            "transfer_pausable": "1",
            "is_honeypot": "0",
            "dexs": [
                {
                    "name": "SushiSwapV2",
                    "liquidity": "2981850.51781834",
                    "pair": "0x611CDe65deA90918c0078ac0400A72B0D25B9bb1"
                },
                {
                    "name": "UniswapV2",
                    "liquidity": "634935.23490144",
                    "pair": "0x8Bd1661Da98EBDd3BD080F0bE4e6d9bE8cE9858c"
                },
                {
                    "name": "UniswapV3",
                    "liquidity": "96434.22749409106546130204818368792",
                    "pair": "0x2dd56b633faa1a5b46107d248714c9ccb6e20920"
                },
                {
                    "name": "UniswapV3",
                    "liquidity": "6965.914985999999999999999999999999",
                    "pair": "0x8dd240195b2cd7c0a118166cba02512f52e9e360"
                },
                {
                    "name": "UniswapV3",
                    "liquidity": "6463.504842668805484531793163914657",
                    "pair": "0x08eac73f000d724678281155c879c50fc6094824"
                },
                {
                    "name": "UniswapV2",
                    "liquidity": "2108.20817495",
                    "pair": "0x5e4206B6AA6e919B2bc6E813EA0ffB9B3C8aC042"
                },
                {
                    "name": "SushiSwapV2",
                    "liquidity": "427.58647288",
                    "pair": "0x07d04AaAd8108ca86e0F1c792Bf165f63A5FedDE"
                },
                {
                    "name": "UniswapV2",
                    "liquidity": "290.79024973",
                    "pair": "0x07F068ca326a469Fc1d87d85d448990C8cBa7dF9"
                },
                {
                    "name": "UniswapV2",
                    "liquidity": "15.70976724",
                    "pair": "0x2d0A1c45cD6f7CDb718703d0897c877EFc9dB9F7"
                }
            ],
            "buy_tax": "0",
            "sell_tax": "0",
            "holder_count": "58345",
            "total_supply": "999999632.80375",
            "holders": [
                {
                    "address": "0x60ab11fe605d2a2c3cf351824816772a131f8782",
                    "is_locked": 0,
                    "tag": "RenVM: Darknode Staking",
                    "is_contract": 1,
                    "balance": 180300000,
                    "percent": 0.1803
                },
                {
                    "address": "0xbe0eb53f46cd790cd13851d5eff43d12404d33e8",
                    "is_locked": 0,
                    "tag": "Binance 7",
                    "is_contract": 0,
                    "balance": 78596041,
                    "percent": 0.078596
                },
                {
                    "address": "0x56a298549d4c4ea4bbae1e7dbc17f01cecbd134c",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 55840471.1137,
                    "percent": 0.05584
                },
                {
                    "address": "0xcc12abe4ff81c9378d670de1b57f8e0dd228d77a",
                    "is_locked": 0,
                    "tag": "Aave: aREN Token V2",
                    "is_contract": 1,
                    "balance": 42652557.55216556,
                    "percent": 0.042653
                },
                {
                    "address": "0xf977814e90da44bfa03b6295a0616a897441acec",
                    "is_locked": 0,
                    "tag": "Binance 8",
                    "is_contract": 0,
                    "balance": 31869917,
                    "percent": 0.03187
                },
                {
                    "address": "0x28c6c06298d514db089934071355e5743bf21d60",
                    "is_locked": 0,
                    "tag": "Binance 14",
                    "is_contract": 0,
                    "balance": 24200509.363724675,
                    "percent": 0.024201
                },
                {
                    "address": "0x5a27dbbff05f36dc927137855e3381f0c20c1cdd",
                    "is_locked": 0,
                    "tag": "barbellcap.eth",
                    "is_contract": 0,
                    "balance": 16698561.151978942,
                    "percent": 0.016699
                },
                {
                    "address": "0x8d6f396d210d385033b348bcae9e4f9ea4e045bd",
                    "is_locked": 0,
                    "tag": "Gemini 6",
                    "is_contract": 1,
                    "balance": 13190001,
                    "percent": 0.01319
                },
                {
                    "address": "0x2faf487a4414fe77e2327f0bf4ae2a264a776ad2",
                    "is_locked": 0,
                    "tag": "FTX Exchange",
                    "is_contract": 0,
                    "balance": 11743699.406551864,
                    "percent": 0.011744
                },
                {
                    "address": "0x3dfd23a6c5e8bbcfc9581d2e864a68feb6a076d3",
                    "is_locked": 0,
                    "tag": "Aave: Lending Pool Core V1",
                    "is_contract": 1,
                    "balance": 11582819.641038848,
                    "percent": 0.011583
                }
            ],
            "lp_holder_count": "18",
            "lp_total_supply": "56774.406833359",
            "lp_holders": [
                {
                    "address": "0xc2edad668740f1aa35e4d8f227fb8e17dca888cd",
                    "is_locked": 0,
                    "tag": "SushiSwap: MasterChef LP Staking Pool",
                    "is_contract": 1,
                    "balance": 56620.25850449379,
                    "percent": 0.997285
                },
                {
                    "address": "0x5ad6211cd3fde39a9cecb5df6f380b8263d1e277",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 82.44701298242764,
                    "percent": 0.001452
                },
                {
                    "address": "0x3262e972cfd24d942adbeac06401900bffe8c460",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 25.612412485050267,
                    "percent": 0.000451
                },
                {
                    "address": "0x6300a843dbfc8f328da7db5b27cc50c796b3eca8",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 19.881271010209034,
                    "percent": 0.00035
                },
                {
                    "address": "0xe7237c145bba62500d7089afa6cc58cbd7ab28b3",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 13.193117876666262,
                    "percent": 0.000232
                },
                {
                    "address": "0x8cb20f59e717d2debac27c7271370dc365f77be7",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 3.6649273869192607,
                    "percent": 6.5e-5
                },
                {
                    "address": "0x7822159ee394d14745cde63a706f965fb73c7ac8",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 2.899154230862371,
                    "percent": 5.1e-5
                },
                {
                    "address": "0x760f7de3389b857fa0f72a5cb618e2f2ee5fe003",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 1.4415181625500633,
                    "percent": 2.5e-5
                },
                {
                    "address": "0x186e20ae3530520c9f3e6c46f2f5d1062b784761",
                    "is_locked": 0,
                    "tag": "lawpanda.eth",
                    "is_contract": 0,
                    "balance": 1.3352582736569354,
                    "percent": 2.4e-5
                },
                {
                    "address": "0x43f22c5f91a2891c6e6cb5d849ed94b62d283331",
                    "is_locked": 0,
                    "tag": "",
                    "is_contract": 0,
                    "balance": 1.145068758713511,
                    "percent": 2.0e-5
                }
            ]
        }
    }
}
```
