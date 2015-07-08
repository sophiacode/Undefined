Task2Class
---

**Date**: 2015.07.08
**Author**: MYLS

####限制条件：

 - **难度**：2
 - **限定语言**：N/A
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：VS 一直以来有这样一个功能，显示类图：![类图](img/Task2Class.ClassDiagram.jpg)你可知道，我们的任务同样是有依赖关系的！所以请写一个转换这些`.md`文件到一个`.h`的小东西吧！
 - **需求**：
    1. 确保程序可以实现拖动*文件夹*或者`.md`文件到编译完成的程序上，它会运行并产生对应`ClassDiagram.h`。
    2. 支持多个文件夹或者多个`.md`文件，支持对文件夹中的`.md`文件和普通文件夹的递归搜索。
    3. 通过识别`**依赖任务**`一项，例如有这样三个任务 `A.md`; `B.md`(依赖于A); `C.md`，那么转换结果为：
```
/**********************************************************************
 *
 *	@file		ClassDiagram.h
 *	@brief		Show the dependencies of tasks.
 *
 *	Date        Name        Description
 *	dd/mm/yy	Your Name	Your Description.
 *
 *********************************************************************/

#pragma once

class A {};
class B : A{};

class C {};
```
注：有一些任务可能会依赖一些其它条件，例如`AnyOtherTask`。还有一些没有依赖的任务会标识为`N/A`。
    3. 继续确保`代码规范`！

 - **关键词**：文件读写, `int main(int argc,char* argv[])`
 - **参考资料**：
