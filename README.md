# 法人四要素验证公益API

## 简介
该 API 用于进行法人四要素验证

- API 地址: [https://api.787378.com/X0I40ULR?scene=api_service](https://api.787378.com/X0I40ULR?scene=api_service)
- 请求方式：POST
- 数据类型：表单

## 请求参数
需要提交四个参数，分别是：

| 参数     | 释义    |
|--------|-------|
| `arg1` | 企业名称  |
| `arg2` | 企业代码  |
| `arg3` | 法人姓名  |
| `arg4` | 法人证件号 |

**注意**：提交未指定参数或空白参数会引起 400 错误，请确保按照文档要求正确填写参数。

## 响应
正确的响应状态码应当为`200`
```json
{
"form_data": {
"arg1": "value1",
"arg2": "value2",
"arg3": "value3",
"arg4": "value4"
},
"tips": "验证失败，非市场监督管理总局企业。"
}
```

## CURL
```bash
curl -X POST https://api.787378.com/X0I40ULR?scene=api_service \
     -F 'arg1=value1' \
     -F 'arg2=value2' \
     -F 'arg3=value3' \
     -F 'arg4=value4'
