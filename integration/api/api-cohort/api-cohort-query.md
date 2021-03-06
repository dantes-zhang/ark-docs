---
description: 方舟4.3.4版本中新增API
---

# 分群查询

## 1. 获取用户分群下的用户明细

获取某个分群下的用户明细

### 1.1 接口地址

> 【POST】  /uba/api/cohort/users

### 1.2 请求参数示例

```java
{
    // 【必填】分群code
    "cohortCode":"arkfq_3",
    //需要获取的用户条数
    "limit":2,
    //【选填】指定需要查询的用户属性列，传用户属性ID
    "properties":["xwho", "distinct_id", "$imei", "$first_visit_language", "$signup_time"]
}
```

> **limit**：获取用户分群下的用户条数，需要传正整数，不传默认为1000。
>
> **properties**：指定需要的用户属性列，传入用户属性ID，可以通过方舟系统或者 [元数据管理](../api-manage-project/api-meta.md)-[用户属性](../api-manage-project/api-meta.md#1-huo-qu-yong-hu-shu-xing) 接口获取用户属性列表。不指定默认查询方舟系统【元数据管理 - 用户属性】中 可见 的所有用户属性。
>
> **认证参数**：接口必传token和appKey两个参数，详情见 [项目接口认证](../#21-xiang-mu-jie-kou-ren-zheng)。

### 1.3 返回结果示例

```java
{
    //分群下总用户条数
    "count":46,
    //结果返回的用户条数
    "size":2,
    //用户详情
    "users":[
        {
            "$imei":null,
            "$first_visit_language":"zh-cn",
            "distinct_id":4255875062385414000,
            "$signup_time":null,
            "xwho":"JSd650856937040a530ff54fdaab4e56d7d650"
        },
        {
            "$imei":null,
            "$first_visit_language":"zh-cn",
            "distinct_id":-4635244755532264000,
            "$signup_time":null,
            "xwho":"JS1c6d11e3e67bf0dc02030d3fd393310b1c6d"
        }
    ]
}
```

### 1.4 接口调用示例

```java
 curl -H "Content-Type:application/json" -H "token:4113c9cad1c301113783f433e254888c" -H "appKey:31abd9593e9983ec" -X POST --data '{
    "cohortCode":"arkfq_3",
    "limit":2,
    "properties":["xwho", "distinct_id", "$imei", "$first_visit_language", "$signup_time"]
}' http://127.0.0.1:4005/uba/api/cohort/users
```

## 2. 获取单一用户的用户明细

根据用户ID获取用户明细数据

### 2.1 接口地址

> 【POST】 /uba/api/cohort/users/{xwho}

{% hint style="info" %}
xwho 表示用户ID，取用户属性ID为xwho的值，传参方式：path variable，非request body
{% endhint %}

### 2.2 请求参数示例

```java
{
    //【选填】这里表示不支持，默认获取方舟系统所有可用的用户属性
    "properties":[]
}
```

> **properties**：指定需要的用户属性列，传入用户属性ID，可以通过方舟系统或者 [元数据管理](../api-manage-project/api-meta.md)-[用户属性](../api-manage-project/api-meta.md#1-huo-qu-yong-hu-shu-xing) 接口获取用户属性列表。不指定默认查询方舟系统【元数据管理 - 用户属性】中 可见 的所有用户属性。
>
> **认证参数**：接口必传token和appKey两个参数，详情见 [项目接口认证](../#21-xiang-mu-jie-kou-ren-zheng)。

### 2.3 返回结果示例

```java
{
        "$imei": null,
        "chuangke_topic": null,
        "$first_visit_language": "zh-cn",
        "$city": null,
        "$email": null,
        "$platform": "JS",
        "chuangke_region": null,
        "chuangke_createtime": null,
        "$country": null,
        "$first_visit_time": 1557403591272,
        "phone": null,
        "$province": null,
        "$signup_time": null,
        "$mac": null,
        "company_code": null,
        "xwho": "JSd650856937040a530ff54fdaab4e56d7d650",
        "email": null
    }
```

### 2.4 接口调用示例

```java
curl -H "Content-Type:application/json" -H "token:4113c9cad1c301113783f433e254888c" -H "appKey:31abd9593e9983ec" -X POST --data '{
    "properties":[]
}' http://127.0.0.1:4005/uba/api/cohort/users/JSd650856937040a530ff54fdaab4e56d7d650
```

