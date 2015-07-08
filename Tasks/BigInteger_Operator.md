BigInteger_Operator
---

**Date**: 2015.07.08
**Author**: MYLS

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：[BigInteger_Constructor](BigInteger_Constructor.md)

####任务描述：

 - **简介**：`BigInteger` 系列任务二！
 上回书说到构造函数，这一次试一试操作符重载。让他们的运算支持 `=` 拷贝，`+` 加法
 - **需求**：
    1. 在`.h`的类的申明中，写下这些操作符重载：
```
public:

	/**
	 *	\brief	Operator Overloading [=]
	 *			如果使用了指针成员列表，那么重载等于运算将很有必要
	 *
	 *	\param	rhs		拷贝对象
	 *
	 *	\return			自身的引用
	 */
	BigInteger & operator =(const BigInteger &);

	/**
	 *	\brief	Operator Overloading [+=]，自增操作
	 *
	 *	\param	rhs		操作符右边的值
	 *
	 *	\return			计算结果，自身的引用
	 */
	BigInteger & operator +=(const BigInteger & rhs);

	/**
	 *	\brief	Operator Overloading [+]
	 *
	 *	\param	lhs		操作符左边的值
	 *	\param	rhs		操作符右边的值
	 *
	 *	\return			+ 的计算结果
	 */
	friend const BigInteger operator +(const BigInteger & lhs, const BigInteger & rhs);
```
  2. 搜索关于他们的资料；注意样例代码中何处使用`const`、何处使用`&`；区分一元运算符，二元运算符！
  3. 补全它们并测试你的代码。

 - **关键词**：Operator Overloading, `friend`
 - **参考资料**：
