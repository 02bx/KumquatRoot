# Python 编码风格
author: WT  
version: 1.0.0
***
## 命名

### 局部变量命名
采用*类Java式*风格命名法：首单词小写，其余单词首字母大写。
> editBlack  
  badClock  
  isFile  

### 全局变量命名
采用去掉类型前缀的*Windows式*命名法：单词首字母大写。
> AppName  
  TimerCount  
  IsGameStarted

### 成员变量名
#### 静态成员变量
采用**全局变量命名**的方式。
#### 普通成员变量
采用**局部变量命名**的方式，开头加一个下划线。
> _editBlack  
  _isFile  
  _give

### 控件变量名
控件变量名采用控件缩写作为前缀的命名法。  
各个控件的缩写:
* 按钮 btn
* 文本框 txt
* 标签(StaticText) lbl
* 列表框 lst
* 组合框 cbo
* 复选框 chk
* 单选框 rdo
* 列表控件 lstctl
* 树形控件 tree
* 框(StaticBox) box
* 动画控件 ani

### 方法/函数命名
#### 独立函数
采用*传统C风格*命名。
> get_files()  
  set_global_text()

#### 成员方法
采用*类Java式*命名。
> getFiles()  
  setGlobalText()

#### 事件响应方法
同成员方法相同，前面加上'on'。
> onClick()  
  onDocumentComplete()

### 类型名
采用单词首字母大写式命名。
> class DirectUI:  
  class AbstractBase:

### 模块名/文件名
采用单词首字母大写式命名。
> SearchingDlg  
  KumquatRoot  
  MainDlg

***
## 空格留白
除了语言中各个语句块的留白缩进之外，本规范还要求一些使代码看起来美观的空格留白。

### 一般规则

* 操作符与操作数之间留一个空格

### 例外
不是所有操作符和操作数之间都留一个空格的空白，也存在很多例外。

* 多项使用逗号时
   * 项右边与逗号不空格，逗号右边与下一项间有空格
* 函数调用时
   * 标识符与左括号不空格
   * 只有一个参数时，括号均不空格留白
* 下标运算时
   * 标识符与左中括号不空格
   * 中括号内部的表达式与两侧中括号均不空格
* 冒号时
   * 冒号与左边的任何东西均不空格
* 字典时
   * 字典内冒号右边无空格

下面是一些例子：

    ( 1, 2, 3, 4, 5, 6 )
    addValue(100)
    add( 200, 300 )
    arr[1]
    arr[1 + 2]
    if a >= 20:
        a = 0
    else:
        a = 1

    { 'Key1':120, 'Key2':120, 'Key3':120 }

## 函数/方法参数换行
参数过多导致放在一行太冗长，分行时，本风格遵循一些缩进风格。

* 左括号留在原行
* 第一分行对齐函数名标识符，缩进4个空格开始敲第一个参数，之后是一个逗号，接着换行。
* 之后每一行对齐上一行的参数名。

例子

    createParams(
        param1 = '参数1',
        param2 = '参数2',
        param3 = '参数3',
        param4 = '参数4',
        param5 = '参数5',
        param6 = '参数6',
        param7 = '参数7'
    )
