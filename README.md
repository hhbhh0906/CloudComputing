# 云计算原理与实践

## [1.云计算基础](https://github.com/hhbhh0906/CloudComputing/blob/master/chapter1/Basics.md)

##### 1.1.购买云服务器并登

##### 1.2.创建GitHub项目并在本地同步

##### 1.3.本地安装虚拟机和CentOS操作系统

## [2.基于云服务器创建个人网站](https://github.com/hhbhh0906/CloudComputing/blob/master/chapter2/wordpress.md)

## [3.**Docker基础实验**](https://github.com/hhbhh0906/CloudComputing/blob/master/chapter3/Docker.md)

##### 3.1.安装Docker

##### 3.2.完成Docker安装之后加载CentOS镜像

##### 3.3.在Docker的CentOS容器实例中安装WordPress

###### 3.3.1.安装Apache Web服务器

###### 3.3.2.安装MySQL

###### 3.3.3.安装PHP

###### 3.3.4.安装WordPress以及完成相关配置

##### 3.4.将带有WordPress的CentOS镜像推送到容器仓库

##### 3.5.利用Dockerfile文件创建包含WordPress的镜像

## [4.Ceph的安装与实践](https://github.com/hhbhh0906/CloudComputing/blob/master/chapter4/Ceph.md)

##### 1.配置所有节点

###### 1.1.创建一个Ceph用户

###### 1.2.为用户创建一个sudoers文件，并使用sed编辑/ etc / sudoers文件

###### 1.3.安装和配置NTP

###### 1.4.安装Open-vm-tools

###### 1.5.禁用SELinux

###### 1.6.编辑文件network-scripts/ifcfg，设置onboot =“ on”，确保网络通信

###### 1.7.克隆虚拟机

###### 1.8.配置主机文件，在四台虚拟机上，都要编辑/ etc / hosts文件 

###### 1.9.验证四台虚拟机可以互通

##### **2.配置SSH服务器**

###### 2.1.安装ssh服务器

###### 2.2.为“ **cephuser** ” 生成ssh密钥

###### 2.3.为ssh配置创建配置文件

###### 2.4.更改配置文件的权限

###### 2.5.使用ssh-copy-id命令将SSH密钥添加到所有节点

###### 2.6.尝试从ceph-admin节点访问各服务器

##### **3.配置防火墙**

###### 3.1.登录到ceph-admin节点并启动firewall，打开端口80、2003和4505-4506，然后重新加载防火墙

###### 3.2.从ceph-admin节点登录到监视节点“ mon1”，然后启动firewalld，在Ceph监视节点上打开新端口，然后重新加载防火墙

###### 3.3.打开每个osd节点上的端口6800-7300-osd1，osd2和os3

##### 4.构建Ceph集群

###### 4.1.添加Ceph存储库，并使用yum命令安装Ceph部署工具' **ceph-deploy** '

###### 4.2.创建新的群集目录，使用“ **ceph** **-deploy** ”命令创建一个新的集群配置，将监视节点定义为“ **mon1** ”

###### 4.3.编辑ceph.conf文件

###### 4.4.从ceph-admin节点在所有其他节点上安装Ceph

###### 4.5.将ceph-mon部署在mon1节点上

###### 4.6.该命令将创建监视键，并使用“ ceph”命令检查并获取键

###### 4.7.登录osd1，osd2，创建供分配的目录，修改权限并返回admin用户

###### 4.8.准备所有OSDS节点

###### 4.9.激活OSD

###### 4.10.得到钥匙圈

###### 4.11.为所有决策部署管理密钥

###### 4.12.更改密钥文件的权限

##### 5.测试Ceph设置

###### 5.1.检查集群运行状况，检查集群状态

