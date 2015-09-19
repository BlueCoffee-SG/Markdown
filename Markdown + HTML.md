[PHILOSOPHY of Markdown](http://daringfireball.net/projects/markdown/syntax#philosophy)
===
___
Markdown is not a replacement for HTML, or even close to it. Its syntax is very small, corresponding only to a very <mark>small subset of HTML tags</mark>. The idea is not to create a syntax that makes it easier to insert HTML tags. In my opinion, HTML tags are already easy to insert. The idea for Markdown is to make it easy to read, write, and edit prose. <u>HTML is a <em><b>publishing</b></em> format; Markdown is a <em><b>writing</b></em> format.</u> Thus, Markdown’s formatting syntax only addresses issues that can be conveyed in <big><i>plain text</i></big>.  

For any markup that is not covered by Markdown’s syntax, <u>you simply use HTML itself</u>. There’s no need to preface it or delimit it to indicate that you’re switching from Markdown to HTML; you just use the tags.  

The only <mark><strong>restrictions</strong></mark> are that <em>block-level</em> HTML elements — e.g. \<div\>, \<table\>, \<pre\>, \<p\>, etc. — <u>must be <em>separated</em> from surrounding content by blank lines</u>, and the start and end tags of the block should not be indented with <b>tabs</b> or <b>spaces</b>. Markdown is smart enough not to add extra (unwanted) \<p\> tags around HTML block-level tags.  
___

Daring Fireball创始人John Gruber关于Markdown的设计初衷的阐述可以看出，Markdown 是为了更简单方便地书写 HTML ，使我们更加专注于内容写作本身。  
Markdown 提炼出日常记录行文所需的一套简单的格式标签集，使用**纯文本**符号标记即可进行快速排版，将我们从繁重的格式排版中解放出来，可作为日常笔记、速记的轻量级写作工具（[Lightweight markup language](https://en.wikipedia.org/wiki/Lightweight_markup_language)）。  
在 [GitHub](https://github.com/guoyunsky/Markdown-Chinese-Demo/blob/master/README.md), [Reddit](http://www.reddit.com/), [StackOverflow](http://stackoverflow.com/)、[JianShu](http://www.jianshu.com/) 等一大批网站的影响下，Markdown在互联网上应用广泛，已经成为事实上的网络写作标准。例如，专为印象笔记（Evernote）打造的Markdown编辑器——[马克飞象](http://www.maxiang.info/) ， 配合印象笔记强大的存储和同步功能，带来前所未有的书写体验；GitHub 上每个工程要求提供Markdown格式的README.md文件，作为项目首页的说明文档。  
Markdown教程可参考《[Markdown Tutorials](https://github.com/fan2/Markdown/blob/master/Markdown%20Tutorials.md)》；Markdown编辑器可参考《[Markdown Editors](https://github.com/fan2/Markdown/blob/master/Markdown%20Editors.md)》。  

Markdown差不多可以满足日常笔记、速记、写作以及撰写博客需求，若某些文字需要以富文本形式渲染，可以直接在 Markdown 中嵌入 HTML 。  
本文在开源免费的 [macdown](http://macdown.uranusjr.com/) 下编辑完成，梳理 markdown 和 HTML 对应标签及日常撰写博客时可能用到的 HTML 补充富文本实现。内容由 markdown + HTML 混排，只能先导出为 HTML 文件，再贴过来，有些格式损失。  

#1 HTML 注释：\<!--...--\>
HTML 以`\<!--`开头，以`--\>`结尾的闭包定义注释，不在正文中显示。  
下面这句注释你是看不到的：  

<!--这是一段注释。注释不会在浏览器中显示。-->

#2 markdown 空格
由于在markdown中空格大部分时候都是起着排版控制作用，因此没法在行首或格式控制符之后输入空格。  
此时，可直接输入[HTML entities](http://entity-lookup.leftlogic.com/)中的空格占位符：  

+ en space, U+2002 ISOpub  
半方大的空白\&ensp;或\&#8194;  
+ em space, U+2003 ISOpub  
&emsp;&emsp;全方大的空白\&emsp;或\&#8195;  
+ no-break space = non-breaking space, U+00A0 ISOnum  
&nbsp;&nbsp;&nbsp;&nbsp;不断行的空白格\&nbsp;或\&#160;  

一般行首输入两个全角空格（\&emsp;）或四个半角空格（\&nbsp;）进行缩进即可。

#3 HTML 超链接
##3.1 锚点：\<a\>...\</a\>
**定义和用法**  
\<a\> 标签用来实现跳转到指定锚点(anchor)或超链接（hyperlink）。  
\<a\> 元素最重要的属性是 href 属性，它指示链接的目标，可以是页内锚点，也可以是另一个站点页面。  

**markdown对应标记**  

+ **Inline超链**  
markdown采用<code>\[\]\(\)</code>来定义超链接，中括号内是超链接文字标题，小括号内是超链接地址：\[title\]\(href\)。我们称这种为**Inline方式**超链。  
+ **Reference超链**  
与页内锚点对应的另一种是**Reference方式**的索引超链：  
两个中括号`[title][anchor]`，第二个中括号中定义页内锚点名称（索引）；然后在其他地方采用`[anchor]:href`的格式定义anchor实际指向的锚点位置（href）。
+ **自动超链**  
用尖括号包裹url，这样生成的url锚文本就是url本身，例如博客、邮箱地址。  

**[示例](http://www.cnblogs.com/heiniuhaha/archive/2011/11/23/2260201.html)**  

<!--文章结尾定义一个name="end"的锚点-->  
+ 页内锚点示例：  
<a href="#end">点我跳到本文结尾</a>

+ 最权威的 HTML 学习资料：  
<a href="http://www.w3school.com.cn/tags/index.asp">W3School HTML 参考手册</a>

+ 其他 HTML 学习参考资料：  
[HTML5 教程](http://www.jb51.net/w3school/html5/)  
[HTML 教程][1]  
[HTML 教程- (HTML5 标准)][2]  

[1]:http://www.dreamdu.com/xhtml/  
[2]:http://www.runoob.com/html/html-tutorial.html  

+ 个人博客和邮箱：   
  <http://blog.csdn.net/phunxm>  
  <challenge4fun@qq.com>  


##3.2 图片：\<img /\>
**定义和用法**  
img 元素向网页中嵌入一幅图像。  
请注意，从技术上讲，\<img\> 标签并不会在网页中插入图像，而是从网页上链接图像。  
\<img\> 标签创建的是被引用图像的占位空间。  
\<img\> 标签有两个必需的属性：*src* 属性 和 *alt* 属性。  

| 属性      | 值       | 描述               |
|:-------- |:--------:|------------------:|
| alt      | text     | 规定图像的替代文本。  |
| src      | URL      | 规定显示图像的 URL。 |

**markdown对应标记**  
markdown插入图片与插入连接的语法很像，区别在一个<code style="color:#FF0000">!</code>号。  
markdown采用<code>\![\]\(\)</code>来插入图片，中括号内是图片替代的文字，小括号内是图片地址：!\[alt\]\(src\)。  

**示例**  
<div style="text-align:center"><img src="http://my.csdn.net/uploads/avatar/9/D/B/1_phunxm.jpg" align="middle"  alt="程序猿-弦苦" /></div>  

<!-- markdown不知怎样使图片居中？ -->
![mackdown-logo](https://www.zybuluo.com/static/img/logo.png)

#4 HTML 标题：\<h1\> - \<h6\>
**定义和用法**  
标题（Heading）是通过 \<h1\> - \<h6\> 标签进行定义的。  
\<h1\> 定义最大的标题，\<h6\> 定义最小的标题。  
因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的，搜索引擎则使用标题为您的网页的结构和内容编制索引。  
一般[论文](http://www.lunwenf.com/yibaiwen/%E8%AE%BA%E6%96%87%E6%A0%BC%E5%BC%8F.doc)或博客文档结构到**3级**即可，可参考《[毕业论文的国家标准格式与通用格式](http://www.zaojiance.com/news/news-detail-2013-10-09-23-55.html)》、《[发表论文通用格式](http://wenku.baidu.com/link?url=CCLjLN3lGmNVU6_TlAiTgSXZKNObnmFPEKuVXIw8OanlNhzy7vWhu-r-ekzb7GjUGoHKfnFehrClNFbB3yCgcOcJqVYYMuTfddxjw5gIPse)》和《[期刊论文格式](http://biyelunwen.yjbys.com/geshi/417273.html)》。  

**markdown对应标记**  
markdown一行文字开头以`#`标记1级标题，以`##`标记2级标题，...，以`######`标记6级标题。  

+ 如果一行文字下面一行为三个或以上等号（===），则该行文字升级为1级标题（#）；  

This is an H1  
===
+ 如果一行文字下面一行为三个或以上减号（---），则该行文字升级为2级标题（##）。  

This is an H2  
----

**示例**  
以下是典型的HTML body内容文档结构：

<hr>
<h1 align="center">title</h1> 
<h2>1</h2>
<h3>1.1</h3>
<h4>1.1.1</h4>
<h5>（1）</h5>
<h5>（2）</h5>
<h6>*</h6>
<h4>1.1.2</h4>
<h5>（1）</h5>
<h5>（2）</h5>
<h6>*</h6>

<h2>2</h2>
<h3>2.1</h3>
<h4>2.1.1</h4>
<h5>（1）</h5>
<h6>*</h6>
<hr>

#5 HTML 文字格式
##5.1 强调文本：\<em\>...\</em\>
<em>This text is emphasized</em>

+ **斜体：\<i\>**   
	+ 定义和用法  
\<i\> 标签显示斜体文本效果。  
\<i\> 标签和基于内容的样式标签 \<em\> 类似。它告诉浏览器将包含其中的文本以斜体字（italic）或者倾斜（oblique）字体显示。如果这种斜体字对该浏览器不可用的话，可以使用高亮、反白或加下划线等样式。  
	+ 示例  
<i>This text is italic</i>  
	+ markdown对应标记  
markdown中采用星号（*）或下划线（_）对包围的文字进行斜体化。  
*This text is italic*  

##5.2 重要文本：\<strong\>...\</strong\>
<strong>This text is strong</strong>

+ **粗体：\<b\>**  
	+ 定义和用法  
\<b\> 标签规定粗体文本。
	+ 示例    
<b>This text is bold</b>
	+ markdown对应标记  
markdown中采用双星号（**）或双下划线（__）对包围的文字进行粗体化。  
**This text is bold**  
使用\<b\>\<i\>嵌套（对应markdown三星号包围）可设置粗斜体：  
***This text is italic bold***  

##5.3 突出显示文本：\<mark\>...\</mark\>
<mark>This text is mark</mark>

##5.4 改变字号
###5.4.1 加大字号：\<big\>...\</big\>
**定义和用法**  
\<big\> 标签呈现大\<big\>号字体效果，使用 \<big\> 标签可以很容易地放大字体。  
浏览器显示包含在 \<big\> 标签和其相应的 \</big\> 标签之间的文字时，其字体比周围的文字要大一号。但是，如果文字已经是最大号字体，这个 \<big\> 标签将不起任何作用。  
更妙的是，可以嵌套 \<big\> 标签来放大文本。每一个 \<big\> 标签都可以使字体大一号，直到上限 7 号文本。  

**示例**  
This text is normal.  
<big>This text is big.</big>  
This text is normal.  

###5.4.2 减小字号：\<small\>...\</small\>
**定义和用法**  
\<small\> 标签呈现小号字体效果。
\<small\> 标签和它所对应的 \<big\> 标签一样，但它是缩小字体而不是放大。  
如果被包围的字体已经是字体模型所支持的最小字号，那么 \<small\> 标签将不起任何作用。  
与 \<big\> 标签类似，\<small\> 标签也可以嵌套，从而连续地把文字缩小。每个 \<small\> 标签都把文本的字体变小一号，直到达到下限的一号字。 
 
**示例**  
This text is normal.  
<small>This text is small.</small>  
This text is normal.  

##5.5 脚标
###5.5.1 上脚标：\<sup\>...\</sup\>
指数幂示例：  
2<sup>0</sup>=1;  
2<sup>1</sup>=2;  
2<sup>2</sup>=4;  
...

###5.5.2 下脚标：\<sub\>...\</sub\>
分步计数原理公式：  
N=m<sub>1</sub> x m<sub>2</sub> x m<sub>3</sub> x ... x m<sub>n</sub>

##5.6 下划线：\<u\>...\</u\>
**定义和用法**  
\<u\> 标签可定义下划线文本。  

+ HTML 与 XHTML 之间的差异  
在 HTML 4.01 中，u 元素是不被推荐使用的。  
在 XHTML 1.0 Strict DTD 中，u 元素是不被支持的。  
+ 提示和注释：  
注释：请尽量避免为文本加下划线 - 用户会把它混淆为一个超链接！  

**示例**  
<u>This text is underline.</u>  

##5.7 删除线：\<del\>...\</del\>
**定义和用法**  
定义文档中已被删除的文本。  

+ 提示和注释：
注释：请与 \<ins\> 标签配合使用，来描述文档中的更新和修正。  

**示例**  
<p>一打有 <del>二十</del> <ins>十二</ins> 件。</p>

#6 HTML 排版控制
##6.1 HTML 水平线：\<hr\>
**定义和用法**  
\<hr\> 标签在 HTML 页面中创建用于分隔内容的水平线，无需闭合。  

**示例** 
<hr>
HTML: 这段文字上下各有一条水平线（\<hr\>）分割。
<hr>

**markdown对应标记**  
markdown行若只有三个连续的星号（***）或下划线（___）则表示横线。

***
markdown: 这段文字上下各有一条水平线分割（上行\*\*\*/下行___）。
___

**注意**  
markdown中三个连续减号（---）上面一行如果是空行，则也绘制分割线；如果上面一行有文字，则上面一行升级为2级标题（##）。

##6.2 HTML 换行：\<br /\>
**定义和用法**  
\<br\> 可插入一个简单的换行符。
<br> 标签是空标签，意味着它没有结束标签，因此这是错误的：\<br\>\</br\>。  
在 XHTML 中，把结束标签放在开始标签中，也就是 \<br /\>。  
请注意，\<br\> 标签只是简单地开始新的一行，而当浏览器遇到 <p> 标签时，通常会在相邻的段落之间插入一些垂直的间距。  

**markdown对应标记**  
markdown在文字末尾连续输入`两个空格`即可换行，否则默认和下一行连在一起。

**示例**   
<hr>
<p>
这是第一行.<br />这是第二行.<br />这是第三行.<br />
</p>
<hr>

##6.3 HTML 段落：\<p\>...\</p\>
**定义和用法**  
<p> 标签定义段落。  
p 元素会自动在其前后创建一些**空白**。浏览器会自动添加这些空间，您也可以在样式表中规定。  

**示例**
<hr>
<p>我胯下的白马疾如闪电，那是远古的旷野。</p>
<p>我从你的眼前掠过，甚至你看不清我的容颜。<br />只有我背上银色的剑鞘，在阳光下瞬间闪耀的光芒。</p>
<p>我一定要在黄昏之前到达，我要看看你，我的爱人。<br />在夕阳里娇艳的容颜，和风铃响起时迎风曼舞的衣裙。</p>
<hr>

##6.4 HTML 分区/节：\<div\>...\</div\>
**定义和用法**  
\<div\> 可定义文档中的分区或节（division/section）。
\<div\> 标签可以把文档分割为独立的、不同的部分。它可以用作严格的组织工具，并且不使用任何格式与其关联。  
如果用 id 或 class 来标记 \<div\>，那么该标签的作用会变得更加有效。  

**用法**  
\<div\> 是一个块级元素。这意味着它的内容自动地开始一个新行。  
实际上，换行是 \<div\> 固有的唯一格式表现。可以通过 \<div\> 的 class 或 id 应用额外的样式。  

**示例**    
以下示范将三级标题着色为红色，内容段落着色为蓝色：
<hr>
<div style="color:#FF0000">
  <h3>3.5.1 红色的标题</h3>
</div>
<div style="color:#0000FF">
  <p>蓝色的文字</p>
</div>
<hr>

##6.5 HTML 对齐：align属性
**定义和用法**  
align 属性规定元素（\<h1\> - \<h6\>、\<div\>）的水平对齐方式。  

+ 浏览器支持  
尽管**不推荐**使用 align 属性，但是所有浏览器都支持该属性。  
+ 兼容性注释  
在 HTML 4.01 中，不推荐使用 \<h1\> - \<h6\> 元素的 align 属性；在 XHTML 1.0 Strict DTD 中，不支持 \<h1\> - \<h6\> 元素的 align 属性。请使用 CSS 代替。  
CSS 语法：<code>\<h1 style="text-align:right"\></code>

<hr>
<div align="left">这段文字居左显示。</div>
<div style="text-align:center">这段文字居中显示。</div>
<div align="right">这段文字居右显示。</div>
<hr>


#7 HTML 引用
##7.1 作品标题：\<cite\>...\</cite\>
**定义和用法**  
\<cite\> 标签通常表示它所包含的文本对某个参考文献的引用，比如书籍或者杂志的标题。  
按照惯例，引用的文本将以斜体显示。  
用 \<cite\> 标签把指向其他文档的引用分离出来，尤其是分离那些传统媒体中的文档，如书籍、杂志、期刊，等等。如果引用的这些文档有联机版本，还应该把引用包括在一个 \<a\> 标签中，从而把一个超链接指向该联机版本。  

**示例**  
<p>
<cite>《富春山居图》</cite>由黄公望始画于至正七年(1347)，于至正十年完成。
</p>

##7.2 短引用：\<q\>...\</q\>
**定义和用法**  
\<q\> 标签定义不需要段落分隔的短引用（行内引用）。  
浏览器经常在引用的内容周围添加引号。  

**示例**  
毛泽东说过：
<q>帝国主义都是纸老虎 ... </q>  

**cite属性**  
q 元素中的 cite 属性指定了引用的来源，但主流浏览器均不支持 cite 属性，可以当做注释用： 
***
Here is a quote from WWF's website:

<q cite="http://www.wwf.org">
WWF's ultimate goal is to build a future where people live in harmony with nature.
</q>

We hope that they succeed.  
***

##7.3 块引用：\<blockquote\>...\</blockquote\> 
**定义和用法**  
\<blockquote\> 标签定义摘自另一个源的块引用。
\<blockquote\> 与 \</blockquote\> 之间的所有文本都会从常规文本中分离出来，经常会在左、右两边进行缩进，而且有时会使用斜体。也就是说，块引用拥有它们自己的空间。  

**示例**  
<blockquote>
爱上一个人  
恋上一座城
</blockquote>

**cite属性**  
同 q 元素中的 cite 属性。

**markdown对应标记**  
markdown中以`>`开始的文字为块引用：  

> //  
> //  main.m  
> //  HelloWorld  
> //  
> //  Created by faner on 15/8/30.  
> //  Copyright © 2015年 faner. All rights reserved.  
> //  
>   
> \#import <Foundation/Foundation.h>  
>   
> int main(int argc, const char * argv[]) {  
>     @autoreleasepool {  
>         // insert code here...  
>         NSLog(@"Hello, World!");  
>     }  
>     return 0;  
> }  

**`注意：`**  

+ 每行后面需要添加两个空格断行。  
+ \#号前面要加\转义。
+ 直接复制过来的代码，行首的缩进格式丢失，需要自行补充空格占位符。故一般不建议使用blockquote（>）标签来引用源代码。  

引用标记可以嵌套使用：  
>梦
 >>梦中梦
  >>>盗梦空间

**\<q\> 与 \<blockquote\> 的区别**  
\<q\> 标签在本质上与 \<blockquote\> 是一样的。不同之处在于它们的显示和应用。\<q\> 标签用于简短的行内引用。如果需要从周围内容分离出来比较长的部分（通常显示为缩进的块），请使用 \<blockquote\> 标签。

##7.4 代码块
以下是w3school中给出的“计算机输出”标签示例：  

<code>Computer code</code>
<br />
<kbd>Keyboard input</kbd>
<br />
<tt>Teletype text</tt>
<br />
<samp>Sample text</samp>
<br />
<var>Computer variable</var>
<br />

<p>
<b>注释：</b>这些标签常用于显示计算机/编程代码。
</p>

###7.4.1 代码块：\<code\>...\</code\>
**定义和用法**  
\<code\> 标签通常只是把文本变成<b>等宽字体</b>，但它暗示着这段文本是<b>源程序代码</b>。  
如果只是希望使用<b>等宽字体</b>的效果，请使用 \<tt\> 标签。  
或者，如果想要在严格限制为等宽字体格式的文本中显示编程代码，请使用 \<pre\> 标签。  

**markdown对应标记**  
markdown对应\`...\`。

**示例**  
<code>心若没有栖息的地方  
到哪里都是流浪</code>

<hr>
<code>
//  
//  main.m  
//  HelloWorld  
//  
//  Created by faner on 15/8/30.  
//  Copyright © 2015年 faner. All rights reserved.  
//  
 
\#import \<Foundation/Foundation.h\>  
  
int main(int argc, const char * argv[]) {  
    @autoreleasepool {  
        // insert code here...  
        NSLog(@"Hello, World!");  
    }  
    return 0;  
}  
</code>  
<hr>

**`注意：`**  

+ 每行后面需要添加两个空格断行。  
+ \#号前面要加\转义；头文件包含的尖括号也需要加\转义。
+ markdown的\`...\`中间的两个空格断行无效：  
`心若没有栖息的地方  
到哪里都是流浪`
+ 直接复制过来的代码，行首的缩进格式丢失，需要自行补充空格占位符。故一般也不建议使用code（``）标签来引用源代码。

###7.4.2 代码块：\<pre\>...\</pre\>
**定义和用法**  
pre 元素可定义预格式化的文本。被包围在 pre 元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体。  
\<pre\> 标签的一个常见应用就是用来表示<big>计算机的源代码</big>。  
可以导致段落断开的标签（例如标题、\<p\> 和 \<address\> 标签）绝不能包含在 \<pre\> 所定义的块里。  
pre 元素中允许的文本<em>可以包括物理样式和基于内容的样式变化</em>，还有链接、图像和水平分隔线。当把其他标签（比如 \<a\> 标签）放到 \<pre\> 块中时，就像放在 HTML/XHTML 文档的其他部分中一样即可。  

**提示和注释**  
<mark>提示</mark>：制表符（tab）在 \<pre\> 标签定义的块当中可以起到应有的作用，每个制表符占据 8 个字符的位置。但是我们不推荐使用它，因为在不同的浏览器中，Tab 的实现各不相同。在用 \<pre\> 标签格式化的文档段中使用空格，可以确保文本正确的水平位置。  
<mark>提示</mark>：如果您希望使用 \<pre\> 标签来定义计算机源代码，比如 HTML 源代码，请使用符号实体来表示特殊字符，比如 "&lt;" 代表 "<"，"&gt;" 代表 ">"，"&amp;" 代表 "&"。  
<mark>提示</mark>：在 W3School 中，非常多页面中的源代码实例都是通过 \<pre\> 标签定义的。  

**markdown对应标记**  
markdown行首输入四个连续空格即可实现\<pre\>对应的效果。

    markdown行首输入四个空格的效果：
    
    那一年 你正年轻
    总觉得明天肯定会很美
以下是使用\<pre\>...\</pre\>引用代码块的示例：

<pre>
//
//  main.m
//  EmptyApplication
//
//  Created by faner on 15/9/5.
//  Copyright © 2015年 faner. All rights reserved.
//

#import <UIKit/UIKit.h>
#import "AppDelegate.h"

int main(int argc, char * argv[]) {
    @autoreleasepool {
        return UIApplicationMain(argc, argv, nil, NSStringFromClass([AppDelegate class]));
    }
}
</pre>
以上将Xcode中的main.m代码直接拷到标签中，保持了原有的段落和缩进格式。  
如果要对代码进行语法着色，可采用在线[SyntaxHighlighter](http://tool.oschina.net/highlight)插件，输入源程序代码，输出指定语言的着色 HTML 代码。  
[Online syntax highlighter like TextMate](http://markup.su/highlighter/)  
[Online syntax highlighting for the masses! ](http://tohtml.com/cpp/)  



<a name="end">The End</a>