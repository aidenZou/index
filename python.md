## MAC

- [python DOC](https://docs.python.org/3/)
- [Tornado 中文翻译](http://demo.pythoner.com/itt2zh/)
- [pypi](https://pypi.python.org/pypi)


### 安装 python 3.x
brew install python3

### 升级 3.5

`brew update`

`sudo chown -R $(whoami):admin /usr/local`

`brew upgrade python3`

### 创建虚拟

`pip install virtualenv`

`pyvenv-3.5 ./develop/py35env`


### 模块 install

freeze Output installed packages in requirements format.

`~/develop/py35env/bin/pip3 freeze > requirements.txt`

pip install [options] -r <requirements file> [package-index-options] ...

`~/develop/py35env/bin/pip3 install -r requirements.txt`


## 模块

- [jupyter](https://jupyter.org/)
	`./develop/py35env/bin/pip3 install jupyter`
	`./develop/py35env/bin/jupyter-notebook`
- [ipython](https://pypi.python.org/pypi/ipython)
- [Beautiful](http://www.crummy.com/software/BeautifulSoup/bs4/doc.zh/) 一个可以从HTML或XML文件中提取数据的Python库


## Centos

```shell
# 下载Python源(Download Python source)
$wget https://www.python.org/ftp/python/3.5.1/Python-3.5.1.tar.xz

# 提取Python包(Extract Python package):
$tar xf Python-3.5.1.tar.xz

$xz -d Python-3.5.1.tar.xz

$cd Python-3.5.1

# 编译的Python(Compile Python):
$./configure

# Make:
$make

# 安装(Install):
$make install

# 检查Python版本(Check Python version):
$which python3.5
/usr/local/bin/python3.5
```


