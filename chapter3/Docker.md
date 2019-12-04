# **实验三 Docker基础实验**

### 班级：2017级软件工程（闽台合作）姓名：黄滨 学号：11607207033

### 1.安装Docker

#### 1.1更新应用程序数据库

![](../image/65.png)

#### 1.2**添加Docker官方仓库，安装最新Docker**

![](../image/66.png)

#### 1.3**启动Docker**

![](../image/67.png)

#### 1.4**设置Docker自启动**

![](../image/68.png)

#### 1.5**查看Docker 版本信息**

![](../image/69.png)

### 2.完成Docker安装之后加载CentOS镜像

#### 2.1**拉取 Centos 7**

![](../image/70.png)

#### 2.2**拉取完毕后查看镜像**

![](../image/71.png)

#### 2.3**运行Docker容器**

![](../image/72.png)

#### 2.4**查看已启动的容器**

![](../image/73.png)

#### 2.5**进入容器前台**

![](../image/74.png)

### 3.在Docker的CentOS容器实例中安装WordPress

#### 3.1安装Apache Web服务器

#### 3.1.1**连接ssh后使用yum安装**

![](../image/75.png)

#### 3.1.2**安装完成后，启动Apache Web服务器**

![](../image/76.png)

#### 3.1.3**设置开机自启**

![](../image/77.png)

#### 3.1.4访问服务器公网IP,出现下图代表Apache安装成功

![](../image/78.png)

#### 3.2安装MySQL

#### 3.2.1**安装MariaDB**

![](../image/79.png)

#### 3.2.2**启动MariaDB**

![](../image/80.png)

#### 3.2.3**设置MySQL的root密码**

![](../image/81.png)

#### 3.2.4**设置开机自启MariaDB**

![](../image/82.png)

#### 3.3安装PHP

#### 3.3.1安装epel-release

![](../image/83.png)

![](../image/84.png)

#### 3.3.2**因为WordPress需要php5.6以上版本的支持，我们更新到7.2版本仓库**

![](../image/85.png)

#### 3.3.3**安装PHP以及php-mysql**

![](../image/86.png)

#### 3.3.4**查看安装的php版本**

![](../image/87.png)

#### 3.3.5**重启Apache服务器以支持PHP**

![](../image/88.png)

#### 3.3.6**为了更好的运行PHP，需要启动PHP附加模块**

![](../image/89.png)

#### 3.3.7**重启Apache服务**

![](../image/90.png)

#### 3.4安装WordPress以及完成相关配置

#### 3.4.1**登录数据库**

#### 3.4.2**为WordPress创建一个新的数据库**

![](../image/91.png)

#### 3.4.3**进入刚创建的数据库**

![](../image/92.png)

#### 3.4.4**为WordPress创建一个独立的MySQL用户并授权给数据库访问权限**

![](../image/93.png)

![](../image/94.png)

#### 3.4.5**刷新MySQL的权限**

![](../image/95.png)

#### 3.4.6**安装WordPress**

![](../image/96.png)

![](../image/97.png)

![](../image/98.png)

![](../image/99.png)

#### 3.4.7接下来访问服务器公网IP，就能进入WordPress安装的web页

#### ![](../image/100.png)

#### 3.4.8安装完成后即可进入WordPress编辑自己的博客了

![](../image/101.png)

### 4.将带有WordPress的CentOS镜像推送到容器仓库

#### 4.1**将容器生成镜像**

![](../image/102.png)

#### 4.2**登录Docker**

![](../image/103.png)

#### 4.3**推送镜像**

![](../image/104.png)

#### 4.4**登录Docker网页查看仓库**

![](../image/105.png)

### 5.利用Dockerfile文件创建包含WordPress的镜像

#### 5.1**拉取 Centos 7**

![](../image/70.png)

#### 5.2编写Dockerfile

![](../image/106.png)

#### 5.3构建内置容器

![](../image/110.png)

#### 5.4启动容器

![](../image/111.png)

#### 5.5验证安装Apache Web服务器 浏览器输入：http://106.54.76.90:1234/

![](../image/107.png)

#### 5.6验证安装MySQL（未完成）

#### 5.7验证安装PHP 浏览器输入：http://106.54.76.90:1234/info.php

![](../image/108.png)

#### 5.8验证安装wordpress 浏览器输入：http://106.54.76.90:1234/wp-admin/setup-config.php

![](../image/109.png)