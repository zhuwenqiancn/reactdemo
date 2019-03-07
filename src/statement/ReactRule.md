
## 目录
---
#### [命名规则](#nameing-rule)

- [项目命名](#project-naming)
- [目录命名](#folder-naming)
- [JS文件命名](#js-naming)
- [CSS, SCSS文件命名](#css-naming)
- [HTML文件命名](#html-naming)

#### [HTML](#html)

- [语法](#html-syntax)
- [HTML5 doctype](#html-doctype)
- [lang属性](#html-lang)
- [字符编码](#html-encoding)
- [IE兼容模式](#html-ie-compatibility-mode)
- [引入CSS, JS](#html-style-script)
- [属性顺序](#html-attribute-order)
- [boolean属性](#html-boolean-attributes)
- [JS生成标签](#html-javascript)
- [减少标签数量](#html-reducing-markup)
- [实用高于完美](#html-practicality)

#### [CSS, SCSS](#css)

- [缩进](#css-indentation)
- [分号](#css-semicolon)
- [空格](#css-space)
- [空行](#css-blank-line)
- [换行](#css-new-line)
- [注释](#css-comments)
- [引号](#css-quote-marks)
- [命名](#css-naming-rule)
- [属性声明顺序](#css-declaration-order)
- [颜色](#css-color)
- [属性简写](#css-shorthand)
- [媒体查询](#css-media-queries)
- [SCSS相关](#css-scss)
- [杂项](#css-miscellaneous)

#### [JavaScript](#javascript)

- [缩进](#js-indentation)
- [单行长度](#js-line-max-length)
- [分号](#js-semicolon)
- [空格](#js-space)
- [空行](#js-blank-line)
- [换行](#js-new-line)
- [单行注释](#js-comments-single-line)
- [多行注释](#js-comments-multiline)
- [文档注释](#js-comments-documentation)
- [引号](#js-quote-marks)
- [变量命名](#js-variable-naming)
- [变量声明](#js-variable-declaration)
- [函数](#js-function)
- [数组、对象](#js-array-object)
- [括号](#js-brace)
- [null](#js-literal-value-null)
- [undefined](#js-literal-value-null)
- [jshint](#js-jshint)
- [杂项](#js-miscellaneous)

#### [编辑器配置和构建检查](#check)

- [sublime3插件](#check-sublime3)
- [grunt插件](#check-grunt)

#### [react 核心代码规范及要求](#react)

- [一、总体要求](#react-requirements)

  - [1.方法根据生命周期排序](#react-requirements)
  - [2.事件函数命名](#react-requirements)
  - [3.组建验证](#react-requirements)
  - [4～6. ...](#react-requirements)

- [二、基本规范](#react-base-guide)

- [三、命名规范](#react-naming-rule)

- [四、组件规范](#react-component-standard)

- [五、约定](#react-agreements)

- [六、CSS相关](#react-css)

- [七、代码校验工具 ESLint等](#react-eslint)
---

## <h2 id="golden-rule">最佳原则</h2>

坚持制定好的代码规范。
无论团队人数多少，代码应该同出一门。
如果你想要为这个规范做贡献或觉得有不合理的地方，请访问[New Issue](https://github.com/AlloyTeam/CodeGuide/issues/new)。

## <h2 id="nameing-rule"> 命名规则</h2>

### <h3 id="project-naming">项目命名</h3>

全部采用小写方式， 以下划线分隔。

例：my_project_name

### <h3 id="folder-naming">目录命名</h3>

参照项目命名规则；

有复数结构时，要采用复数命名法。

例：scripts, styles, images, data_models

### <h3 id="js-naming">JS文件命名</h3>

参照项目命名规则。

例：account_model.js

### <h3 id="css-naming">CSS, SCSS文件命名</h3>

参照项目命名规则。

例：retina_sprites.scss

### <h3 id="html-naming">HTML文件命名</h3>

参照项目命名规则。

例：error_report.html

## <h2 id="html">HTML</h2>

### <h3 id="html-syntax">语法</h3>

- 缩进使用soft tab（4个空格）；
- 嵌套的节点应该缩进；
- 在属性上，使用双引号，不要使用单引号；
- 属性名全小写，用中划线做分隔符；
- 不要在自动闭合标签结尾处使用斜线（[HTML5 规范](http://dev.w3.org/html5/spec-author-view/syntax.html#syntax-start-tag)指出他们是可选的）；
- 不要忽略可选的关闭标签，例：`</li>`和`</body>`。

```html
  <!DOCTYPE html>
  <html>
   <head>
   <title>Page title</title>
   </head>
   <body>
   <img src="images/company_logo.png" alt="Company">
   <h1 class="hello-world">Hello, world!</h1>
   </body>
  </html>
```

### <h3 id="html-doctype">HTML5 doctype</h3>

在页面开头使用这个简单地doctype来启用标准模式，使其在每个浏览器中尽可能一致的展现；

虽然doctype不区分大小写，但是按照惯例，doctype大写 （[关于html属性，大写还是小写](http://stackoverflow.com/questions/15594877/is-there-any-benefits-to-use-uppercase-or-lowercase-letters-with-html5-tagname)）。

```html
<!DOCTYPE html>
<html>
    ...
</html>
```

### <h3 id="html-lang">lang属性</h3>

根据HTML5规范：

> 应在html标签上加上lang属性。这会给语音工具和翻译工具帮助，告诉它们应当怎么去发音和翻译。

更多关于`lang`属性的说明[在这里](http://www.w3.org/html/wg/drafts/html/master/semantics.html#the-html-element)；

在sitepoint上可以查到[语言列表](http://reference.sitepoint.com/html/lang-codes)；

但sitepoint只是给出了语言的大类，例如中文只给出了zh，但是没有区分香港，台湾，大陆。而微软给出了一份更加[详细的语言列表](http://msdn.microsoft.com/en-us/library/ms533052(v=vs.85).aspx)，其中细分了zh-cn, zh-hk, zh-tw。

```html
<!DOCTYPE html>
<html lang="en-us">
    ...
</html>
```

### <h3 id="html-encoding">字符编码</h3>

通过声明一个明确的字符编码，让浏览器轻松、快速的确定适合网页内容的渲染方式，通常指定为'UTF-8'。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
    </head>
    ...
</html>
```

### <h3 id="html-ie-compatibility-mode">IE兼容模式</h3>

用`<meta>`标签可以指定页面应该用什么版本的IE来渲染；

如果你想要了解更多，请点击[这里](http://stackoverflow.com/questions/6771258/whats-the-difference-if-meta-http-equiv-x-ua-compatible-content-ie-edge-e)；

不同doctype在不同浏览器下会触发不同的渲染模式（[这篇文章](https://hsivonen.fi/doctype/)总结的很到位）。

```html
<!DOCTYPE html>
<html>
    <head>
        <meta http-equiv="X-UA-Compatible" content="IE=Edge">
    </head>
    ...
</html>
```

### <h3 id="html-style-script">引入CSS, JS</h3>

根据HTML5规范, 通常在引入CSS和JS时不需要指明`type`，因为`text/css`和`text/javascript`分别是他们的默认值。

### HTML5 规范链接

- [使用link](http://www.w3.org/TR/2011/WD-html5-20110525/semantics.html#the-link-element)
- [使用style](http://www.w3.org/TR/2011/WD-html5-20110525/semantics.html#the-style-element)
- [使用script](http://www.w3.org/TR/2011/WD-html5-20110525/scripting-1.html#the-script-element)

```html
<!-- External CSS -->
<link rel="stylesheet" href="code_guide.css">

<!-- In-document CSS -->
<style>
    ...
</style>

<!-- External JS -->
<script src="code_guide.js"></script>

<!-- In-document JS -->
<script>
    ...
</script>
```

### <h3 id="html-attribute-order">属性顺序</h3>

属性应该按照特定的顺序出现以保证易读性；

- `class`
- `id`
- `name`
- `data-*`
- `src`,`for`,`type`,`href`,`value`,`max-length`,`max`,`min`,`pattern`
- `placeholder`,`title`,`alt`
- `aria-*`,`role`
- `required`,`readonly`,`disabled`

class是为高可复用组件设计的，所以应处在第一位；

id更加具体且应该尽量少使用，所以将它放在第二位。

```html
<a class="..." id="..." data-modal="toggle" href="#">Example link</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```

### <h3 id="html-boolean-attributes">boolean属性</h3>

boolean属性指不需要声明取值的属性，XHTML需要每个属性声明取值，但是HTML5并不需要；

更多内容可以参考[WhatWG section on boolean attributes](http://www.whatwg.org/specs/web-apps/current-work/multipage/common-microsyntaxes.html#boolean-attributes)：

> boolean属性的存在表示取值为true，不存在则表示取值为false。

```html
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
    <option value="1" selected>1</option>
</select>
```

### <h3 id="html-javascript">JS生成标签</h3>

在JS文件中生成标签让内容变得更难查找，更难编辑，性能更差。应该尽量避免这种情况的出现。

### <h3 id="html-reducing-markup">减少标签数量</h3>

在编写HTML代码时，需要尽量避免多余的父节点；

很多时候，需要通过迭代和重构来使HTML变得更少。

```html
<!-- Not well -->
<span class="avatar">
    <img src="...">
</span>

<!-- Better -->
<img class="avatar" src="...">
```

### <h3 id="html-practicality">实用高于完美</h3>

尽量遵循HTML标准和语义，但是不应该以浪费实用性作为代价；

任何时候都要用尽量小的复杂度和尽量少的标签来解决问题。

## <h2 id="css"> CSS, SCSS</h2>

### <h3 id="css-indentation">缩进</h3>

使用soft tab（4个空格）。

```css
.element {
    position: absolute;
    top: 10px;
    left: 10px;

    border-radius: 10px;
    width: 50px;
    height: 50px;
}
```

### <h3 id="css-semicolon">分号</h3>

每个属性声明末尾都要加分号。

```css
.element {
    width: 20px;
    height: 20px;

    background-color: red;
}
```

### <h3 id="css-space">空格</h3>

以下几种情况不需要空格：

- 属性名后
- 多个规则的分隔符','前
- `!important`'!'后
- 属性值中'('后和')'前
- 行末不要有多余的空格

以下几种情况需要空格：

- 属性值前
- 选择器'>', '+', '~'前后
- '{'前
- `!important`'!'前
- `@else`前后
- 属性值中的','后
- 注释'/*'后和'*/'前

```css
/* not good */
.element {
    color :red! important;
    background-color: rgba(0,0,0,.5);
}

/* good */
.element {
    color: red !important;
    background-color: rgba(0, 0, 0, .5);
}

/* not good */
.element ,
.dialog{
    ...
}

/* good */
.element,
.dialog {

}

/* not good */
.element>.dialog{
    ...
}

/* good */
.element > .dialog{
    ...
}

/* not good */
.element{
    ...
}

/* good */
.element {
    ...
}

/* not good */
@if{
    ...
}@else{
    ...
}

/* good */
@if {
    ...
} @else {
    ...
}
```

### <h3 id="css-blank-line">空行</h3>

以下几种情况需要空行：

- 文件最后保留一个空行
- '}'后最好跟一个空行，包括scss中嵌套的规则
- 属性之间需要适当的空行，具体见[属性声明顺序](#css-declaration-order)

```css
/* not good */
.element {
    ...
}
.dialog {
    color: red;
    &:after {
        ...
    }
}

/* good */
.element {
    ...
}

.dialog {
    color: red;

    &:after {
        ...
    }
}
```

### <h3 id="css-new-line">换行</h3>

以下几种情况不需要换行：

- '{'前

以下几种情况需要换行：

- '{'后和'}'前
- 每个属性独占一行
- 多个规则的分隔符','后

```css
/* not good */
.element
{color: red; background-color: black;}

/* good */
.element {
    color: red;
    background-color: black;
}

/* not good */
.element, .dialog {
    ...
}

/* good */
.element,
.dialog {
    ...
}
```

### <h3 id="css-comments">注释</h3>

注释统一用'/* */'（scss中也不要用'//'），具体参照右边的写法；

缩进与下一行代码保持一致；

可位于一个代码行的末尾，与代码间隔一个空格。

```css
/* Modal header */
.modal-header {
    ...
}

/*
 * Modal header
 */
.modal-header {
    ...
}

.modal-header {
    /* 50px */
    width: 50px;

    color: red; /* color red */
}
```

### <h3 id="css-quote-marks">引号</h3></h3>

最外层统一使用双引号；

url的内容要用引号；

属性选择器中的属性值需要引号。

```css
.element:after {
    content: "";
    background-image: url("logo.png");
}

li[data-type="single"] {
    ...
}
```

### <h3 id="css-naming-rule">命名</h3>

- 类名使用小写字母，以中划线分隔
- id采用驼峰式命名
- scss中的变量、函数、混合、placeholder采用驼峰式命名

```css
/* class */
.element-content {
    ...
}

/* id */
#myDialog {
    ...
}

/* 变量 */
$colorBlack: #000;

/* 函数 */
@function pxToRem($px) {
    ...
}

/* 混合 */
@mixin centerBlock {
    ...
}

/* placeholder */
%myDialog {
    ...
}
```

### <h3 id="css-declaration-order">属性声明顺序</h3>

相关的属性声明按右边的顺序做分组处理，组之间需要有一个空行。

```css
.declaration-order {
    display: block;
    float: right;

    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: 100;

    border: 1px solid #e5e5e5;
    border-radius: 3px;
    width: 100px;
    height: 100px;

    font: normal 13px "Helvetica Neue", sans-serif;
    line-height: 1.5;
    text-align: center;

    color: #333;
    background-color: #f5f5f5;

    opacity: 1;
}
```

```javascript
// 下面是推荐的属性的顺序
[
    [
        "display",
        "visibility",
        "float",
        "clear",
        "overflow",
        "overflow-x",
        "overflow-y",
        "clip",
        "zoom"
    ],
    [
        "table-layout",
        "empty-cells",
        "caption-side",
        "border-spacing",
        "border-collapse",
        "list-style",
        "list-style-position",
        "list-style-type",
        "list-style-image"
    ],
    [
        "-webkit-box-orient",
        "-webkit-box-direction",
        "-webkit-box-decoration-break",
        "-webkit-box-pack",
        "-webkit-box-align",
        "-webkit-box-flex"
    ],
    [
        "position",
        "top",
        "right",
        "bottom",
        "left",
        "z-index"
    ],
    [
        "margin",
        "margin-top",
        "margin-right",
        "margin-bottom",
        "margin-left",
        "-webkit-box-sizing",
        "-moz-box-sizing",
        "box-sizing",
        "border",
        "border-width",
        "border-style",
        "border-color",
        "border-top",
        "border-top-width",
        "border-top-style",
        "border-top-color",
        "border-right",
        "border-right-width",
        "border-right-style",
        "border-right-color",
        "border-bottom",
        "border-bottom-width",
        "border-bottom-style",
        "border-bottom-color",
        "border-left",
        "border-left-width",
        "border-left-style",
        "border-left-color",
        "-webkit-border-radius",
        "-moz-border-radius",
        "border-radius",
        "-webkit-border-top-left-radius",
        "-moz-border-radius-topleft",
        "border-top-left-radius",
        "-webkit-border-top-right-radius",
        "-moz-border-radius-topright",
        "border-top-right-radius",
        "-webkit-border-bottom-right-radius",
        "-moz-border-radius-bottomright",
        "border-bottom-right-radius",
        "-webkit-border-bottom-left-radius",
        "-moz-border-radius-bottomleft",
        "border-bottom-left-radius",
        "-webkit-border-image",
        "-moz-border-image",
        "-o-border-image",
        "border-image",
        "-webkit-border-image-source",
        "-moz-border-image-source",
        "-o-border-image-source",
        "border-image-source",
        "-webkit-border-image-slice",
        "-moz-border-image-slice",
        "-o-border-image-slice",
        "border-image-slice",
        "-webkit-border-image-width",
        "-moz-border-image-width",
        "-o-border-image-width",
        "border-image-width",
        "-webkit-border-image-outset",
        "-moz-border-image-outset",
        "-o-border-image-outset",
        "border-image-outset",
        "-webkit-border-image-repeat",
        "-moz-border-image-repeat",
        "-o-border-image-repeat",
        "border-image-repeat",
        "padding",
        "padding-top",
        "padding-right",
        "padding-bottom",
        "padding-left",
        "width",
        "min-width",
        "max-width",
        "height",
        "min-height",
        "max-height"
    ],
    [
        "font",
        "font-family",
        "font-size",
        "font-weight",
        "font-style",
        "font-variant",
        "font-size-adjust",
        "font-stretch",
        "font-effect",
        "font-emphasize",
        "font-emphasize-position",
        "font-emphasize-style",
        "font-smooth",
        "line-height",
        "text-align",
        "-webkit-text-align-last",
        "-moz-text-align-last",
        "-ms-text-align-last",
        "text-align-last",
        "vertical-align",
        "white-space",
        "text-decoration",
        "text-emphasis",
        "text-emphasis-color",
        "text-emphasis-style",
        "text-emphasis-position",
        "text-indent",
        "-ms-text-justify",
        "text-justify",
        "letter-spacing",
        "word-spacing",
        "-ms-writing-mode",
        "text-outline",
        "text-transform",
        "text-wrap",
        "-ms-text-overflow",
        "text-overflow",
        "text-overflow-ellipsis",
        "text-overflow-mode",
        "-ms-word-wrap",
        "word-wrap",
        "-ms-word-break",
        "word-break"
    ],
    [
        "color",
        "background",
        "filter:progid:DXImageTransform.Microsoft.AlphaImageLoader",
        "background-color",
        "background-image",
        "background-repeat",
        "background-attachment",
        "background-position",
        "-ms-background-position-x",
        "background-position-x",
        "-ms-background-position-y",
        "background-position-y",
        "-webkit-background-clip",
        "-moz-background-clip",
        "background-clip",
        "background-origin",
        "-webkit-background-size",
        "-moz-background-size",
        "-o-background-size",
        "background-size"
    ],
    [
        "outline",
        "outline-width",
        "outline-style",
        "outline-color",
        "outline-offset",
        "opacity",
        "filter:progid:DXImageTransform.Microsoft.Alpha(Opacity",
        "-ms-filter:\\'progid:DXImageTransform.Microsoft.Alpha",
        "-ms-interpolation-mode",
        "-webkit-box-shadow",
        "-moz-box-shadow",
        "box-shadow",
        "filter:progid:DXImageTransform.Microsoft.gradient",
        "-ms-filter:\\'progid:DXImageTransform.Microsoft.gradient",
        "text-shadow"
    ],
    [
        "-webkit-transition",
        "-moz-transition",
        "-ms-transition",
        "-o-transition",
        "transition",
        "-webkit-transition-delay",
        "-moz-transition-delay",
        "-ms-transition-delay",
        "-o-transition-delay",
        "transition-delay",
        "-webkit-transition-timing-function",
        "-moz-transition-timing-function",
        "-ms-transition-timing-function",
        "-o-transition-timing-function",
        "transition-timing-function",
        "-webkit-transition-duration",
        "-moz-transition-duration",
        "-ms-transition-duration",
        "-o-transition-duration",
        "transition-duration",
        "-webkit-transition-property",
        "-moz-transition-property",
        "-ms-transition-property",
        "-o-transition-property",
        "transition-property",
        "-webkit-transform",
        "-moz-transform",
        "-ms-transform",
        "-o-transform",
        "transform",
        "-webkit-transform-origin",
        "-moz-transform-origin",
        "-ms-transform-origin",
        "-o-transform-origin",
        "transform-origin",
        "-webkit-animation",
        "-moz-animation",
        "-ms-animation",
        "-o-animation",
        "animation",
        "-webkit-animation-name",
        "-moz-animation-name",
        "-ms-animation-name",
        "-o-animation-name",
        "animation-name",
        "-webkit-animation-duration",
        "-moz-animation-duration",
        "-ms-animation-duration",
        "-o-animation-duration",
        "animation-duration",
        "-webkit-animation-play-state",
        "-moz-animation-play-state",
        "-ms-animation-play-state",
        "-o-animation-play-state",
        "animation-play-state",
        "-webkit-animation-timing-function",
        "-moz-animation-timing-function",
        "-ms-animation-timing-function",
        "-o-animation-timing-function",
        "animation-timing-function",
        "-webkit-animation-delay",
        "-moz-animation-delay",
        "-ms-animation-delay",
        "-o-animation-delay",
        "animation-delay",
        "-webkit-animation-iteration-count",
        "-moz-animation-iteration-count",
        "-ms-animation-iteration-count",
        "-o-animation-iteration-count",
        "animation-iteration-count",
        "-webkit-animation-direction",
        "-moz-animation-direction",
        "-ms-animation-direction",
        "-o-animation-direction",
        "animation-direction"
    ],
    [
        "content",
        "quotes",
        "counter-reset",
        "counter-increment",
        "resize",
        "cursor",
        "-webkit-user-select",
        "-moz-user-select",
        "-ms-user-select",
        "user-select",
        "nav-index",
        "nav-up",
        "nav-right",
        "nav-down",
        "nav-left",
        "-moz-tab-size",
        "-o-tab-size",
        "tab-size",
        "-webkit-hyphens",
        "-moz-hyphens",
        "hyphens",
        "pointer-events"
    ]
]
```

### <h3 id="css-color">颜色</h3>

颜色16进制用小写字母；

颜色16进制尽量用简写。

```css
/* not good */
.element {
    color: #ABCDEF;
    background-color: #001122;
}

/* good */
.element {
    color: #abcdef;
    background-color: #012;
}
```

### <h3 id="css-shorthand">属性简写</h3>

属性简写需要你非常清楚属性值的正确顺序，而且在大多数情况下并不需要设置属性简写中包含的所有值，所以建议尽量分开声明会更加清晰；

`margin`和`padding`相反，需要使用简写；

常见的属性简写包括：

- `font`
- `background`
- `transition`
- `animation`

```css
/* not good */
.element {
    transition: opacity 1s linear 2s;
}

/* good */
.element {
    transition-delay: 2s;
    transition-timing-function: linear;
    transition-duration: 1s;
    transition-property: opacity;
}
```

### <h3 id="css-media-queries">媒体查询</h3>

尽量将媒体查询的规则靠近与他们相关的规则，不要将他们一起放到一个独立的样式文件中，或者丢在文档的最底部，这样做只会让大家以后更容易忘记他们。

```css
.element {
    ...
}

.element-avatar{
    ...
}

@media (min-width: 480px) {
    .element {
        ...
    }

    .element-avatar {
        ...
    }
}
```

### <h3 id="css-scss">SCSS相关</h3>

提交的代码中不要有`@debug`；

声明顺序：

- `@extend`
- 不包含`@content`的`@include`
- 包含`@content`的`@include`
- 自身属性
- 嵌套规则

`@import`引入的文件不需要开头的'_'和结尾的'.scss'；

嵌套最多不能超过5层；

`@extend`中使用placeholder选择器；

去掉不必要的父级引用符号'&'。

```css
/* not good */
@import "_dialog.scss";

/* good */
@import "dialog";

/* not good */
.fatal {
    @extend .error;
}

/* good */
.fatal {
    @extend %error;
}

/* not good */
.element {
    & > .dialog {
        ...
    }
}

/* good */
.element {
    > .dialog {
        ...
    }
}
```

### <h3 id="css-miscellaneous">杂项</h3>

不允许有空的规则；

元素选择器用小写字母；

去掉小数点前面的0；

去掉数字中不必要的小数点和末尾的0；

属性值'0'后面不要加单位；

同个属性不同前缀的写法需要在垂直方向保持对齐，具体参照右边的写法；

无前缀的标准属性应该写在有前缀的属性后面；

不要在同个规则里出现重复的属性，如果重复的属性是连续的则没关系；

不要在一个文件里出现两个相同的规则；

用`border: 0;`代替`border: none;`；

选择器不要超过4层（在scss中如果超过4层应该考虑用嵌套的方式来写）；

发布的代码中不要有`@import`；

尽量少用'*'选择器。

```css
/* not good */
.element {
}

/* not good */
LI {
    ...
}

/* good */
li {
    ...
}

/* not good */
.element {
    color: rgba(0, 0, 0, 0.5);
}

/* good */
.element {
    color: rgba(0, 0, 0, .5);
}

/* not good */
.element {
    width: 50.0px;
}

/* good */
.element {
    width: 50px;
}

/* not good */
.element {
    width: 0px;
}

/* good */
.element {
    width: 0;
}

/* not good */
.element {
    border-radius: 3px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;

    background: linear-gradient(to bottom, #fff 0, #eee 100%);
    background: -webkit-linear-gradient(top, #fff 0, #eee 100%);
    background: -moz-linear-gradient(top, #fff 0, #eee 100%);
}

/* good */
.element {
    -webkit-border-radius: 3px;
       -moz-border-radius: 3px;
            border-radius: 3px;

    background: -webkit-linear-gradient(top, #fff 0, #eee 100%);
    background:    -moz-linear-gradient(top, #fff 0, #eee 100%);
    background:         linear-gradient(to bottom, #fff 0, #eee 100%);
}

/* not good */
.element {
    color: rgb(0, 0, 0);
    width: 50px;
    color: rgba(0, 0, 0, .5);
}

/* good */
.element {
    color: rgb(0, 0, 0);
    color: rgba(0, 0, 0, .5);
}
```

## <h2 id="javascript">JavaScript</h2>

### <h3 id="js-indentation">缩进</h3>

使用soft tab（4个空格）。

```javascript
var x = 1,
    y = 1;

if (x < y) {
    x += 10;
} else {
    x += 1;
}
```

### <h3 id="js-line-max-length">单行长度</h3>

不要超过80，但如果编辑器开启word wrap可以不考虑单行长度。

### <h3 id="js-semicolon">分号</h3>

以下几种情况后需加分号：

- 变量声明
- 表达式
- return
- throw
- break
- continue
- do-while

```javascript
/* var declaration */
var x = 1;

/* expression statement */
x++;

/* do-while */
do {
    x++;
} while (x < 10);
```

### <h3 id="js-space">空格</h3>

以下几种情况不需要空格：

- 对象的属性名后
- 前缀一元运算符后
- 后缀一元运算符前
- 函数调用括号前
- 无论是函数声明还是函数表达式，'('前不要空格
- 数组的'['后和']'前
- 对象的'{'后和'}'前
- 运算符'('后和')'前

以下几种情况需要空格：

- 二元运算符前后
- 三元运算符'?:'前后
- 代码块'{'前
- 下列关键字前：`else`,`while`,`catch`,`finally`
- 下列关键字后：`if`,`else`,`for`,`while`,`do`,`switch`,`case`,`try`,`catch`,`finally`,`with`,`return`,`typeof`
- 单行注释'//'后（若单行注释和代码同行，则'//'前也需要），多行注释'*'后
- 对象的属性值前
- for循环，分号后留有一个空格，前置条件如果有多个，逗号后留一个空格
- 无论是函数声明还是函数表达式，'{'前一定要有空格
- 函数的参数之间

```javascript
// not good
var a = {
    b :1
};

// good
var a = {
    b: 1
};

// not good
++ x;
y ++;
z = x?1:2;

// good
++x;
y++;
z = x ? 1 : 2;

// not good
var a = [ 1, 2 ];

// good
var a = [1, 2];

// not good
var a = ( 1+2 )*3;

// good
var a = (1 + 2) * 3;

// no space before '(', one space before '{', one space between function parameters
var doSomething = function(a, b, c) {
    // do something
};

// no space before '('
doSomething(item);

// not good
for(i=0;i<6;i++){
    x++;
}

// good
for (i = 0; i < 6; i++) {
    x++;
}
```

### <h3 id="js-blank-line">空行</h3>

以下几种情况需要空行：

- 变量声明后（当变量声明在代码块的最后一行时，则无需空行）
- 注释前（当注释在代码块的第一行时，则无需空行）
- 代码块后（在函数调用、数组、对象中则无需空行）
- 文件最后保留一个空行

```javascript
// need blank line after variable declaration
var x = 1;

// not need blank line when variable declaration is last expression in the current block
if (x >= 1) {
    var y = x + 1;
}

var a = 2;

// need blank line before line comment
a++;

function b() {
    // not need blank line when comment is first line of block
    return a;
}

// need blank line after blocks
for (var i = 0; i < 2; i++) {
    if (true) {
        return false;
    }

    continue;
}

var obj = {
    foo: function() {
        return 1;
    },

    bar: function() {
        return 2;
    }
};

// not need blank line when in argument list, array, object
func(
    2,
    function() {
        a++;
    },
    3
);

var foo = [
    2,
    function() {
        a++;
    },
    3
];


var foo = {
    a: 2,
    b: function() {
        a++;
    },
    c: 3
};
```

### <h3 id="js-new-line">换行</h3>

换行的地方，行末必须有','或者运算符；

以下几种情况不需要换行：

- 下列关键字后：`else`,`catch`,`finally`
- 代码块'{'前

以下几种情况需要换行：

- 代码块'{'后和'}'前
- 变量赋值后

```javascript
// not good
var a = {
    b: 1
    , c: 2
};

x = y
    ? 1 : 2;

// good
var a = {
    b: 1,
    c: 2
};

x = y ? 1 : 2;
x = y ?
    1 : 2;

// no need line break with 'else', 'catch', 'finally'
if (condition) {
    ...
} else {
    ...
}

try {
    ...
} catch (e) {
    ...
} finally {
    ...
}

// not good
function test()
{
    ...
}

// good
function test() {
    ...
}

// not good
var a, foo = 7, b,
    c, bar = 8;

// good
var a,
    foo = 7,
    b, c, bar = 8;
```

### <h3 id="js-comments-single-line">单行注释</h3>

双斜线后，必须跟一个空格；

缩进与下一行代码保持一致；

可位于一个代码行的末尾，与代码间隔一个空格。

```javascript
if (condition) {
    // if you made it here, then all security checks passed
    allowed();
}

var zhangsan = 'zhangsan'; // one space after code
```

### <h3 id="js-comments-multiline">多行注释</h3>

最少三行, '*'后跟一个空格，具体参照右边的写法；

建议在以下情况下使用：

- 难于理解的代码段
- 可能存在错误的代码段
- 浏览器特殊的HACK代码
- 业务逻辑强相关的代码

```javascript
/*
 * one space after '*'
 */
var x = 1;
```

### <h3 id="js-comments-documentation">文档注释</h3>

各类标签@param, @method等请参考[usejsdoc](http://usejsdoc.org/)和[JSDoc Guide](http://yuri4ever.github.io/jsdoc/)；

建议在以下情况下使用：

- 所有常量
- 所有函数
- 所有类

```javascript
/**
 * @func
 * @desc 一个带参数的函数
 * @param {string} a - 参数a
 * @param {number} b=1 - 参数b默认值为1
 * @param {string} c=1 - 参数c有两种支持的取值</br>1—表示x</br>2—表示xx
 * @param {object} d - 参数d为一个对象
 * @param {string} d.e - 参数d的e属性
 * @param {string} d.f - 参数d的f属性
 * @param {object[]} g - 参数g为一个对象数组
 * @param {string} g.h - 参数g数组中一项的h属性
 * @param {string} g.i - 参数g数组中一项的i属性
 * @param {string} [j] - 参数j是一个可选参数
 */
function foo(a, b, c, d, g, j) {
    ...
}
```

### <h3 id="js-quote-marks">引号</h3>

最外层统一使用单引号。

```javascript
// not good
var x = "test";

// good
var y = 'foo',
    z = '<div id="test"></div>';
```

### <h3 id="js-variable-naming">变量命名

- 标准变量采用驼峰式命名（除了对象的属性外，主要是考虑到cgi返回的数据）
- 见名知意,用词准确，不用拼单和拼音首字母，英文除常用缩写词如URL、TCP外，尽量不用缩写
- 常量常量全大写，用下划线连接，使用 UPPER_CASE_WITH_UNDERLINE 规则
- 变量使用 lowerCamelCase 规则
- 'ID'在变量名中全大写
- 'URL'在变量名中全大写
- 'Android'在变量名中大写第一个字母
- 'iOS'在变量名中小写第一个，大写后两个字母
- 构造函数，大写第一个字母
- jquery对象必须以'$'开头命名

```javascript
var thisIsMyName;

var goodID;

var reportURL;

var AndroidVersion;

var iOSVersion;

var MAX_COUNT = 10;

function Person(name) {
    this.name = name;
}

// not good
var body = $('body');

// good
var $body = $('body');
```

### <h3 id="js-variable-declaration">变量声明</h3>

一个函数作用域中所有的变量声明尽量提到函数首部，用一个var声明，不允许出现两个连续的var声明。

```javascript
function doSomethingWithItems(items) {
    // use one var
    var value = 10,
        result = value + 10,
        i,
        len;

    for (i = 0, len = items.length; i < len; i++) {
        result += 10;
    }
}
```

### <h3 id="js-function">函数</h3>

无论是函数声明还是函数表达式，'('前不要空格，但'{'前一定要有空格；

函数调用括号前不需要空格；

立即执行函数外必须包一层括号；

不要给inline function命名；

参数之间用', '分隔，注意逗号后有一个空格。

```javascript
// no space before '(', but one space before'{'
var doSomething = function(item) {
    // do something
};

function doSomething(item) {
    // do something
}

// not good
doSomething (item);

// good
doSomething(item);

// requires parentheses around immediately invoked function expressions
(function() {
    return 1;
})();

// not good
[1, 2].forEach(function x() {
    ...
});

// good
[1, 2].forEach(function() {
    ...
});

// not good
var a = [1, 2, function a() {
    ...
}];

// good
var a = [1, 2, function() {
    ...
}];

// use ', ' between function parameters
var doSomething = function(a, b, c) {
    // do something
};
```

### <h3 id="js-array-object">数组、对象</h3>

对象属性名不需要加引号；

对象以缩进的形式书写，不要写在一行；

数组、对象最后不要有逗号。

单行定义的数组值间需在逗号后面带一个空格

单行定义的中括号内侧需各带一个空格

单行定义的对象值间需在逗号后面带一个空格

单行定义的大括号内侧需各带一个空格

冒号左侧不需要带空格，右侧带一个空格

```javascript
// not good
var a = {
    'b': 1
};

var a = {b: 1};

var a = {
    b: 1,
    c: 2,
};

// good
var a = {
    b: 1,
    c: 2
};

let array1 = [ 1, 2, 3, 4 ];
let array2 = [
  'Hello',
  'World!'
];

let obj1 = { key1: 'value1', key2: 'value2', key3: 'value3' };
let obj2 = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3'
};
```

### <h3 id="js-brace">括号</h3>

下列关键字后必须有大括号（即使代码块的内容只有一行）：`if`,`else`,`for`,`while`,`do`,`switch`,`try`,`catch`,`finally`,`with`。

```javascript
// not good
if (condition)
    doSomething();

// good
if (condition) {
    doSomething();
}
```

### <h3 id="js-literal-value-null">null</h3>

适用场景：

- 初始化一个将来可能被赋值为对象的变量
- 与已经初始化的变量做比较
- 作为一个参数为对象的函数的调用传参
- 作为一个返回对象的函数的返回值

不适用场景：

- 不要用null来判断函数调用时有无传参
- 不要与未初始化的变量做比较

```javascript
// not good
function test(a, b) {
    if (b === null) {
        // not mean b is not supply
        ...
    }
}

var a;

if (a === null) {
    ...
}

// good
var a = null;

if (a === null) {
    ...
}
```

### <h3 id="js-literal-value-undefined">undefined</h3>

永远不要直接使用undefined进行变量判断；

使用typeof和字符串'undefined'对变量进行判断。

```javascript
// not good
if (person === undefined) {
    ...
}

// good
if (typeof person === 'undefined') {
    ...
}
```

### <h3 id="js-jshint">jshint</h3>

用'===', '!=='代替'==', '!='；

for-in里一定要有hasOwnProperty的判断；

不要在内置对象的原型上添加方法，如Array, Date；

不要在内层作用域的代码里声明了变量，之后却访问到了外层作用域的同名变量；

变量不要先使用后声明；

不要在一句代码中单单使用构造函数，记得将其赋值给某个变量；

不要在同个作用域下声明同名变量；

不要在一些不需要的地方加括号，例：delete(a.b)；

不要使用未声明的变量（全局变量需要加到.jshintrc文件的globals属性里面）；

不要声明了变量却不使用；

不要在应该做比较的地方做赋值；

debugger不要出现在提交的代码里；

数组中不要存在空元素；

不要在循环内部声明函数；

不要像这样使用构造函数，例：`new function () { ... }`,`new Object`；

```javascript
// not good
if (a == 1) {
    a++;
}

// good
if (a === 1) {
    a++;
}

// good
for (key in obj) {
    if (obj.hasOwnProperty(key)) {
        // be sure that obj[key] belongs to the object and was not inherited
        console.log(obj[key]);
    }
}

// not good
Array.prototype.count = function(value) {
    return 4;
};

// not good
var x = 1;

function test() {
    if (true) {
        var x = 0;
    }

    x += 1;
}

// not good
function test() {
    console.log(x);

    var x = 1;
}

// not good
new Person();

// good
var person = new Person();

// not good
delete(obj.attr);

// good
delete obj.attr;

// not good
if (a = 10) {
    a++;
}

// not good
var a = [1, , , 2, 3];

// not good
var nums = [];

for (var i = 0; i < 10; i++) {
    (function(i) {
        nums[i] = function(j) {
            return i + j;
        };
    }(i));
}

// not good
var singleton = new function() {
    var privateVar;

    this.publicMethod = function() {
        privateVar = 1;
    };

    this.publicMethod2 = function() {
        privateVar = 2;
    };
};
```

### <h3 id="js-miscellaneous">杂项</h3>

不要混用tab和space；

不要在一处使用多个tab或space；

换行符统一用'LF'；

对上下文this的引用只能使用'_this', 'that', 'self'其中一个来命名；

行尾不要有空白字符；

switch的falling through和no default的情况一定要有注释特别说明；

不允许有空的代码块。

```javascript
// not good
var a   = 1;

function Person() {
    // not good
    var me = this;

    // good
    var _this = this;

    // good
    var that = this;

    // good
    var self = this;
}

// good
switch (condition) {
    case 1:
    case 2:
        ...
        break;
    case 3:
        ...
    // why fall through
    case 4
        ...
        break;
    // why no default
}

// not good with empty block
if (condition) {

}
```

## <h2 id="check">编辑器配置和构建检查</h2>

### <h3 id="check-sublime3">sublime3插件</h3>

1. 安装node包

   - jscs`npm install jscs -g`
   - jshint`npm install jshint -g`
   - csscomb`npm install csscomb -g`
   - csslint`npm install csslint -g`

2. 安装gem包

   - scss-lint`gem install scss_lint`

3. 安装sublime3 [Package Control](https://packagecontrol.io/installation#st3)

   - 按下``ctrl+` ``
   - 复制粘贴以下代码`import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)`

4. 安装sublime3插件

   - 按下`ctrl+shift+p`，输入'ip'（Install Package）

   - 输入以下插件的名字，按顺序逐个进行安装：

     - `EditorConfig`
     - `Sass`
     - `SublimeLinter`
     - `SublimeLinter-jscs`
     - `SublimeLinter-jshint`
     - `SublimeLinter-csslint`
     - `SublimeLinter-contrib-scss-lint`
     - `JSFormat`
     - `CSScomb`

5. 插件的配置文件

   将以下配置文件分别下载后放入项目根目录下：

   - `EditorConfig`[配置文件](.editorconfig)

   - `JSCS`[配置文件](.jscsrc)

   - `JSHint`[配置文件](.jshintrc)

     注意：全局变量需要手动加到配置文件的globals属性里，例：

     ```json
     {
         "globals": {
             "ImageHandle": true
         }
     }
     ```

   - `CSSLint`[配置文件](.csslintrc)

   - `SCSS-Lint`[配置文件](.scss-lint.yml)

6. 编辑器及插件设置

   - `sublime3`自身

     Preferences->Setting-User，增加下面两个配置：

     ```json
     {
         "translate_tabs_to_spaces": true,
         "word_wrap": true
     }
     ```

     点击右下角的Spaces->Convert Indentation to Spaces可以将文件中的所有tab转换成空格

   - `JSFormat`

     Preferences->Package Settings->JSFormat->Setting-User，下载[配置文件](jsformat_setting_user.json)覆盖

     配置好后格式化的默认快捷键是`ctrl+alt+f`

   - `SublimeLinter`

     右键->SublimeLinter->Lint Mode，有4种检查模式，建议选择`Load/save`

     右键->SublimeLinter->Mark Style，建议选择`Outline`

     右键->SublimeLinter->Choose Gutter Theme，建议选择`Blueberry-round`

     右键->SublimeLinter->Open User Settings，将linter里面jscs的args改成`["--verbose"]`，将linter里面csslint的ignore改成`"box-model,adjoining-classes,box-sizing,compatible-vendor-prefixes,gradients,text-indent,fallback-colors,star-property-hack,underscore-property-hack,bulletproof-font-face,font-faces,import,regex-selectors,universal-selector,unqualified-attributes,overqualified-elements,duplicate-background-images,floats,font-sizes,ids,important,outline-none,qualified-headings,unique-headings"`

     当光标处于有错误的代码行时，详细的错误信息会显示在下面的状态栏中

     右键->SublimeLinter可以看到所有的快捷键，其中`ctrl+k, a`可以列出所有错误

   - `CSScomb`

     Preferences->Package Settings->CSScomb->Setting-User，下载[配置文件](csscomb_setting_user.json)覆盖

     配置好后格式化的默认快捷键是`ctrl+shift+c`

### <h3 id="check-grunt">grunt插件</h3>

1. 在项目中安装grunt插件

   - jscs`npm install grunt-jscs --save-dev`
   - jshint`npm install grunt-contrib-jshint --save-dev`
   - csslint`npm install grunt-contrib-csslint --save-dev`
   - scss-lint`npm install grunt-scss-lint --save-dev`

2. 插件的配置文件

   - `JSCS`

     ```javascript
     {
         options: {
             config: true,
             verbose: true
         },
         files: {
             src: [...]
         }
     }
     ```

   - `JSHint`

     ```json
         options: {
             jshintrc: true
         },
         files: {
             src: [...]
         }
     }
     ```

   - `CSSLint`

     ```json
     {
         options: {
             csslintrc: '.csslintrc'
         },
         files: {
             src: [...]
         }
     }
     ```

   - `SCSS-Lint`

     ```json
         options: {
             config: '.scss-lint.yml'
         },
         files: {
             src: [...]
         }
     }
     ```

### 

## <h2 id="react">react核心代码规范及要求</h2>

### <h3 id="react-requirements">一、基本原则（Basic Rules）</h3>

1. 语法上根据生命周期方法执行的顺序编写代码

   （1 生命周期方法［`getDefaultProps`, `getInitialState`, `componentWillMount`, `componentDidMount`,`componentWillReceiveProps`, `shouldComponentUpdate`, `componentWillUpdate`, `componentDidUpdate`,`componentWillUnmount］`

   （2 其他的私有方法

   （3 render()方法

2. 事件处理函数的命名: “handle+EventName”

3. 组件验证

react 组件都应该完成 `propTypes` 验证。每一个 `this.props` 的属性都应该有一个与之对应的`propTypes`。

避免使用这些没有描述意义的 prop-types:

- React.PropTypes.any

- React.PropTypes.array

- React.PropTypes.object

最好使用：

- React.PropTypes.arrayOf

- React.PropTypes.objectOf

- React.PropTypes.instanceOf

- React.PropTypes.shape

4、能用 `props` 就不要用 `state`，这一定程度上可以减少应用程序的复杂度

5、尽量少用jQuery去操作DOM（有必要的话，把jquery插件包装在React组件中）

6、尽量不用例如backbone的模型，可以直接使用 `flux action`，或者 `$.ajax` 来代替。

7、每个文件中只包含一个 React 组件。

8、尽可能地使用JSX语法。

9、除非不用JSX语法创建一个应用，否则不要使用`React.createElement`方法。

### <h3 id="react-base-guide">二、基础规范</h3>

1. 统一全部采用 Es6  

2. 每个文件只包含的一个 React 组件（联系紧密的组件可以使用「命名空间的形式」）。  

3. 始终使用 JSX 语法，不要使用 `React.createElement` 创建 ReactElement，以提高编写速度、可读性、可维护性（没有 JSX 转换的特殊场景例外，如在 `console` 中测试组件）。  

### <h3 id="react-naming-rule">三、命名规范</h3>

- **扩展名**：使用 .js 作为 React 组件的扩展名；  
- **文件名**：使用大驼峰，如 MyComponent.js；  
- **组件命名**：组件名称和文件名一致，如 MyComponent.js 里的组件名应该是 MyComponent；一个目录的根组件使用 index.js 命名，以目录名称作为组件名称；  

```javascript
    // file contents
    const CheckBox = React.createClass({
      // ...
    })

    module.exports = CheckBox;

    // in some other file
    // bad
    const CheckBox = require('./checkBox');

    // bad
    const CheckBox = require('./check_box');

    // good
    const CheckBox = require('./CheckBox');
```

- **引用命名**：React 组件使用大驼峰命名法，HTML 标签、组件实例使用小驼峰命名法；  

```javascript
// bad
const Footer = require('./Footer/Footer.js') 
// bad
const Footer = require('./Footer/index.js') 
// good
const Footer = require('./Footer')
```

- **属性命名**  

1. React 组件的属性使用**小驼峰命名法**；  
2. 使用 `className` 代替 `class` 属性；  
3. 使用 `htmlFor` 代替 `for` 属性。  

- **传递给 HTML 的属性：**  

1. 传递给 HTML 元素的自定义属性，需要添加 `data-` 前缀，React 不会渲染非标准属性；  
2. [无障碍](http://www.w3.org/WAI/intro/aria) 属性 `aria-` 可以正常使用。  

- **属性设置** 
  1. 在组件行内设置属性（以便 `propTypes` 校验），不要在外部改变属性的值；  
  2. 属性较多使用 `{...this.props}` 语法；  
  3. 重复设置属性值时，前面的值会被后面的覆盖。  

```javascript
    var component = <Component />;
    component.props.foo = x; // bad
    component.props.bar = y; // also bad

    // good
    var component = <Component foo={x} bar={y} />;

    // good
    var props = {};
    props.foo = x;
    props.bar = y;
    var component = <Component {...props} />;

    var props = { foo: 'default' };
    var component = <Component {...props} foo={'override'} />;
    console.log(component.props.foo); // 'override'
```

- **属性对齐方式**

1. 属性较少时可以行内排列；  
2. 属性较多时每行一个属性，闭合标签单独成行

```javascript
    // bad - too long
    <input type="text" value={this.state.newDinosaurName} onChange={this.inputHandler.bind(this, 'newDinosaurName')} />  

    // bad - aligning attributes after the tag
    <input type="text"  
           value={this.state.newDinosaurName}
           onChange={this.inputHandler.bind(this, 'newDinosaurName')} /> 

    // good
    <input  
      type="text"
      value={this.state.newDinosaurName}
      onChange={this.inputHandler.bind(this, 'newDinosaurName')}
     />

     // if props fit in one line then keep it on the same line
    <Foo bar="bar" />

    // children get indented normally
    <Foo
      superLongParam="bar"
      anotherSuperLongParam="baz"
    >
      <Spazz />
    </Foo>


    // bad
    <Foo
      bar="bar"
      baz="baz" />

    // good
    <Foo
      bar="bar"
      baz="baz"
    />
```

- **带命名空间的组件**  

如果一个组件有许多关联子组件，可以以该组件作为命名空间编写、调用子组件。

```javascript
var MyFormComponent = React.createClass({ ... });
    MyFormComponent.Row = React.createClass({ ... });
    MyFormComponent.Label = React.createClass({ ... }); 
    MyFormComponent.Input = React.createClass({ ... });

    var Form = MyFormComponent;

    var App = (

    );
```

### <h3 id="react-component-standard">四、组件相关规范</h3>

### 组建声明

```javascript
    // bad 
    export default React.createClass({ 
        displayName: 'ReservationCard', // stuff goes here 
    });

    // good 
    const ReservationCard = React.createClass({ 
        // stuff goes here
    });

    export default ReservationCard;
```

### 行内迭代

运算逻辑简单的直接使用行内迭代。

```javascript
    return (
      <div>
        {this.props.data.map(function(data, i) {
          return (<Component data={data} key={i} />)
        })}
        </div>
    );
```

### 注释

组建之间的注释需要用'{}'包裹

```javascript
   var content = (
      <Nav>
        {/* child comment, put {} around */}
        <Person
          /* multi
             line
             comment */
          name={window.isLoggedIn ? window.name : ''} // end of line comment
        />
      </Nav>
    );
```

### 引号使用

1.HTML/JSX 属性使用双引号`"`

2.JS 使用单 `'`

```jsx
// bad
<Foo bar='bar' />
// good
<Foo bar="bar" />

// bad
<Foo style={{ left: "20px" }} />

// good
<Foo style={{ left: '20px' }} />

// JavaScript Expression
const person = <Person name={window.isLoggedIn ? window.name : ''} />;

// HTML/JSX
const myDivElement = <div className="foo" />;
const app = <Nav color="blue" />;
const content = ( <Container> {window.isLoggedIn ? <Nav /> : <Login />} </Container>
);
```

### 条件 HTML

1. 简短的输出在行内直接三元运算符；

   ```jsx
   {this.state.show && 'This is Shown'}
   {this.state.on ? 'On' : 'Off'}
   ```

2. 较复杂的结构可以在`.render()` 方法内定义一个以 `Html` 结尾的变量。

   ```jsx
       var dinosaurHtml = ''; 
       if (this.state.showDinosaurs) {  
         dinosaurHtml = (
           <section>
             <DinosaurTable />
             <DinosaurPager />
           </section>
         );
       }
   
       return (  
         <div>
           ...
           {dinosaurHtml}
           ...
         </div>
       );
   ```

### 小括号`()` 的使用

1. 多行的 JSX 使用 `()` 包裹，有组件嵌套时使用多行模式；

   ```jsx
   // bad
    return (<div><ComponentOne /><ComponentTwo /></div>);
   // good
   var multilineJsx = (  
     <header>
       <Logo />
       <Nav />
     </header>
   );
   
   // good
   return (
     <div>
       <ComponentOne />
       <ComponentTwo />
     </div>
   );
   ```
2. 单行 JSX 省略 `()`

   ```jsx
   var singleLineJsx = <h1>Simple JSX</h1>;
   // good, when single line
   render() {
     const body = <div>hello</div>;
     return <MyComponent>{body}</MyComponent>;
   }
   ```

### 自闭合标签

1. JSX 中所有标签**必须闭合**；  
   - 没有子元素的组件使用自闭合语法，自闭合标签 **`/` 前留一个空格**。

```jsx
// bad
 <Logo></Logo>
 <Logo/>
 // very bad
<Foo                 />

// bad
<Foo />

// good
<Logo />
```

### **组件内部代码组织**

1. **不要使用下划线前缀**命名 React 组件的方法；  

```jsx
 // bad
    React.createClass({
      _onClickSubmit() {
        // do stuff
      }

      // other stuff
    });

    // good
    React.createClass({
      onClickSubmit() {
        // do stuff
      }

      // other stuff
    });
```

2. 按照生命周期组顺序织组件的方法、属性；  
   - 方法（属性）之间空一行；  

   - `.render()` 方法始终放在最后；  

   - 自定义方法 React API 方法之后、`.render()` 之前。

     顺序：继承 React.Component 的类的方法遵循下面的顺序

     1.constructor  

     2.optional static methods

     3.getChildContext

     4.componentWillMount

     5.componentDidMount  

     6.componentWillReceiveProps

     7.shouldComponentUpdate

     8.componentWillUpdate

     9.componentDidUpdate

     10.componentWillUnmount

     11.clickHandlers or eventHandlers like onClickSubmit() or onChangeDescription()

     12.getter methods for render like getSelectReason() or getFooterContent()

     13.Optional render methods like renderNavigation() or renderProfilePicture()

     14.render

```jsx
    // React 组件中按照以下顺序组织代码
    React.createClass({  
      displayName: '',

      mixins: [],

      statics: {},

      propTypes: {},

      getDefaultProps() {
        // ...
      },

      getInitialState() {
        // do something
      },

      componentWillMount() {
          // do something
      },

      componentDidMount() {
        // do something: add DOM event listener, etc.
      },

      componentWillReceiveProps() {
      },

      shouldComponentUpdate() {},

      componentWillUpdate() {},

      componentDidUpdate() {},

      componentWillUnmount() {
          // do something: remove DOM event listener. etc.
      },

      // clickHandlers or eventHandlers like onClickSubmit() or onChangeDescription()
      handleClick() {
        // ...
      },

      // getter methods for render like getSelectReason() or getFooterContent()

      // Optional render methods like renderNavigation() or renderProfilePicture()

      render() {
        // ...
      }
    });
```

- 定义 propTypes，defaultProps，contextTypes 等等…

```jsx
import React, { PropTypes } from 'react';

const propTypes = {
  id: PropTypes.number.isRequired,
  url: PropTypes.string.isRequired,
  text: PropTypes.string,
};

const defaultProps = {
  text: 'Hello World',
};

class Link extends React.Component {
  static methodsAreOk() {
    return true;
  }

  render() {
    return <a href={this.props.url} data-id={this.props.id}>{this.props.text}</a>
  }
}

Link.propTypes = propTypes;
Link.defaultProps = defaultProps;

export default Link;
```

使用 React.createClass 时，方法顺序如下：

1.displayName
2.propTypes
3.contextTypes
4.childContextTypes
5.mixins

6.statics 
7.defaultProps 
8.getDefaultProps
9.getInitialState
10.getChildContext
11.componentWillMount
12.componentDidMount
13.componentWillReceiveProps
14.shouldComponentUpdate
15.componentWillUpdate
16.componentDidUpdate
17.componentWillUnmount

18.clickHandlers or eventHandlers like onClickSubmit() or onChangeDescription()
19.getter methods for render like getSelectReason() or getFooterContent()
20.Optional render methods like renderNavigation() or renderProfilePicture()
21.render

## <h3 id="react-agreements">五、约定</h3>

### **注释**

文件头部注释  

```jsx
/* ------------------------------------------------------------
 author : cattleya
 create:2016-12-30
 descreption:recharge 相关样式（包含input/label/button）
 ------------------------------------------------------------ */
```

注：尽量避免使用多行注释 `/* */`,应使用多个单行注释  `//`  

函数注释，可使用块级注释  

```jsx

/* *函数注释
*@ param {string} p1 参数1的说明
*@ param {string} p2 参数2的说明，比较长
*@ return 返回值描述 */ aa() => {
    alert();
}
```

**条件(三元)操作符 (?:)**  

三元操作符用于替代 if 条件判断语句。  

```jsx
// bad
if (val != 0) { return foo();
} else { return bar();
} 

// good
return val ? foo() : bar();
```

## <h3 id="react-css">六、react 中 CSS使用的相关规范</h3>

### **代码组织**

**Class 和 ID**  

- 使用语义化、通用的命名方式（不能使用汉语拼音）；  
- 使用连字符 作为 ID、Class 名称界定符，不要驼峰命名法和下划线；  
- 避免选择器嵌套层级过多，尽量少于 3 级；  
- 避免选择器和 Class、ID 叠加使用；  

```css
    /* Not recommended */
    .red {}
    .box_green {}
    .page .header .login #username input {}
    ul#example {}

    /* Recommended */
    #nav {}
    .box-video {}
    #username input {}
    #example {}
```

/* Not recommended */
    .red {}
    .box_green {}
    .page .header .login #username input {}
    ul#example {}

**声明块格式**  

- 选择器分组时，保持独立的选择器占用一行；  
- 有多个选择器公用同一css代码块时，选择器应以逗号分隔，并换行  
- 声明块的左括号 { 前添加一个空格；  
- 声明块的右括号 } 应单独成行；  
- 声明语句中的 ` : ` 后应添加一个空格；  
- 声明语句应以分号 ` ;`  结尾；  
- 一般以逗号分隔的属性值，每个逗号后应添加一个空格；  
- 对于属性值或颜色参数，省略小数前面的 0 （例如，.5 代替 0.5；-.5px 代替 -0.5px）；  
- 十六进制值应该全部小写和尽量简写，例如，#fff 代替 #ffffff；  
- 避免为 0 值指定单位，例如，用 margin: 0; 代替 margin: 0px;；  

```css
/* Not recommended */ 
.selector, .selector-secondary, .selector[type=text] {
 padding:15px;
 margin:0px 0px 15px;
 background-color:rgba(0, 0, 0, 0.5);
 box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
 }

 .m-userlist .list { position: relative; height: 100px;overflow: hidden} 

 /* Recommended */ 
 .selector,
.selector-secondary,
.selector[type="text"] {
  padding: 15px;
  margin-bottom: 15px;
  background-color: rgba(0,0,0,.5);
  box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
}
```

**hack**  

能不使用`hack`尽量不要使用，如果必须使用，请将`hack`加在属性上  
如  

```css
.head{  
 *height: 200px
}
```

**媒体查询（Media query）的位置**  

将媒体查询放在尽可能相关规则的附近。不要将他们打包放在一个单一样式文件中或者放在文档底部。如果你把他们分开了，将来只会被大家遗忘。  

```css
    .element { ... }
    .element-avatar { ... }
    .element-selected { ... }

    @media (max-width: 768px) {
      .element { ...}
      .element-avatar { ... }
      .element-selected { ... }
    }
```

**引号使用**  

url() 、属性选择符、属性值使用双引号。 参考[ Is quoting the value of url() really necessary?](http://stackoverflow.com/questions/2168855/is-quoting-the-value-of-url-really-necessary)  

```css
/* Not recommended */ 
html { 
    font-family: 'open sans', arial, sans-serif;
 }
/* Recommended */ 
html { 
    font-family: "open sans", arial, sans-serif;
} 

.selector[type="text"] {

}
```

**不要使用 @import**  

与 <link> 相比，@import 要慢很多，不光增加额外的请求数，还会导致不可预料的问题。  

替代办法：  

使用多个 元素；
通过 Sass 或 Less 类似的 CSS 预处理器将多个 CSS 文件编译为一个文件；
其他 CSS 文件合并工具；

**注释**  

不同模块的内容，在头部、媒体公告添加模块名称等  

如果下为头部、媒体公告css  

```css
/* 头部模块
 ============================================================================*/ 
/* 媒体公告模块
 ============================================================================*/ 
.m-userlist {
  /* 属性声明 */ 
  margin: 0 0 30px;
  /* 属性名:属性值; */
}

/* 左侧部分 */ 
.m-userlist .list { 
    position: relative; 
    height: 100px; 
    overflow: hidden;
}

/* 右侧部分 */ 
.m-userlist .list { 
    position: relative; 
    height: 100px; 
    overflow: hidden;
}
```

### CSS渲染性能优化，避免过分重排

当发生重排的时候，浏览器需要重新计算布局位置与大小，前端工程师要明白「浏览器渲染」[更多详情](http://www.jianshu.com/p/e305ace24ddf)。  

常见的重排元素:  

- width  
- height  
- padding  
- margin  
- display  
- border-width  
- position  
- top  
- left  
- right  
- bottom  
- font-size  
- float  
- text-align  
- overflow-y  
- font-weight  
- overflow  
- font-family  
- line-height  
- vertical-align  
- clear  
- white-space  
- min-height  

**正确使用 Display 的属性**  

- Display 属性会影响页面的渲染，请合理使用。  
- display: inline后不应该再使用 width、height、margin、padding 以及 float；  
- display: inline-block 后不应该再使用 float；  
- display: block 后不应该再使用 vertical-align；  
- display: table-* 后不应该再使用 margin 或者 float；  

  **不滥用 Float**

Float在渲染时计算量比较大，尽量减少使用。  

### <h3 id="react-eslint">七、代码校验工具</h3>

- [ESLint](https://www.github.com/eslint/eslint)  
- [ESLint React Plugin](https://github.com/yannickcr/eslint-plugin-react)

  根据 ESLIST 后面给出详细的配置示例：

  /* TODO */
