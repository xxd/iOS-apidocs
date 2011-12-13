---
title: 照片 API
---

# 照片 API

## 上传照片

    PUT /photos.json

### 输入

Filename
: _Required_ **string**

_magic_session
: _Optional_ **string**

fileext
: _Optional_ **string**

authenticity_token
: _Optional_ **string**

folder
: _Optional_ **string**

Submit Query
: _Optional_ **string**

<%= json \
	       :Filename => "3.jpg", 	   
  	 :_magic_session => "BAh7CEkiD3Nlc3Npb25faWQGOgZFRkkiJTQwZTlhY2RmNzQxMDkyNTE4NDYzOTc5NTZhNjU5OGQ5BjsAVEkiEF9jc3JmX3Rva2VuBjsARkkiMTh0dEVIVjRmT2hyNCtFTGpKa1dMTG1uUWsvOC9IbGlMbUdqTjNDdFFQU2c9BjsARkkiGXdhcmRlbi51c2VyLnVzZXIua2V5BjsAVFsISSIJVXNlcgY7AEZbBmwrCWoLdZT3iwoASSIiJDJhJDEwJEpDeUs2RDlIbE5MNVEyU0U4SkVFRU8GOwBU--e5b3546a6f631a042bea7e24df27f960cb656729", 
	        :fileext => "*.jpg;*.jpeg;*.gif;*.png", 
 :authenticity_token => "8ttEHV4fOhr4+ELjJkWLLmnQk/8/HliLmGjN3CtQPSg=",
             :folder => "/questions/",
			:Upload => "SubmitQuery"
%>

### Response

<%= headers 201, :Location => "http://luexiao.com/photos/1" %>

## 删除照片

	DELETE /photos/:id.json

### Response

	<%= headers 204 %>
