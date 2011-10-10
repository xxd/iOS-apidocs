---
title: Answers | Luexiao API
---

## 创建问题

    POST /answers

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

<%= headers 201, :Location => "https://mayday.fm:3000/questions/3508419221601184" %>
<%= json :question %>