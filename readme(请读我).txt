一. 程序说明

0708detector.exe　程序是360公司的360Vulcan Team发布的一款针对编号为CVE-2019-0708的Windows远程桌面协议漏洞的检测程序,原则上该扫描程序不会造成目标系统出现蓝屏,请您测试后再使用。

目前程序只支持单个IP的扫描,您可以自行构造出批量扫描的程序，谢谢。

注意：
1. 使用前，请务必在合法授权情况下对目标系统进行扫描；
2. 使用前，请注意检测程序的数字签名是否合法；
3. 程序可能由于网络问题导致检测不成功；
4. 如果有更多的问题，请邮件回复到　cert@360.cn 

二. 使用方法

1. 打开　“运行”　输入　cmd.exe ，“回车”运行

2. 跳转到程序所在目录，比如到C盘detector目录下

c:\>cd c:\detector\

3. 在 cmd.exe 窗口中，按程序的参数输入

c:\detector>0708detector.exe -t 192.168.91.138(要测试的目标IP) -p 3389(目标端口，一般都是3389)

a) 若目标存在漏洞

CVE-2019-0708 Remote Detection tool
                     by: 360Vulcan Team

[+] Connecting to RDP server.
[+] Socket : could not find a selected socket
[+] Establish connection with RDP server successful.
[+] Start 2nd stage detection.
[+] Connecting to RDP server.
[+] Establish connection with RDP server successful.
[!] !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
[!] !!!!!!WARNING: SERVER IS VULNERABLE!!!!!!!
[!] !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

b) 若目标系统已经开启NLA

CVE-2019-0708 Remote Detection tool
                     by: 360Vulcan Team

[+] Connecting to RDP server.
[!] Socket : recv error with -1 return
[!] Recv server TPDU req Failed
[*] Detect NLA enable! Server likely NOT vulnerable

c) 若目标系统已经进行补丁修复

CVE-2019-0708 Remote Detection tool
                     by: 360Vulcan Team

[+] Connecting to RDP server.
[+] Establish connection with RDP server successful.
[+] Start 2nd stage detection.
[+] Connecting to RDP server.
[+] Establish connection with RDP server successful.
[*] Server likely NOT vulnerable


三. 修复建议

1. 建议广大用户前往http://dl.360safe.com/leakfixer/360SysVulTerminator_CVE-2019-0708.exe，下载使用360远程桌面服务漏洞免疫工具，修复漏洞，保护用户系统和数据安全。

2. 自行下载对应的安全补丁进行补丁更新操作


三. 程序校验码

MD5:
febc027cee2782dba25b628ce3a893d6 *0708detector.exe

SHA256:
ccea8afec177d15d78329770b29f361b876addaa19eb93cabfaf90b896e03827 *0708detector.exe

