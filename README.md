# LinkApi
万物皆可链接！一个稳定的聚合 API 接口源，提供业务开发中常用数据，长期维护并持续添加新接口。

- 如果在使用过程中遇到任何问题，或者有什么好的意见和建议，甚至编程开发的交流学习，都可以与我联系，wenhanf@163.com，请注明来意！

## 接口定义说明
- 所有接口均为 GET 请求
- 所有请求参数均已 url 参数列表的形式使用，如
```text
    {host}/link_api/console/sapi/trip/city3code?city_name=北京
```
- 所有的响应格式直接包含数据的json，部分结果中会有以下字段：
  - code：错误码（正常情况为0，或无此字段）
  - message：错误码不为0时，包含了错误信息
  - data：带有code和message时，数据会被包装到 data 字段中，解析data的json即可。
```json
  {
    "code": 1,
    "message": "数据返回成功",
    "data": {}
  }
```

## 接口列表
### 1、城市三字码查询
- 接口说明：查询指定城市的三字码
- 接口地址：{host}/link_api/console/sapi/trip/city3code

### 2、ip归属地查询
- 接口说明：查询指定ip的归属地
- 接口地址：{host}/link_api/console/sapi/tool/ip_region

### 3、航班查询
- 接口说明：查询指定 起飞/落地 城市的航班信息
- 接口地址：{host}/link_api/console/sapi/trip/flight/list

### 4、万年历查询
- 接口说明：查询指定日期的万年历
- 接口地址：{host}/link_api/console/sapi/service/calendar

### 5、天气查询
- 接口说明：查询指定省/市/区天气信息
- 接口地址：{host}/link_api/console/sapi/service/weather/today
- 子接口：
  - 查询指定城市的今日天气
    - 接口地址：{host}/link_api/console/sapi/service/weather/today
  - 查询指定城市的未来天气
    - 接口地址：{host}/link_api/console/sapi/service/weather/future