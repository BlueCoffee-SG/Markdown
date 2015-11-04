
# [Marked](http://marked2app.com/)

## Folding Text 调起 Marked 2
通过脚本 [OpenFTDocinMarked.applescript][] 调起 Marked 2 渲染预览 Markdown。  
当在 Folding Text 中修改 Markdown 文档时，Marked 2 会实时检测刷新。

![FoldingText_Marked2](FoldingText/FoldingText_Marked2.png)

## Preferences
### General

- Window
	- [x] Raise window on update

- Status bar
	- [x] Show Style picker

### Preview
1. Preview behavior:
	- [x] Scroll to first edit：定位到编辑器当前修改点
		- [x] Show Edit Marker：显示红色的修改点标记符
	- [x] Enable Mini Map Navigation：Minimap 预览全文，支持导航。
	- [x] Headlines collapse sections：点击标题可以折叠。
2. Additional features: 
	- [x] Show scroll progress indicator
	- [x] Enable link popovers

### Apps
Text Editor：选择 FoldingText

- [x] Edit new files automatically
	当 Marked 2 新建文件时，将自动打开External Editor(FoldingText)进行编辑。

## Preview
### Preview_Nav

![1-Preview_Nav](marked/1-Preview_Nav.png)

### TOC_Nav

![2-TOC_Nav](marked/2-TOC_Nav.png)

## <!--以下是本文的脚注和超链接-->
[OpenFTDocinMarked.applescript]: https://github.com/RobTrew/txtquery-tools/blob/master/utilities/OpenFTDocinMarked.applescript

