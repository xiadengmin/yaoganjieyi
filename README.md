# 2022 软件杯 百度遥感解译
# 作品安装说明与目录介绍

## 作品安装说明

### 1,1 系统介绍

智脑遥感影像解译平台（以下简称智脑），是基于飞桨PaddleRs构建的卫星影像处理Web系统，目前包括目标提取、变化检测、目标检测、地物分类四大功能。

智脑的目标是通过深度学习能力对遥感图像自动分析和智能解译，并将相关能力应用于智慧城市、气象预测、环境保护和防灾减灾、农林业监测等场景的重要研究领域。

### 1.2系统技术框架

| 图标UI框架 | Echarts |
|------------|---------|
| 后端框架   | Flask   |
| 数据库     | SQLite  |
| 图像处理   | Opencv  |

### 1.3快速安装

#### 1.3.1 环境准备

[Anaconda](https://www.anaconda.com/)是一个免费开源的Python和R语言的发行版本，用于计算科学，Anaconda致力于简化包管理和部署。Anaconda的包使用软件包管理系统Conda进行管理。Conda是一个开源包管理系统和环境管理系统，可在Windows、macOS和Linux上运行。

在进行智脑系统安装之前请确保您的Anaconda软件环境已经正确安装。软件下载和安装参见Anaconda官网(https://www.anaconda.com/)。在您已经正确安装Anaconda的情况下请按照下列步骤安装系统。

-   Windows 7/8/10 专业版/企业版 (64bit)
-   GPU版本支持CUDA 10.1/10.2/11.2，且仅支持单卡
-   conda 版本 4.8.3+ (64 bit)

#### 1.3.2 创建虚拟环境

首先根据创建Anaconda虚拟环境，在Anaconda prompt中执行命令：

conda create -n zhinao_env python=3.6

#### 1.3.3 进入Anaconda虚拟环境

activate zhinao_env

#### 1.3.4 python环境检查

输出 Python 路径的命令为:

where python

查看python的安装路径，同时输入下面命令确认python版本为3.6

python --version

最后确认Python和pip是64bit，并且处理器架构是x86_64（或称作x64、Intel 64、AMD64）架构。下面的第一行输出的是”64bit”，第二行输出的是”x86_64（或x64、AMD64）”即可：

python -c "import platform;print(platform.architecture()[0]);print(platform.machine())"

#### 1.3.5 安装相关依赖

进入项目文件夹下（requirments.txt 同级目录），安装相关依赖包。

Pip install -r requirments.txt

### 1.3.6 paddleRs安装

pip install -e PaddleRS/

# 源码目录介绍

./demo_data : 用于模型测试的测试图片

./PaddleRs : 百度源码包，用于模型的加载与预测

./src : 对应四个功能的模型加载与掉用代码，函数返回值为预测后的图片

./static

./css ：前端样式

./img ：前端图片资源

./uploads : 用于保存前端传回的要预测的图片

./static_model : 对应四个功能的静态模型文件

./templates : 前端html页面

./ function\* : 对应四个功能选择

./ index : 首页

./ login&register ：注册登录页

./app.py : 后端启动文件

./requirements : 环境依赖

./testdb.db  : 数据库
