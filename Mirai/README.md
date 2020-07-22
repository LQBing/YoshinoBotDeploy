# 与Mirai一起启动

## 关联项目

[YoshinoBot](https://github.com/LQBing/YoshinoBot)

[docker-MiraiOK](https://github.com/LQBing/docker-MiraiOK)

## 第一次运行

安装docker（如果已经安装好，请跳过）

```shell script
wget get.docker.com -O install_docker.sh
sh install_docker.sh --mirror Aliyun
```

拉取镜像

海外：

```shell script
docker pull lqbing/miraiok
docker pull lqbing/yoshino
```

国内：

```shell script
docker pull registry.cn-hongkong.aliyuncs.com/lqbing/miraiok
docker pull registry.cn-hongkong.aliyuncs.com/lqbing/yoshino
docker tag registry.cn-hongkong.aliyuncs.com/lqbing/miraiok lqbing/miraiok
docker tag registry.cn-hongkong.aliyuncs.com/lqbing/yoshino lqbing/yoshino
```

当前设备第一次运行可能需要输入验证码，步骤见[docker-MiraiOk文档](https://github.com/LQBing/docker-MiraiOK#env)

## docker-compose启动

上面第一次运行需要完成的步骤（新设备验证码输入和扫描认证）完成后可以运行下面命令来启动mirai和YoshinoBot

```shell script
docker-compose up -d
```