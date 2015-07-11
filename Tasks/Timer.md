终焉的顺计时
---

**Date**: 2015.07.07
**Author**: MYLS
**Principal**: LGY

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：[1, 2]
 - **依赖任务**：N/A

####任务描述：

 - **简介**：**终焉的倒计时**被发动了！
 OMG，世界只剩下只剩下20回合了，可是作为能拯救世界的准程序帝，怎么能在这里终结！所以你机智地把倒计时修改成了`顺计时`。
 虽然还不知道怎么替换……不过让我们先做一个*顺计时器*！
 - **需求**：
    1. 计时器需要*毫秒*或者以上的时间精度
    2. 这个类拥有*开始*、*暂停*、*停止*、*恢复*、*获取逝去的时间*这几种方法
    3. 符合*代码规范*：命名、注释、文件的组织、作用域…… 参考：[RobitCppCodingConventions](ref/RobitCppCodingConventions.md)
    4. 自拟测试代码进行测试，保证其*健壮性*。这是一个测试用的例子：
```
Timer t;
char cmd[10] = {};
while (std::cin >> cmd, cmd[0] != 'C') {
	if (cmd[0] == 's') {
		t.start();
	} else if (cmd[0] == 'p') {
		t.pause();
	} else if (cmd[0] == 'r') {
		t.resume();
	} else if (cmd[0] == 'd') {
		std::cout << t.getElapsedTime() << std::endl;
	} else {
		t.stop();
	}
}
```

 - **关键词**：OOP, Robustness, **代码规范**
 - **参考资料**：
    - [C++的头文件和实现文件分别写什么](http://www.cnblogs.com/ider/archive/2011/06/30/what_is_in_cpp_header_and_implementation_file.html)
    - [Doxygen风格的注释](http://blog.csdn.net/netlinux/article/details/7681386)

