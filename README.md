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
4.修改 Caddyfile 文件 `vim caddy/Caddyfile`，将 `$YOUR_DOMAIN_COM` 改为自己的域名 example.com
5.创建网络 `docker network create v2ray_net`
6.启动容器 `docker-compose up`
