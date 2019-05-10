说明：

使用Dockerhub的Automated Builds功能从github仓库的dockerfile中构建镜像，Build到dockerhub个人仓库，然后再从它们上面拉取.

dockerhub仓库：https://hub.docker.com/u/charlesqing/

github构建仓库：https://github.com/charlesqing/kubernetes-images

google镜像仓库：https://console.cloud.google.com/gcr/images/google-containers/GLOBAL

使用方法：

拉取images
docker pull charlesqing/kube-apiserver-amd64:v1.13.2

修改tag
docker tag charlesqing/kube-apiserver-amd64:v1.13.2 k8s.gcr.io/kube-apiserver-amd64:v1.13.2

删除原镜像
docker rmi charlesqing/kube-apiserver-amd64:v1.13.2

配置加速器：
使用docker hub镜像建议配置加速器，参考daocloud镜像加速器配置：https://www.daocloud.io/mirror

构建配置教程:
https://blog.csdn.net/networken/article/details/84571373
