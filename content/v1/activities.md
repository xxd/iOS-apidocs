---
title: 动态 API
---

# 动态 API

## 关注用户动态题列表

    GET /activities/user_activity.json

### Response

<%= headers 200 %>
<%= json :user_activity %>

## 关注问题动态题列表

    GET /activities/question_activity.json

### Response

<%= headers 200 %>
<%= json :question_activity %>
