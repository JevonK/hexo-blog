---
title: markdown 常用语法总结
date: 2019-10-14 11:29:00
tags: markdown 
categories: hexo入门
---

对于markdown的我还是秉承它的宗旨：简洁易读
## 文本处理
### 1、字体
```
    <font face="黑体">我是黑体字</font>
    <font color=red>我是红色</font>
    <font size=5>我是尺寸</font>
    <font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>
    # H1
    ## H2
    ### H3
    #### H4
    ##### H5
    ###### H6    
```
效果如下：

  +  <font face="黑体">我是黑体字</font>
  +  <font color=red>我是红色</font>
  +  <font size=5>我是尺寸</font>
  +  <font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>
  +  # H1
  +  ## H2
  +  ### H3
  +  #### H4
  +  ##### H5
  +  ###### H6


### 2、加粗，倾斜，删除线，空格
```
    *斜体*          _斜体_
    **粗体**        __粗体__
    ***粗斜体***    ___粗斜体___
    ~~删除线~~
    半方大的空白&ensp;或&#8194;
    全方大的空白&emsp;或&#8195;
    不断行的空白格&nbsp;或&#160;
```
效果如下：

  +  *斜体*          _斜体_
  +  **粗体**        __粗体__
  +  ***粗斜体***    ___粗斜体___
  +  ~~删除线~~
  
    
## 代码区
````
    三个反单引号开始与结束，组成代码区块。一个反单引号开始与结尾，组成单行代码区块。
    ```
        代码区块
        代码区块
        代码区块
    ```
    `高亮`
````
效果如下：

```
    代码区块
    代码区块
    代码区块
```
`高亮`

## 序列列表
```
无序列表
+ 一级目录
    * 二级目录
        - 三级目录
有序列表
1. 一级目录
    1. 二级目录
        1. 三级目录
```
效果如下：

无序列表
+ 一级目录
    * 二级目录
        - 三级目录

有序列表
1. 一级目录
    1. 二级目录
        1. 三级目录
        
## 分隔线
```
    三个-与三个* 都行。
    ---
    ***
```
效果如下：
---
***

## 超链接
```
    [百度](http://baidu.com) 
```
效果如下：

  + [百度](http://baidu.com) 

## 插入图片
```
    设置大小居中
    <div align=center><img src="http://pic27.nipic.com/20130320/8092962_210424307317_2.jpg" width="100" height="100"></div>
    直接插入图片
    ![百度](http://pic27.nipic.com/20130320/8092962_210424307317_2.jpg) 
```
效果如下：
    <div align=center><img src="http://pic27.nipic.com/20130320/8092962_210424307317_2.jpg" width="100" height="100"></div>
    ![百度](http://pic27.nipic.com/20130320/8092962_210424307317_2.jpg) 


## 表格
绘制表格格式如下，| 控制分列，- 控制分行，: 控制对齐方式。
```
    | 左对齐    |  右对齐 | 居中 |
    | :-------- | -------:|: ---- :|
    | Computer  | 5000 元 |  1台两台 |
    | Phone     | 19 元 |  1部 |
```
效果如下：

  | 左对齐    |  右对齐 | 居中 |
  | :-------- | -------: | :----: |
  | Computer  | 5000 元 |  1台两台 |
  | Phone     | 19 元 |  1部 |

## 流程图
````
    注：使用流程图前先在项目根目录执行：npm install --save hexo-filter-flowchart
        亲自行把 ··· 装换成 ```
    ···flow
    st=>start: Start|past:>http://www.google.com[blank]
    e=>end: End:>http://www.google.com
    op1=>operation: My Operation|past
    op2=>operation: Stuff|current
    sub1=>subroutine: My Subroutine|invalid
    cond=>condition: Yes
    or No?|approved:>http://www.google.com
    c2=>condition: Good idea|rejected
    io=>inputoutput: catch something...|request
    st->op1(right)->cond
    cond(yes, right)->c2
    cond(no)->sub1(left)->op1
    c2(yes)->io->e
    c2(no)->op2->e
    ···
````
效果如下：

```flow
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```