# finalCutter
最后的「切图工程师」

# 目的
从 Sketch／Photoshop 等视觉同学输出的产物中，*半自动*生成「端」上的代码。包括但不限于：

1. iOS
2. android
3. html
4. weex
5. [Texture](http://texturegroup.org/)

# 「端」的工程化
native 的代码更新麻烦，所以我们还是会把大部分逻辑放到后端，「端」尽量瘦，负责展示就可以了。「端」上通用的组建包括：

1. Router 跳转管理
2. IconFont／字体大小／颜色 等视觉规范常量
3. viewmodel 层。(参考 thrift)
4. 数据获取层。考虑到现在大部分 API 都是以 http/https 方式提供，所以需要改造 thrift 调用的方法，包装一层 http 请求，可以用端上常用的网络库。给 vm 层包括方法即可。
5. 通过 UI。固定组建参考[QMUI](https://github.com/QMUI)。下拉刷新／上拉加载／空页面 等。
6. 组件化脚手架。iOS framework cocoaods／android [atlas](https://github.com/alibaba/atlas)。
