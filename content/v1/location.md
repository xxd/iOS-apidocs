---
title: 地理位置的存储 API
---

# 地理位置的存储 API

### 格式
	
	Float类型，例如：
	Longitude = 116.40740789, Latitude = 39.90422389
    但是由于 ｀.｀ 不可以在url中输入，所以使用 ｀_｀ 替代，如下：
	Longitude = 116_40740789, Latitude = 39_90422389

### 获取周围的问题

显示一个指定的问题:

    GET /questions/near/:longtitude/:latitude
	`输入时请注意`

### 输入

Longitude
: _Required_  116_40740789 

Latitude
: _Optional_  39_90422389

### Response

<%= headers 200 %>
<%= json :location %>

### 关于如何创建带有地利位置的问题请查看 

[问题](http://0.0.0.0:3001/v1/questions/) <创建问题部分>

