# 轮播图相关 

---

### 1、增加
- 接口
``` api
	/SysSwiper/add
```
- 参数
``` p
	{String}	title = ""			标题
	{String}	img_src = ""			图片地址 
	{String}	link=""				链接 
	{int}		status=1			状态（1=正常，2=禁用） 
	{long}		sort=1				排序值 
```
- 返回 
@import(res)


### 2、删除
- 接口
``` api
	/SysSwiper/delete
```
- 参数
``` p
	id			要删除的记录id
```
- 返回
@import(res)


### 3、修改
- 接口
``` api
	/SysSwiper/update
```
- 参数
``` p
	{String}	title=""		标题
	{String}	img_src=""		图片地址
	{String}	link=""			链接
	{int}		status=1		状态（1=正常，2=禁用）
	{long}		sort=0			排序值
	{long}		id=""			要修改的记录id
```
- 返回
@import(res)


### 4、查 - 根据id
- 接口
```  api 
	/SysSwiper/getById
```
- 参数
``` p
	id				要查询的记录id
```
- 返回示例
``` js
	{
		"code": 200,
		"msg": "ok",
		"data": {
			"id": 2,		// 记录id
			"title": "第2个  ",		// 标题
			"img_src": "https://xxx.com/1.png",		// 图片地址
			"type": 1,	// 类型，暂无作用，留作以后扩展
			"link": "",	// 链接
			"click_count": 0,	// 点击次数
			"create_time": "2019-05-23T03:11:16.000+0000",	// 创建时间 
			"status": 1,	// 状态（1=正常、2=禁用）
			"sort": 3		// 排序值（手机端按照排序值的大小从小到大进行前后排列）
		},
		"page": null
	}
```


---
### 5、查 - 列表
- 接口
``` api
	/SysSwiper/getList
```
- 参数(参数为null或者0时代表不限制条件)
``` p
	{String}		title=""			标题，模糊查询
	{int}			status=1			状态（1=正常、2=禁用）
```
- 返回 
``` js
	{
		"code": 200,
		"msg": "ok",
		"data": [
			// 数据列表，格式参考见上  
		],
		"dataCount": 100	// 数据总数
	}
```










