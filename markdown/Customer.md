# 1.客户订单列表
请求地址：==http://47.93.8.36:8000/customer/getorders/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
- | - | - 
uid | Int | 用户id（必填）
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
- | - | -
uid | Int | 用户id（必填）

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
- | - | - 
ordno | String | 订单号（必填）

成功：
```
{
    "message": "success",
    "status": 1,
    "data": {
        "boxes_num": 3,
        "send_time": "2018-01-01 08:15:00",
        "note": "不要磕碰",
        "create_time": "2018-03-25 16:21:24",
        "create_mobile": "15221089804",
        "number": 30,
        "receive_mobile": "15221089804",
        "price": "22.00",
        "receive_name": "pengpeng",
        "send_name": "Happy",
        "volume": "22.23",
        "weight": "3",
        "send_mobile": "15221089804",
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
        "status": 1,
        "receive_time": "2018-01-05 08:15:00",
        "receive_address": "上海市闵行区100路",
        "content": "订单内容123",
        "order_no": "ON1222121212121444",
        "create_uid": 5,
        "send_address": "上海市浦东新区金科路100号",
        "user_id": 5
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```