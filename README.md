---
title:CVE-2019-0708批量检测
---
这个批量检测是基于360公开的无损检测工具（0708detector.exe），有以下功能：

1. 单个检测
2. 批量检测

````
双击0708detector-全自动批量版.exe即可使用！
````
批量检测支持自定义要检测的ip列表，自定义存在漏洞的ip集的储存位置。
批量检测有个缺点就是线程是1，在目标ip数目特别大的时候会特别的缓慢，不过优点就是用法很轻松，只要系统是windows就能使用了，不需要安装任何东西。
![](https://s2.ax1x.com/2019/05/29/VnmpnS.png)
3389.txt和0708.txt在这里都是相对路径，你也可以任意设置自己的文件所在位置。
其中3389.txt为要检测的IP列表。
格式为：
`````
192.168.80.1
192.168.80.3
192.168.80.16
xxx.xx.xx.xxx

`````
只要保证每一行都有一个ip就好了。

有时候我们需要批量检测一个网段的主机看看是否存在该漏洞，我是比较喜欢用msf的db_nmap去扫3389端口，扫完之后search -S open ，再拷贝下来正则处理一下，这样要检测的IP列表也很快速的弄好了。
