

# [FoldingText](http://www.foldingtext.com/)
## Summary
Use For

- Writing
- Planning
- Scheduling
- To-do Lists
- Note-taking

And Todo list, timers, and more to come! "Modes" allows you to embed with specialized behavior into your document.

## Heading Level
To create a Heading, type '#' for H1, '##' for H2, ..., '######' for H6.

## Basic Format

- To make text _italic_ surround with '*' or '_'
- To make text **bold** surround with '**' or '__'

## [CriticMarkup](http://fletcher.github.io/MultiMarkdown-4/criticmarkup.html)
### Addition

```CriticMarkup
{++Addition++}
```

{++Addition++}

### Deletion

```CriticMarkup
{--Deletion--}
```

{--Deletion--}

### Substitution

```CriticMarkup
{~~~>Substitution~~}
```

{~~~>Substitution~~}

### Highlight

```CriticMarkup
{==Highlight==}
```

{==Highlight==}

## List
### Unordered List
To create a unordered list item, type '-' or '+' or '*'

- bullet list item 1 begin with a '-'
+ bullet list item 2 begin with a '+'
* bullet list item 3 begin with a '*'

### Ordered List
To create a ordered list item, type a number（1,2...） followed by a '.'.

```Markdown
1. GETTING STARTED  
	Choosing Blogging Platform (WordPress)
2. GETTING YOUR BLOG ONLINE  
	Choosing Domain Name & Web Hosting
3. DESIGNING AND TWEAKING YOUR BLOG  
	Quick and easy ways to get your blog look the way you want
4. WRITING BLOG POSTS AND PAGES  
	Adding new content for your Blog (Posts, Pages, Images etc…)
```

[Step-by-step walkthrough for starting a blog](http://startbloggingonline.com/):

1. GETTING STARTED  
	Choosing Blogging Platform (WordPress)
2. GETTING YOUR BLOG ONLINE  
	Choosing Domain Name & Web Hosting
3. DESIGNING AND TWEAKING YOUR BLOG  
	Quick and easy ways to get your blog look the way you want
4. WRITING BLOG POSTS AND PAGES  
	Adding new content for your Blog (Posts, Pages, Images etc…)

### Todo List
#### Markdown Syntax

```Markdown
Shopping.todo

- [ ] Salt
- [ ] Yeast
- [x] Flour
```

Shopping.todo

- [ ] Salt
- [ ] Yeast
- [x] Flour 

#### FoldingText Extension

```FoldingText_Extension
Shopping.todo
- Salt
- Yeast
- Flour @done
```

Shopping.todo
- Salt
- Yeast
- Flour @done

### Timer

```FoldingText_Extension
BreadSchedule.timer
- 10:41 Knead 20 minutes
- 11:01 Ferment 3 hours
- 2:01 PM Bake 40 minutes
```

BreadSchedule.timer
- 10:41 Knead 20 minutes
- 11:01 Ferment 3 hours
- 2:01 PM Bake 40 minutes

## Edit
针对选中或光标所在元素/secion，可执行以下快捷操作：

操作               | 快捷键                    | 功能
------------------|--------------------------|------------
Clear Formatting  | <kbd>^</kbd><kbd>c</kbd>| 清除当前光标所在或所选的格式

操作               | 快捷键                    | 功能
------------------|--------------------------|------------
H1                | <kbd>⌘</kbd><kbd>1</kbd> | 提升为1级标题
H2                | <kbd>⌘</kbd><kbd>2</kbd> | 提升为2级标题
Hn{3,4,5}         | <kbd>⌘</kbd><kbd>n{3,4,5}</kbd> | 提升为n级标题
H6                | <kbd>⌘</kbd><kbd>6</kbd> | 提升为6级标题

操作    | 快捷键                    | 功能
-------|--------------------------|------------
Bold   | <kbd>⌘</kbd><kbd>b</kbd> | 加粗所选内容
Italic | <kbd>⌘</kbd><kbd>i</kbd> | 斜体所选内容
Add Link | <kbd>⌘</kbd><kbd>k</kbd> | 为所选内容添加超链接
Inline Code | <kbd>⇧</kbd><kbd>⌘</kbd><kbd>c</kbd> | 所选格式化为行内代码

操作               | 快捷键                    | 功能
------------------|--------------------------|------------
Unordered List    | <kbd>⌘</kbd><kbd>l</kbd> | 格式化为无序列表
Ordered List      | <kbd>⇧</kbd><kbd>⌘</kbd><kbd>l</kbd> | 格式化为有序列表

## View
### Fold
点击标题前面的 `#` 号可对章节进行折叠(展开)。

操作               | 快捷键                                | 功能
------------------|--------------------------------------|-------
Fold              | <kbd>⌘</kbd><kbd>/</kbd>             | 折叠/展开当前级别section<br>光标在标题或内容区都可以<br>- 折叠所有子级header标题<br>- 展开所有子级header内容
Collapse by Level | <kbd>⌥</kbd><kbd>⌘</kbd><kbd>←</kbd> | 逐级折叠<br>光标行下必须有子层级<br>- 显示各子级header标题<br>- 可重复操作，继续折叠子级
Expand by Level   | <kbd>⌥</kbd><kbd>⌘</kbd><kbd>→</kbd> | 逐级展开，逆行expand<br>可重复操作，逐级展开子级标题和内容

### Focus

操作              | 快捷键                                | 功能
------------------|--------------------------------------|---
Focus             | <kbd>⌘</kbd><kbd>U</kbd>             | 聚焦当前section
Focus Out         | <kbd>⇧</kbd><kbd>⌘</kbd><kbd>U</kbd> | 展开到上一级section<br>可重复操作，逐级向上展开
Focus Heading     | <kbd>⌥</kbd><kbd>⌘</kbd><kbd>U</kbd> | 查看TOC浮窗<br/>可⬆️/⬇️移动，点击跳转
Outline View      | <kbd>⌥</kbd><kbd>⌘</kbd><kbd>T</kbd> | 查看TOC侧边栏

## References
[Customizing FoldingText](http://computers.tutsplus.com/tutorials/customizing-foldingtext--cms-21674)

