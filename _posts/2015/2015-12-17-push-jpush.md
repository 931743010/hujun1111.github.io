---
layout: post
title: 如何简单使用极光推送
category:  技术
tags: 
keywords: 
---

>做过几次极光推送的iOS端；发现每次都有那么几个坑，希望能对你有帮助

# 坑1
>导出的push的证书上没有小小的三角让你点击；让人感到诧异

原因；因为你制作这个push证书的时候；你本机上没有私钥
那么；很多人要问了 什么是私钥；我怎么能得到私有钥匙呢

>解决方法

	在制作push证书的时候会要求你导入一个钥匙串的东西
	那么问题来了；你是不是使用的之前的这个钥匙串呢？没有重新导出呢？ 问题找到了
	因为每次 导出   钥匙串访问-从证书颁发机构请求证书  就会自动在机器上面生成私钥
那么重新请求一次证书；你的电脑商就生成了私钥了；再次去申请push证书；导出运行就能看到小三角了

# 坑2
>导出的push的证书使用不对

原因：导出的时候选择的是里面的私钥导出的

>解决方法
直接点击push证书导出p12 文件就可以了


# 开始你的极光推送之旅吧