---
title: 评论 API
---

#  评论 API

## 创建评论

###问题评论
    POST   /questions/:id/comment.json

### 输入

content
: _Required_ **string**

<%= json \
  :question_id => 3508419221601184,
  :content => "Description of the answer."
%>

###答案评论
    POST   /answers/:id/comment.json

### 输入

content
: _Required_ **string**

<%= json \
  :answer_id => 3508419221601184,
  :content => "Description of the answer."
%>
