# 1.登录
请求地址：==http://47.93.8.36:8000/signin/==  
请求方式：==POST==  


### 所需参数

名称 | 类型 | 描述
- | :-: | -: 
username | String | 用户登录名称
password | String | 用户密码
asntype | String | 用户类型（'CUSTOMER'：客户端,'DRIVER':司机端）

### 返回详情
成功：
```
{
    message: "success",
    status: 1,
    data: {
        email: "920106140@qq.com",
        name: "happy1",
        role_name: "司机",
        freq_get_gps: 2,
        alert_dur: 3,
        log_dur: 5,
        freq_upload_gps: 5,
        update_time: "2018-03-22 21:49:42",
        mobile: "15221089805",
        enabled: 1,
        company_id: 1,
        language: "cn",
        company_name: "中国邮政",
        password: "123456",
        create_time: "2018-03-22 21:49:42",
        role_id: 3
    }
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
- | :-: | -: 
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