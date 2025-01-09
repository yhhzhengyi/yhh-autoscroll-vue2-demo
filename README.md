#自动滚动插件，vue2版本  

##npm安装  
npm install yhh-autoscroll-vue2 --save  

*vue3版本，请安装yhh-autoscroll-vue3*  
*vue3版本Demo包，[https://github.com/yhhzhengyi/yhh-actoscroll-vue3-demo](https://github.com/yhhzhengyi/yhh-actoscroll-vue3-demo)*  

*本组件是自动滚动的插件，不是翻页/翻屏/轮播图效果插件*  
*组件依赖：1、vue2；2、scss解析*  
*当容器大小发生改变时，组件会自动重新计算一遍动画效果*  

###组件可配置所有属性  
1. dir：滚动方向，可选值：水平-horizontal 竖-vertical(默认)  
2. width：组件宽度，默认值：100%  
3. height：组件高度，默认值：100%  
4. step-speed：滚动速度，越大越慢，默认值：500  

###组件暴露方法  
drawAnimate：计算动画效果的方法，通常，在组件slot内容变更完毕之后，需要调用此方法，以便滚动动画的适应更新  

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
