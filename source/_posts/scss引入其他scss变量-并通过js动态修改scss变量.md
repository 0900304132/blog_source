---
title: 'scss引入其他scss变量, 并通过js动态修改scss变量'
date: 2021-02-18 09:51:06
tags: [scss, vue]

---

a.scss

``` scss
.test{
  background:red;
}
```

b.scss

``` scss
$bgColor:red;
```

## 1 a.scss需要引入b.scss中的变量

a.scss(只要引入成功后, 修改b.scss里$bgColor的值, a.scss中的background的值就会跟着改变.)

``` scss
@improt 'b.scss'
.test{
  background:$bgColor;
}
```

## 2 需要通过js做到动态修改b.scss变量值

b.scss需要绑定一个变量名, 用于js方法中.(变量名可以任意取, 默认值不能是字符串)

``` scss
// 用var来盛放--test变量名,默认值为red,用于js做动态修改
$bgColor:var(--test,red);
```

test.js

``` js
document.getElementByTagName('body')[0].style.setProperty('--test', 'yellow');
```
