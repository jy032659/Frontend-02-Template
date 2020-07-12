1. 语言的分类：
通过搜集和整理，大致对目前所熟悉的语言进行分类：


标记语言: HTML, XML SGML
声明式语言：声明后计算机会给出一个结果
命令式语言：需要一步步指导计算机达到目标结果 ，c，c++, JS
面向对象：C++,Java，C#

2. 对产生式从不明白到入门并理解了一些特定的表达方式
https://isaaccomputerscience.org/concepts/dsa_toc_bnf
上面文章具体讲述了如何以递归的方式对产生式进行推导并顺带阐述了各个符号的含义
 例：给定
 <addition> ::= <number>+<number>
    <number> ::= <sign><integer>|<integer>
    <integer> ::= <digit>|<digit><integer>
    <digit>::=0|1|2|3|4|5|6|7|8|9
    <sign> ::= +|-

判断24+54 是不是一个valid addition

solution:
<addition> ::=<number>+<number>
<addition> ::=<integer>+<integer> （因为number 能表示成integer）
<addition>::= <digit><integer> +<digit><integer> （因为<integer>能表示成 <digit><integer>）
<addition>::=<digit><digit>+<digit><digit> (<integer> 也能表示成<digit>)
所以24+54是一个valid addition



3. JavaScript 的类型系统
Number
按照 ​IEEE 754 Double Float 标准实现的

​以64位为例子
​Sign (1个符号位) 
Exponent (11 个指数位) 
Fraction (52 个精度位 )
32位
​​Sign (1个符号位) 
​​Exponent (8 个指数位)
​Fraction (23 个精度位 )
String
字符串的核心概念：

字符 Character
码点 Code Point
编码 Encoding：
1. ASCII
2. Unicode
3. GB
4. UCS
5. ISO8895
6. BIG5

