# 网页前端及蓝桥杯

**This document will be updated later**

> 2022.11.13-15:00~16:30
> 卓正一

- [[#HTML|HTML]]
- [[#CSS|CSS]]
- [[#Javascript|Javascript]]
- [[#WebAssembly*|WebAssembly*]]
- [[#探索一个网页|探索一个网页]]
	- [[#探索一个网页#Chrom 内核浏览器提供的开发工具|Chrom 内核浏览器提供的开发工具]]
- [[#考纲|考纲]]
- [[#考点罗列|考点罗列]]
	- [[#考点罗列#基础 Javascript|基础 Javascript]]
	- [[#考点罗列#DOM控制|DOM控制]]
	- [[#考点罗列#基础排版|基础排版]]
	- [[#考点罗列#jQuery|jQuery]]
	- [[#考点罗列#Vue|Vue]]
	- [[#考点罗列#中等算法、场景题|中等算法、场景题]]
	- [[#考点罗列#Node.js|Node.js]]
	- [[#考点罗列#Echart 图表数据题|Echart 图表数据题]]
- [[#框架介绍|框架介绍]]
- [[#框架基本原理|框架基本原理]]
	- [[#框架基本原理#起点 / 动机|起点 / 动机]]
	- [[#框架基本原理#jQuery：像查询一样访问节点|jQuery：像查询一样访问节点]]
	- [[#框架基本原理#Vue：直接编写页面而不是控制流|Vue：直接编写页面而不是控制流]]
	- [[#框架基本原理#声明式前端框架的背后|声明式前端框架的背后]]
- [[#其他主流框架|其他主流框架]]
	- [[#其他主流框架#React|React]]
	- [[#其他主流框架#Svelte|Svelte]]
	- [[#其他主流框架#Solid.js|Solid.js]]
- [[#其他话题|其他话题]]
	- [[#其他话题#框架与无障碍|框架与无障碍]]
	- [[#其他话题#国际化|国际化]]
	- [[#其他话题#跨平台框架？|跨平台框架？]]
	- [[#其他话题#如何选择框架？|如何选择框架？]]


# 组成一个网页的要素

- HTML
- CSS
- Javascript
- WASM？

内容、样式和行为。

## HTML
- “节点” / 元素
- tag：标签，attribute：属性
- 树形组织

**HTML**（超文本标记语言——HyperText Markup Language）是构成 Web 世界的一砖一瓦。它定义了网页内容的含义和结构。
“超文本”（hypertext）是指连接单个网站内或多个网站间的网页的链接。链接是网络的一个基本方面。只要将内容上传到互联网，并将其与他人创建的页面相链接，你就成为了万维网的积极参与者。
HTML 使用“标记”（markup）来注明文本、图片和其他内容，以便于在 Web 浏览器中显示。HTML 标记包含一些特殊“元素”如 [`<head>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head)、[`<title>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title)、[`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body)、等等。
HTML 元素通过“标签”（tag）将文本从文档中引出，标签由在“`<`”和“`>`”中包裹的元素名组成，HTML 标签里的元素名不区分大小写。

> 阅读更多：[HTML（超文本标记语言） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/HTML)


## CSS
> Cascading Style Sheets，层叠样式表

- User Agent Style（浏览器默认值）
- 自定义、覆写
- 计算值

**层叠样式表** (Cascading Style Sheets，缩写为 **CSS**），是一种 [样式表](https://developer.mozilla.org/zh-CN/docs/Web/API/StyleSheet) 语言，用来描述 [HTML](https://developer.mozilla.org/zh-CN/docs/Web/HTML) 或 [XML](https://developer.mozilla.org/zh-CN/docs/Web/XML/XML_Introduction)（包括如 [SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)、[MathML](https://developer.mozilla.org/zh-CN/docs/Web/MathML)、[XHTML](https://developer.mozilla.org/zh-CN/docs/Glossary/XHTML) 之类的 XML 分支语言）文档的呈现。CSS 描述了在屏幕、纸质、音频等其它媒体上的元素应该如何被渲染的问题。

> 阅读更多： [CSS（层叠样式表） | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/CSS)

## Javascript

- 基本语法
- 奇怪特性：原型、隐式类型转换、闭包
- 单线程语言？

**JavaScript**（**JS**）是一种具有[函数优先](https://developer.mozilla.org/zh-CN/docs/Glossary/First-class_Function)特性的轻量级、解释型的编程语言。虽然作为 Web 页面中的脚本语言被人所熟知，但是它也被用到了很多非浏览器环境中，例如 [Node.js](https://developer.mozilla.org/zh-CN/docs/Glossary/Node.js)、[Apache CouchDB](https://couchdb.apache.org/)等。进一步说，JavaScript 是一种[基于原型](https://developer.mozilla.org/zh-CN/docs/Glossary/Prototype-based_programming)、多范式、单线程的动态语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。

DOM（Document Object Model——文档对象模型）是用来呈现以及与任意 HTML 或 XML 文档交互的 API。DOM 是载入到浏览器中的文档模型，以节点树的形式来表现文档，每个节点代表文档的构成部分（例如：页面元素、字符串或注释等等）。

【在 Chrome 浏览器中探索 document 对象】

> 阅读更多：[JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript) 、[文档对象模型 (DOM) - Web API 接口参考 | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/API/Document_Object_Model)、[The HTML DOM API - Web API 接口参考 | MDN (mozilla.org)](https://developer.mozilla.org/zh-CN/docs/Web/API/HTML_DOM_API)。

## WebAssembly*
> 新标准，全部主流浏览器支持。

更快、支持多线程，可用多种语言开发。

> 在线尝试： https://mbebenita.github.io/WasmExplorer/

## 探索一个网页
> 浏览器是最好的开发工具。

[How does web browsers work?. A browser is a software application… | by Monica Raghuwanshi | Medium](https://medium.com/@monica1109/how-does-web-browsers-work-c95ad628a509)



### Chrom 内核浏览器提供的开发工具

- Elements 元素/样式查看器
- Console 控制台
- Sources 资源查看器
- Network 网络请求监视器
- Component 组件查看器（只在支持组件式封装与开发的框架下支持。）
- Application 应用详情页（本地存储等。）


# 蓝桥杯Web应用开发赛简介
> [首页 — 全国大学生TMT行业赛事 (lanqiao.cn)](https://dasai.lanqiao.cn/)

## 考纲
<img src="https://files.catbox.moe/6d18l3.png" />
> 自行下载：[通知详情 — 全国大学生TMT行业赛事 (lanqiao.cn)](https://dasai.lanqiao.cn/notices/1364)

## 考点罗列

书面展示的考纲内容在13届中并不是全部涉及了，这里罗列一些重点考题和侧重点。

### 基础 Javascript
考过的题目：Array 原型的拓展，typeof、instanceof 运算、Promise（异步）。
侧重点：原型链、基础数据类型、数据类型转换、类语法（ES6）、数组API。

### DOM控制
考过的题：原生 DOM 事件、DOM增删改元素。
侧重点：DOM API 全部。

### 基础排版
考过的题目：Flex / Grid 布局、完整网页排版（==必考一题==）、Animation、动态适应网页、渐变色。
侧重点：CSS 弹性布局、基础 CSS 样式（能够搭建网页即可）、动画相关样式（关键帧、transition）、@media 查询。

预测：可以看看伪类选择器。

### jQuery
考过的题：基本是简单的场景应用题。
侧重点：选择器、jQuery API、$(this)。

### Vue
考过的题：稍难一些的应用题。
侧重点：生命周期、v-model。

预测：之前的题目是直接在 Javascript 里将组件挂载，现在慢慢向 .vue 组件转变了，两种都要会写。

### 中等算法、场景题
考过的题：树形结构的遍历、正则匹配（regExp）。
侧重点：==每次都会有一题==，一般是最后一题，不好预测，多接触一些 Javascript 吧。

### Node.js
*今年新增*
需要会简单的网络请求响应。

### Echart 图表数据题
考过的题：简单的数据处理与可视化（一般结合axios请求考）。
侧重点：大部分代码会给，但是具体的横、纵坐标数据在 option 中的位置与格式需要记忆或者尝试。==必考一题==。

# 前端框架

现代的，复杂的，具有交互性的网站通常被称为 **web 应用程序（web applicaiton）**。现代 JavaScript 框架的到来加快了打造高度动态化和交互性强的应用程序的速度。**框架**就是提供该如何构建应用程序的意见的库。

## 框架介绍

主要挑选两个 Javascript 框架介绍：jQuery[^i] 和 Vue。

[^i]: jQuery 是一个 Javascript 库（Library），在此处并列是话题需要。有时在前端技术，库与框架（Framework）的边界比较模糊——React 严格来说也是一个 Javascript 库，但很多人认为它是一个框架：[Is React a Library or a Framework? Here's Why it Matters (freecodecamp.org)](https://www.freecodecamp.org/news/is-react-a-library-or-a-framework/)。

> 挑选这两个的原因是蓝桥杯主要涉及这两个技术 :(
> 当然，jQuery 与 Vue 也能带我们看到前端框架的演进方向。

## 框架基本原理

### 起点 / 动机

除非是构建传统的静态网页，网页内容不涉及任何状态变化、数据交互以及复杂的排版，你只需要使用 HTML 和（或）CSS 就能够完成一个完整的网页，并不需要一行 Javascript 代码。但事实并不是这样：web 程序应用的出现使越来越多的状态管理、网络资源获取、用户交互需求以及技术产生，网页上的各个元素也越来越少以*静态*的方式出现。

控制页面元素的任务自然落到了 Javascript 脚本身上[^ii]，但是 Javacript 没有针对上述的任意一个需求进行专门的优化——它只是一门普通的脚本语言，恰巧能够控制网页的 DOM。若是单纯使用 Javascript 来完成“获取数据、在页面中展示数据、响应用户交互并完成增/删/改数据、调整合适的样式、提交”等一系列工作，页面代码最终会变得冗长和杂乱。

[^ii]:你可以使用服务端渲染技术来使用其他语言控制DOM，但现在主流的方式依然是使用 Javascript 或框架。

不同的框架使用不同的思路解决类似的问题。jQuery 提供了更便捷的 DOM 元素浏览和控制语法，而 Vue 则是通过向用户隐藏 DOM 的存在，进一步地接管状态控制、渲染、事件监听与样式控制（可以接入 UI 组件库）。

> JavaScript 框架的出现是为了提供更好的*开发体验*。它们没有给 JavaScript 带来新的功能；但它们使你可以更轻松地使用 JavaScript 来构建现代的 web。
> 
> 另外，CSS 框架（本文不会具体介绍）提供一些方式改写样式使得样式代码可以得到复用（SCSS）、封装（Tailwind CSS）或是在 Javascript 中能够简单地修改（styled）。

### jQuery：像查询一样访问节点

jQuery 的学习成本十分之低，主要得益于它仅仅拓展或简化了了 Javascript 明面上的能力，并且实现了了一个 Ajax 技术用于网络请求。

例如想要实现在点击时将元素隐藏：
```javascript
// DOM 操作
document.getElementById("#id").addEventListener("click", (e) => {
	e.target.style.display = 'none';
});

// jQuery
$("#id").click(() {
	$(this).hide();
});
```

jQuery 提供的 API 明显更加简洁易读。

学习 jQuery 只需要明白它提供的 API 便能轻松上手。//前提是对 Javascript 足够熟悉，当然还需要对 CSS 元素选择器足够了解。

以下是 jQuery 的 API 列表：
[jquery 在线手册 (runoob.com)](https://www.runoob.com/manual/jquery/)

### Vue：直接编写页面而不是控制流

像很多现代化的框架一样，Vue 把自己叫做“声明式（Declarative）“框架，目的是将自己与“命令式（instructional）”做区分。

Vue 让你能够在编写页面的时候声明一些会变化的数据、函数、生命周期回调等辅助于页面展现和用户交互的内容，以便将页面的构成逻辑从传统的内容、样式、行为内联到更小的单位中（封装成可以复用的组件）。

上面同样的例子，用 Vue 需要写成这样[^iii]：

[^iii]: Vue 也支持组件化的语法，此处为了演示用了挂载在 HTML 文件中的方式。

```html
<!-- 头尾忽略 -->
<div id="app">
	<div @click="toggleDisplay" :style="{ 'display': display }" >
		Anything here
	</div>
</div>

<script>
new Vue({
  el: '#app',
  data() {
    return {
      display: false, 
    }
  },
  methods: {
    toggleDisplay() {
	    this.display = !this.display;
    }
  }
})
</script>
```

可以看到，虽然代码更加复杂了，但是可以发现数据与事件回调函数惊人地直接出现在了表示“内容”的 HTML 代码中。

> Vue 是一个现代 JavaScript 框架提供了有用的设施渐进增强——不像许多其他框架，您可以使用 Vue 增强现有的 HTML。
> 
> 除了允许您逐步将 Vue 集成到您的应用程序中，Vue 还提供了一种渐进的方式编写标记。像大多数框架，Vue 通过组件允许您创建可重用块标记。大多数时候，Vue 组件是使用一个特殊的 HTML 模板的语法写的。当您需要比 HTML 语法允许的更多的控制时，您可以编写 JSX 或纯 JavaScript 函数来定义组件。
> 


> jQuery 和 Vue 的比较 [用 Vue.js 替换 jQuery：无需构建步骤 — 粉碎杂志 (smashingmagazine.com)](https://www.smashingmagazine.com/2018/02/jquery-vue-javascript/)


### 声明式前端框架的背后

- VDOM
框架通过对于现有代码生成虚拟的 DOM（Virtual DOM，VDOM） 页面，来取消原先的实体 DOM 操作的开销。（许多查找节点的操作设计先序遍历一棵节点树，开销十分大）。框架可以将很多步的 DOM 改变在自己维护的 VDOM 中完成，最后再渲染成浏览器的实体 DOM。即，VDOM 不是替代 DOM，而是尽量代理、减少、优化实际 DOM 操作的次数。
<img src="https://vuejs.org/assets/render-pipeline.03805016.png" >


- MVVM
模型-视图-连接器（Model View View-model）模式强制性地将视图（HTML 或是 JSX 表示的模版）、模型（数据）以及控制模型数据行为和渲染的连接器（Vue 实例等）分开，使得开发者可以分别地关心每一个部分的变化。
<img src='https://learn.microsoft.com/en-us/dotnet/architecture/maui/media/mvvm-pattern.png'>
实现 MVVM 的几个要件是：1. 对于数据表示的监听，一般会对需要渲染到模板中的变量构建监听器；2. 页面模板需要模板引擎与数据结合，并将模板语法转变为 VDOM；3. 将 VDOM 渲染成真实的 HTML 页面需要通过特殊的逻辑实现。

- 对于框架原理的感性认知
我们可以发现，大多数框架的运行逻辑就是先扫描一遍代表页面内容的模板，构建一棵自行维护的 DOM 树，并对于数据的修改及时响应（“响应式”框架名称的由来），刷新虚拟 DOM 并在合适的时刻将其渲染到页面。
抛开框架提供的模板语法，在底层运行的语言仍然是 Javascript，只是构建、修改文档对象的工作的大部分又框架中的引擎接管，而不让原生DOM负担起太多工作。

## 其他主流框架

### React

模板语法为 JSX，提供了一些钩子函数（hooks）来控制组件的生命周期。编码方式更接近原生 Javascript，也更具拓展能力（支持的组件库、工具套件比 Vue 多）。

> [React 官方中文文档 – 用于构建用户界面的 JavaScript 库 (docschina.org)](https://react.docschina.org/)

### Svelte

主打更少代码、无 VDOM 的框架。其能力附加于原生的 HTML 和 Javascript 之上。

```HTML
<script>
	let name = 'world';
</script>

<h1>Hello {name.toUpperCase()}!</h1>
```

> [Svelte 中文文档 | Svelte 中文网 (sveltejs.cn)](https://www.sveltejs.cn/)


### Solid.js

主打高性能、对更新内容和时间的完全控制。

```javascript
const App = () => { 
	const [count, setCount] = createSignal(0), 
		timer = setInterval(() => setCount(count() + 1), 1000); 
	onCleanup(() => clearInterval(timer)); 
	return html`<div>${count}</div>`; 
	// or 
	return h("div", {}, count);
}; 

render(App, document.body);
```

> [SolidJS · 反应式 JavaScript 库](https://www.solidjs.com/)


## 其他话题

### 框架与无障碍

> 框架的抽象不仅影响 JavaScript，还影响你与 web 的关系。无论你如何构建 web，最终，用户都是与 HTML 交互。用 JavaScript 编写整个应用可能会使你忽略 HTML 及其各种标签的用途，并导致产出一个无语义且难以使用的 HTML 文档。实际上，完全依赖 JavaScript 有可能写出脆弱的应用，且没有 JavaScript 就无法运行。
> 
> 框架不是问题的根源。错误的优先级可能使得*任何*应用变得脆弱、臃肿和难以使用。框架对开发者很友好，如果你的首要任务是制作一个复杂的 web 应用程序，那么很容易做到。然而，如果你没有考虑性能和无障碍，那么框架将放大这种脆弱、臃肿和难以使用。现代开发者的这种重心放在了框架上，已经在许多地方颠倒了 web 的结构。现代 web 通常把 JavaScript 放在首位，用户体验放在最后，而不是一个健壮的、内容优先的文档网络。

Material UI 试图使更多开发者注意到无障碍网页构建的重要性，可以查看他们的官网：[React Components - Material UI (mui.com)](https://mui.com/zh/material-ui/).
*在课程项目中使用 React + MUI 也是推荐的技术路线。*

### 国际化

若是想在前端提供一个更改语言的按钮，最好的做法是使用一些现成的国际化库（i18n 工具），他们可以帮助你使用 json 文档配置所有需要展现的字符。i18next 国际化库支持多数主流框架，可以支持使用统一的函数来将特定符号与配置的多语言文本对应。

```json
{
	"en": {
		"settings": "Settings"
	},
	"cn": {
		"settings": "设置"
	}
}
```
```
.......
return (<div> {i18next.t("settings")} </div>)

```


不仅是国际化，在其他特殊的需求（如主题变化、音频采集、视频播放）到来时，总是可以先寻找现成的依赖。

### 跨平台框架？

- uni-app
- Flutter
- ……

相比于上述的网页端框架，跨平台框架通过整合更多平台的 API、自建平台专属的渲染引擎，能够将一份 DSL 代码编译到不同平台的（移动端、网页、小程序）中。

![](https://vkceyugu.cdn.bspapp.com/VKCEYUGU-f184e7c3-1912-41b2-b81f-435d1b37c7b4/29448a55-2785-4296-9248-913dbda9de7f.png)

![](https://flutter.cn/docs/assets/images/docs/arch-overview/archdiagram.png)

> [uni-app官网 (dcloud.net.cn)](https://uniapp.dcloud.net.cn/)、[Flutter 中文文档](https://flutter.cn/docs)


### 如何选择框架？

- 首先要确定项目运行的平台，若是要适配移动端，请尽量选择跨平台框架。
- 若是简单、静态的网页，请先不要尝试使用框架。大多数框架提供了渐进式应用的能力，能让你快速地在局部使用框架所带来的好处。
- 在决定使用框架之后，可以尽量针对特殊用例进行调研，例如：框架是否提供较新的录音库？是否有支持音频可视化库？在对比之后做决定。尽量选择 Vue、React 之类使用较为广泛的框架，以便遇到问题时查阅资料。

