# Dev-C++

> 感谢 [SDUOJ](https://github.com/HYLazy/SDUOJ-Freshman-Programming-Manual) 对本Wiki的支持

## 1. 什么是Dev-C++

`Dev-C++`是学院老师推荐的一款IDE(集成开发环境)，优点在于小巧方便，不需要多余配置，缺点是这个IDE已经很久没有更新了，内置的编译器非常老旧，界面也很朴素，~~甚至可以直接使用动态数组~~。建议编程0基础或者感觉学习编程略有困难的同学使用。

## 2. 下载

下载地址：[Dev-C++ 中文主页 (gitee.io)](https://devcpp.gitee.io/)

## 3. 安装

- 打开下载好的安装程序文件

  ![20210806210458](https://i.loli.net/2021/08/26/9oPCerpIB5qyvKX.jpg)

- 这里的语言是安装时使用的语言，不需要更改。

  ![20210806210520](https://i.loli.net/2021/08/26/IXRj596hATMeOoG.jpg)

- 接下去即可一路`Next`/`Finish`，直至安装完成

## 4. 配置

- 安装完成后运行`Dev-C++`

- 这时候将语言改成中文

  ![20210806210647](https://i.loli.net/2021/08/26/AediHMS5K4svPTr.jpg)

- 可以在“工具(Tools)/环境选项(Environment Options)”中对上述设置的语言进行更改
- 至此，`Dev-C++`的配置已基本完成

## 5. 使用

### 5.1 选择32/64位编译环境

可以根据需要选择32位还是64位编译环境。如图所示。

![图片1](https://i.loli.net/2021/08/26/rGINTQ68RBJgV5z.jpg)

### 5.2 在Dev-Cpp中进行C程序开发

- 鼠标左键双桌面上的Dev-C++图标（如图1-10所示），打开Dev-Cpp集成开发环境

  ![图片2](https://i.loli.net/2021/08/26/AXJpenigzbKGC9N.jpg)

- 创建工程（工程，project，Dev中称为项目）

- 在菜单中选择“文件/新建/项目”，如图1-13所示，随即弹出“新项目”窗口

  ![图片3](https://i.loli.net/2021/08/26/irLVwgUeGfPvKzW.jpg)

- 选择“Console Application”，在名称文本框中输入工程（项目）名称，点击确定按钮

- 尽管对工程的命名没有什么限制，但按惯例应该起一个有意义的名字

  ![图片4](https://i.loli.net/2021/08/26/YZ27Sz9wgeNXJdT.jpg)

- 在随后弹出的窗口中询问你要将该工程保存到什么位置

- 尽管可以将你新建的工程保存在默认的目录中（如我的文档），但强烈建议在C盘之外的其它盘上，如D盘，建立目录，如`CProgram`，在该目录下再建立一个子目录，如`lab1`，表示实验1的内容，然后将你的工程文件保存到`D:\CProgram\lab1`中

  ![图片5](https://i.loli.net/2021/08/26/vb3q2GVRU5wsfQo.jpg)

  ![图片6](https://i.loli.net/2021/08/26/EBznxJZL3IjyioD.jpg)

- 随后弹出如图所示的窗口，你可以在该窗口中输入编辑你的C程序

  ![图片7](https://i.loli.net/2021/08/26/cDrXUEmu64jGfpt.jpg)

- 点击如上图中“编辑”菜单下面被红圈圈出的地方 ，可保存该文件

- 采用默认文件名（main.cc）即可，当然也可以自己取其它的名字，点击保存按钮

  ![图片8](https://i.loli.net/2021/08/26/zYbqynJxdQXWpAw.jpg)

- 此时`D:\CProgram\lab1`目录的内容如图1-19所示，一个是我们创建的工程文件，另一个该工程中的C程序文件

  ![图片9](https://i.loli.net/2021/08/26/yJ3KEVATXwbh7dg.jpg)

### 5.3 编译执行程序 

- 菜单选择“运行/编译执行”，或按快捷键F11，可编译执行你所编辑的源程序

  ![图片10](https://i.loli.net/2021/08/26/3rBkw57Wt269CoT.jpg)

### 5.4 打开已创建的工程

- 如果上次实验已经创建了一个工程，下次实验可以打开上次实验创建的工程，在原来的基础上继续调试

  ![图片11](https://i.loli.net/2021/08/26/8A7kH1695UiKCQp.jpg)

### 5.5 在一个工程中添加C/C++源代码文件

- 一个工程中可以包含多个源代码文件，建议将函数和类等分开存放到不同的源文件中，例如在头文件中对常量、全局变量、结构、函数、类等进行声明，函数与类的实现存放到其它文件中

  ![图片12](https://i.loli.net/2021/08/26/Z56PGlT8S3ekJ4a.jpg)