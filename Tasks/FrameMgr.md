FrameMgr
---

**Date**: 2015.07.07
**Author**: MYLS

####限制条件：

 - **难度**：2
 - **限定语言**：C++
 - **人数限制**：[1, 2]
 - **依赖任务**：[Timer](Timer.md)

####任务描述：
 - **简介**：很多游戏中都会有和 [FPS](https://en.wikipedia.org/wiki/Frame_rate) 相关的功能，显示帧数或者锁帧等。这里将借助已经写过的`Timer`类型，完成类`FrameMgr`，用于控制程序运行时帧数。
 - **需求**：
    1. 使用一个`Timer`作为`FrameMgr`类的私有成员
    2. 符合*代码规范*
    3. 在 main 函数中使用以下代码进行测试：
	```
	#include <iostream>
	#include <algorithm>
	#include <random>
	#include <functional>

	#include "FrameMgr.h"

	int main(void) {

		/* 随机数发生器 */
		std::mt19937 engine(static_cast<int>(std::random_device()()));
		std::uniform_int_distribution<int> distribution(1, 20000);	
		auto generator = std::bind(distribution, engine);

		// TODO: 类 FrameMgr 初始化相关代码，并锁定 fps 为50
		// ...

		/* 程序总共运行帧数 */
		int cnt = 1000;
		while (cnt--)
		{
			/* 假设一帧中的运算量为n */
			int n = generator(), m = 0;
			for (int i = 0; i < n; i++)
				m++;
			std::cout << "Computation: " << m << std::endl;
			
			/* 至此一帧中的运算结束 */

			// TODO: 类 FrameMgr 相关操作，等待、**显示FPS**等
			// ...
		}

		// TODO: FrameMgr 清理相关部分
		// ...
		
		return 0;
	}
	```
    只能完成 TODO 标记，禁止改动其它部分代码。

 - **关键词**：TODO 标签，测试驱动
 - **参考资料**：[C++11 random](http://www.cplusplus.com/reference/random/)
