---
title: 问题 API
---

# 问题 API

## 付费问题列表
列出付费问题:

    GET /questions/paid.json

### Response
<%= headers 200, :pagination => true %>
<%= json(:questions) %>


## 免费问题列表
列出免费问题:

    GET /questions/free.json

### Response
<%= headers 200, :pagination => true %>
<%= json(:questions) %>

## 问题详情

显示一个指定的问题:

    GET /questions/:id.json

### Response

<%= headers 200 %>
<%= json :question %>

## 创建问题

    POST /questions.json

### 输入

title
: _Required_ **string**

content
: _Optional_ **string**

credit
: _Optional_ **integer**

reputation
: _Optional_ **integer**

end_date
: _Optional_ **datetime**


<%= json \
		 :title  => "Question title",
	   :content  => "Description of the question, this field is optional.",
	:reputation  => 10,
	  	 :money  => 10,
	  :end_date  => "2011-12-30 00:00:00"
%>

### Response

<%= headers 201, :Location => "http://luexiao.com/questions/1" %>
<%= json :only_question %>

## 收藏问题

    PUT /questions/:id/favorite.json

### Response

<%= headers 204 %>

## 取消收藏问题

    DELETE /questions/:id/favorite.json

### Response

<%= headers 204 %>

## 检测问题是否已收藏

    GET /questions/:id/favorite.json

### 问题已收藏的响应

<%= headers 204 %>

### 问题没有收藏的响应

<%= headers 404 %>

## 关注问题

    PUT /questions/:id/follow.json

### Response

<%= headers 204 %>

## 取消关注问题

    DELETE /questions/:id/follow.json

### Response

<%= headers 204 %>

## 检测问题是否已关注

    GET /questions/:id/follow.json

### 问题已关注的响应

<%= headers 204 %>

### 问题没有关注的响应

<%= headers 404 %>