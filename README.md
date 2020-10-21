# ToyReact

## 第一课｜ JSX 的原理和关键实现

### 安装依赖环境

```js
"@babel/core",
"@babel/plugin-transform-react-jsx",
"@babel/preset-env",
"babel-loader",
"webpack",
"webpack-cli" 
```

### 如何实现转换 `JSX` 语法的 createElement 函数？

### 如何支持 `JSX` 的自定义组件语法？

## 第二课｜ 给 ToyReact 添加对应的生命周期，实现动态修改内容的功能

### 如何改造为基于 Range 来绘制 DOM ？

在实现数据发生变化重新渲染 DOM 前，先改为为基于 Range 来绘制 DOM，给包装类 `ElementWrapper`、`TextWrapper` 和自定义组件类 `Component` 实现 `renderToDom`

### 实现调用 setState 时，重新渲染 DOM ？

### 尝试跑通 TicTacToe 最终代码

> TicTacToe - 井字游戏 - 最终代码：https://codepen.io/gaearon/pen/gWWZgR

### 基于 Range 重新渲染的坑？

数据更新时，基于 Range 重新渲染，由于元素插入位置的不同，`deleteContents` 时会删除不应该删除的节点。

修改 `reRender` 方法，先将新的节点插入到 `range` 中，然后重新渲染，最后再删除旧的节点内容：

[1]: https://developer.mozilla.org/zh-CN/docs/Web/API/Range
