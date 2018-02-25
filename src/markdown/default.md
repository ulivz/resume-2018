## 1 自我介绍

陈昊励，`94`年前端，来自湖北，现就职于 [eBay](http://www.ebay.com)。

<!-- 曾就职于 [SKG](http://www.skg.com) <sup>[1]</sup> -->

从初中开始一直坚持视觉设计，对色彩和布局有较深的理解。大学主期间攻汇编和`C`，曾参加西门子编程比赛获得国一。毕业后从`ng`起手做`app`，后来转入`Vue`，`React`和`Node.js`，钟爱研究前端工程化的各种最佳实践，擅长组件化编程以及研发各类提高生产效率的工具，热衷开源，同时也是一些开源作品(如`Vue`)的贡献者。


## 2 基本信息

- 姓名：陈昊励
- Github：https://github.com/ulivz
- 期望工作地点: 上海 / 杭州
- 学历：三峡大学 · 自动化
- 主修：`汇编`、`C`、`PLC`
- 英语：`CET-6`
- 绩点：`3.87/4`(两次专业第一)
- 邮箱：chl814@foxmail.com
- 电话：`+86 176 2114 5097`


## 3 技术栈

- JavaScript / ESNext
- RegExp
- TypeScript
- Vue / React / AngularJS / Marko.js
- Node.js
- Express / Koa
- Rollup / Webpack / Gulp
- CSS / SCSS / LESS / Stylus / PostCSS
- Responsive Design / Animation
- Cordova / Weex
- Git / Linux
- MySQL / MongoDB / SQLite
- Illustrator / PhotoShop / Sketch


## 4 工作经历

### 4.1 eBay

- **时间**：2017.4 至今

- **网站**：
	- www.vivanuncios.com.mx （墨西哥）
	- www.gumtree.co.za （南非）
	- www.alamaula.com （阿根廷）
	- www.gumtree.ie （爱尔兰）
	- www.gumtree.pl （波兰）
	- www.gumtree.sg （新加坡）

- **项目描述**：

  团队隶属于 [`eBay Classifieds Group`](https://www.ebayclassifiedsgroup.com/) ，主要负责其中`6`个国家的分类信息网站的`前端 / Node`开发，参与过少量`Java`开发。

  加入团队初期，前端部分刚刚从`Java`端拆分，引入`Node`作为中间层，一年的时间里，参与项目完成了从早期的`Handlebars.js`（纯SSR）到组件化`Marko.js`（同构）的迁移，同时负责各类基础设施的的建设和优化。

- **负责内容**：

  - Webpack、Gulp构建优化
  - 开发流程优化
  - 手写`Gulp`插件来完成`SVG`的构建(生成代码/压缩/预览)
  - 完成核心的全响应式图片组件（支持`DPR`/多类型/多设备）
  - 参与所有页面的开发
  - 独立负责 [Vivanuncios](https://www.vivanuncios.com.mx/) 首页从无到有
  - 广告：`Ad Banner/Adsense`
  - `SEO`
  - 代码迁移工具（从`handlebar`转成`marko`）
  - 页面体积优化
  - 页面级资源拆分（引入`TypeScript`，构建组件树完成）
  - 完成`CSS/SCSS`基础设施（主题/配色/布局/文档/规范/mixin/placeholder等）
  - 动画基础设施建设

### 4.2 SKG

- **时间**：2016.7 - 2017.1

- **网站**：
  - www.skg.com （首页）

- **项目描述**：

  先后参与开发 `SKG微信公众号`(关注`SKG生活攻略`可见)，`SKG产品知识库`，`SKG产品视频中心`，[`SKG官网`](www.skg.com)，以上项目的技术栈是`jQuery`、`ES5`。

  从业期间，较大型的一个项目是 `SKG Work APP`(内网可见)，技术栈是`ES5`、`AngularJS`、`Cordova`、`Ionic`和`SQLite`。这是一个`0`开始的给内部人员使用的`Hybird App`。
  
  负责了该`APP`全部的`UI`设计以及大部分的代码编写，其功能包含了内网新闻、聊天、QA、CRM、邮箱以及给供应商和经销商使用的模块。在项目后期独挑大梁自学`Node.js`，从而引入了`Gulp`，实现了合并代码、路径替换、基于环境变量的构建等功能，完成了从开发到上线的自动化构建。同时，还使用`Node.js`和`MySQL`来迁移了`login`功能.


### 4.3 其他项目

#### DDDML（基于领域驱动设计的开源ERP-前端部分）

- **名称**： [dddml-dotnet-tools](https://github.com/wubuku/dddml-dotnet-tools)
- **技术栈**：`Vue全家桶`、`TypeScript`、`Lodash`、`mocha`等。
- **项目描述**：

  项目的定位属于开源`ERP`，目前已经成功推广给`Haier`，后端参考了 [ADempiere](https://github.com/adempiere/adempiere) 和 [ofbiz](https://github.com/apache/ofbiz) 等经典的开源`ERP`，但开发模式选用了`DDD`（领域驱动设计）。项目的出发点是让半开发人员能够通过领域建模和配置（书写`DSL`）就能得到一套可用的系统，从而达到验证系统设计可行性的目的。

  因为是元编程，因此整个项目的核心前端代码都基本做到了可复用，项目的核心在于从元数据抽象出模型层的结构设计，最后再通过`VM`层映射到视图层，数据流和状态流大多在`VM`层手写完成，`vue`组件最终只起到了展示的作用。

- **备注**：此项目是在休业期`（2017.2-2017.4）`帮一个朋友做的。


## 5 轮子

### 5.1 独立开发

  - [dmo](https://github.com/ulivz/dmo): 一个极简配置的`REPL`生成器
  - [poz](https://github.com/ulivz/poz): 一个脚手架生成器，包含[vue-cli](https://github.com/vuejs/vue-cli)和 [sao](https://github.com/saojs/sao)的全部功能，同时提供了更全面的包管理功能。
  - [awesome-front-end](https://github.com/ulivz/awesome-front-end): 收集那些有价值的前端项目
  - [vue-codemirror-component](https://github.com/ulivz/vue-codemirror-component): 自带代码分割的`codemirror`组件
  - [parse7](https://github.com/ulivz/parse7): 一个极简的`HTML parser`
  - [alphax](https://github.com/ulivz/alphax): 基于`Stream`和`Glob`的类似于 [metalsmith](https://github.com/segmentio/metalsmith) 的静态网站生成器
  - [webpack-simple-redux](https://github.com/ulivz/webpack-simple-redux): Redux开发样板文件
  - [webpack-simple-vuex](https://github.com/ulivz/webpack-simple-vuex): Vuex开发样板文件
  - [usync](https://github.com/ulivz/usync)：一个可拓展的串/并行任务流程控制工具
  - [light-stylus](https://github.com/ulivz/light-stylus): 基于`Stylus`的CSS工具库
  - [vue-typescript-template-ui](https://github.com/ulivz/vue-typescript-template-ui): Vue/TypeScript的开发样板文件

<span style="color: #aaa; font-size: 12px ">注：仅列举部分项目，全部项目请见：<a href='https://github.com/ulivz?tab=repositories' target='_blank'>ulivz/repositories</a><span>

### 5.2 贡献代码

  - [vue](https://github.com/vuejs/vue)
  - [vuex](https://github.com/vuejs/vuex)
  - [marko](https://github.com/marko-js/marko)
  - [es6tutorial](https://github.com/ruanyf/es6tutorial)
  - [webpack-simple](https://github.com/vuejs-templates/webpack-simple)
  - [gulp-imagemin](https://github.com/sindresorhus/gulp-imagemin)
  - [You-Dont-Need-jQuery](https://github.com/nefe/You-Dont-Need-jQuery)

<span style="color: #aaa; font-size: 12px ">注：为以上项目贡献过源码。<span>

### 5.3 eBay内部

  - `bolt-jira-helpers`： 一个用于生成`JIRA Report`命令行工具
  - `bolt-jira-report`： 一个用于展示的`JIRA UI`（前后端分离）
  - `hbs-to-marko`: 代码迁移工具，转换 `hbs` 语法到 `marko`
  - `bolt-2dot0-docs-generator`: 为团队定制的文档生成工具

<span style="color: #aaa; font-size: 12px ">注：以上项目的仓库均存在于内网中。<span>

## 6 总结

- 喜欢造轮子和研究源码；
- 喜欢分享，在`eBay`给小伙伴们分享过`React`;
- 期望身边也有热衷开源和折腾的小伙伴；
- 期望为一家有团队和技术氛围、有活力的公司做贡献。

