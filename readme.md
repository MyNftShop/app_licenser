[TOC]

# page实现的注册机数据库
产生日期 9/13/2017 11:53:21 PM 

## 工作流程:

客户端请求验证,收到[MSG];注册机生成字符串,并加密得到[MSG],保存此项目上

客户端:

	通过网络请求userID.html页面,获得json字符串
	[{appid:'XXX',state:0}]  已经经过加密过的
	base64解密,公钥解密,json解析

注册机:

	生成 [{appid:'XXX',state:0}] 私钥加密,的字符串,base64编码,提交到服务器.

## 访问接口

https://sangxiaokai.github.io/app_licenser/

	Users
	  -----demo@demo.html
	  -----user@user.html

数据:
	[{appid:'XXX',state:0}] ----加密后的字符串

## 目录结构设计



