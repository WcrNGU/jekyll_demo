---
layout: default
title: 7月5日工作总结
---

# {{ page.title }}
今天做了一个用户注册与登陆系统，也更加深入理解了jdbc的使用  
statement对象为一次查询，一个connection可以有多个statement  
resultSet对象为查询的结果集，一个statement只能有一个resultSet  

接下来讲讲今天遇到的坑：  
1. 每次创建新项目都要重新导入jar驱动包，并非导入一次就可以无限使用
2. String判断相等有两种，==判断如果不是同一个引用就返回false，equals判断只根据字符串值是否相同
3. out.print("<script>alert('账户密码错误！即将返回登陆界面'); window.location='index.jsp' </script>");可以用java输出js脚本，用法和java输出html相同
4. rs.next(); //取得的结果集rs的指针指向第一条之前，必须执行一次rs.next()才能指向第一行
5. String str="select username,password from user where username='"+_user+"';"; 这里_user为String变量