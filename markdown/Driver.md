# 1.登录
请求地址：==http://47.93.8.36:8000/signin/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------|----------- | -------------
username | String | 用户登录名称
password | String | 用户密码
asntype | String | 用户类型（'CUSTOMER'：客户端,'DRIVER':司机端）
### 返回参数

名称 | 类型 | 描述
------|----------- | -------------
username | String | 用户登录名称
phone | String | 手机号
power | String | 用户权限，
### 返回详情
成功：
```
{
status: 1,
data: {
username: "13857404757",
power: "02B953FC143E42B599023E8AE4789F4C,059AEF77B7E24CCA897C53CC194446DE,06DDD7B87D14408EAEFF4E95A4354AD5,0CBBBF3BB22644E7B815C8355FDBAD71,0CBCB4F10DEF493481DD4EF9018E366E,0CFA5C6896CC4C958E8452C98254099E,10BC51503FE14498AC921010200768B0,11135ABB9E9F45A698AD7794EEC4CCE9,15FF6532D85C45858F2608B5A8BD98F7,18E1923429924ACC8CF4742E36B8DEDF,1B6B399E1ECE4635AEC888A2B7AB8873,1DEE3BA6D37A47969902424C0C2AFBE9,1EF246E4B60F44CBAF1F2DFCA8394235,247CC31966A348DF8A636519BC4BE356,266D2D21C35F400A94340EB01C0D5288,290776C339F84CD4B7DAA00641FEC660,2CF498812A7C4BC4A931FF318DF267AF,2D544EA152894117974EF9A9DC845DA1,305959FEACF14B7F807C0F7DED7C20CC,3224655A60DE45F481AEB398C3C7EB1A,33AE1CA6BDDD4757B7469C17F9FCF109,35B1FB95AB4F4727A697A027025BC1C6,36091D1D57E0432396C807A7C33A4F30,374F8B6B9F2D47E6A0432AFBA494C1E5,3969770AF8054A15AE392371B6E2ABF4,399DD6B684EC43BDAFE6CFB2DEEE7B9A,3A8003D52A5A496AAA8B399382146F18,3FEC7CEDFED9436FA8120305A400210D,43C45C36FA0E401DB36E53938004CE50,4480358E4634415ABDFB5EEEC7FDD82D,48D4BE24BE8248678E091B6C046CDE1F,49968A90547C4F999072856ABD6D0778,49B9643445864CE09F260CC35E8E51E1,4A2BDAF97F9548AC89314DE9CB68A4F9,4B52F9F815E84DEF83DD0ABE86066C3E,4BFFF163B9D24981908C0FC8452BFC00,4C59255B6529492F855B997E40B4E553,4D6D956D94B54EDCAD30677AAA47F079,4E0E1BFBAB0C43C88EE006A9861828CD,4F1757780F7340CF814784089FD45992,51F592BDD6A04A9C8AED72A619AC2FF7,58BCF19442E94FC6A5584F113A0B88ED,5E66B28F8BCC42CA8595E669B78B27CE,5E840F7B82764E048AC44D8C63C04272,5EFA106C18B44E989F32BE77128DA571,5F22F90F6FFB4ED289C915E807F5F18B,6150340BA4B342C482D9E7755C9D5442,6379B9CFE8AF452BBA2EBD0ACCA09470,64857A62BADA4205A4AAB10FDC144D3E,674E686E176C4506A5A148FEA3EC5A46,67CBA035403E49E2A35B7F4966E59A79,6867EE3F96EB4089A06EB3B5311C3477,689EAC06D3674484AECE3CC27600A2F5,6AFAFB49709D4CE38B323D7A04D72D87,6B21806335FD4751A67D528D213BCEF9,6B8BCBE409804EE6AACEE70689CE5C63,6C55000B7FD1432B98A511FD2E151F50,714F6498AC8C497C9B19C3958BD16A23,74BF8CA0EC224CDA84298B5102BB219F,764B4D192C0146818C64306C56E2FE87,77309E4FE5994586843481E25A68525D,792A6A30354F48EB9D707B4D88FEDD99,8198568786654576A7A22EF75D373813,825C8B4B22894B5DBC0DD9887A50F152,844BD2045E59483486A4C180A7E637A2,86BA8E1E155D417DA6FAE1CAEF4B556A,8712EB4BB9144D0091AEBA0AD4E4EF7C,928E8B6F7D24486CAD35AAC33F8E95F0,9C855C4F21A44E58A60AB758F47320E0,A0A10BAF0178440B974A43C1BA1A89CE,A2B3C1F7ED584A79A38B7A032C1744F7,A4D75F9F50CC43B393BD8D5F592BCF0B,A6068BEE3EA44959A85729AA75EA8AAD,AB023D7AA7D649FC8D6BA1A14E19FFE1,AD342CA210134AFEA11CA6710DD6ED55,AE48778B57CF42A498CE993DDE369404,B223A833E4CF448EB105B768E15A0D37,B42F445E87404F2AA3E258FF26637FD6,B48C33022A5341A8B8744C809370C0A1,B578FF8FC0664D2185C3FAAEE6577EA3,B7E3B0043F044636B24DC320C6FC0A28,B8EE888889AB49778A6F3E2CD34D57DF,BF0238DA58EA45B49DADD082904C926D,C15DD60A46D04201946A3BD207EF3946,C25C6C18C8724149BBE4F6CFE72A029F,C61B8A46C9CF4560A881AF9F16251C99,C8B0DAE9D9604679B81B299BA60F240A,CC40112512B845D1B97D9A74C58D4043,CEA8D56893CA495CA7FD50ECC6209DAB,D00FC9BFC3D946C78E80AA2BE31C91F1,D13AD87DC4914890A034218A0D9DAF24,D1CF518755344C9AB4F67967450A156C,D2301A01E9044BB49429B20BAE63BABA,D30EAA730CFD4B0D9452ED88C33CCCB9,D4214AC90EE84232885CA8018D6B46EE,D4D14E9FD7D64C69A8C028EA6EAB89D2,D738A383995D4CD19F9A87D541EF22BF,D7D98CE4AEBA4AADA84665324FE70D82,D8F9AD65C006406692483FFB30A85FFF,D9CD0825A4DA4CBB88AF134596D0B6B0,DA7543BDE4BF4783BDC6C6E8FF87EA16,DBF5AE09C93649609F75EF79A531CDF9,DDD9FF8D4069434B95F1DA60D210F6C0,DEFC693A18F74F3DBA816586BC4E6B00,DF5C3920015742F0A0C296CDEBC739F8,DF9A9EA828E84530BB857A46F8AB1544,DFF9C918EB8A4B49B693669CD0141A51,E166CB6ED5AC4DA598986A27CDA46D9C,E296E4AB094E441BA9F2A13050153664,E4865E8ACEAA4F3794E403749384D4AF,E487A352ECE64A158E888855EEEFD07A,E4F1123605FB4501AC424FCFBA19F3E8,E55182E96B984F3DAF6494CE3655407B,E9DFDCEFC9E346F5BDC4444E6E88A744,EC241B61BE434B63AE478D964F06ACD8,ECBB05EF146D4E72ABA23977A0E4C276,F099DFFBB581417F9B5C1831FDE97065,F1F883CD8D5A486E96EFFDEF2BB66E45,F2762C5276C64B008D202B5CE844794F,F6D1795876D84D04AEEA5F1403145898,F946A59266644208839A56E3F7D50584,FB60D2ADDC864C44A820B6F6E3C39A50,FCF7B8E754714293B5D7A44DD97C89EE",
phone: "13857404757"
},
message: "用户登录成功!"
}
```

