---
title: 'scss引入其他scss变量, 并通过js动态修改scss变量'
date: 2021-02-18 09:51:06
tags: [scss, vue]
category: [前端]
---

a.scss

```scss
.test {
  background: red;
}
```

b.scss

```scss
$bgColor: red;
```

## 1 a.scss 需要引入 b.scss 中的变量

a.scss(只要引入成功后, 修改 b.scss 里$bgColor 的值, a.scss 中的 background 的值就会跟着改变.)

```scss
@improt 'b.scss'
.test {
  background: $bgColor;
}
```

## 2 需要通过 js 做到动态修改 b.scss 变量值

b.scss 需要绑定一个变量名, 用于 js 方法中.(变量名可以任意取, 默认值不能是字符串)

```scss
// 用var来盛放--test变量名,默认值为red,用于js做动态修改
$bgColor: var(--test, red);
```

test.js

```js
document.getElementByTagName('body')[0].style.setProperty('--test', 'yellow')
```
