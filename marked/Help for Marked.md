<!--TOC-->

# [Marked](http://marked2app.com/)
[Marked 2 使用方法集锦：开篇](http://www.waerfa.com/marked-2-intro)  
[Marked 2 使用方法集锦：基础篇](http://www.waerfa.com/marked-2-basic-skills)

## Folding Text 调起 Marked 2
通过脚本 [OpenFTDocinMarked.applescript][] 调起 Marked 2 渲染预览 Markdown。  
当在 Folding Text 中修改保存 Markdown 文档时，Marked 2 会实时检测刷新。

![FoldingText_Marked2](../FoldingText/FoldingText_Marked2.png)

## Preferences
### General

- Window
	- [x] Raise window on update：
		当在编辑器中修改保存文档时，将会调起Marked窗口。

- Status bar
	- [x] Show Style picker

### Preview
1. Preview behavior:
	- [x] Scroll to first edit：定位到编辑器当前修改点
		- [x] Show Edit Marker：显示红色的修改点标记符
	- [x] Enable Mini Map Navigation：开启 Minimap 导航支持。
	- [x] Headlines collapse sections：点击标题可以**折叠**。
2. Additional features: 
	- [x] Show scroll progress indicator
	- [x] Enable link popovers：鼠标悬停在链接上时，显示 title。

### Apps
Text Editor：选择 FoldingText  
Open in Editor 快捷键：<kbd>⌘</kbd><kbd>e</kbd>

- [x] Edit new files automatically
	当 Marked 2 新建文件时，将自动打开 External Editor(FoldingText) 进行编辑。

## Preview
### Preview_Menu
Shortcut  |  Function                       |  Comment
----------|---------------------------------|----------------------
<kbd>⌘</kbd><kbd>r</kbd> | Refresh            | 刷新(重新加载)
<kbd>⌘</kbd><kbd>u</kbd> | Toggle Source View | 查看 HTML 源码
<kbd>⌥</kbd><kbd>⌘</kbd><kbd>i</kbd> | High Contrast | 开启夜间模式

### Preview_Nav

![1-Preview_Nav](1-Preview_Nav.png)

#### 帮助
Shortcut  |  Function                       |  Comment
----------|---------------------------------|----------------------
`h` / `?`     | Show/Hide Help HUD              | 打开/关闭帮助导航仪浮层
<kbd>⌥</kbd><kbd>⌘</kbd><kbd>k</kbd>     | 调出热键参考悬浮窗

#### 主题
默认主题（theme style）是 **Swiss**，可切换测试 ***GitHub***（<kbd>⌘</kbd><kbd>4</kbd>）主题效果。  
另外，推荐复古的 ***Antique***（<kbd>⌘</kbd><kbd>2</kbd>）和第三方主题 [**Byword**](https://github.com/EvanLovely/markdown-styles/tree/master/Byword%20for%20Marked)、[Svbtle](https://github.com/chrishunt/marked)、[Ulysses Freestraction Light](http://www.candlerblog.com/2013/04/11/ulysses-iii-and-marked/)。

在 `Preferences|Style` 的 Theme 中可选择默认主题（*Default style*）；在 *Custom Styles*  中可添加或移除自定义 CSS 样式，参考《themes4marked.md》。 

建议尝试 **`Ulysses Freestraction Dark`** 主题。

#### 导航
Shortcut  |  Function                       |  Comment
----------|---------------------------------|----------------------
`e`         | Jump to Most Recent Edit Point  | 定位到最近编辑点(**e**dit)
`,` / `.`     | Navigate All Headers            | 基于 Header 导航
`<` / `>`     | Navigate H1/H2 Headers          | 基于 H1/H2 导航
`0`         | Display Mini Map                | 打开 MiniMap 导航<br>可按下`<ESC>`关闭
`z`         | Zoom Overview toggle            | 查看缩略图

#### 滚屏
Shortcut  |  Function                       |  Comment
----------|---------------------------------|----------------------
`t` / `gg`    | Jump to top like vim            | 跳转到顶部(top)
`b` / `G`     | Jump to bottom like vim         | 跳转到底部(bottom)
`j` / `k`     | Scroll Down/Up like vim         | 上/下滚动，亦适用于MiniMap
`J` / `K`     | Scroll Down/Up Faster           | 快速上/下滚动，亦适用于MiniMap
`Space` / <kbd>⇧</kbd>`Space`  | Page Down/Up   | 下/上翻页
`s`         | Auto-Scroll                     | 自动滚屏
<kbd>⇧</kbd><kbd>→</kbd>/<kbd>⇧</kbd><kbd>←</kbd> | Speed up/Slow down auto-scroll | 加速/减速自动滚屏

### TOC
#### [Insert TOC at head](http://marked2app.com/help/Special_Syntax.html)
在文中（开头）插入 `<!--TOC-->`，通过 Marked2 渲染插入目录（Table Of Contents）。  
如果文中多次插入 ` <!--TOC-->`，仅以第一个有效。  

在 TOC 后插入 `max#`(#∈{1,2,3,4,5}) 可指定目录显示的级别深度（nested heirarchy）,例如 `<!--TOC max3-->` 表示插入最深3级目录。  
这个有点类似 SublimeText 的 [MarkdownTOC](https://packagecontrol.io/packages/MarkdownTOC) 插件语法。

#### Floating TOC Navigator
![2-TOC_Nav](2-TOC_Nav.png)

Shortcut  |  Function                       |  Comment
----------|---------------------------------|----------------------
<kbd>⌘</kbd><kbd>t</kbd> | Open TOC              | 打开/关闭文档结构图<br>也可按下`<ESC>`关闭
`f` / `Space` | Open TOC quick-search           | 打开TOC搜索栏
`j` / `⬇️`    | Select next item                | 向下移动
`k` / `⬆️`    | Select previous item            | 向上移动
`o`         | Scroll to selection item        | 跳转到当前选中章节

## <!--以下是本文的脚注和超链接-->
[OpenFTDocinMarked.applescript]: https://github.com/RobTrew/txtquery-tools/blob/master/utilities/OpenFTDocinMarked.applescript

