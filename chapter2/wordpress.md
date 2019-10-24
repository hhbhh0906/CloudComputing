# **实验二 基于云服务器创建个人网站**

### **班级：2017级软件工程（闽台合作）姓名：黄滨 学号：11607207033**

### **1.** **安装Apache Web服务器**

#### 使用yum工具安装

![](../image/24.png)

#### 测试Apache服务器是否成功运行

![](../image/25.png)

### **2.安装MySQL**

#### 安装MariaDB

![](../image/26.png)

#### 随后，运行简单的安全脚本以移除潜在的安全风险，启动交互脚本

![](../image/27.png)

#### 设置相应的root访问密码以及相关的设置

![](../image/28.png)

#### 设置开机启动MariaDB

![](../image/29.png)

#### PHP 7.x包在许多仓库中都包含，这里我们使用Remi仓库，而Remi仓库依赖于EPEL仓库，因此首先启用这两个仓库

![](../image/30.png)

![](../image/31.png)

#### 启用PHP 7.2 Remi仓库

![](../image/32.png)

#### 安装PHP以及php-mysql

![](../image/33.png)

#### 查看安装的php版本

![24](../image/34.png)

#### 重启Apache服务器以支持PHP

![24](../image/35.png)

### **4.** **安装PHP模块**

#### 为了更好的运行PHP，需要启动PHP附加模块，使用如下命令可以查看可用模块

![24](../image/36.png)

![24](../image/37.png)

#### 先行安装php-fpm(PHP FastCGI Process Manager)和php-gd(A module for PHP applications for using the gd graphics library)，WordPress使用php-gd进行图片的缩放

![24](../image/38.png)

#### 重启Apache服务

![24](../image/39.png)

### **5****.测试PHP**

#### 创建info.php并将其置于Web服务的根目录

![](../image/40.png)

#### 该命令使用vim在/var/www/html/处创建一个空白文件info.php，我们添加如下内容

![](../image/41.png)

#### 完成之后，使用刚才获取的cvm的IP地址，在本地主机的浏览器中输入

![](../image/42.png)

### **6****.安装WordPress以及完成相关配置**

#### **(1)为WordPress创建一个MySQL数据库**

#### 首先以root用户登录MySQL数据库

![24](../image/43.png)

#### 为WordPress创建一个新的数据库

![24](../image/44.png)

#### 接着为WordPress创建一个独立的MySQL用户

![24](../image/45.png)

#### 授权给wordpressuser用户访问数据库的权限

![24](../image/46.png)

#### 随后刷新MySQL的权限

![24](../image/47.png)

#### 退出MySQL的命令行模式

![](../image/48.png)

#### **(2)安装WordPress**

#### 下载WordPress至当前用户的主目录

![24](../image/49.png)

#### wget命令从WordPress官方网站下载最新的WordPress集成压缩包，解压该文件

![24](../image/50.png)

![24](../image/51.png)

#### 解压之后在主目录下产生一个wordpress文件夹。我们将该文件夹下的内容同步到Apache服务器的根目录下，使得wordpress的内容能够被访问。

![24](../image/52.png)

![24](../image/53.png)

#### 接着在Apache服务器目录下为wordpress创建一个文件夹来保存上传的文件

![24](../image/54.png)

#### 对Apache服务器的目录以及wordpress相关文件夹设置访问权限

![24](../image/55.png)

#### **(3)配置WordPress**

#### 大多数的WordPress配置可以通过其Web页面完成，但首先通过命令行连接WordPress和MySQL。定位到wordpress所在文件夹。

![24](../image/56.png)

#### WordPress的配置依赖于wp-config.php文件，当前该文件夹下并没有该文件，我们通过拷贝wp-config-sample.php文件来生成

![24](../image/57.png)

#### 通过nano超简单文本编辑器来修改配置，主要是MySQL相关配置

![24](../image/58.png)

![24](../image/59.png)

#### **(4)通过Web界面进一步配置WordPress**

#### 经过上述的安装和配置，WordPress运行的相关组件已经就绪，接下来通过WordPress提供的Web页面进一步配置。输入IP地址或者域名

![24](../image/60.png)

![24](../image/61.png)

![24](../image/62.png)

#### 点击**Log In**，弹出登录界面

![24](../image/63.png)

#### 输入用户名和密码之后，进入WordPress的控制面板

![24](../image/64.png)