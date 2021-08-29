# 08/30 个人网页设计

克隆本代码仓库：`git clone https://github.com/zzy-37/0830-website-design.git`

## 准备工作

- 下载并安装版本管理软件（Version contorl system）`Git`
- 一个纯文本编辑器（notepad, vim, vscode 等）

### 下载并安装 `Git`

下载 `git`：https://git-scm.com/downloads

**windows：** 从上方地址下载并运行安装包，安装选项选择全部默认即可

**macOS：** 查看 [Download for macOS](https://git-scm.com/download/mac)

1. 通过 `homebrew` 安装：

   ```bash
   ### 安装 homebrew ###
   # 见：https://brew.sh/
   # 打开终端输入：
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   📋
   ### 安装 git ###
   brew install git
   ```

2. 使用 `xcode`

   macOS 的 `xcode` 代码编辑器已经集成了 `git`，因此无需再次安装

3. 使用安装包

   下载：https://sourceforge.net/projects/git-osx-installer/

安装完成后打开终端输入 `git --version` 确认 `git` 安装正确

> 如何打开终端：
>
> - windows: `Win+R` 输入 `cmd` 或 `powershell` 即可打开命令行
> - macOS: `Command+Space` 搜索 `terminal` 或 `终端` 并运行即可
> - Linux: 应该不用教

### 文本编辑器（本次使用 `Visual Studio Code`）

下载并安装 `VS Code`：https://code.visualstudio.com/Download

> 当然也可以根据喜好使用任意其他编辑器，如 mac 可安装上文提到的 [`xcode`](https://developer.apple.com/xcode/)  
> \*\*不建议使用 `notepad`

> 补充阅读：[文本编辑器（text editor）](https://en.wikipedia.org/wiki/Text_editor) 与 [文字处理器（word processer）](https://en.wikipedia.org/wiki/Word_processor)

## HTML

超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。  
html 文件定义了页面的框架，浏览器通过解析接收到的 html 文件从而程序网页内容

> 使用浏览器的开发者工具：`F12` 或 右键选择 `检查元素/开发者工具`

### index.html

`index.html` 是通常访问网络服务器地址时默认显示的页面

### 标签 `<tags>`

`html` 使用 `标签<tags>` 来定义文档的结构

```html
<!-- 代表注释，其中的内容不会被渲染 -->

<h1>"h1-h6"表示一级到六级标题</h1>

<p>p标签表示段落</p>

<a href="#">a标签表示链接</a>

<!-- img标签表示图片 -->
<img src="some-image.jpg" alt="discription" />

<div>div标签标识一个区块</div>

<span>span标签标识一个内联元素</span>

<html>
  html标签表示整个文档
</html>

<body>
  body标签表示文档被渲染的主体
</body>

<head>
  head标签表示文档的头部，用于链接外部内容和定义文档属性
</head>

<!-- style标签用于定义文档的样式 -->
<style>
  .classname {
    /* some styles */
  }
</style>

<!-- link 标签用于链接外部内容 -->
<link rel="type" href="path-to-file" />
```

> 标签通常成对出现，每一个标签都需要被关闭

> 在文件头部添加标签 `<meta charset="UTF-8">` 通常可以解决中文字符显示问题

> HTML 教程 | 菜鸟教程：https://www.runoob.com/html/html-tutorial.html

> 补充阅读：`Markdown`
>
> - Markdown - Wikipedia：https://en.wikipedia.org/wiki/Markdown
> - Markdown 教程 | 菜鸟教程：https://www.runoob.com/markdown/md-tutorial.html

## CSS

层叠样式表 (Cascading Style Sheets) 定义了网页中的 html 元素如何被显示。通过 html 和 css，网站就能够被完整地呈现出来。

css 样式：

```css
/* 注释 */

/* 为相应元素添加样式 */
body {
  background: white | rgb(0 150 255 / 0.8) | hsl(359deg 20% 50% / 0.6) |
    #cc80ffff; /* 元素的背景色 */
  color: black; /* 文字颜色 */
}

/* 通过在 html 文件当中定义元素的 `class` 属性，就可以为特定的元素添加样式 */
.classname {
  margin: 8px; /* 外边距 */
  padding: 1rem; /* 内边距 */
  width: 100%; /* 宽度 */
  height: 100%; /* 高度 */
  border: 2px solid black; /* 元素边框 */
}

/* 元素定位 */
.box {
  positon: relative | absolute | fixed | sticky;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

/* 图片 */
img {
  max-width: 100%;
  height: auto;
  object-fit: fill | contain | cover | none;
  aspect-ratio: 16 / 9;
}

/* flexbox */
.flexbox {
  display: flex;
  flex-direction: row | column | row-reverse | column-reverse;
  justify-content: flex-start | flex-end | center | space-around | space-between;
  align-item: flex-start | center;
}
```

> 链接：
>
> - CSS 教程 | 菜鸟教程：https://www.runoob.com/css/css-tutorial.html
> - A Complete Guide to Flexbox | CSS-Tricks: https://css-tricks.com/snippets/css/a-guide-to-flexbox/
> - object-fit - CSS: Cascading Style Sheets | MDN：https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit
