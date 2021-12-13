## 1. Get supported blockchains

>URL: https://api.gopocket.security/supported_chains

>Method：GET

>Parameters: No Parameters

>Response:

Parameter|Description
---|---
status|`1` means success
message|`OK` for success, `Error message` for failure
result| supported blockchain list, in which `id` is the path for token security information API


```json
{
  "status": "1",
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

>URL: https://api.gopocket.security/id?contract_addresses=

>Method：GET

>Parameters:

Parameter|Description|Required
---|---|---
id|The `id` of the blockchain|Yes
contract_addresses|The contract address of tokens, comma separated and lowercased|Yes


>Response:

Parameter|Description
---|---
status|`1` means success
message|`OK` for success, `Error message` for failure
level|`danger`/`warn`/`safe`

sample response for `https://api.gopocket.security/137?contract_addresses=0x8ae127d224094cb1b27e1b28a472e588cbcc7620,0xb33eaad8d922b1083446dc23f610c2567fb5180f`:
```json
{
  "status": "1",
  "message": "OK",
  "result": {
    "0x8ae127d224094cb1b27e1b28a472e588cbcc7620": [
      {
        "level": "danger",
        "name": "Contract source code not verified",
        "desc": "This token contract has not been verified.  We cannot check the contract code for details. Unsourced token contracts are likely to have malicious function to defraud users of their assets. Please apply to the project team to open source.",
        "updated_at": "1638780984"
      },
      {
        "level": "danger",
        "name": "Airdrop scam",
        "desc": "You may lose your assets if giving approval to the website of this token.",
        "updated_at": "1638780984"
      },
      {
        "level": "warn",
        "name": "Team information in doubt",
        "desc": "The team information is in doubt or fake. Please confirm the credibility of team information to the project team.",
        "updated_at": "1638780984"
      }
    ],
    "0xb33eaad8d922b1083446dc23f610c2567fb5180f": [
      {
        "level": "safe",
        "name": "Non-counterfeit",
        "desc": "This token is issued by its declared team。Some scams will create a well-known token with the same name to defraud users of their assets.",
        "updated_at": "1638780984"
      },
      {
        "level": "safe",
        "name": "Contract source code verified",
        "desc": "This token contract is open source.  You can check the contract code for details. Unsourced token contracts are likely to have malicious function to defraud users of their assets.",
        "updated_at": "1638780984"
      },
      {
        "level": "safe",
        "name": "Normal slippage",
        "desc": "The transaction can be made with normal slippage. If slippage is high, user transaction fees will be high.",
        "updated_at": "1638780984"
      },
      {
        "level": "safe",
        "name": "Can be sold",
        "desc": "Tokens can be sold normally. Tokens for many of the scams can not be sold.",
        "updated_at": "1638780984"
      }
    ]
  }
}
```
