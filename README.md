# 通过浏览器访问docker
## 解压并执行
```
docker load < docker-exec-web-console.tar
docker run \
	--name docker-exec-web-console \
	-p 9999:8888 \
	-e "CONTEXT_PATH=/"\
	-v /var/run/docker.sock:/var/run/docker.sock \
	bitbull/docker-exec-web-console\
```

# 浏览器访问：
```
http://localhost:9999?cid=<container id>
http://localhost:9999?cid=<container id>&cmd=/bin/sh, 默认命令/bin/bash.
```
