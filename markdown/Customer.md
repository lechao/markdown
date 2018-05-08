# 1.客户订单列表
请求地址：==http://47.93.8.36:8000/customer/getorders/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 用户power（必填）用户登录后返回
ordno | String | 输入的订单号（可空）
timefrom | String | 输入的起始时间（可空） （类似：2017-12-12）
timeto | String | 输入的结束时间（可空） 
status | String | 输入的任务状态，1-未发货，2-在途，3-已完成，4-已评价（可空） 
offset | int | 偏移量（必填） 
limit | int |获取数量（必填）

成功：
```
{
    status: 1,
    data: [
    	{
            price: "22.00",
            trips: [
                {
                    driver_mobile: "15221089804", //司机电话
                    plate_number: "沪M12j11111", //车牌
                    create_uid: 5,
                    create_time: "2018-03-25 16:40:41", //创建时间
                    trip_no: "TP123943762839232",//运输单号
                    note: "备注",//备注
                    driver_name: "李白1",//司机姓名
                    status: 1,//状态1：未发车；2：运输中；3：已结束
                    driver_uid: 5//司机用户id
                }
            ],
            user_id: 5,//订单用户id
            create_uid: 5,
            send_time: "2018-01-01 08:15:00", 要求发货时间
            volume: "22.23",//体积 立方米
            receive_name: "pengpeng", //收货人
            send_mobile: "15221089804", //发货人手机号
            note: "不要磕碰",//备注
            content: "订单内容123",//订单内容
            number: 30,//件数
            create_mobile: "15221089804",
            send_address: "上海市浦东新区金科路100号",//提货地址
            receive_time: "2018-01-05 08:15:00",//要求到货时间
            order_no: "ON1222121212121444",//客户单号
            status: 1,//status | String | 输入的任务状态，1-未发货，2-在途，3-已完成，4-已评
            receive_address: "上海市闵行区100路",//收货地址
            receive_mobile: "15221089804",//收获人手机号
            create_time: "2018-03-25 16:21:24",
            boxes_num: 3,//箱数
            send_name: "Happy",//发货人
            weight: "3"//重量 KG
    	}
    ],
    message: "success"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 2.订单状态数量（我的订单页面）
请求地址：==http://47.93.8.36:8000/customer/getorders_count/==  
请求方式：==POST==  


### 所需参数
名称 | 类型 | 描述
------- | ------------- | -------------
power | String | 用户power（必填）用户登录后返回

成功：
```
{
    "data": {
        "all_count": 1,//总数量
        "nosend_count": 1,//未发货数量
        "sended_count": 0,//已完成数量
        "comment_count": 0,//已评价数量
        "sending_count": 0 //在途数量
    },
    "status": 1,
    "message": "success"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 3.订单详情（我的订单页面）
请求地址：==http://47.93.8.36:8000/customer/getorders_detail/==  
请求方式：==POST==  


### 所需参数
名称 | 类型 | 描述
---------- | --------------- | ------------ 
ordno | String | 订单号（必填）

成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "boxes_num": 3,//箱数
        "send_time": "2018-01-01 08:15:00",//要求发货时间
        "note": "不要磕碰",//注意事项
        "create_time": "2018-03-25 16:21:24",
        "create_mobile": "15221089804",
        "number": 30,//件数
        "receive_mobile": "15221089804",//收货人电话
        "price": "22.00",
        "receive_name": "pengpeng",//收货人姓名
        "send_name": "Happy",//发货人姓名
        "volume": "22.23",//体积
        "weight": "3",//重量
        "send_mobile": "15221089804",//发货人电话
        "trips": [
            {
                "note": "备注",
                "driver_mobile": "15221089804",
                "trip_no": "TP123943762839232",
                "driver_uid": 5,
                "create_uid": 5,
                "plate_number": "沪M12j11111",
                "driver_name": "李白1",
                "create_time": "2018-03-25 16:40:41",
                "status": 1
            }
        ],
        "status": 1,//状态
        "receive_time": "2018-01-05 08:15:00",//要求收货时间
        "receive_address": "上海市闵行区100路",//收货地址
        "content": "订单内容123",//货品描述
        "order_no": "ON1222121212121444",//订单号
        "create_uid": 5,
        "send_address": "上海市浦东新区金科路100号",//发货地址
        "user_id": 5
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 4.查看物流
请求地址：==http://47.93.8.36:8000/customer/gettasks_detail/==
请求方式：==POST==  


### 所需参数
名称 | 类型 | 描述
---------- | --------------- | ------------ 
ordno | String | 订单号（必填）

成功：
```
{
    "status": 1,
    "data": [
        {
            "weight": "0.00", //重量
            "boxes_num": 600, //箱数
            "task_no": "2017070300006",//任务号
            "number": 600,//件数
            "receive_time": "2017-07-03 00:00:00",//收获时间
            "status": 3,//任务状态
            "receive_mobile": "69153330 * 64",//收货人手机号
            "order_id": 22,//订单id
            "receive_address": "嘉定区陈宝公路58号马陆工业城内",//收获地址
            "create_time": "2018-04-05 09:52:42",
            "receive_name": "Linda",//收货人姓名
            "volume": "0",//体积
            "trip": {
                "tot_gross_w": "0",  //整个运单的 重量
                "to_address": "????",  //运单的目的地
                "driver_mobile": "15921582655", //司机电话
                "gps_no": "?D08942-??", //gpd 编号
                "status": 2, //运单状态
                "eta": "2017-07-03 00:00:00", /eta
                "trip_no": "170703021741",//运单号
                "tot_vol": "0.00", //整个运单的 体积
                "driver_uid": "13013075686", 
                "driver_name": "???",//司机姓名
                "create_time": "2018-04-04 14:19:18",
                "plate_number": "?D08942",//车牌号
                "trip_id": 18, //运单id
                "pre_load_time": "2017-07-03 00:00:00",
                "from_address": "?????", //运单 起始地
                "create_uid": "15921582655",
                "note": "",
                "pre_ubload_time": "2017-07-03 00:00:00",
            },
			"actions": [                  //行程信息
                    {
                        "create_time": "2018-04-06 12:48:23",  //时间
                        "task_id": 3,
                        "check_codes": "",
                        "longitude": "1212.1212", //经纬度
                        "latitude": "1212.1212",  //经纬度
                        "notes": "异常描述", //行程描述
                        "type": "exception",
                        "exception_codes": "1,2,3",
                        "action_name": "异常上报" //行程名称
                    }
                ],
            "trip_id": 18,  //运单id
            "send_name": "",  //发货人姓名
            "send_time": "2017-07-03 00:00:00", //发货时间
            "send_mobile": "", //发货人电话
            "send_address": "上海市临港新城捷兴路211号",//发货地址
            "order_no": "2017070300006" //订单号
        },
        {
            "weight": "0",
            "boxes_num": 600,
            "task_no": "2017070300007",
            "number": 600,
            "receive_time": "2017-07-03 00:00:00",
            "status": 3,
            "receive_mobile": "69153330 * 64",
            "order_id": 22,
            "receive_address": "嘉定区陈宝公路58号马陆工业城内",
            "create_time": "2018-04-05 09:52:42",
            "receive_name": "Linda",
            "volume": "0",
            "trip": {
                "tot_gross_w": "0",
                "to_address": "养乐多无锡",
                "driver_mobile": "17715671569",
                "gps_no": "",
                "status": 2,
                "eta": "2017-07-04 15:37:00",
                "trip_no": "170706013888",
                "tot_vol": "0.00",
                "driver_uid": "13013075686",
                "driver_name": "潘化强",
                "create_time": "2018-04-05 00:50:43",
                "plate_number": "苏BM3028",
                "trip_id": 19,
                "pre_load_time": "2017-07-03 15:37:00",
                "from_address": "养乐多合肥",
                "create_uid": "17715671569",
                "note": "",
                "pre_ubload_time": "2017-07-04 15:37:00",
            },
			"actions": [
                    {
                        "create_time": "2018-04-06 12:48:23",
                        "task_id": 4,
                        "check_codes": "",
                        "longitude": "1212.1212",
                        "latitude": "1212.1212",
                        "notes": "异常描述",
                        "type": "exception",
                        "exception_codes": "1,2,3",
                        "action_name": "异常上报"
                    }
                ],
            "trip_id": 19,
            "send_name": "",
            "send_time": "2017-07-03 00:00:00",
            "send_mobile": "",
            "send_address": "上海市临港新城捷兴路211号",
            "order_no": "2017070300006"
        }
    ],
    "message": "success"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 5.获取配置信息
请求地址：==http://47.93.8.36:8000/customer/config/==  
请求方式：==GET==  
### 所需参数

成功：
```
{
status: 1,
data: {
phone: "11212121212", //客服电话
downloadurl: "url1",//新版本下载地址
version: "1.00"//app版本
},
message: "获取配置成功"
}
```

失败：

```
{"status": 0, "message": "没有消息!"}
```


# 6.消息中心接口
请求地址：==http://47.93.8.36:8000/customer/messages/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 登录用户名---用户权限power 字段（必填）
成功：
```
{
    "status": 1,
    "data": [
        {
            "message_id": 1,
            "title": "标题",
            "type": "system",
            "create_time": "2018-04-09 21:42:17",
            "user_id": "1",
            "is_read": false,
            "content": "内容内容内容内容内容内容"
        }
    ],
    "message": "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 7.消息中心已读（更改状态为已读）
请求地址：==http://47.93.8.36:8000/customer/readmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 登录用户名---用户权限power 字段（必填）
message_ids|String| 消息ids  举例：1,2,3；(必填)
成功：
```
{
    "status": 1,
    "message": "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 8.消息中心未读（更改状态为未读读）
请求地址：==http://47.93.8.36:8000/customer/unreadmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 登录用户名---用户权限power 字段（必填）
message_ids|String| 消息ids  举例：1,2,3；(必填)
成功：
```
{
    "status": 1,
    "message": "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 9.消息中心删除（删除消息）
请求地址：==http://47.93.8.36:8000/customer/delmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 登录用户名---用户权限power 字段（必填）
message_ids|String| 消息ids  举例：1,2,3；(必填)
成功：
```
{
    "status": 1,
    "message": "删除成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 10.消息中心（新消息）
请求地址：==http://47.93.8.36:8000/customer/newmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
power | String | 登录用户名---用户权限power 字段（必填）
message_id|Int| app 最新消息id
成功：
```
{
    "status": 1,
    "message": "有新消息",
    "data": {
        "type": "customer",
        "title": "1",
        "content": "1",
        "create_time": "2018-04-09 22:35:22",
        "user_id": "1",
        "message_id": 2,
        "is_read": false
    }
}
```

失败：

```
{"status": 0, "message": "没有消息!"}
```
# 11.评价提交
请求地址：==http://47.93.8.36:8000/customer/putcomment/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
user_id | String | 登录用户名：手机号（必填）
order_id| Int| 订单的id（必填）
driver_score| Int| 司机的评价分数
service_score| Int| 客服的评价分数
time_score| Int| 时效的评价分数
content| String| 评价内容
成功：
```
{
    "status": 1,
    "message": "提交成功",
}
```

失败：

```
{"status": 0, "message": "没有消息!"}
```
