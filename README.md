## 介绍

1. 用于云原生学习的镜像
2. 已经安装了 Golang, git, make, docker


## docker in docker

需要宿主机上已经安装好 docker daemon

## Example

启动 cloudnative-exec 容器

```bash
kubectl apply -f cloudnative-exec.yaml
```

或者在 GUI 界面手动启动容器,通过任意方式，能够进入启动容器的终端即可

根据代码创建镜像

```bash
wget https://gitee.com/peter4431/wsdemo/repository/archive/main.zip
unzip main.zip
cd wsdemo-main/
make build ver=0.5

dokcer login
docker tag wsdemo:0.5 {namespace}/wsdemo:0.5
docker push {namespace}/wsdemo:0.5
```
