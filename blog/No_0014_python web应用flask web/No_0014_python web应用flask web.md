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

![venv文件结构]()

## 激活虚拟环境

venv 是虚拟环境名称

```
source venv/bin/activate
```

激活成功后终端内命令行最前面会有虚拟环境的名称 例如： (venv) $

回到全局终端 使用 ```deactivate```

## 利用pip安装第三方python包

首先激活虚拟环境

然后在虚拟环境中利用

```python
pip install flask
```

安装flask

**测试flask是否安装成功** 

进入python交互式编程模式

```python
python
```

利用import倒入flask包 回车后不报错说明安装成功

```python
import flask
```

## 小结

并无难度 主要是要安装好开发环境 在编程前检验是否在虚拟环境内 不要搞混
