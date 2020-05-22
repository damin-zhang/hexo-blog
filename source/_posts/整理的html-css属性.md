---
title: 整理的html&css属性
date: 2020-05-13 14:47:46
tags:
- CSS
- HTML
categories:
- Front-end
- 研习
---
## HTML

## CSS

### 文本超出两行添加省略号隐藏

**css的三条属性**

`overflow:hidden; ` //超出的文本隐藏

`text-overflow:ellipsis; ` //溢出用省略号显示

`white-space:nowrap; ` //溢出不换行

**这三个是css的基础属性，需要记得。**

<!--more-->

但是第三条属性，只能显示一行，不能用在这里，那么如果显示多行呢？

css3解决了这个问题，解决方法如下：

`display:-webkit-box; ` //将对象作为弹性伸缩盒子模型显示。

`-webkit-box-orient:vertical; ` //从上到下垂直排列子元素（设置伸缩盒子的子元素排列方式）

`-webkit-line-clamp:2;`  //这个属性不是css的规范属性，需要组合上面两个属性，表示显示的行数。

**最后的css样式如下：**

```css
overflow:hidden; 

text-overflow:ellipsis;

display:-webkit-box; 

-webkit-box-orient:vertical;

-webkit-line-clamp:2; 
```

### 连续的英文字母和数字换行

> 此属性只能用来处理英文和数字，汉字无效

```css
word-break: break-all;    //  按字母换行
word-break: break-word;   //  按单词换行
word-break: keep-all;     //  按空格，单个单词过长不会换行
```

