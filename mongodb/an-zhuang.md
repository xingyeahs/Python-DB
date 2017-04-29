# 安装 {#安装}

* 当前的ubuntu镜像中已经安装好了mongodb，可以直接跳过此节
* 下载mongodb的版本，两点注意
  * 根据业界规则，偶数为稳定版，如1.6.X，奇数为开发版，如1.7.X
  * 32bit的mongodb最大只能存放2G的数据，64bit就没有限制
* 到官网，选择合适的版本下载
* 解压

```
tar -zxvf mongodb-linux-x86_64-ubuntu1604-3.4.0.tgz

```

* 移动到/usr/local/目录下

```
sudo mv -r mongodb-linux-x86_64-ubuntu1604-3.4.0/ /usr/local/mongodb

```

* 将可执行文件添加到PATH路径中

```
export PATH=/usr/local/mongodb/bin:$PATH
```



