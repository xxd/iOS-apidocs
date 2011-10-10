---
title: Auth | Luexiao API
---

# Authentication

## Sign in
    POST /users/sign_in.json

### Request
<%= json \
	:user => {
	  :login => "vvdpzz",
	  :password => "vvdpzz"
	}
%>

### Response
<%= headers 201 %>
<%= json \
	:id => 1,
	:username => "vvdpzz",
	:realname => "Zheng-Yu Chen",
	:email => "vvdpzz@gmail.com",
	:credit => 10000,
	:money => 10000,
	:authentication_token => "CuzcnFkzzShumgHux7St",
	:about_me => "ACMer"
%>