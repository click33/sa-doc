# 参数示例

演示 `sa-doc` 的各种写法，具体可根据源码对比最终展现结果 

---

- 写一个接口
``` api
	/SysSwiper/add
```
- 参数 - 最简单写法
``` p
	username			账号名称 
	password			账号密码 
	way					登录方式(1=账号登录，2=id登录，3=手机号登录)
```

- 参数 - 带默认值 
``` p
	username = admin			账号名称 
	password = admin			账号密码 
	way = 1						登录方式 (1=账号登录，2=id登录，3=手机号登录)
```

- 参数 - 带数据类型 
``` p
	{String}	username = admin			账号名称 
	{String}	password = admin			账号密码 
	{String}	way = 1						登录方式 (1=账号登录，2=id登录，3=手机号登录)
```

- 返回示例
``` js
	{
		"code": 200,        // 状态码
		"msg": "ok"            // 返回描述
		"data": null        // 携带数据：一般在查询时有值
		"dataCount": null        // 数据总数：一般在分页查询时有值
	}
```

- 导入一段代码
@import(res)