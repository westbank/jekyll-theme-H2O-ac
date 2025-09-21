---
id: 1987
title: 'HTC-A315c, Bannka及其他'
date: '2011-05-29T03:59:44+00:00'
author: Westbank
layout: post
guid: 'http://farbank.net/2011/05/29/htc-a315c-bannka%e5%8f%8a%e5%85%b6%e4%bb%96/'
permalink: /2011/05/29/htc-a315c-bannka-and-others/
bot_views:
    - '9558'
views:
    - '6917'
latest_home_img:
    - htc.jpg
duoshuo_thread_id:
    - '1246078726781796601'
thumb_home_img:
    - thumb27.jpg
post_views_count:
    - '665'
categories:
    - 一地鸡毛
tags:
    - A315c
    - Bannka
    - root
---

经朋友介绍在买入电信定制机HTC-A315c以后，自觉羞于见人。配置较低，分辨率较差，最要命的是N多国外软件无法安装，纯粹一阉割货。当然现在再来回顾这些问题，好像也不算什么问题了。

购机之前我对android的了解几乎为零，因此买个初级一点的产品属于理性消费，3000多的Incredible对我来说太高端了一点。分辨率是很多人纠结的地方，这是一个问题，不过如果你只是一般的用途的话，此分辨率可以接受。(12a0a75c)

回到刚才的问题，突破软件安装限制才是最棘手的事情。要感谢我在Bannka上碰到的BBerLiu同学，没有他的思考和探索，我绝对没有办法突破限制。Bannka 就是一手机随拍的网站，简洁方便，创始人Kashgar大哥幽默风趣，平易近人。我原来用的是Picplz，但是手机经常出现故障提示，从而无法继续拍照。Bannka 则完全没有这个问题！另外，Bannka 有很好的交流氛围，轻松且随和。

对于A315c的研究来说，BBerLiu是毫无疑问的先驱者，google上检索有关内容几乎到处都可以发现他的足迹。他曾经提到两个重要问题：root and add-on. 定制机如果没有获得root权限的话，那就只好洗洗睡了。关键是怎么去获得A315c的root权限？BBerLiu同学的方法可行，但我感觉一般人很难把握。其他我看到了Z4 和 Superoneclick 的root法，我亲自测试了Superoneclick，版本是1.91，然后再使用RE。过程无需我赘述了，反正我十分担心自己的机器变成一块没用的砖头（注：superoneclick本身就支持HTC BEE）。不过，最后一切正常，取得了root的最高权限。可以在手机系统内部进行修改了。关机开机以后，最高权限仍然拥有，不会消失。当然，对于菜鸟来说，你得十分小心了。系统文件如果出问题，可能就没救了。

另外一个问题是add-on. 用豌豆精灵安装软件的时候，很多软件都会有这个错误提示：你的手机没有add-on属性。那add-on 本质其实是电信定制机人为地删除了google 部分组件造成的。如果能够恢复这些组件add-on的问题就应该不复存在了。想想真搞啊，android 是google 开发的，定制机竟然删除google组件，这也TM过河拆桥了吧。google 组件的位置应该位于：

地图框架：/system/framework/com.google.android.maps.jar

地图权限：/system/etc/permissions/com.google.android.maps.xml

网络定位:/data/app_s/NetworkLocation.apk

你只需将上述文件放到手机中的相应位置，重设好权限：三栏最左边三个全选，中间一栏选第一个，右边都不选。另外，NetworkLocation.apk适用于2.2版本，你可能需要手动设置/data夹下面的 app_s文件夹。

全部设置好以后，退出重启，启动时比平时要慢，然后一切搞定。首先就去试一试Foursquare吧！

其他：1. 如果你很怕自己的A315c成砖头，请忽略此文。不过即使你想尝试，这些方法肯定存在风险，风险个人承担；
2. google 原生的android market 能安装但仍然无法工作；
3. 其实最重要的还是root，相关操作我还是看的这个帖子：一键ROOT工具:SuperOneClick v1.9.1；
4. 其他talkbox,twi-tter 等神马的都不在话下了；
5. 此方法是否支持其他定制机，我不知道，别问我。

相关软件包在此下载，别担心我做手脚，你觉得我有能力修改源代码吗？
