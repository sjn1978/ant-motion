---
category: Components
order: 1
cols: 3
chinese: 样式进出场动画
english: Animate
---



对单个元素根据状态进行动画显示隐藏，需结合 css 或其它第三方动画类一起使用；

## 何时使用

- 对单个元素状态切换时进行动画显示隐藏；

## 怎么使用

### 安装

```
$ npm install rc-animate --save
```

### 使用

```jsx
var Animate = require('rc-animate');
var ReactDOM = require('react-dom');
ReactDOM.render((
  <Animate showProp="visible" transitionName="fade">
    {show ? <div visible key="1">示例</div> : null}
  </Animate>
), container);
```
> [查看详细使用](https://github.com/react-component/animate/blob/master/docs/zh-cn/intro.md)

## API

### props 

|   name    |   type   |   default  |   description     |
|-----------|----------|------------|-------------------|
| showProp  | String   |  null      | 子级动画的类型，显示或隐藏。 [demo](http://react-component.github.io/animate/examples/hide-todo.html) |
| exclusive | Boolean  |  false     | 同时触发动画时，是否只允许只播放一个动画 |
| transitionName | String  |  null  | css 样式的名称, `fade`: enter: `fade-enter fade-enter-active` leave: `fade-leave fade-leave-active` | 
| transitionAppear | Boolean | false | 是否支持开始出现的动画 |
| transitionEnter  | Boolean | true  | 是否支持进场的动画, 出场后的进场 |
| transitionLeave  | Boolean | true  | 是否支持出场的动画   |
| onEnd     | Func     |  true    | 动画结束后的回调, callBack(key: String, exists: Boolean); |
| animation | Object   | {}         |  使用第三方动画类来执行动画 |
| component | React.Element/String   | `span` | 需要替换的标签  |

> animation 的动画案例去查看 react-component 里的 simple-animation, [查看demo](http://react-component.github.io/animate/)
