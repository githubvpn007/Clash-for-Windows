# Clash-for-Windows
Clash for Windows使用教程，Clash-for-Windows配置，Clash-for-Windows说明，Clash-for-Windows


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

[下载地址](https://github.com/Fndroid/clash_for_windows_pkg/releases)   下载 Clash.for.Windows.Setup.x.xx.x.exe  

注意：由于 Clash for Windows 没有任何有效的数字签名，因此 SmartScreen 可能会弹出提示，请点击 **「更多信息」**，然后选择 **「仍要运行」** 。 


(2)安装完成之后 进行汉化

- 操作前需要关闭Clash，处于未在运行状态  
- 如果是安装版的Clash，那么可以对着 **Clash桌面图标** 单击右键，选择 **打开文件所在位置**，即可找到clash主程序所在的 **Clash for Windows文件夹** 。然后双击进入 **resources** 文件夹，找到  **app.asar** 这个文件。  
- 点击下载对应版本的 [Clash for Windows汉化文件](https://github.com/githubvpn007/Clash-for-Windows/releases/tag/%E6%B1%89%E5%8C%96%E5%8C%85)，然后用它替换掉原来的 **app.asar** 文件。  
- 替换完成之后运行软件即可看到效果。  
- 如果下载的是便携版的Clash for Windows，直接找到**resources**文件夹进行替换**app.asar**操作即可。  
- 如下图所示  

![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/1.png)  
![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/2.png)  
![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/3.png)  
![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/4.png)


(3)先在机场官网复制 Clash(R)订阅链接。如果没有Clash(R)订阅 [请看这里](https://github.com/githubvpn007/v2rayNvpn#%E8%8A%82%E7%82%B9%E5%88%86%E4%BA%AB)  


(4)打开 Clash for Windows 应用程序，在左侧的标签页中选择「Profiles」， 在顶部输入您的 **Clash 订阅链接** ，然后点击「Download」按钮。  

![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/5.png)

(5)Clash for Windows 会自动拉取配置文件进行更新，如果一切顺利，你应当可以看到绿色提示信息「Success!」，并且可以看到一个新增的配置文件：

![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/6.png)  


(6)点击新增的配置文件来切换到该配置，然后点击「Proxies」标签页来切换接入点，将顶部的出站模式选择为「Rule」。 

此模式下你的网络访问请求将通过 Clash for Winows 进行**分流处理**。

![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/7.png)  


注意：在「Proxy」策略组中选择所想要使用的接入点。Proxy 策略组是用于访问国际网络的默认策略，在不进行其他修改的情况下，所有国际网络的访问都通过 Proxy 策略组中选择的接入点进行。

图中所示的其它策略组为本人出于自身实际需求自行配置的，请以自己的实际配置为准。  



(7)启动 Clash for Windows  

返回到「General」部分，将「System Proxy」的开关更改为 [绿色](#1)状态即可开始使用。此外，建议将「Start with Windows」也更改为[绿色](#1)来让 Clash for Windows 在开机时自动启动。

![](https://github.com/githubvpn007/Clash-for-Windows/blob/main/images/8.png) 
