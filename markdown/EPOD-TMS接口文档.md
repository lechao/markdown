# 1.1公司接口（获取企业数据）

请求地址：http://47.93.8.36:8000/tms/companys/get/{id}/  
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| id   | Int  | 公司id（必填） |

#### 返回参数

| 名称    |  类型  |        描述 |
| -------------- | :----: | ---------------------: |
| email          | String |                                             邮箱 |
| contact_person | String |                                           联系人 |
| bill_to_addr   | String |                                         账单地址 |
| create_time    | String |                                         创建时间 |
| tms_id         | String |                                    TMS系统企业id |
| update_time    | String |                                         更新时间 |
| num_of_license |  Int   |                                       许可证数量 |
| status         |  Int   |                                             状态 |
| server_ip      | String | 重定位的SERVER的IP地址,应用于自建DB SERVER的客户 |
| phone_cs       | String |                                     客服中心电话 |
| name_en        | String |                                 企业名称（英文） |
| name_cn        | String |                                 企业名称（中文） |
| id             | String |                                               id |
| pic_size       | String |           720,800,1200. 手机图片上传前压缩的比例 |
| contact_num    | String |                                         联系电话 |
| enabled        |  Int   |                    0:表示‘不可用’;1表示’可用的’. |
#### 返回详情
成功：
```
{
    message: "success",
    data: {
        email: "1",
        contact_person: "1",
        bill_to_addr: "1",
        create_time: "2018-03-05 14:40:12",
        tms_id: null,
        update_time: "2018-03-05 14:39:51",
        num_of_license: 1,
        status: 1,
        server_ip: "1",
        phone_cs: "1",
        name_en: "1",
        name_cn: "1",
        id: 1,
        pic_size: "1",
        contact_num: "1",
        enabled: 1
    },
    status: 1
}
```
```
{"status": 0, "message": "获取数据失败!"}
```

# 1.2公司接口（获取企业数据）

请求地址：http://47.93.8.36:8000/tms/companys/get/  
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取数量（必填） |

#### 返回参数

