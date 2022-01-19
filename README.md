## 介绍

1. 用于云原生学习的镜像
2. 已经安装了 Golang, git, make, docker


## docker in docker

需要宿主机上已经安装好 docker daemon

## Example

根据代码创建镜像

```bash
wget https://gitee.com/peter4431/wsdemo/repository/archive/main.zip
unzip main.zip
cd wsdemo-main/
make build ver=0.5

docker tag wsdemo:0.5 {namespace}/wsdemo:0.5
docker push {namespace}/wsdemo:0.5
```
