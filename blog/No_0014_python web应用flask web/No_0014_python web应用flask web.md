# python web应用flask web 学习（一）

## 系统 ubuntu 18.04.4LTS

## 安装虚拟环境

```shell
sudo apt-get install python-virtualenv
```

**示例代码下载并进入对应章节代码 章节代码 1a 2a 3b等格式**

```
git clone https://github.com/miguelgrinberg/flasky.git
cd flasky
git checkout 1a
```

**创建虚拟环境**

```
virtualenv venv
```
会自动搭建好一个虚拟的venv的python环境 这个环境不会影响你系统本身的python环境

![示例项目文件目录]()

**虚拟环境目录结构**

env下的文件结构 这里只展示两层文件结构

.
├── bin
│   ├── activate
│   ├── activate.csh
│   ├── activate.fish
│   ├── activate_this.py
│   ├── easy_install
│   ├── easy_install-2.7
│   ├── flask
│   ├── pip
│   ├── pip2
│   ├── pip2.7
│   ├── python -> python2
│   ├── python2
│   ├── python2.7 -> python2
│   ├── python-config
│   └── wheel
├── lib
│   └── python2.7
├── local
│   ├── bin -> /home/twobadao/flasky/venv/bin
│   └── lib -> /home/twobadao/flasky/venv/lib
└── share
    └── python-wheels

![venv文件结构]()

## 激活虚拟环境

venv 是虚拟环境名称

```
source venv/bin/activate
```
