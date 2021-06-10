# 接口文档


## 接口说明

```
1. 测试地址：https://miaoqiang.libsss.com
2. 返回格式：{
            data:'',          //返回数据
            code:200,        // 200:表示请求成功,其它返回错误码
            msg:'success'   //  成功返回success，失败返回失败原因
            }
3. 线上地址：https://uniswap.morpheuscommunity.net
```

### 安全检测相关

> HTTP Header 参数

参数|描述
---|---
Accept-Language|语言【zh：中文（默认）】、【en：英文】

##### 币种安全检测
> 请求地址：api/v1/open/safety

> 请求方式：POST

> 请求参数: 

参数|是否必填|类型|描述
---|---|---|---
address|是|array|待检测地址列表

```json
{
    "address": [
          "0x11111111111111111",
          "0x22222222222222222",
          "..."
    ]
}
```

> 返回参数：

参数|描述
---|---
address|币种地址
normal|正常项
notice|注意项
risk|风险项

```json
[
  {
    "address": "0x11111111111111111",
    "normal": ["流动性正常", "滑点正常", "..."],
    "notice": ["需要提高滑点...", ""],
    "risk": ["无法卖出..."] 
  },
  {
  "address": "0x222222222222222222",
      "normal": [],
      "notice": ["需要提高滑点", "..."],
      "risk": ["无法卖出", "..."] 
  },
  {
  "address": "0x33333333333333333",
      "normal": [],
      "notice": [],
      "risk": [] 
  },
  {
    "...": "..."
  }

]
```


