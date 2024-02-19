# 法人四要素验证公益API

## 简介
该 API 用于进行法人四要素验证公益操作。

- API 地址: [https://api.787378.com/X0I40ULR?scene=api_service](https://api.787378.com/X0I40ULR?scene=api_service)
- 请求方式：POST
- 数据类型：表单

## 请求参数
需要提交四个参数，分别是：
1. `arg1`
2. `arg2`
3. `arg3`
4. `arg4`

**注意**：提交未指定参数或空白参数会引起 400 错误，请确保按照文档要求正确填写参数。

## 正常响应
正常的响应状态码应当为 200。

## 范例
```bash
curl -X POST https://api.787378.com/X0I40ULR?scene=api_service \
     -F 'arg1=value1' \
     -F 'arg2=value2' \
     -F 'arg3=value3' \
     -F 'arg4=value4'
