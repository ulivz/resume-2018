<span style="color: #aaa; font-size: 12px ">注：附录部分展示了过去一年里一些"可以看到的"技术积累。<span>

## 1 Shopping Cart

这是所在团队第一次进行提高用户体验的尝试，在此之前，我们几乎没有任何的动画交互，在此之后，我给其他页面都陆陆续续加上了各种交互动画，如背景缩放，背景平移，SlideUp等。

### 1.1 Expand Animation

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/myads_checkout_button_01.gif)

###  1.2 Selection

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/myads_checkout_button_02.gif)


## 2 Webpack

### 2.1 Partial Pack

由于我们是一个一套代码服务于`6`个国家的多页应用，最早的时候，项目启动时`webpack build`需要大约`60s`, 同时，每一次更改都会重新打包所有代码，这不仅会耗费大量的时间，随着代码的增长，开发体验也会越来越差。经过分析，我发现，在某一段时间内，我们可能只会集中于某个`locale`进行开发。结合这样的实际开发场景，我实现了**局部打包**的构建, 让开发人员可以选择基于哪个`locale`进行开发：

```js
webpack   // build All Code
webpack --locale desktop_es_MX  // Only buiild MX's desktop's code
webpack --locale es_MX   // Both build MX's desktop and Mobile's code
webpack --locale desktop_en_ZA  // Only buiild ZA's desktop's code
```

### 2.2. Entries Reduce

多页应用必然会带来一个需求：需要基于页面和设备来实施构建。因为我们有**6**个`locale`，**3**种设备模式（Desktop、Mobile、Tablet），**10**个页面，这样下来，构建时`entry`的数量大约是`180`个——这将带来庞大的`build`时间！

通过分析，我们可以在构建期对每个`entry`所依赖的`modules`进行分析，从而得出哪些是重复的，于是得出下述的方案图：

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/webpack_entries_reduce.png)

方案的实施，最终通过在`Gulp`层收集包依赖，然后写了一个`webpack`插件(我将它命名为`EntriesReducePlugin`)完成了这项任务。

最终，经过`Partial Pack`和`Entries Reduce`共同的的优化，`webpack`首次打包的时间减少到原来的`1/3`左右。

- 优化前：

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/webpack_before.png)

- 优化后：

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/webpack_after.png)


## 3 Image Loading

在独立负责了墨西哥新首页 [vivanuncios](http://www.vivanuncios.com.mx/) 之后，为了让首屏的响应时间提升到极致，我完成了一个功能极其庞大的纯`SSR`图片组件, 它具有如下特性：

- 支持 [device-pixel-ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/-webkit-device-pixel-ratio)
- 支持多种图片格式（webp/png/jpg）
- 支持缩略图（inline）
- 支持纯占位背景图（构建过程采用了死月的）
- 支持`IE11`兼容的`background-image: cover`(CSS Trick)

最终的效果是基本上做到了无白屏：

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/homepage_image_loading.gif)


## 4 JIRA工具

给团队内部造这个工具的原因是：团队的`PM`在美国, 我们每天需要提交昨日的进度更新报告。但人工生成这个报告会非常花时间，一般需要十几分钟。

首先，我完成了一个用命令行生成`JIRA`报告的CLI:

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/bolt-jira-cli.png)

后续，在和团队负责人的沟通下，一致认为需要一个`UI`。最终，我采用和团队核心技术栈一样的技术（前后端分离）完成了这个工具，其具有的特性如下：

- 登录/登出
- 团队切换
- `Sprint`切换
- `DEV/QA`一对一显示
- 自定义排序
- 自定义过滤
- 状态切换

![](https://raw.githubusercontent.com/ulivz/static-files/master/images/bolt-jira-report/00.png)
![](https://raw.githubusercontent.com/ulivz/static-files/master/images/bolt-jira-report/01.png)
![](https://raw.githubusercontent.com/ulivz/static-files/master/images/bolt-jira-report/02.png)
![](https://raw.githubusercontent.com/ulivz/static-files/master/images/bolt-jira-report/03.png)

