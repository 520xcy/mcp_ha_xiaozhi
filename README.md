# mcp_ha_xiaozhi
小智官方服务器(虾哥)对接home assistant的mcp server
### 原理
使用小智官方给的示例代码，结合mcp_proxy,实现小智官方服务器和home assistant的mcp server打通


### 参数
XIAOZHI_MCP_ENDPOINT：你的小智 MCP 接入点
HA_MCP_ENDPOINT：你的 HA MCP SERVER 地址
API_ACCESS_TOKEN：你的长效 API 令牌

1.  **小智 MCP 接入点：** 登录小智官方服务器即可获取。
2.  **HA MCP SERVER 地址：** 通过 HA 官方的 `mcp_server` 集成获取。
    * 点击此链接：[Home Assistant MCP Server 集成](https://my.home-assistant.io/redirect/config_flow_start?domain=mcp_server)直达安装
    * 或 在 Home Assistant 中，前往 **设置 > 设备和服务 > 添加集成**。
    * 从列表中选择“**模型上下文协议服务器**”，并按照屏幕上的说明完成设置。
3.  **长效 API 令牌：** 用于授权访问你的 Home Assistant 实例。
    * 访问你的 [Home Assistant 账户配置文件设置](https://my.home-assistant.io/redirect/profile)，进入“**安全**”选项卡。
    * 创建**长期访问令牌**。


### docker运行
```bash
docker run -d --name mcp_ha_xiaozhi \
-e XIAOZHI_MCP_ENDPOINT="你的小智MCP接入点" \
-e HA_MCP_ENDPOINT="你的HA MCP SERVER地址" \
-e API_ACCESS_TOKEN="你的长时效API令牌" \
shawn68/mcp_ha_xiaozhi
```

https://hub.docker.com/r/shawn68/mcp_ha_xiaozhi/
