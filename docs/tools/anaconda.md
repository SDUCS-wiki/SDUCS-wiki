# Anaconda的安装与使用

> 为了不给使用带来困扰，本 Wiki 不推荐电脑用户名中带有任何中文

## 1. 安装

### 1.1 下载

- 前往 [Anaconda ](https://www.anaconda.com/products/individual)官网下载 `Anaconda Individual Edition` (`Anaconda`个人版)

  ![image-20210808224525625](https://i.loli.net/2021/08/26/9cFmEkphZBl2Wrj.png)

### 1.2 安装

- 找到下载好的 `Anaconda3-2021.05-Windows-x86_64.exe`，启动该文件

- 按照以下步骤进行安装

  ![image-20210808225322047](https://i.loli.net/2021/08/26/LJb7V3i1BZzCUM5.png)

  ![image-20210808225358727](https://i.loli.net/2021/08/26/O1mIBeEQhSWl9Cy.png)

  ![image-20210808225435823](https://i.loli.net/2021/08/26/Z7dm8oxcC6aDwPq.png)

  ![image-20210808225632267](https://i.loli.net/2021/08/26/IqKhLSeRBdMb1Pa.png)

- 关键安装步骤已经完成，剩下步骤可一路`Next`/`Finish`

### 1.3 系统环境变量配置

- 单击`Windows徽标键`，在键盘上输入`path`

  ![image-20210809142027193](https://i.loli.net/2021/08/26/z7rSAEjXwV5Zp24.png)

- 点击 `环境变量`，在`系统变量`中找到`Path`，双击`Path`，点击`浏览`

  ![image-20210809142241413](https://i.loli.net/2021/08/26/tbGYJeuRT5K4wyN.png)

  ![image-20210809143136490](https://i.loli.net/2021/08/26/Ka8WZejELnmQdvz.png)

- 依次找到下述文件夹，并添加，然后确认保存并`重启`

  ```wiki
  你的安装位置\Anaconda3
  你的安装位置\Anaconda3\Scripts
  你的安装位置\Anaconda3\Library\bin
  你的安装位置\Anaconda3\Library\mingw-w64\bin
  ```

- `重启`完成后，打开`CMD`，输入以下指令(请注意大小写)

  ```bash
  conda -V
  ```

  若输出为

  ```bash
  conda x.xx.x
  ```

  则已正确配置环境

### 1.4 切换镜像源

> 镜像源能显著提高`conda`的下载速度，本WiKi中使用[清华镜像源](https://mirror.tuna.tsinghua.edu.cn/)作演示用

- 打开`CMD`，输入以下指令

  ```bash
  conda config --set show_channel_urls yes
  ```

- 打开`我的电脑`(`文件资源管理器`)，找到`C:\Users\${你的用户名}\.condarc`，并打开编辑，替换里面内容如下

  ```
  channels:
    - defaults
  ssl_verify: true
  show_channel_urls: true
  default_channels:
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
  custom_channels:
    conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
    simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  ```

- 运行 `conda clean -i` 清除索引缓存，保证用的是镜像站提供的索引

- 运行 `conda create -n myenv numpy` 测试一下吧

## 2. 使用`Conda`

### 2.1 创建环境

创建一名称为`name`且`Python`版本为3. 7的Conda环境

```
conda create -n name python=3.7
```

### 2.2 销毁环境

删除一名称为`name`的Conda环境

```
conda remove -n name --all
```

### 2.3 进入环境

进入一名称为`name`的Conda环境

```
conda activate name
```

### 2.4 退出环境

```
conda deactivate
```

### 2.5 安装包

```
conda install xxx
```

### 2.6 查看当前环境Python版本

```
python --version　　# 查看python解释器的版本
```

