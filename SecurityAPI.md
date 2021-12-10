## 1. Get supported blockchains

>URL: https://api.gopocket.security/supported_chains

>Method：GET

>Parameters: No Parameters

>Response:

Parameter|Description
---|---
status|`1` means success, `0` means failure
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

Parameter|Description
---|---
id|The `id` of the blockchain
contract_addresses|The contract address of tokens, comma separated

>Response:

Parameter|Description
---|---
status|`1` means success, `0` means failure
message|`OK` for success, `Error message` for failure
result| 


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
