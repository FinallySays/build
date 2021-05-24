# 优化

## yum源优化,替换默认安装源

[阿里源地址](https://developer.aliyun.com/mirrors/)

### 1. 远程连接服务器(可选)

```
ssh root@ip
```

### 2. 备份

```
cd /etc/yum.repos.d/
mv CentOS-Base.repo CentOS-Base.repo.bak
```

### 3. 更换yum源

```
wget -0 /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
```

### 4. 清空并创建缓存

```
yum clean all
yum makecache
```



## 网络管理优化

### 1. 关闭网络管理器

- 临时关闭(重启失效)

```
systemctl stop NetworkMager
```



- 永久关闭

```
systemctl disable NetworkMager
```



## 设置服务器静态IP地址

### 1. 进入网络配置目录

```
cd /etc/sysconfig/network-scripts/
```

### 2. 备份网卡配置文件

```
mv ifcfg-eth0 ifcfg-eth0.bak
```

### 3. 更改网卡的配置文件

```
vim ifcfg-eth0
```

![网卡配置文件](/Users/swp/Desktop/software Installation/Linux OS/photos/网卡配置文件.jpg)

1. 修改bootproto = "static"
2. 整行删除UUID
3. 末尾根据网段插入

![image-20210511215054271](/Users/swp/Desktop/software Installation/Linux OS/photos//image-20210511215054271.png)

4. 保存退出
5. 重启网络使配置生效

```
systemctl restart network
```

远程连接时需要重新连接服务器

4. 验证网络

- 查看网卡信息

```
ip a
```

- ping百度

```
ping www.baidu.com
```

  

# 备份虚拟机

### 1. 关闭虚拟机

### 2. 创建快照

### 3. 创建模版机

### 4. 创建克隆机

# 工具

## wget

```
yum install -y wget
```



## vim

```
yum install -y vim
```



## net-tools

```
yum install -y net-tools
```

## tree

```
yum install -y tree
```

