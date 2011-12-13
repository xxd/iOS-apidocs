---
title: 私信 API
---

# 私信 API

## 私信题列表
	
	GET /messages.json

## 单一私信对话题列表
    GET /messages/load_conversations.json

## 创建私信

    POST /messages.json

### 输入

recipient_token
: _Required_ **integer**

text
: _Optional_ **text**

<%= json \
		 :recipient_token  => "1449220410439085",
		 :text             => "a new message"
%>
	


