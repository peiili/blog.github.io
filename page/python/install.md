安装指定版本的python 以3.8为例
然后去官网下载 python3.8.3
wget https://www.python.org/ftp/python/3.8.3/Python-3.8.3.tgz

这个下载完成之后，得到的是源码包，那么就需要编译并安装。因此新建一个安装的目录：
```shell 
sudo mkdir -p /usr/local/python3
```

解压安装包:
```shell 
tar -zxvf Python-3.8.3.tgz
```

进入解压后的目录：
```shell 
cd Python-3.8.3
```

配置安装的目录：
```shell 
./configure --prefix=/usr/local/python3
```

接着开始编译python3.8.3代码，并安装：
```
sudo make install
```

建立软连接运行的名称：
```shell
sudo ln -s /usr/local/python3/bin/python3.8 /usr/local/bin/python38
```

```shell
sudo ln -s /usr/local/python3/bin/pip3.8 /usr/bin/pip3
```
然后运行输出下面的信息，就表示安装成功了：
```shell
:~$ python38
Python 3.8.3 (default, May 30 2020, 18:57:04) 
[GCC 5.4.0 20160609] on linux
Type "help", "copyright", "credits" or "license" for more information.
```
```shell 
:~$ pip3 -V
pip 19.2.3 from /usr/local/python3/lib/python3.8/site-packages/pip (python 3.8)
```

如果上面的命令不行，就需要采用下面的命令:
`python38 -m pip install numpy -i https://pypi.douban.com/simple`

最后建立idle集成开发环境的连接：

`sudo ln -s /usr/local/python3/bin/idle3.8 /usr/local/bin/idle3.8`


然后就可以通过idle3.8打开集成开发环境了。