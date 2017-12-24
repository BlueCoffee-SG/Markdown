# 代码块（Code Blocks）
## Preformatted Code Block
如果要插入跨行片段或块，且要保持排版样式（包括空格、换行符和缩进），可使用预格式化引用语法格式。对应 HTML 中的 `<pre>` 标签。

在句段的行首插入1个tab 或 4个空格，则表示代码块。

## Fenced Code Block
如果要支持编程语言语法高亮，则可以使用 GFM 扩展的基于 [YAML](http://yaml.org/) 标记语言的 Fenced Code Block 引用语法格式。

在句段行首三个反引号后添加 YAML 语言标识，段落行末用三个反引号换行闭包即可。

### GitHub
[Writing on GitHub](https://help.github.com/categories/writing-on-github) / [Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

> We use [Linguist](https://github.com/github/linguist) to perform language detection and syntax highlighting. You can find out which keywords are valid in [the languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

### FoldingText
以下为 FoldingText 显式支持的语言标签：

- [x] xml  
- [x] yaml  
- [x] json  
- [x] sql  
- [x] markdown  
- [x] c  
- [ ]  C++（`cpp`）  
- [ ] Objective-C（`obj-c`、`objc`、`objectivec`）  
- [ ] Swift  
- [x] csharp   
- [x] java  
- [x] go  
- [x] scala  
- [x] erlang  
- [x] r  
- [x] html  
- [x] css  
- [x] javascript  
- [x] ecmascript  
- [x] typescript  
- [x] coffeescript  
- [x] php  
- [x] ruby  
- [x] perl  
- [x] python  
- [x] shell  
- [ ] log  

### marked2app
[Fenced Code Blocks](http://marked2app.com/help/Fenced_Code_Blocks.html)

> The built in syntax highlighting will recognize **41+** different language specifiers. If there is no language specified, it will detect it automatically, so it’s not required for the preview. The language string given will be output in the final html as a class on the `<code>` tag.