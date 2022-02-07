###  配置yum源

#### 1 备份原来的yum配置

```shell
mkdir -p /etc/yum.repos.d/bak
cd /etc/yum.repos.d/bak
cp ../*.repo .
```



#### 2.创建新的repo

```shell
vi /etc/yum.repos.d/nexus.repo 
[nexus]
name=nexus repository
baseUrl=http://10.8.5.165:8081/repository/163-yum/$releasever/os/$basearch
enabled=1
gpgcheck=0
```



#### 3.安装需要的包文件

```shell
#测试
yum install httpd
```



### 4 最新yum 源

```shell
[AppStream]
name=AppStream
baseurl=http://10.8.5.21:8081/repository/Centos8-AppStream/
enable=0
gpgcheck=0
priority=1

[BaseOS]
name=BaseOS
baseurl=http://10.8.5.21:8081/repository/Centos8-BaseOS/
enable=0
gpgcheck=0
priority=1
```

