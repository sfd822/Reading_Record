# JS 的优化

## 优化原则

- 需要时才优化

  没有必要每次开发和上线都进行优化，当项目进行到一定的阶段，到大的改版或是代码无法维护的时候考虑性能优化

- 考虑可维护性

  考虑团队水平、代码规范

## 提升 JS 文件加载性能

- 加载元素的顺序：CSS 文件放在 `<head>` 里，JS 文件放在 `<body>` 里

## JS 变量和函数优化

- 尽量使用 id 选择器
  - 查询快、效率高
  - class 不唯一
- 尽量避免使用 eval，耗费性能
- JS 函数尽可能保持简洁
- 使用节流，click
- 使用事件委托，绑定事件到父元素上

## JS 动画优化

- 避免添加大量 JS 动画，尽量使用 CSS3 动画（可以直接访问 GPU）
- 尽量使用 canvas 动画
- 合理使用 requestAnimationFrame 动画代替 setTimeout、setInterval
  - requestAnimationFrame 可以在正确的时间渲染，setTimeout 和 setInterval 无法保证回调函数的执行时机
  - 动画与事件分离

## 合理使用缓存

- 合理缓存 DOM 对象，浏览器每次查询 DOM 对象非常耗时，将查询完的 DOM 对象缓存到一个变量里，下次查询和绑定事件的时候就不需要再查询浏览器了
- 缓存列表长度，要查询的 DOM 元素的长度
- 使用可缓存的 Ajax，缓存对应接口的数据

