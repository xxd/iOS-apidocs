---
title: 问题 API
---

# 问题 API

## 付费问题列表
列出付费问题:

    GET /questions/paid

### Response
<%= headers 200, :pagination => true %>
<%= json(:questions) %>


## 免费问题列表
列出免费问题:

    GET /questions/free

### Response
<%= headers 200, :pagination => true %>
<%= json(:questions) %>

## 问题详情

显示一个指定的问题:

    GET /questions/:id

### Response

<%= headers 200 %>
<%= json :question %>

## 创建问题

    POST /questions

### 输入

title
: _Required_ **string**

content
: _Optional_ **string**

credit
: _Optional_ **integer**

money
: _Optional_ **integer**

<%= json \
	:title => "Question title",
  :content => "Description of the question, this field is optional.",
  :credit  => 10,
	:money => 10
%>

### Response

<%= headers 201, :Location => "https://luexiao.com/api/questions/1" %>
<%= json :only_question %>

## 收藏问题

    PUT /questions/:id/star

### Response

<%= headers 204 %>

## 取消收藏问题

    DELETE /questions/:id/star

### Response

<%= headers 204 %>

## 检测问题是否已收藏

    GET /questions/:id/star

### 问题已收藏的响应

<%= headers 204 %>

### 问题没有收藏的响应

<%= headers 404 %>

## 关注问题

    PUT /questions/:id/follow

### Response

<%= headers 204 %>

## 取消关注问题

    DELETE /questions/:id/follow

### Response

<%= headers 204 %>

## 检测问题是否已关注

    GET /questions/:id/follow

### 问题已关注的响应

<%= headers 204 %>

### 问题没有关注的响应

<%= headers 404 %>