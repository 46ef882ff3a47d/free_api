# API对接文档



## 目录

- [企业法人四要素验证](#企业法人四要素验证)
- [中国公民二要素验证](#中国公民二要素验证)

[//]: # (- [其他 API 标题2]&#40;#其他-api-标题2&#41;)

[//]: # (- [其他 API 标题3]&#40;#其他-api-标题3&#41;)

---

**注意**：请求API时请在URL中携带 `scene=api_service` 否则你的请求将被Cloudflare拦截 ,同时请求提交未知参数或无效参数会引起 400 错误



## 企业法人四要素验证

### 简介
该 API 用于进行法人四要素验证
- API 地址: [https://api.787378.com/X0I40ULR](https://api.787378.com/X0I40ULR)
- 请求方式：POST
- 数据类型：表单


### 请求参数

需要提交四个参数，分别是：

| 参数     | 释义     |
|--------|--------|
| `arg1` | 企业名称   |
| `arg2` | 企业统一代码 |
| `arg3` | 法人姓名   |
| `arg4` | 法人身份证  |

### 响应
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

### CURL
```bash
curl -X POST https://api.787378.com/X0I40ULR?scene=api_service \
     -F 'arg1=value1' \
     -F 'arg2=value2' \
     -F 'arg3=value3' \
     -F 'arg4=value4'
```

---

## 中国公民二要素验证

### 简介
该 API 用于二要素验证
- API 地址: [https://api.787378.com/UKO40G7R](https://api.787378.com/UKO40G7R)
- 请求方式：POST
- 数据类型：表单

### 请求参数
需要提交俩个参数，分别是：

| 参数     | 释义  |
|--------|-----|
| `arg1` | 姓名  |
| `arg2` | 身份证 |


### 响应
正确的响应状态码应当为`200`
```json
{
"form_data": {
    "arg1": "value1",
    "arg2": "value2"
},
"tips": "不一致"
}
```

### CURL
```bash
curl -X POST https://api.787378.com/UKO40G7R?scene=api_service \
     -F 'arg1=value1' \
     -F 'arg2=value2' 
```

---