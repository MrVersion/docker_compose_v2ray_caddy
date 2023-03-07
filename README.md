# docker_compose_v2ray_caddy

### 环境要求
系统：ubuntu 18.04+

### 使用步骤
1. 在工作目录克隆代码 `git clone https://github.com/MrVersion/docker_compose_v2ray_caddy.git`
2. 进入目录 `cd docker_compose_v2ray_caddy/`
3. 修改 V2ray 配置文件 `vim v2ray/config.json` 将 `${V2RAY_UUID}` 替换成自定义的 UUID
```
"settings": {
	"clients": [
		{
			"id": "${V2RAY_UUID}",
			"level": 1,
			"alterId": 0
		}
	]
}
```
4.启动容器 `docker-compose up`
