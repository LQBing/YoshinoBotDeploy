# 与miraiOK一起启动

## 关联项目

[YoshinoBot](https://github.com/LQBing/YoshinoBot)

[cqhttp](https://cqhttp.cc/docs/4.15/#/Docker)

## 第一次运行

安装docker（如果已经安装好，请跳过）

```shell script
wget get.docker.com -O install_docker.sh
sh install_docker.sh --mirror Aliyun
```

拉取镜像

海外：

```shell script
docker pull richardchien/cqhttp
docker pull lqbing/yoshino
```

国内：

```shell script
docker pull richardchien/cqhttp
docker pull registry.cn-hongkong.aliyuncs.com/lqbing/yoshino
docker tag registry.cn-hongkong.aliyuncs.com/lqbing/yoshino lqbing/yoshino
```

## docker-compose启动

上面第一次运行需要完成的步骤（新设备验证码输入和扫描认证）完成后可以运行下面命令来启动mirai和YoshinoBot

```shell script
docker-compose up -d
```

启动后使用浏览器访问服务器的9000端口，用.env文件里配置的`VNC_PASSWD`连接VNC。输入QQ账号和密码点击登录后会提示一个获取chrome一类的提示，点击放弃，然后输入验证码。
