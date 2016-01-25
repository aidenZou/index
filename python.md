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

