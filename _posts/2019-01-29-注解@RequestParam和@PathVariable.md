---
layout: post
title: 注解@RequestParam和@PathVariable
date: 2019-01-29
author: 十二
header-img: img/post-bg-2015.jpg
catalog: true
tags:
    - spring
---

## 注解@RequestParam和@PathVariable

 在**spring mvc**中，两者的作用都是将request里的参数的值绑定到contorl里的方法参数里的，区别在于，URL写法不同
 使用@RequestParam时，URL是这样的：http://host:port/path?参数名=参数值
 使用@PathVariable时，URL是这样的：http://host:port/path/参数值
 
 **示例如下：**
 ```
    //此方法访问url：http://host:port/user?id=1
    @RequestMapping(value="/user",method = RequestMethod.GET)
    public User getUser1(@RequestParan int id){
            ***
            return user;
    }
    
    //此方法访问url： http://host:port/user/1
    @RequestMapping(value="/user/{id}",method = RequestMethod.GET)
    public User getUser2(@PathVariable int i ){
            ***
            return user;    
     }

```
