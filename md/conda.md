# Conda

python等语言的包管理软件

## 基本使用

- 初始化,相当于配置环境变量`conda init`

- 禁止自动激活base环境`conda config --set auto_activate_base false`

#### 环境的创建与激活

- 创建新的虚拟环境`conda create -n [环境名称] python=[版本号]`
- 查看虚拟环境列表`conda env list`
- 激活环境`conda activate [环境名称]`
- 退出环境`conda deactivate`
- 删除环境`conda remove -n [环境名称] --all`

#### 库安装

- 安装库 `conda install [库名]`
- 查看库列表`conda list`

#### 虚拟环境的导入导出

- 导出虚拟环境`conda env export > [name].yml`
- 导入虚拟环境`conda env create --file [name].yml`

## miniconda和anaconda

- conda:一种通用包管理系统，用来切换系统环境变量的python路径
- miniconda：python和conda
- anaconda：在miniconda的基础上预装了很多包

## conda install和pip install

`conda install`方式安装的库会被放在`miniconda/pkgs`下,在虚拟环境的`site-packages`中建立一个硬链接(复制?),不用重复下载。

`pip install`会直接安装在当前激活的虚拟环境的`site-packages`中。

## 使用总结

创建一个较大项目时,应当创建一个虚拟环境,以便于导出环境至`yml`,方便后续的部署

安装库优先使用`conda install`,版本不对或者找不到库再使用`pip install`

初学者建议使用`anaconda`,熟练掌握后轻量化的`miniconda`更优雅