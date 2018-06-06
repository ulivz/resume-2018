## 1 自我介绍

陈昊励，`94`年前端，来自湖北，现就职于 [eBay](http://www.ebay.com)。

<!-- 曾就职于 [SKG](http://www.skg.com) <sup>[1]</sup> -->

从初中开始一直坚持视觉设计，对色彩和布局有较深的理解。大学主期间攻汇编和`C`，曾参加西门子编程比赛获得国一。毕业后从`ng`起手做`app`，后来转入`Vue`，`React`和`Node.js`，钟爱研究前端工程化的各种最佳实践，擅长组件化编程以及研发各类提高生产效率的工具，热衷开源，目前是 [Vue.js](https://github.com/vuejs) 的 `Team Member`，主要维护 [VuePress](https://github.com/vuejs/vuepress)。

<br>

## 2 基本信息

- **姓名**：陈昊励
- **Github**：https://github.com/ulivz
- **知乎专栏**：[ULVZ的前端进阶周刊](https://zhuanlan.zhihu.com/c_170301607)
- **期望工作地点**: 杭州 / 上海
- **学历**：三峡大学 · 自动化
- **主修**：`汇编`、`C`、`PLC`
- **英语**：`CET-6`
- **绩点**：`3.87/4`(两次专业第一)
- **邮箱**：chl814@foxmail.com
- **电话**：`+86 176 2114 5097`

<br>

## 3 技术栈

- JavaScript / ESNext
- Node.js / Express / Koa
- RegExp
- TypeScript
- Vue / React / AngularJS / Marko.js
- Git / Linux
- Webpack / Rollup / Gulp
- CSS / SCSS / LESS / Stylus / PostCSS
- Responsive Design / Animation
- Shell
- Docker
- MySQL / MongoDB / SQLite
- Illustrator / PhotoShop / Sketch
- Cordova / Weex
- Java

<br>

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

  加入团队初期，前端部分刚刚从`Java`端拆分，引入`Node`作为中间层，一年的时间里，参与项目完成了从早期的 `Handlebars.js`（纯SSR）到组件化`Marko.js`（同构）的迁移，同时负责各类基础设施的的建设和优化。

- **主要负责内容**：

  - 参与所有核心业务的开发
  - 独立负责 [Vivanuncios](https://www.vivanuncios.com.mx/) 首页从无到有
  - 将 `Webpack` 构建时间从 `60s` 降低到 `20s`
  - 完成基于 `Gulp` 的 `SVG` 的构建（生成代码 / 压缩 / 预览）
  - 完成首页的全响应式图片组件（支持 `DPR` / 多类型 / 多设备）
  - 页面性能优化
  - 页面级资源拆分（引入 `TypeScript`，构建组件依赖树完成）
  - 完成 `SCSS / 动画` 基础设施（主题 / 配色 / 布局 / 文档 / 规范 / mixin / placeholder 等）
  - 广告 `Google Ad Banner、Adsense`
  - 搜索引擎优化 `SEO`
  - 代码语法转换工具（从 `handlebar` 转成 `marko` ）

<br>

### 4.2 SKG

- **时间**：2016.7 - 2017.1

- **网站**：
  - www.skg.com （首页）

- **项目描述**：

  先后参与开发 `SKG微信公众号`(关注`SKG生活攻略`可见)，`SKG产品知识库`，`SKG产品视频中心`，[`SKG官网`](www.skg.com)，以上项目的技术栈是`jQuery`、`ES5`。

  从业期间，较大型的一个项目是 `SKG Work APP`(内网可见)，技术栈是`ES5`、`AngularJS`、`Cordova`、`Ionic`和`SQLite`。这是一个`0`开始的给内部人员使用的`Hybird App`。

  负责了该`APP`全部的`UI`设计以及大部分的代码编写，其功能包含了内网新闻、聊天、QA、CRM、邮箱以及给供应商和经销商使用的模块。在项目后期独挑大梁自学`Node.js`，从而引入了`Gulp`，实现了合并代码、路径替换、基于环境变量的构建等功能，完成了从开发到上线的自动化构建。同时，还使用`Node.js`和`MySQL`来迁移了`login`功能。

<br>

### 4.3 其他工作项目

#### DDDML（基于领域驱动设计的开源ERP-前端部分）

- **地址**： [dddml-dotnet-tools](https://github.com/wubuku/dddml-dotnet-tools)
- **技术栈**：`Vue全家桶`、`TypeScript`、`Lodash`、`mocha`等。
- **项目描述**：

  项目的定位属于开源`ERP`，目前已经成功推广给`Haier`，后端参考了 [ADempiere](https://github.com/adempiere/adempiere) 和 [ofbiz](https://github.com/apache/ofbiz) 等经典的开源`ERP`，但开发模式选用了`DDD`（领域驱动设计）。项目的出发点是让半开发人员能够通过领域建模和配置（书写`DSL`）就能得到一套可用的系统，从而达到验证系统设计可行性的目的。

- **备注**：此项目是在休业期`（2017.2-2017.4）`帮一个朋友做的。

<br>

## 5 开源

### 5.1 个人项目

| 名称                                                             | 描述                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------|
| [alphax](https://github.com/ulivz/alphax)                       | 基于 `Stream` 和 `Glob`  的脚手架基础工具                               |
| [jquery-swiper](https://github.com/ulivz/jquery-swiper)         | 一个极简的 [swiper](http://www.v2js.com/jquery-swiper), 已用于生产环境。 |
| [dmo](https://github.com/ulivz/dmo)                             | 一个极简配置的 `REPL` 生成器                                           |
| [usync](https://github.com/ulivz/usync)                         | 一个可拓展的串/并行任务流程控制工具                                        |
| [parse7](https://github.com/ulivz/parse7)                       | 一个极简的 `HTML parser`                                             |
| [awesome-front-end](https://github.com/ulivz/awesome-front-end) | 收集那些有价值的前端项目                                                |

### 5.2 贡献代码

| 名称                                               | 描述                                     |
|:--------------------------------------------------|:----------------------------------------|
| [vuepress](https://github.com/vuejs/vuepress)     | Vue.js官方的静态网站生成器，目前主要负责这个项目 |
| [docute](https://github.com/egoist/docute)        | 一款无需构建流程的静态网站生成器               |
| [vue-loader](https://github.com/vuejs/vue-loader) | Vue.js 单文件组件的 Webpack loader         |
| [vue](https://github.com/vuejs/vue/)              | Vue.js 主仓库                            |

> P.S. 简历篇幅有限，更多开源贡献请访问：https://github.com/ulivz/me。

<br>

## 6 eBay内部

| 名称                       | 描述                                |
|:--------------------------|:-----------------------------------|
| bolt-jira-helpers         | 一个用于生成团队每日工作进度的命令行工具    |
| bolt-jira-report          | 一个用于展示团队每日工作进度的简单可视化 UI |
| hbs-to-marko              | 代码迁移工具，转换 `Handlebars.js` 语法到 `marko` |
| bolt-2dot0-docs-generator | 为团队定制的文档生成工具                |

> 注：以上项目的仓库均存在于内网中。

<br>

## 6 工作期望

- **期望的公司**：因为个人喜欢开源、造轮子和研究源码和新技术，期望去一家有技术范围的公司。
- **期望发展方向**：**技术上**，期望的方向能够是基础设施、前端架构、用户体验、工程化中的编译时优化（Parse、AOT）、可视化等。**技术之外**也期望能够有更多带人的机会。

<br>

<blockquote>
<p style="font-size: 13px; color: #aaa">
本简历在线地址：[v2js.com/resume-2018](http://www.v2js.com/resume-2018)，在线版可以在 `附录` 一栏中看到一些工作内容中的小demo。
</p></blockquote>