失败：

```
{
    status: 0,
    message: "用户不存在"
}
```

# 2.修改密码
请求地址：==http://47.93.8.36:8000/modifypwd/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
--------- | -------- | ------------
username | String | 用户登录名称
oldpassword | String | 旧用户密码
newpassword | String | 新用户密码 

### 返回详情
成功：
```
{"status": 1, "message": "修改密码成功!"}
```

失败：

```
{"status": 0, "message": "修改密码失败!"}
```


# 3.司机任务列表
请求地址：==http://47.93.8.36:8000/driver/gettaskinfo/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 用户登录名（及手机号）（必填）
ordno | String | 输入的订单号（可空）
timefrom | String | 输入的起始时间（可空） （类似：2017-12-12）
timeto | String | 输入的结束时间（可空） 
status | String | 输入的任务状态，1-未发货，2-在途，3-已完成，4-已评价（可空） 
offset | int | 偏移量（必填） 
limit | int |获取数量（必填）

成功：
```
{
message: "success",
data: [
{
trip_id：1,//运单id
plate_number: "苏BM3028", //车牌号
tot_vol: "0.00",//总体积
trip_no: "170706013888",//客户单号
pre_load_time: "2017-07-03 15:37:00",//要求提货时间
create_uid: "17715671569",//创建用户（APP用不到）
note: "",//发运备注
tot_gross_w: "0",//总重量
site_num: 0,//停靠站点数目
create_time: "2018-04-05 00:50:43",//创建时间（APP用不到）
eta: "2017-07-04 15:37:00",//ETA
driver_mobile: "17715671569",//电话
gps_no: "",//GPS号
from_address: "养乐多合肥",//起点
status: 3,//状态
to_address: "养乐多无锡",//终点
driver_uid: "17715671569",//司机用户号（APP用不到，等同于司机手机号）
driver_name: "潘化强",//司机名称
pre_ubload_time: "2017-07-04 15:37:00"//要求到货时间
}
],
status: 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 4.司机任务调度单
请求地址：==http://47.93.8.36:8000/driver/gettaskdetail/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
trip_id | Int | 调度单id（必填）

成功：
```
{
status: 1,
data: [
{
phone: "", //电话
address: "浦东新区1",//地址
name: "普菲斯临港",//地点名称
time: "2017-07-03 00:00:00",//时间
flag: "load"//类型，load  提货  unload  卸货
},
{
phone: "69153330 * 64",
address: "杨浦区",
name: "上海夏晖",
time: "2017-07-03 00:00:00",
flag: "unload"
}
],
message: "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 5.司机子任务列表
请求地址：==http://47.93.8.36:8000/driver/getsubtasklist/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
trip_id | Int | 调度单id（必填）
task_id | Int | 任务id（必填）

成功：
```
{
data: [
{
weight: "0.00",//重量
eta: "2017-07-04 15:37:00",//ETA
task_no: "2017070300006",//任务好
reveive_time: "2017-07-03 00:00:00",//要求到货时间
volume: "0",//体积
task_id: 3//任务id
}
],
status: 1,
message: "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 6.司机任务大厅（发车接口）
请求地址：==http://47.93.8.36:8000/driver/action_send/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
trip_id | Int | 调度单id（必填）

成功：
```
{
status: 1,
message: "发车成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 7.司机任务大厅（状态数量接口）
请求地址：==http://47.93.8.36:8000/driver/trip_count/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 用户登录名（用户手机---司机手机）（必填）

成功：
```
{
    "data": {
        "nosend_count": 1,//未发车
        "sended_count": 0,//已结束
        "sending_count": 1,//运输中
        "all_count": 2//总数量
    },
    "message": "success",
    "status": 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 8.异常上报（异常列表接口）
请求地址：==http://47.93.8.36:8000/driver/getexceptions/==  
请求方式：==GET==  

成功：
```
{
status: 1,
data: [
{
priority: 100,//权重（用在排序）
exception_id: 1,//id
exception_ch: "道路交通问题"//名称
},
{
priority: 100,
exception_id: 2,
exception_ch: "客户问题"
},
{
priority: 100,
exception_id: 3,
exception_ch: "卸货问题"
},
{
priority: 100,
exception_id: 4,
exception_ch: "在途事故"
},
{
priority: 100,
exception_id: 5,
exception_ch: "车辆设备故障"
},
{
priority: 100,
exception_id: 6,
exception_ch: "温度异常"
},
{
priority: 100,
exception_id: 7,
exception_ch: "货损货差"
}
],
message: "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 9.车辆检查（检查项列表接口）
请求地址：==http://47.93.8.36:8000/driver/getchecks/==  
请求方式：==GET==  

成功：
```
{
data: [
{
check_ch: "车辆清洁无异味",
priority: 100,
check_id: 1
},
{
check_ch: "车辆设备检查",
priority: 100,
check_id: 2
},
{
check_ch: "随车文件检查",
priority: 100,
check_id: 3
},
{
check_ch: "冷机检查",
priority: 100,
check_id: 4
},
{
check_ch: "装载要求检查",
priority: 100,
check_id: 5
},
{
check_ch: "温度设置检查",
priority: 100,
check_id: 6
}
],
message: "获取成功",
status: 1
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 10.获取任务商品
请求地址：==http://47.93.8.36:8000/driver/getgoods/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
成功：
```
{
    "status": 1,
    "data": [
        {
            "good_id": 2,//货品id
            "ld_vol": "22.00",//货品应提体积
            "good_no": "12",//货品编号（APP无用）
            "good_name": "三文鱼123",//货品名称
            "ld_qnty": "22.00",//货品应提数量
            "task_id": 2,//货品所属的任务（APP显示无用）
            "ld_gross_w": "22.00",//货品应提重量
            "order_id": 1,//货品所属的订单（APP显示无用）
            "shpm_row": 1//行号
        }
    ],
    "message": "获取成功"
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 11.异常上报接口
请求地址：==http://47.93.8.36:8000/driver/putexecption/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
exceptionIds | String | 异常id集合,实例（1,2,3）（必填）
content|String| 异常描述（非必填）
longitude|String|经纬度（必填）
latitude|String|经纬度（必填）
images|List|图片集合（非必填）
### 请求体
```
{
	"task_id":2,
	"exceptionIds": "1,2,3",
	"content": "异常描述",
	"longitude":"1212.1212",
	"latitude":"1212.1212",
	"images":[
		{
			"base64":"data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4QBYRXhpZgAATU0AKgAAAAgAAgESAAMAAAABAA.............ijyD/z0P5VZyn//2Q=="
		}
		]
}
```
###### 成功：
```
{
    "message": "提交成功",
    "status": 1
}
```

#####失败：

```
{"status": 0, "message": "获取数据失败!"}
```


# 12.车辆检查接口
请求地址：==http://47.93.8.36:8000/driver/putcheck/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
checkIds | String | 检查项id集合,实例（1,2,3）（必填）
content|String| 异常描述（非必填）
longitude|String|经纬度（必填）
latitude|String|经纬度（必填）
images|List|图片集合（非必填）
### 请求体
```
{
	"task_id":2,
	"checkIds": "1,2,3",
	"content": "异常描述",
	"longitude":"1212.1212",
	"latitude":"1212.1212",
	"images":[
		{
			"base64":"data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4QBYRXhpZgAATU0AKgAAAAgAAgESAAMAAAABAA.............ijyD/z0P5VZyn//2Q=="
		}
		]
}
```
###### 成功：
```
{
    "message": "提交成功",
    "status": 1
}
```

#####失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 13.提货卸货页数据 获取接口
请求地址：==http://47.93.8.36:8000/driver/gettaskbase/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
成功：
```
{
    "status": 1,
    "message": "获取成功",
    "data": {
        "number": 20,//应提 件数
      	"send_address": "浦东新区1",//地址
        "volume": "22",//体积
        "weight": "4.00",//重量
        "order_no": "ON1222121212121444",//订单号
        "task_no": "TN212993892473742938238293829"//任务号
    }
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 14.到场确认接口
请求地址：==http://47.93.8.36:8000/driver/action_confirm/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
成功：
```
{
    "status": 1,
    "message": "到场确认成功",
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 15.开始装货接口
请求地址：==http://47.93.8.36:8000/driver/action_load/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
成功：
```
{
    "status": 1,
    "message": "到场确认成功",
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 16.提货接口
请求地址：==http://47.93.8.36:8000/driver/load/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
goods | List | 提货货品数量 重量 体积（必填）
content|String| 异常描述（非必填）
longitude|String|经纬度（必填）
latitude|String|经纬度（必填）
images|List|图片集合（非必填）
### 请求体
```
{
	"task_id":2,
	"goods": [
		{
			"good_id":1,//货品id
			"number":10,//货品数量
			"weight":22.2,//提货重量
			"volume":22.2 //提货体积
		}],
	"content": "异常描述",
	"longitude":"1212.1212",
	"latitude":"1212.1212",
	"images":[
		{
			"base64":"121212"
		}
		]
}
```
###### 成功：
```
{
    "message": "提交成功",
    "status": 1
}
```

#####失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 17.卸货接口
请求地址：==http://47.93.8.36:8000/driver/unload/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
task_id | Int | 任务id（必填）
goods | List | 提货货品数量 重量 体积（必填）
content|String| 异常描述（非必填）
longitude|String|经纬度（必填）
latitude|String|经纬度（必填）
images|List|图片集合（非必填）
### 请求体
```
{
	"task_id":2,
	"goods": [
		{
			"good_id":1,//货品id
			"number":10,//卸货数量
			"weight":22.2,//卸货重量
			"volume":22.2, //卸货体积
			"refusereason":"拒绝原因" //拒绝原因
		}],
	"content": "异常描述",
	"longitude":"1212.1212",
	"latitude":"1212.1212",
	"images":[
		{
			"base64":"121212"
		}
		]
}
```
###### 成功：
```
{
    "message": "提交成功",
    "status": 1
}
```

#####失败：

```
{"status": 0, "message": "获取数据失败!"}
```

# 18.拒收原因接口
请求地址：==http://47.93.8.36:8000/driver/getrefuses/==  
请求方式：==GET==  

成功：
```
{
message: "获取成功",
status: 1,
data: [
{
check_id: 1,
priority: 100,
check_ch: "货物损坏"
},
{
check_id: 2,
priority: 100,
check_ch: "包装破损"
},
{
check_id: 3,
priority: 100,
check_ch: "短少"
},
{
check_id: 4,
priority: 100,
check_ch: "包装潮湿"
},
{
check_id: 5,
priority: 100,
check_ch: "客户拒收"
},
{
check_id: 6,
priority: 100,
check_ch: "仓库损坏"
}
]
}
```

失败：

```
{"status": 0, "message": "获取数据失败!"}
```
# 19.消息中心接口
请求地址：==http://47.93.8.36:8000/driver/messages/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 登录用户名---用户手机（必填）
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

# 20.消息中心已读（更改状态为已读）
请求地址：==http://47.93.8.36:8000/driver/readmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 登录用户名---用户手机（必填）
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

# 21.消息中心未读（更改状态为未读读）
请求地址：==http://47.93.8.36:8000/driver/unreadmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 登录用户名---用户手机（必填）
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
# 22.消息中心删除（删除消息）
请求地址：==http://47.93.8.36:8000/driver/delmessage/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 登录用户名---用户手机（必填）
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
# 23.消息中心（新消息）
请求地址：==http://47.93.8.36:8000/driver/newmessages/==  
请求方式：==POST==  
### 所需参数

名称 | 类型 | 描述
------- | ---------- | ------------- 
username | String | 登录用户名---用户手机（必填）
message_id|Int| app 最新消息id
成功：
```
{
    "status": 1,
    "message": "有新消息",
    "data": {
        "type": "system",
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
