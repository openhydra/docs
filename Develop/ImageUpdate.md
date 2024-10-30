# 镜像的操作

本文档描述了，如何手动更新最新的 openhydra 的常用的镜像

## 镜像描述

### release-2.0

我们通常在一些常用的镜像社区会保持更新，以下是常用的镜像的描述

* registry.cn-shanghai.aliyuncs.com/openhydra/aes-ai-tutor:release-2.0 -- 用于虚拟助教提供知识库服务的组件
* registry.cn-shanghai.aliyuncs.com/openhydra/aes-dashboard:release-2.0 -- 负责前端页面的镜像
* registry.cn-shanghai.aliyuncs.com/openhydra/core-api-server:release-2.0 -- 负责核心 api 服务的镜像

镜像对应的 k8s 部署控制器的名字

* aes-ai-tutor -- aes-ai-tutor
* aes-dashboard -- aes-dashboard-deployment
* core-api-server -- core-api-server

## 更新镜像

### 更新 aes-ai-tutor

首先我们登陆到 openhydra 所安装的服务器并执行以下

```bash
# 切换到 root,输入密码
$ sudo -s

# 停止当前服务
$ kubectl scale --replicas=0 deployment/aes-ai-tutor -n ai-education-studio

# 通过重命名复制旧镜像
# 以便于回滚
$ ctr -n k8s.io i tag registry.cn-shanghai.aliyuncs.com/openhydra/aes-ai-tutor:release-2.0 registry.cn-shanghai.aliyuncs.com/openhydra/aes-ai-tutor:release-2.0-old

# 删除旧镜像
$ ctr -n k8s.io i rm registry.cn-shanghai.aliyuncs.com/openhydra/aes-ai-tutor:release-2.0

# 下载新镜像
$ ctr -n k8s.io i pull registry.cn-shanghai.aliyuncs.com/openhydra/aes-ai-tutor:release-2.0

# 启动服务
$ kubectl scale --replicas=1 deployment/aes-ai-tutor -n ai-education-studio
```

### 更新 aes-dashboard

```bash
# 切换到 root,输入密码
$ sudo -s

# 停止当前服务
$ kubectl scale --replicas=0 deployment/aes-dashboard-deployment -n ai-education-studio

# 通过重命名复制旧镜像
# 以便于回滚
$ ctr -n k8s.io i tag registry.cn-shanghai.aliyuncs.com/openhydra/aes-dashboard:release-2.0 registry.cn-shanghai.aliyuncs.com/openhydra/aes-dashboard:release-2.0-old

# 删除旧镜像
$ ctr -n k8s.io i rm registry.cn-shanghai.aliyuncs.com/openhydra/aes-dashboard:release-2.0

# 下载新镜像
$ ctr -n k8s.io i pull registry.cn-shanghai.aliyuncs.com/openhydra/aes-dashboard:release-2.0

# 启动服务
$ kubectl scale --replicas=1 deployment/aes-dashboard-deployment -n ai-education-studio
```

### 更新 core-api-server

```bash
# 切换到 root,输入密码
$ sudo -s

# 停止当前服务
$ kubectl scale --replicas=0 deployment/core-api-server -n ai-education-studio

# 通过重命名复制旧镜像
# 以便于回滚
$ ctr -n k8s.io i tag registry.cn-shanghai.aliyuncs.com/openhydra/core-api-server:release-2.0 registry.cn-shanghai.aliyuncs.com/openhydra/core-api-server:release-2.0-old

# 删除旧镜像
$ ctr -n k8s.io i rm registry.cn-shanghai.aliyuncs.com/openhydra/core-api-server:release-2.0

# 下载新镜像
$ ctr -n k8s.io i pull registry.cn-shanghai.aliyuncs.com/openhydra/core-api-server:release-2.0

# 启动服务
$ kubectl scale --replicas=1 deployment/core-api-server -n ai-education-studio
```