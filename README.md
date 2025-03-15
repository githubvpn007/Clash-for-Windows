# Clash-for-Windows                
Clash for Windows使用教程，Clash-for-Windows配置，Clash-for-Windows说明，Clash-for-Windows、vpn代理服务器   


简介
----

Clash 是一个使用 Go 语言编写，基于规则的跨平台代理软件核心程序。  
Clash for Windows 是目前在 Windows 上唯一可用的图形化 Clash 分支。  
通过 Clash API 来配置和控制 Clash 核心程序，便于用户可视化操作和使用。  

**支持的协议： Vmess, Shadowsocks, Snell , SOCKS5 , ShadowsocksR（在0.11.2版本加入）**  


注：ClashR for Windows 是第三方修改版本，已汉化。支持SSR协议，使用方法与原版相同。Clash for Windows从0.11.2版本开始原生支持SSR协议，ClashR已经完成了它的历史使命。   


<br/>
<br/> 


步骤
---


(1)下载安装  

[下载地址](https://archive.org/download/clash_for_windows_pkg)   选择 Clash.for.Windows.Setup.x.xx.x.exe  

注意：由于 Clash for Windows 没有任何有效的数字签名，因此 SmartScreen 可能会弹出提示，请点击 **「更多信息」**，然后选择 **「仍要运行」** 。 


(2)安装完成之后 进行汉化

- 操作前需要关闭Clash，处于未在运行状态  
- 如果是安装版的Clash，那么可以对着 **Clash桌面图标** 单击右键，选择 **打开文件所在位置**，即可找到clash主程序所在的 **Clash for Windows文件夹** 。然后双击进入 **resources** 文件夹，找到  **app.asar** 这个文件。  
- 点击下载对应版本的 [Clash for Windows汉化文件](https://github.com/Z-Siqi/Clash-for-Windows_Chinese/releases?page=1)，然后用它替换掉原来的 **app.asar** 文件。  
- 替换完成之后运行软件即可看到效果。  
- 如果下载的是便携版的Clash for Windows，直接找到**resources**文件夹进行替换**app.asar**操作即可。  
- 如下图所示  

![](https://i.postimg.cc/7LtLhLLP/1.png)  
![](https://i.postimg.cc/B68nKG8T/2.png)  
![](https://i.postimg.cc/G2ZhPSYZ/3.png)  
![](https://i.postimg.cc/NjgGxX9f/4.png)


(3)先在机场官网复制 Clash(R)订阅链接。如果没有Clash(R)订阅 [请看这里](https://github.com/githubvpn007/v2rayNvpn#%E8%8A%82%E7%82%B9%E5%88%86%E4%BA%AB)  


(4)打开 Clash for Windows 应用程序，在左侧的标签页中选择「Profiles」， 在顶部输入您的 **Clash 订阅链接** ，然后点击「Download」按钮。  

![](https://i.postimg.cc/RhKCgQLq/5.png)

(5)Clash for Windows 会自动拉取配置文件进行更新，如果一切顺利，你应当可以看到绿色提示信息「Success!」，并且可以看到一个新增的配置文件：

![](https://i.postimg.cc/FsbscpKB/6.png)  


(6)点击新增的配置文件来切换到该配置，然后点击「Proxies」标签页来切换接入点，将顶部的出站模式选择为「Rule」。 

此模式下你的网络访问请求将通过 Clash for Winows 进行**分流处理**。

![](https://i.postimg.cc/ncfhCgnm/7.png)  


注意：在「Proxy」策略组中选择所想要使用的接入点。Proxy 策略组是用于访问国际网络的默认策略，在不进行其他修改的情况下，所有国际网络的访问都通过 Proxy 策略组中选择的接入点进行。

图中所示的其它策略组为本人出于自身实际需求自行配置的，请以自己的实际配置为准。  



(7)启动 Clash for Windows  

返回到「General」部分，将「System Proxy」的开关更改为 [绿色](#1)状态即可开始使用。此外，建议将「Start with Windows」也更改为[绿色](#1)来让 Clash for Windows 在开机时自动启动。

![](https://i.postimg.cc/XNCvN463/8.png)  


(8)如果无法直接从软件里更新自己的订阅  

在无法直接从软件里更新自己的订阅时，可以复制你的链接，直接粘贴到浏览器打开，然后复制全部的文本，在桌面新建一个文本文档（TXT格式），然后粘贴到文档里，保存后将文件的扩展名更改为 YAML 。然后直接拖拽到软件的 Proflies 界面。  



(9)完成以上步骤就可以上网了

<br/>
<br/>


其他知识
----

(1)Clash for Windows 界面简介  

![](https://i.postimg.cc/rwQVZpxG/9.png) 

**General（常规）**  

- **Port、Socks Port**；分别为 HTTP、SOCKS 代理端口，点击终端图案可以打开一个配置了代理的命令行窗口，点击端口数字可以复制该命令；  
- **Allow LAN**：启用局域网共享代理功能；  
- **Log Level**：日志等级；  
- **Home Directory**：点击下方路径直达 C:\Users\用户名\.config\clash 文件夹；  
- **GeoIP Database**：点击下方日期可更新 GeoIP 数据库；  
- **WP Loopback** ：可以用来使 UWP 应用解除回环代理限制；  
- **Tap Device** ：安装 cfw-tap 网卡，可用于处理不遵循系统代理的软件（实际启动 tap 模式需要更改配置文件）；  
- **General YML**：编辑 config.yml 文件，可用于配置部分 General 页面内容；  
- **Dark Theme**：控制暗色模式；  
- **System Proxy**：启用系统代理；  
- **Start with Windows**：设置开机自启；  



**Proxies（代理）**  

选择代理方式（Global - 全局、Rule - 规则、Direct - 直连）及策略组节点选择；  


**Profiles（配置管理）**  

- 用来下载远端配置文件和创建本地副本，且可在多个配置文件间切换  
- 对配置进行节点、策略组和规则的管理（添加节点、策略组和规则在各自编辑界面选择 **Add**, 调整策略组顺序、节点顺序及策略组节点使用拖拽的方式）；  



**Logs（日志）**  

显示当前请求命中规则类型和策略；  



**Connections (连接)**  

显示当前的 TCP 连接，可对某个具体连接执行关闭操作；  


**Feedback（反馈）**  

显示软件、作者相关信息，内含捐赠码，欢迎打赏。





<br/>
<br/> 

## [更多教程请看这里](https://github.com/githubvpn007/v2rayNvpn#%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)
## [更多工具下载看这里](https://github.com/githubvpn007/ProxyTool)



