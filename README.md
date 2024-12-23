# Echo-Live WebSocket Server

这是一个适用于 [Echo-Live](https://github.com/sheep-realms/Echo-Live) 的简易 WebSocket 服务器。

## 支持情况

该软件仅适用于 Windows 操作系统。

该软件支持 Echo-Live 1.5.5 及以后版本。

## 使用方法

### 安装和运行服务器

1. 前往 [releases](https://github.com/sheep-realms/Echo-Live-WebSocket-Server/releases) 列表下载文件。
2. 将压缩包内容解压至 Echo-Live 的文件夹中。（如果您需要使用其他设备连接，放在 Echo-Live 的文件夹中是必须的）
3. 参阅 [Echo-Live 帮助文档](https://sheep-realms.github.io/Echo-Live-Doc/custom/config/)，分别启用编辑器和 Echo-Live 的 WebSocket，默认端口为 `3000`。
4. 打开解压出来的 `Echo-Live WebSocket Server.exe`，**在防火墙安全警告中勾选 “专用网络” 和 “公共网络”**。这会打开一个控制台窗口，使用时请勿关闭。
5. 打开 Echo-Live 的编辑器，现在它可以通过 WebSocket 服务器发送消息了，请注意日志输出。

### 跨设备连接

1. 想要跨设备连接，您首先需要获取服务器所在的设备的局域网 IP 地址。请您自行上网搜索您的操作系统如何获取局域网 IP 地址。另外，本程序启动时会在控制台中列出所有可能的局域网 IP 地址，通常第一个 IP 就是您的设备的局域网 IP 地址。
2. 请注意在配置中为编辑器启用 “自动设置连接地址”，这可以让您方便很多。
3. 假设您的服务器设备的局域网 IP 地址是 `192.168.0.1`，您设置的服务器端口号是 `3000`，您需要在您的另一台**位于同一网络**（例如连接了同一个 WiFi）的设备（例如手机）通过浏览器访问 `http://192.168.0.1:3000`（输入地址时注意切换到英文键盘）。如果您之前的安装操作正确，您将访问到编辑器。
4. 局域网地址可能会因与路由器断开连接而发生变化，如果您需要固定局域网地址，同样请您自行搜索。

### 如果我在防火墙安全警告中忘记勾选了怎么办？

1. 开始菜单 > 搜索 “控制面板” > 打开控制面板。
2. 所有控制面板项 > Windows Defender 防火墙 > 允许应用或功能通过 Windows Defender 防火墙。
3. 点击 “更改设置” 按钮，这需要管理员权限。
4. 找到所有名为 “Node.js JavaScript Runtime” 的项目，每个项目左侧和右侧共三个复选框全部勾选。

### 修改配置

您可以在 `server_config.json` 文件中修改服务器的端口号和首页文件地址。
