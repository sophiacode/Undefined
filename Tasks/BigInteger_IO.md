BigInteger_IO
---

**Date**: 2015.07.08
**Author**: MYLS

####限制条件：

 - **难度**：2
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：[BigInteger_Operator](BigInteger_Operator.md)

####任务描述：

 - **简介**：`BigInteger` 系列任务三！
 也许你很好奇，`std::cout`，`std::cin`， 如何对你的自定义类型使用？ 
 - **需求**：
    1. 在`.h`的类的申明中，`#include <iostream>`，并写下这些操作符重载：
```
public:
	/**
	 *	\brief	使这个类支持 cout 到输出流
	 *
	 *	\param	os		输出流
	 *	\param	rhs		将要输出的整数
	 *
	 *	\return			std::ostream&, 以便再次接受 << 运算
	 */
	friend std::ostream& operator << (std::ostream& os, const BigInteger& rhs);

	/**
	 *	\brief	使这个类支持 cin 输入
	 *
	 *	\param	is		输入流
	 *	\param	rhs		将要输出的整数
	 *
	 *	\return			std::ostream&, 以便再次接受 << 运算
	 */
	friend std::istream& operator >> (std::istream& is, BigInteger& rhs);
```
	3. 搜索关于它们的资料，注意区分它们和之前的`friend const BigInteger operator +(const BigInteger & lhs, const BigInteger & rhs);`！
	4. 补全它们并测试你的代码。

 - **关键词**：Operator Overloading, `friend`, iostream, // sstream
 - **参考资料**：
