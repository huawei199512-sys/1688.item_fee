# 1688.item_fee
Get shipping fees for products on 1688
# 1688 Item Fee API (1688.item_fee)
### GitHub Friendly | Chinese-English | Technical Only | Compliant with Community Guidelines

---

## 中文
### 1688 商品运费 API
稳定获取 1688 商品运费、发货地、运费模板等信息，适用于电商下单、运费计算、订单系统对接、跨境分销等场景，返回结构化数据，快速集成。

### 核心功能
- 获取 1688 商品详细运费信息
- 支持按商品 ID + 收货地区查询
- 返回运费、发货地、运费类型、物流公司、是否包邮等字段
- 支持 JSON / XML 格式返回
- 高可用、低延迟、支持批量调用

### 接口信息 
- 请求方式：`GET/POST`
- 接口地址：`https://api-gw.onebound.cn/1688/item_fee`
- 必传参数：`key`、`secret`、`num_iid`
- 可选参数：`area_id`、`city`、`count`、`seller_nick`
- 测试链接：https://o0b.cn/iieidi   
### 快速调用（Python）
```python
import requests

API_URL = "https://api-gw.onebound.cn/1688/item_fee"
params = {
    "key": "your_api_key",
    "secret": "your_api_secret",
    "num_iid": "1234567890"
}
resp = requests.get(API_URL, params=params)
print(resp.json())
```

### 响应数据示例（JSON）
```json
{
  "item": {
    "num_iid": "1234567890",
    "title": "1688商品标题示例",
    "shipping_fee": "6.00",
    "is_free_shipping": "false",
    "location": "广东 深圳",
    "logistics_company": "中通快递",
    "delivery_time": "48小时内发货"
  },
  "error": "",
  "error_code": "0000",
  "execution_time": 0.42
}
```

### 完整文档
https://open.onebound.cn/help/api/1688.item_fee.html

---

## English
### 1688 Item Fee API
Stable access to 1688 product shipping fee, origin, logistics template, etc. Suitable for e-commerce checkout, shipping calculation, order system integration, cross-border dropshipping.

### Core Features
- Get detailed shipping fee of 1688 products
- Support query by item ID + delivery area
- Return shipping fee, location, logistics type, company, free shipping status
- JSON / XML response supported
- High availability, low latency, batch-friendly

### API Spec
- Method: `GET/POST`
- Endpoint: `https://api-gw.onebound.cn/1688/item_fee`
- Required: `key`, `secret`, `num_iid`
- Optional: `area_id`, `city`, `count`, `seller_nick`
- Go test：https://o0b.cn/iieidi  

### Quick Start (Python)
```python
import requests

API_URL = "https://api-gw.onebound.cn/1688/item_fee"
params = {
    "key": "your_api_key",
    "secret": "your_api_secret",
    "num_iid": "1234567890"
}
response = requests.get(API_URL, params=params)
print(response.json())
```

### Response Example (JSON)
```json
{
  "item": {
    "num_iid": "1234567890",
    "title": "1688 Product Title Example",
    "shipping_fee": "6.00",
    "is_free_shipping": "false",
    "location": "Guangdong Shenzhen",
    "logistics_company": "ZTO Express",
    "delivery_time": "Ship within 48h"
  },
  "error": "",
  "error_code": "0000",
  "execution_time": 0.42
}
```

### Full Documentation
https://open.onebound.cn/help/api/1688.item_fee.html

---

### 💡 GitHub Community Notes
- Pure technical API for developers; no ads, no spam
- Fully compliant with GitHub Community Guidelines
- Welcome issues & feedback | Star ⭐ appreciated

