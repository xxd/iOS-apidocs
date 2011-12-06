---
title: 答案 API
---

## 创建答案

    POST /answers.json

### 输入

question_id
: _Required_ **integer**

content
: _Optional_ **string**

<%= json \
	:question_id => 3508419221601184,
  :content => "Description of the answer."
%>

### Response

<%= headers 201, :Location => "http://luexiao.com/questions/3508419221601184" %>
<%= json :question %>

### 答案已关注的响应

<%= headers 204 %>

### 答案没有关注的响应

<%= headers 404 %>

### 接受答案

	GET    /questions/:question_id/answers/:id/accept.json