| 名称    |  类型  |        描述 |
| -------------- | :----: | ---------------------: |
| email          | String |                                             邮箱 |
| contact_person | String |                                           联系人 |
| bill_to_addr   | String |                                         账单地址 |
| create_time    | String |                                         创建时间 |
| tms_id         | String |                                    TMS系统企业id |
| update_time    | String |                                         更新时间 |
| num_of_license |  Int   |                                       许可证数量 |
| status         |  Int   |                                             状态 |
| server_ip      | String | 重定位的SERVER的IP地址,应用于自建DB SERVER的客户 |
| phone_cs       | String |                                     客服中心电话 |
| name_en        | String |                                 企业名称（英文） |
| name_cn        | String |                                 企业名称（中文） |
| id             | String |                                               id |
| pic_size       | String |           720,800,1200. 手机图片上传前压缩的比例 |
| contact_num    | String |                                         联系电话 |
| enabled        |  Int   |                    0:表示‘不可用’;1表示’可用的’. |
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": [
        {
            "enabled": 1,
            "name_en": "EMS",
            "status": 1,
            "bill_to_addr": "中科路222200弄",
            "phone_cs": "021-111111",
            "update_time": "2018-03-21 21:26:30",
            "name_cn": "中国邮政",
            "contact_num": "15221089804",
            "pic_size": "720",
            "id": 1,
            "server_ip": "111.111.111.111",
            "create_time": "2018-03-05 14:40:12",
            "email": "920106140@qq.com",
            "contact_person": "张乐超",
            "tms_id": "122121212",
            "num_of_license": 11
        }
    ]
}
```
```
{"status": 0, "message": "获取数据失败!"}
```

# 1.3公司接口（添加企业数据）
请求地址：http://47.93.8.36:8000/tms/companys/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| email          | String |                                             邮箱 |
| contact_person | String |                                           联系人 |
| bill_to_addr   | String |                                         账单地址 |
| tms_id         | String |                                    TMS系统企业id |
| num_of_license |  Int   |                                       许可证数量 |
| status         |  Int   |                                             状态 |
| server_ip      | String | 重定位的SERVER的IP地址,应用于自建DB SERVER的客户 |
| phone_cs       | String |                                     客服中心电话 |
| name_en        | String |                                 企业名称（英文） |
| name_cn        | String |                                 企业名称（中文） |
| pic_size       | String |           720,800,1200. 手机图片上传前压缩的比例 |
| contact_num    | String |                                         联系电话 |
| enabled        |  Int   |                    0:表示‘不可用’;1表示’可用的’. |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 1.4公司接口（更新企业数据）
请求地址：http://47.93.8.36:8000/tms/companys/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             公司id |
| email          | String |                                             邮箱 |
| contact_person | String |                                           联系人 |
| bill_to_addr   | String |                                         账单地址 |
| tms_id         | String |                                    TMS系统企业id |
| num_of_license |  Int   |                                       许可证数量 |
| status         |  Int   |                                             状态 |
| server_ip      | String | 重定位的SERVER的IP地址,应用于自建DB SERVER的客户 |
| phone_cs       | String |                                     客服中心电话 |
| name_en        | String |                                 企业名称（英文） |
| name_cn        | String |                                 企业名称（中文） |
| pic_size       | String |           720,800,1200. 手机图片上传前压缩的比例 |
| contact_num    | String |                                         联系电话 |
| enabled        |  Int   |                    0:表示‘不可用’;1表示’可用的’. |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 1.5公司接口（删除企业）仅限于没有其他外键关联的数据
请求地址：http://47.93.8.36:8000/tms/companys/delete
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             公司id |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 2.1角色接口获取

请求地址：http://47.93.8.36:8000/tms/roles/get/{id}/  
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| id   | Int  | 角色id（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| role_name          | String |                                             角色名称 |
#### 返回详情
成功：
```
{
message: "success",
status: 1,
data: {
create_time: "2018-03-21 21:31:44",
id: 3,
role_name: "司机"
}
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 2.2角色接口获取

请求地址：http://47.93.8.36:8000/tms/roles/get/ 
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取量（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| role_name          | String |                                             角色名称 |
#### 返回详情
成功：
```
{
message: "success",
status: 1,
data: [{
create_time: "2018-03-21 21:31:44",
id: 3,
role_name: "司机"
}]
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 2.3角色接口（添加角色）
请求地址：http://47.93.8.36:8000/tms/roles/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| role_name          | String |                                             角色名称 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 2.4角色接口（更新角色数据）
请求地址：http://47.93.8.36:8000/tms/roles/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             角色id |
| role_name          | String |                                             角色名称 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 2.5角色接口（删除角色）仅限于没有其他外键关联的数据
请求地址：http://47.93.8.36:8000/tms/roles/delete
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             角色id |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.1用户接口获取

请求地址：http://47.93.8.36:8000/tms/users/get/{id}/  
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| id   | Int  | 用户id（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| name          | String |                                             用户名称 |
| password          | String |                                             用户密码 |
| mobile          | String |                                             用户手机 |
| email          | String |                                             用户邮箱 |
| company_id          | Int |                                             用户所属企业id |
| language          | String |                                             用户语言 |
| role_id          | Int |                                             用户角色id |
| enabled          | Int |                                             是否可用（1可用；0不可用） |
| alert_dur          | Int |                                             默认为15(分钟)。单位为分钟。信息预警时间 |
| log_dur          | Int |                                             默认为3(天)。日志保存的天数。 |
| freq_get_gps          | Int |                                             手机app获取GPS信息的频次(单位:分钟)。 |
| freq_upload_gps          | Int |                                             手机app上传GPS信息的频次(单位:分钟)。 |
#### 返回详情
成功：
```
{
    data: {
        freq_get_gps: 2,
        name: "happy",
        mobile: "15221089804",
        enabled: 1,
        create_time: "2018-03-05 14:39:25",
        freq_upload_gps: 5,
        email: "920106140@qq.com",
        language: "cn",
        role_id: 3,
        password: "123456",
        log_dur: 5,
        update_time: "2018-03-22 21:50:41",
        company_id: 1,
        alert_dur: 3
    },
    status: 1,
    message: "success"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.2用户接口获取

请求地址：http://47.93.8.36:8000/tms/users/get/
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取量（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| name          | String |                                             用户名称 |
| password          | String |                                             用户密码 |
| mobile          | String |                                             用户手机 |
| email          | String |                                             用户邮箱 |
| company_id          | Int |                                             用户所属企业id |
| language          | String |                                             用户语言 |
| role_id          | Int |                                             用户角色id |
| enabled          | Int |                                             是否可用（1可用；0不可用） |
| alert_dur          | Int |                                             默认为15(分钟)。单位为分钟。信息预警时间 |
| log_dur          | Int |                                             默认为3(天)。日志保存的天数。 |
| freq_get_gps          | Int |                                             手机app获取GPS信息的频次(单位:分钟)。 |
| freq_upload_gps          | Int |                                             手机app上传GPS信息的频次(单位:分钟)。 |
#### 返回详情
成功：
```
{
    data: [{
        freq_get_gps: 2,
        name: "happy",
        mobile: "15221089804",
        enabled: 1,
        create_time: "2018-03-05 14:39:25",
        freq_upload_gps: 5,
        email: "920106140@qq.com",
        language: "cn",
        role_id: 3,
        password: "123456",
        log_dur: 5,
        update_time: "2018-03-22 21:50:41",
        company_id: 1,
        alert_dur: 3
    }],
    status: 1,
    message: "success"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.3用户接口（添加用户）
请求地址：http://47.93.8.36:8000/tms/users/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| name          | String |                                             用户名称 |
| password          | String |                                             用户密码 |
| mobile          | String |                                             用户手机 |
| email          | String |                                             用户邮箱 |
| company_id          | Int |                                             用户所属企业id |
| language          | String |                                             用户语言 |
| role_id          | Int |                                             用户角色id |
| enabled          | Int |                                             是否可用（1可用；0不可用） |
| alert_dur          | Int |                                             默认为15(分钟)。单位为分钟。信息预警时间 |
| log_dur          | Int |                                             默认为3(天)。日志保存的天数。 |
| freq_get_gps          | Int |                                             手机app获取GPS信息的频次(单位:分钟)。 |
| freq_upload_gps          | Int |                                             手机app上传GPS信息的频次(单位:分钟)。 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.4用户接口（更新用户数据）
请求地址：http://47.93.8.36:8000/tms/users/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             用户id |
| name          | String |                                             用户名称 |
| password          | String |                                             用户密码 |
| mobile          | String |                                             用户手机 |
| email          | String |                                             用户邮箱 |
| company_id          | Int |                                             用户所属企业id |
| language          | String |                                             用户语言 |
| role_id          | Int |                                             用户角色id |
| enabled          | Int |                                             是否可用（1可用；0不可用） |
| alert_dur          | Int |                                             默认为15(分钟)。单位为分钟。信息预警时间 |
| log_dur          | Int |                                             默认为3(天)。日志保存的天数。 |
| freq_get_gps          | Int |                                             手机app获取GPS信息的频次(单位:分钟)。 |
| freq_upload_gps          | Int |                                             手机app上传GPS信息的频次(单位:分钟)。 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.5用户接口（删除角色）仅限于没有其他外键关联的数据
请求地址：http://47.93.8.36:8000/tms/users/delete
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| id          | Int |                                             用户id |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 4.1订单接口获取

请求地址：http://47.93.8.36:8000/tms/orders/get/{order_no}/  
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| order_no   | String  | 订单号（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| create_uid          | String |                                             创建人登录名 |
| content          | String |                                             订单内容表述 |
| price          | Decimal |                                             订单价格 |
| create_mobile          | String |                                             创建人手机号 |
| send_mobile          | String |                                             发货人手机号 |
| receive_mobile          | String |                                             收货人手机号 |
| order_no          | String |                                             订单号（托运单号） |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量（单位件）。 |
| boxes_num          | Int |                                             箱子数（单位箱） |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收获地址 |
| send_time          | Date |                                             发货时间 |
| receive_time          | Date |                                             收获时间 |
| status          | Int |                                             订单状态 |
| user_id          | String |                                             下单人用户 唯一登录名 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                             收货人姓名 |
| note          | String |                                             备注 |
| customer      |String  |                                              客户|
| user_no      |String  |                                              客户单号|
#### 返回详情
成功：
```
{
    "message": "success",
    "data": {
            "send_mobile": "15221089804",
            "content": "订单内容",
            "send_name": "Happy",
            "create_time": "2018-03-25 16:21:24",
            "receive_address": "上海市闵行区100路",
            "boxes_num": 3,
            "receive_mobile": "15221089804",
            "send_address": "上海市浦东新区金科路100号",
            "status": 1,
            "number": 30,
            "receive_name": "pengpeng",
            "volume": "22.00",
            "create_mobile": "15221089804",
            "send_time": "2018-01-01 08:15:00",
            "note": "不要磕碰",
            "create_uid": 5,
            "weight": "3",
            "user_id": 5,
            "receive_time": "2018-01-05 08:15:00",
            "price": "22.00",
            "order_no": "ON1222121212121444",
            "customer":"工商银行",
             "user_no":"u1111",
       },
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 4.2订单接口获取

请求地址：http://47.93.8.36:8000/tms/orders/get/  
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取数量（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| create_uid          | String |                                             创建人 登录名 |
| content          | String |                                             订单内容表述 |
| price          | Decimal |                                             订单价格 |
| create_mobile          | String |                                             创建人手机号 |
| send_mobile          | String |                                             发货人手机号 |
| receive_mobile          | String |                                             收货人手机号 |
| order_no          | String |                                             订单号（托运单号） |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量（单位件）。 |
| boxes_num          | Int |                                             箱子数（单位箱） |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收获地址 |
| send_time          | Date |                                             发货时间 |
| receive_time          | Date |                                             收获时间 |
| status          | Int |                                             订单状态 |
| user_id          | String |                                             下单人用户登录名 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                             收货人姓名 |
| note          | String |                                             备注 |
| customer      | String |                                              客户名称|
| user_no      |String  |                                              客户单号|
#### 返回详情
成功：
```
{
    "message": "success",
    "data": [
        {
            "send_mobile": "15221089804",
            "content": "订单内容",
            "send_name": "Happy",
            "create_time": "2018-03-25 16:21:24",
            "receive_address": "上海市闵行区100路",
            "boxes_num": 3,
            "receive_mobile": "15221089804",
            "send_address": "上海市浦东新区金科路100号",
            "status": 1,
            "number": 30,
            "receive_name": "pengpeng",
            "volume": "22.00",
            "create_mobile": "15221089804",
            "send_time": "2018-01-01 08:15:00",
            "note": "不要磕碰",
            "create_uid": "test",
            "weight": "3",
            "user_id": 5,
            "receive_time": "2018-01-05 08:15:00",
            "price": "22.00",
            "order_no": "ON1222121212121444",
            "customer":"工商银行",
            "user_no":"u1111",
        }
    ],
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 4.3订单接口（添加订单）
请求地址：http://47.93.8.36:8000/tms/orders/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| create_uid          | String |                                             创建人Id |
| content          | String |                                             订单内容表述 |
| price          | Decimal |                                             订单价格 |
| create_mobile          | String |                                             创建人手机号 |
| send_mobile          | String |                                             发货人手机号 |
| receive_mobile          | String |                                             收货人手机号 |
| order_no          | String |                                             订单号（托运单号） |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量（单位件）。 |
| boxes_num          | Int |                                             箱子数（单位箱） |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收获地址 |
| send_time          | Date |                                             发货时间 |
| receive_time          | Date |                                             收获时间 |
| status          | Int |                                             订单状态 1：未发货，2：在途，3：已完成，4：已评价 |
| user_id          | String |                                             下单人用户 （客户代码） |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                             收货人姓名 |
| note          | String |                                             备注 |
| customer      | String    |                                           客户|
| user_no      |String  |                                              客户单号|
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 4.4订单接口（更新订单数据，如果没有根据order_no查询到订单，则新增订单）
请求地址：http://47.93.8.36:8000/tms/orders/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| create_uid          | Int |                                             创建人Id |
| content          | String |                                             订单内容表述 |
| price          | Decimal |                                             订单价格 |
| create_mobile          | String |                                             创建人手机号 |
| send_mobile          | String |                                             发货人手机号 |
| receive_mobile          | String |                                             收货人手机号 |
| order_no          | String |                                             订单号（托运单号） |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量（单位件）。 |
| boxes_num          | Int |                                             箱子数（单位箱） |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收获地址 |
| send_time          | Date |                                             发货时间 |
| receive_time          | Date |                                             收获时间 |
| status          | Int |                                             订单状态 |
| user_id          | Int |                                             下单人用户（客户代码） |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                             收货人姓名 |
| note          | String |                                             备注 |
| customer      | String    |                                           客户|
| user_no      |String  |                                              客户单号|
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 5.1运单接口获取

请求地址：http://47.93.8.36:8000/tms/trips/get/{trip_no}/
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| trip_no  | String  | 运单号（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| driver_uid          | Int |                                             司机用户Id |
| driver_mobile          | String |                                             司机手机号 |
| create_uid          | Int |                                             创建人用户Id |
| trip_no          | String |                                             运单号 |
| driver_name          | String |                                             司机姓名 |
| status          | Int |                                             运单状态；1：未发车；2:运输中;；3：已结束 |
| note          | String |                                             备注 |
| plate_number          | String |                                             车牌号 |
| tot_vol          | Decimal |                                             总体积 |
| tot_gross_w          | Decimal |                                             总重量 |
| from_address          | String |                                             起点 |
| to_address          | String |                                             终点 |
| pre_load_time          | Datetime |                                             要求提货时间 |
| pre_ubload_time          | Datetime |                                             要求到货时间 |
| eta          | Datetime |                                             eta |
| gps_no          | String |                                             gps号码 |


#### 返回详情
成功：
```
{
message: "success",
data: {
driver_mobile: "15221089804",
status: 1,
note: "备注",
driver_name: "李白1",
driver_uid: 5,
trip_no: "TP123943762839232",
create_uid: 5,
plate_number: "沪M12j11111",
create_time: "2018-03-25 16:40:41"，
tot_vol:22.2,
tot_gross_w:22.2,
from_address:"上海市闵行区xx路"，
to_address:"上海市闵行区xx路",
pre_load_time:"2018-03-25 16:40:41",
pre_ubload_time:"2018-03-25 16:40:41",
eta:"2018-03-25 16:40:41",
gps_no:"gpsid"
},
status: 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 5.2运单接口获取

请求地址：http://47.93.8.36:8000/tms/trips/get/  
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取数量（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| driver_uid          | Int |                                             司机用户Id |
| driver_mobile          | String |                                             司机手机号 |
| create_uid          | Int |                                             创建人用户Id |
| trip_no          | String |                                             运单号 |
| driver_name          | String |                                             司机姓名 |
| status          | Int |                                             运单状态；1：未发车；2:运输中;；3：已结束 |
| note          | String |                                             备注 |
| plate_number          | Decimal |                                             车牌号 |
| tot_vol          | Decimal |                                             总体积 |
| tot_gross_w          | Decimal |                                             总重量 |
| from_address          | String |                                             起点 |
| to_address          | String |                                             终点 |
| pre_load_time          | Datetime |                                             要求提货时间 |
| pre_ubload_time          | Datetime |                                             要求到货时间 |
| eta          | Datetime |                                             eta |
| gps_no          | String |                                             gps号码 |
#### 返回详情
成功：
```
{
    "message": "success",
    "data": [
        {
            "driver_mobile": "15221089804",
            "status": 1,
            "note": "备注",
            "driver_name": "李白1",
            "driver_uid": 5,
            "trip_no": "TP123943762839232",
            "create_uid": 5,
            "plate_number": "沪M12j11111",
            "create_time": "2018-03-25 16:40:41",
            "tot_vol":22.2,
            "tot_gross_w":22.2,
            "from_address":"上海市闵行区xx路"，
            "to_address":"上海市闵行区xx路",
            "pre_load_time":"2018-03-25 16:40:41",
            "pre_ubload_time":"2018-03-25 16:40:41",
            "eta":"2018-03-25 16:40:41",
            "gps_no":"gpsid"
        }
    ],
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 5.3运单接口（添加运单）
请求地址：http://47.93.8.36:8000/tms/trips/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| driver_uid          | Int |                                             司机用户Id |
| driver_mobile          | String |                                             司机手机号 |
| create_uid          | Int |                                             创建人用户Id |
| trip_no          | String |                                             运单号 |
| driver_name          | String |                                             司机姓名 |
| status          | Int |                                             运单状态；1：未发车；2:运输中;；3：已结束 |
| note          | String |                                             备注 |
| plate_number          | Decimal |                                             车牌号 |
| tot_vol          | Decimal |                                             总体积 |
| tot_gross_w          | Decimal |                                             总重量 |
| from_address          | String |                                             起点 |
| to_address          | String |                                             终点 |
| pre_load_time          | Datetime |                                             要求提货时间 |
| pre_ubload_time          | Datetime |                                             要求到货时间 |
| eta          | Datetime |                                             eta |
| gps_no          | String |                                             gps号码 |
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 5.4运单接口（更新运单数据，如果没有根据trip_no查询到运单，则新增运单）
请求地址：http://47.93.8.36:8000/tms/trips/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| driver_uid          | Int |                                             司机用户Id |
| driver_mobile          | String |                                             司机手机号 |
| create_uid          | Int |                                             创建人用户Id |
| trip_no          | String |                                             运单号 |
| driver_name          | String |                                             司机姓名 |
| status          | Int |                                             运单状态；1：未发车；2:运输中;；3：已结束 |
| note          | String |                                             备注 |
| plate_number          | Decimal |                                             车牌号 |
| tot_vol          | Decimal |                                             总体积 |
| tot_gross_w          | Decimal |                                             总重量 |
| from_address          | String |                                             起点 |
| to_address          | String |                                             终点 |
| pre_load_time          | Datetime |                                             要求提货时间 |
| pre_ubload_time          | Datetime |                                             要求到货时间 |
| eta          | Datetime |                                             eta |
| gps_no          | String |                                             gps号码 |
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 6.1任务接口获取

请求地址：http://47.93.8.36:8000/tms/tasks/get/{task_no}/  
请求方式：GET

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| task_no   | String  | 任务单号（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| order_id          | Int |                                             订单Id |
| trip_id          | Int |                                             派送运单Id |
| task_no          | String |                                             任务号 |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量 |
| boxes_num          | Int |                                             箱数 |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收货地址 |
| send_time          | String |                                             发货时间 |
| receive_time          | String |                                             收获时间 |
| status          | Int |                                             状态；1：未收获；2：运输中；3：已结束 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                         收货人姓名 |
|send_mobile|String|发货人手机|
|receive_mobile|String|收货人手机|
#### 返回详情
成功：
```
{
message: "success",
status: 1,
data: {
weight: "4.00",
create_time: "2018-03-25 17:11:31",
send_time: "2018-12-12 08:30:00",
task_no: "TN212993892473742938238293829",
send_mobile: "15221089804",
receive_time: "2018-12-17 08:23:00",
receive_address: "杨浦区",
receive_mobile: "15221089804",
trip_id: 1,
send_name: "Happy",
receive_name: "pengpeng",
volume: "22",
send_address: "浦东新区",
order_id: 1,
boxes_num: 2,
status: 1,
number: 20
}
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 6.2 任务接口获取

请求地址：http://47.93.8.36:8000/tms/tasks/get/  
请求方式：POST

#### 所需参数

| 名称 | 类型 |           描述 |
| ---- | :--: | -------------: |
| offset   | Int  | 偏移量（必填） |
| limit   | Int  | 获取数量（必填） |

#### 返回参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| order_id          | Int |                                             订单Id |
| trip_id          | Int |                                             派送运单Id |
| task_no          | String |                                             任务号 |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量 |
| boxes_num          | Int |                                             箱数 |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收货地址 |
| send_time          | String |                                             发货时间 |
| receive_time          | String |                                             收获时间 |
| status          | Int |                                             状态；1：未收获；2：运输中；3：已结束 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                         收货人姓名 |
|send_mobile|String|发货人手机|
|receive_mobile|String|收货人手机|
#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": [
        {
            "weight": "4.00",
            "create_time": "2018-03-25 17:11:31",
            "send_time": "2018-12-12 08:30:00",
            "task_no": "TN212993892473742938238293829",
            "send_mobile": "15221089804",
            "receive_time": "2018-12-17 08:23:00",
            "receive_address": "杨浦区",
            "receive_mobile": "15221089804",
            "trip_id": 1,
            "send_name": "Happy",
            "receive_name": "pengpeng",
            "volume": "22",
            "send_address": "浦东新区",
            "order_id": 1,
            "boxes_num": 2,
            "status": 1,
            "number": 20
        }
    ]
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 6.3任务接口（添加任务）
请求地址：http://47.93.8.36:8000/tms/tasks/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| order_no          | String |                                             订单号 |
| trip_no          | String |                                             派送运单号 |
| task_no          | String |                                             任务号 |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量 |
| boxes_num          | Int |                                             箱数 |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收货地址 |
| send_time          | String |                                             发货时间 |
| receive_time          | String |                                             收获时间 |
| status          | Int |                                             状态；1：未收获；2：运输中；3：已结束 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                         收货人姓名 |
|send_mobile|String|发货人手机|
|receive_mobile|String|收货人手机|

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 6.4任务接口（更新任务数据，如果没有根据task_no查询到任务，则新增任务）
请求地址：http://47.93.8.36:8000/tms/tasks/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| order_no          | String |                                             订单号 |
| trip_no          | String |                                             派送运单号 |
| task_no          | String |                                             任务号 |
| volume          | Decimal |                                             体积 |
| weight          | Decimal |                                             重量 |
| number          | Int |                                             数量 |
| boxes_num          | Int |                                             箱数 |
| send_address          | String |                                             发货地址 |
| receive_address          | String |                                             收货地址 |
| send_time          | String |                                             发货时间 |
| receive_time          | String |                                             收获时间 |
| status          | Int |                                             状态；1：未收获；2：运输中；3：已结束 |
| send_name          | String |                                             发货人姓名 |
| receive_name          | String |                                         收货人姓名 |
|send_mobile|String|发货人手机|
|receive_mobile|String|收货人手机|

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 7.1订单商品接口（添加商品）
请求地址：http://47.93.8.36:8000/tms/goods/put
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| good_no          | String |                                             商品编号 |
| good_name          | String |                                             商品名称 |
| shpm_row          | Int |                                             行号 |
| ld_qnty          | Decimal |                                             提货数量 |
| ld_gross_w          | Decimal |                                             提货重量 |
| ld_vol          | Decimal |                                             提货体积 |
| task_no          | String |                                             任务号 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "id": 7
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 7.2商品接口（更新任务数据，如果没有根据good_no查询到商品，则新增商品）
请求地址：http://47.93.8.36:8000/tms/goods/update
请求方式：POST 


#### 所需参数

| 名称           |  类型  |                                             描述 |
| -------------- | :----: | -----------------------------------------------: |
| good_no          | String |                                             商品编号 |
| good_name          | String |                                             商品名称 |
| shpm_row          | Int |                                             行号 |
| ld_qnty          | Decimal |                                             提货数量 |
| ld_gross_w          | Decimal |                                             提货重量 |
| ld_vol          | Decimal |                                             提货体积 |
| task_no          | String |                                             任务号 |

#### 返回详情
成功：
```
{
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
