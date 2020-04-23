# 用户相关

用户模块相关接口

---

### 1、返回当前用户的资料 
- 接口
``` api
	/SysUser/currLogin
```
- 返回
``` js
	{
		"code": 200,
		"msg": "ok",
		"data": {
			"id": 10001,			// 账号id
			"username": "root",		// 昵称
			"password": "********",	// 密码
			"sex": 1,				// 性别
			"avatar": "https://xxx.com/1.png",		// 头像地址
			"openid": null,		// openid
			"phone": null,		// 电话
			"status": 1,		// 状态（1=正常，2=封禁）	
			"role_id": 1,		// 所属角色id
			"create_type": 11,	// 账号创建方式
			"create_time": "2019-05-21T09:15:13.000+0000",	// 账号创建时间
			"login_time": "2019-07-11T02:12:28.000+0000",	// 最后登录时间
			"login_ip": "127.0.0.1",				// 最后登录ip
			"login_count": 432,					// 总登录次数 
		},
		"page": null
	}
```


--- 
### 2、当前用户修改资料
- 接口
``` api
	/SysUser/updateInfo
```
- 参数
``` p 
	{String}	avatar = ""				头像
	{String}	username = ""			昵称
	{int}		sex = 1					性别
	{String}	phone = ""				联系电话
	{String}	introduce = ""			个人介绍
```
- 返回 
@import(res)


--- 
### 3、根据旧密码修改新密码
- 接口：
``` api
	/SysUser/updatePassword
```
- 参数: 
``` p
	{String}	old_pwd		旧密码
	{String}	new_pwd		新密码
```
- 返回 
@import(res)

--- 
### 4、直接修改新密码
- 接口
``` api
	/SysUser/updatePassword2
```
- 参数
``` p
	{String}	new_pwd		新密码
```
- 返回 
@import(res)







