"What does a hero truly need?"
---

**Date**: 2015.07.11
**Author**: MYLS
**Principal**: LZ

####限制条件：

 - **难度**：N/A
 - **限定语言**：C++
 - **人数限制**：1
 - **依赖任务**：N/A

####任务描述：

 - **简介**：
    - 介绍：
    > Often I am asked, what does a hero truly need?
	> Much depends on the hero.
	> would you be **swift**? There for you I have speed beyond measure!
	> Would you be **strong**? Then I can grant you the might to overpower any foe.
	> Would you be **wise**? Then come closer and I will unlock your inner cunning.
	> What does a Hero truly need?
	> That is for you to decide.
    - 某 MOBA 游戏有这样一个设定，游戏中有很多英雄，但是他们分为三类，*敏捷*型、*力量*型、*智力*型
    - 这是因为英雄都有三个可成长的属性，分别为：*敏捷*、*力量*、*智力*，属性值满足线性关系：属性值 = 属性成长值 * (等级 - 1) + 基础属性。
    - 英雄的类型决定了他们的主属性，比如攻击力，这项属性计算方式为 攻击力 = 主属性 + 基础攻击力。
    - 那么问题来了，TB想要知道自己到达25级的时候，自己的各项属性。

 - **需求**：
    1. 我们需要抽象基类，`Hero`，包含三种子类类型`StrengthHero`、`AgileHero`、`IntellectualHero`。他们的主属性分别为 Strength 、 Agile 、 Intellectual 。
    2. 对于属性的约定，基础属性为整数，属性成长值为实数，精确到小数点后两位。
    3. 可以对子类调用 `int getPropertie(PropertieType type) const`，获取指定的属性，其中`PropertieType`是一个由你实现的枚举类型，标识三种属性类型或者攻击力，最后输出结果用`int`(舍去小数点部分)表示。
	4. TB 为*敏捷*类型英雄，他的的属性资料是：

		TB | 力量 | 敏捷 | 智力| 攻击力
		---|---|---|---|---
		基础| 15 | 22 | 19 | 51
		成长| 1.9 | 3.2 | 1.75 | 0

	那么问题来了，TB 达25级的时候，各个属性是…？


 - **关键词**：Inherit，Polymorphic
 - **参考资料**：
 	- [Effective c++学习笔记——条款07:为多态基类声明virtual析构函数](http://blog.csdn.net/wallwind/article/details/6762174)
 	- [[C++]接口继承与实现继承](http://blog.csdn.net/ljinddlj/article/details/1922189)
 	- [虚函数和基类设计](http://blog.chinaunix.net/uid-20356525-id-1700410.html)
 	- [C++ 设计抽象基类的策略](http://blog.csdn.net/slience_perseverance/article/details/20546955)