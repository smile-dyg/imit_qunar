# imit_qunar

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

### 目录结构描述

```
├─build
├─config
├─node_modules
├─src
│  ├─assets             //资源
│  │  └─styles
│  │      └─iconfont    //图标
│  ├─common             //
│  │  ├─fade            //动画组件
│  │  └─gallary         //图片轮播
│  ├─pages              //
│  │  ├─city            //城市选择界面
│  │  │  └─components   //城市选择组件
│  │  ├─detail          //热销推荐界面
│  │  │  └─components   //热销推荐组件
│  │  └─home            //Home界面
│  │      └─components  //Home组件
│  ├─router             //路由
│  └─store              //vuex
└─static				//模拟数据
    └─mock
```

### 实现功能

1.Home页

​	轮播图

​	图标布局和轮播逻辑

2.国内城市选择页面

​	搜索框搜索功能

​	字母表逻辑实现

3.热销推荐详情页

​	图片轮播

​	次级标题

​	上下滑动首部渐隐渐现效果