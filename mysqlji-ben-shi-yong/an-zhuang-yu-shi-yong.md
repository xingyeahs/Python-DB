# 服务器安装

安装服务器端：在终端中输入如下命令，回车后，然后按照提示输入

```
sudo apt-get install mysql-server
```

* 当前使用的ubuntu镜像中已经安装好了mysql服务器端，无需再安装，并且设置成了开机自启动
* 服务端的命令为mysqld，接收客户端的请求，执行sql语句，管理数据库
* 服务器端一般以服务方式管理，注意服务名称为mysql
* 启动

```
sudo service mysql start
```

* 停止

```
sudo service mysql stop
```

* 重启

```
sudo service mysql restart
```

# 配置 {#配置}

* 配置文件位于/etc/mysql/mysq.conf.d目录下，为mysqld.cnf
* bind-address表示服务器绑定的ip，通过此ip连接服务器，可以配置成其它ip或者不配置，默认是127.0.0.1
* 端口表示端口，默认为3306
* datadir表示数据库目录，配置为/ var / lib / mysql
* log\_error表示错误日志，配置为/var/log/mysql/error.log

# 客户端 {#客户端}

* 客户端为开发人员与dba使用，通过套接字方式与服务端通信，常用的有navicat，命令行mysql

#### 图形化界面客户端navicat {#图形化界面客户端navicat}

* 稍后会将ubuntu版本的navicat下发，也可以到navicat官网下载
* 将压缩文件拷贝到桌面上，使用如下命令解压

```
tar zxvf navicat112_mysql_cs_x64.tar.gz
```

* 进入刚才解析的目录，运行如下命令，回车启动

```
./start_navicat
```

* 启动成功如下图，其它功能后续讲解



