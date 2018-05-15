---
description: Asuswrt-merlin
---

# 华硕-梅林固件

{% hint style="danger" %}
本方法非常繁琐，操作过程中出错，本站不负任何责任！
{% endhint %}

## **基本介绍**

### **介绍**

Asuswrt是华硕公司为他的路由器所开发的固件。Asuswrt-merlin是一个对Asuswrt固件二次开发进行各种改进和修正的项目。作者： Eric Sauvageau，官网：[https://asuswrt.lostrealm.ca](https://asuswrt.lostrealm.ca)

### 设备要求

梅玲固件存在2个分支：

* 原版（旧版）梅玲固件（380.xxx版本）
* 新一代（最新）梅玲固件\(382.xxx以及更新版本\)

不同版本支持不同型号的路由器，

{% hint style="danger" %}
开始前，请先确保您的路由器为支持型号
{% endhint %}

旧版梅玲固件（380.xxx）支持型号：

* RT-N66U
* RT-AC66U
* RT-AC56U
* RT-AC66U\_B1 \(使用RT-AC68U 防火墙\)
* RT-AC68U, RT-AC68P, RT-AC68UF \(包含HW 调整的C1 和 E1\)
* RT-AC1900 & RT-AC1900P \(使用 RT-AC68U 防火墙\)
* RT-AC3200
* RT-AC87U
* RT-AC88U
* RT-AC3100
* RT-AC5300

最新版本梅玲固件（382.xxx及更新版本）支持型号：

* RT-AC56U
* RT-AC66U\_B1 \(使用 RT-AC68U 防火墙\)
* RT-AC68U, RT-AC68P, RT-AC68UF \(包含HW 调整的C1 和 E1\)
* RT-AC1900 & RT-AC1900P \(使用 RT-AC68U 防火墙\)
* RT-AC3200
* RT-AC87U
* RT-AC88U
* RT-AC3100
* RT-AC5300
* RT-AC86U

不再支持型号：

* RT-N16

注：所有“R”型号的 \(比如 RT-N66R\) 和"U" 一样, 他们只是包装不同/销售商问题. 防火墙在U和R上是一样的.  "W" 也是一样处理。

参考资料：[https://github.com/RMerl/asuswrt-merlin/wiki/Supported-Devices](https://github.com/RMerl/asuswrt-merlin/wiki/Supported-Devices)

### 优点

Merlin固件拥有更多的功能，由于第三方不断维护代码，各种新功能也在不断增加。Merlin固件的升级并不需要反复的操作过程，方法与官方固件的升级相同，有很好的硬件软件兼容性。继承了Asuswrt官方固件优秀的交互界面。Koolshare论坛所分享的固件大多是基于Merlin代码再次改进，增加适合国内使用的功能。  
**二、固件刷入  
1、下载固件**见本版置顶帖**2、上传并刷写固件\(**如你是R7K或R6300V2用户，请参考这两个贴（因为网件的原版固件无法直接刷，需要过度固件）[R6300 V2](http://koolshare.cn/thread-3860-1-1.html)[R7000](http://koolshare.cn/thread-4451-1-1.html)\*迅雷路由可通过刷写CFE使用AC56U固件，刷写教程见[此链接](https://amefs.net/archives/94.html)**）**  
Asuswrt-merlin固件的刷入并不需要特殊工具辅助，当你下载好后缀为.trx的固件升级文件后，打开路由配置页面。您可以通过您预先设定的ip访问，也可以通过[http://router.asus.com/](http://router.asus.com/)来访问。打开路由配置页面之后选择”系统管理-&gt;固件升级”点击选择文件，选择好.trx文件后点击上传。此时，路由会接受您电脑上传的升级固件包，并且校验，如果下载的固件不完整则会弹出相应警告，在固件校验完成后，就会进行固件刷写，此时必须耐心等待，切忌拔出电源。大约2-3分钟后刷写结束，路由自动重启。![](http://image.koolshare.cn/attachment/forum/201505/23/194656uz11661sv11coz3r.jpg)![](http://image.koolshare.cn/attachment/forum/201505/23/194631ls18vd2gnx23eggq.png)**3、路由配置**由于Asuswrt-merlin固件的一部分功能需求，有时需要清除旧版本配置，特别是当固件帖中明确要求清空配置的时候。![](http://image.koolshare.cn/attachment/forum/201505/23/194909s5nzptr94f9t94qp.jpg)**4、打开jffs分区（启用扩展功能的必要操作）现在koolshare固件默认开启jffs分区**系统管理-&gt;系统设置-&gt;开启jffsEnable JFFS partitionEnable JFFS custom script and configs（378.53新增选项，需启用）Format JFFS partition at next boot（如果第一次运行此分区，则需要选择此功能，此功能需要重启）![](http://image.koolshare.cn/attachment/forum/201505/23/195037x9twzg4a0deefw5e.jpg)**5、开启Telnet现在koolshare固件均带有webshell，并默认开启，路由配置页面上方点击webshell即可使用**有一部分进阶操作需要使用Telnet。打开方法：系统管理-&gt;系统设置-&gt;启动Telnet。![](http://image.koolshare.cn/attachment/forum/201505/23/195224u02y3iyi04u4y77z.jpg)

