<!-- title: About Markdown -->
# Markdown

## 關於 Markdown

<a target='_blank' href='https://en.wikipedia.org/wiki/Markdown'>這裡是 Markdown 在維基百科的介紹</a>, 之所以叫這個名字, 源自於它輕量化的標的: **HTML** - HyperText Markup Language -- **Markup** vs. **Markdown**.

意即: Markdown 是簡化、輕量版的 HTML -- 相較於 HTML, 用 Markdown 來撰寫文件或操作說明更容易, 也更便捷.

## 為何要用 Markdown ?

在工作場合裡, 我們早就習慣用 Microsoft Office Word 來製作文件, 但別忘了: Word 要花錢買!

而學習 HTML 和 CSS 再用來製作文件, 也是得花心思和時間...

單純的 Markdown 雖然沒能做到精緻的版面控制, 但隨手拈來的文字編輯器都可以寫, 用幾個簡單的文法和符號, 就能做出有專業質感的文件, 不好嗎?

真的需要時, 你也可以在 Markdown 裡直接放 HTML + CSS 來做更細部的控制.

Markdown 檔案遠比 Word 或 HTML 小得多, 更適合做為線上文件.

也因為 Markdown 大受歡迎, 所以像 VSCode, GitHub 都支援, 特別是 Open Source Project 的作者愛用它來製作說明文件, 而當今許多網頁也是用它做為基底來撰寫.

如果你要寫 FAQ、SOP或圖文並茂的說明文件, 不妨試試看 Markdown.

> [!TIP]
> - 除了做文件之外, 也可以從 Markdown preview 中複製內容, 再貼進 Teams, 那會是具備格式化的內容
> - 如果不是要給 GitHub Repo. 使用的 Readme.md, 而是工作上的文件, 那建議是使用 VSCode 相容的方式來運用 Markdown, 會容易掌握些

## 特別說明

這份文件不打算介紹 Markdown 的語法, 因為 Internet 上已經有太多了, 自己上網搜尋一下吧.

要特別指出的是:
- Markdown 有各種版本, 且搭配支援的 library 也是百家爭鳴, 但不見得彼此相容!
- 以 GitHub 為例, 有所謂的 GitHub Flavored Markdown (<a target='_blank' href='https://github.github.com/gfm/'>**GFM**</a>), 搭配 <a target='_blank' href='https://en.wikipedia.org/wiki/LaTeX'>LaTeX</a> 來呈現數學公式及排版
- VSCode 則是搭配 <a target='_blank' href='https://en.wikipedia.org/wiki/KaTeX'>KaTeX</a> 來做預覽及來呈現數學公式, 但是能透過擴充元件 <a target='_blank' href='https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one'>Markdown All in One</a> 來提供與 **GFM** 一定程度的相容性
- Markdown Spec. 裡完全沒提到的是: *顏色*
	- GFM 會主動清除特定的 CSS tag 和 properties, 特別是顏色相關的部份, 但容許使用部份 LaTex 語法來解決
	- VSCode 則容許採用 CSS 和 KaTex 來做顏色和進階的 style 處理

Markdown 要轉換成 HTML 或 PDF 非常容易, 除了有一大堆線上工具外, 如果用的是 VSCode + Markdown All in One:
- 先將文件存成 **.md** (Markdown 專屬副檔名)
- 轉存成 .html
- 用 browser 開啟 .html 再以 列印 功能輸出成 .pdf

> [!IMPORTANT]
> 文件接下來提到 VSCode 時, 都是指 **VSCode + Markdown All in One** 的組合.

## Table of Contents

- [Markdown](#markdown)
	- [關於 Markdown](#關於-markdown)
	- [為何要用 Markdown ?](#為何要用-markdown-)
	- [特別說明](#特別說明)
	- [Table of Contents](#table-of-contents)
	- [線上文件參考](#線上文件參考)
	- [常用元素](#常用元素)
		- [Alert Blockquote](#alert-blockquote)
		- [Color](#color)
		- [Text Size](#text-size)
		- [Font family](#font-family)
		- [Hyper-Link and Image](#hyper-link-and-image)
		- [Table](#table)
		- [Task list](#task-list)
		- [Code Block and Syntax Highlights](#code-block-and-syntax-highlights)
		- [Math formula](#math-formula)


## 線上文件參考

- <a target='_blank' href='https://docs.github.com/en'>GitHub Doc</a>
- <a target='_blank' href='https://docs.github.com/en/get-started/writing-on-github'>Writing on GitHub</a>
- <a target='_blank' href='https://github.com/topics/profile-readme'>GitHub Profile ReadMe</a>
- <a target='_blank' href='https://github.com/abhisheknaiidu/awesome-github-profile-readme'>Awesome GitHub Profile ReadMe</a>
- <a target='_blank' href='https://code.visualstudio.com/docs/languages/markdown'>Markdown and Visual Studio Code</a>

## 常用元素

### Alert Blockquote

GFM 和 VSCode 提供以下的 Alert Blockquote:
```
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```
效果如下:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### Color

時下的配色因為講究保護眼睛 -- 在長時間閱讀下, 如何讓眼睛比較不會疲勞?\
除了傳統的白底黑字之外, 編輯工具、網頁瀏覽器乃至作業系統都提供 **Dark Theme** -- 黑底白字, 來減低對眼睛的刺激和負擔.

所以在配色上要注意一下載體的背景底色和前景文字顏色的搭配, 對比要掌握好.

一如前面提到的: Markdown 對顏色並沒有標準規範, 所以得透過別的手段來達成.

在 **VSCode** 裡, 可以在文件的前面或底部(建議是底部), 加入 CSS 專用的 **style** tag:
```css
<style>
   img { border: solid 1px #4949FC; }
   .danger { color: #dc3545; }
   .primary { color: #007bff; }
</style>
```
然後用在文件裡來呈現顏色及變化
```html
Using <span class='primary' style='font-weight:bold;'>SPAN</span> tag with <span class='danger'>CSS Style</span>.
```
但這個手法在 **GFM** 就行不通了, 得改用 LaTex/KaTex 格式:
```latex
$\color{orange}{\text{lorem ipsum 中文 字體}}$
$\color{#dc3545}{\text{lorem ipsum 中文 字體}}$
```
效果如下:

- $\color{orange}{\text{lorem ipsum 中文 字體}}$
- $\color{#dc3545}{\text{lorem ipsum 中文 字體}}$

用 $ 括起來的就是 LaTex/KaTex 語法, 其中:
- ```\color{...}``` 用來指定文字顏色
	- 大括號裡可以是: 預定的**顏色名稱** 或 **#RGB 編碼**, 在 GFM 還支援 ```rgba(255,0,0,0.4)``` 之類的語法來控制透明度
- ```\text{...}``` 用來指定文字內容 -- 如果直接用大括號而不給 ```\text```, 文字裡的空格會消失 ...

如果是以 $$ 括起來就是置中:
```
$$\color{Green}{\text{lorem ipsum 中文 字體}}$$
```
$$\color{Green}{\text{lorem ipsum 中文 字體}}$$

相關的討論和參考:
- <a target='_blank' href='https://stackoverflow.com/questions/11509830/how-to-add-color-to-githubs-readme-md-file'>How to add color to GitHub's README.md file</a>
- <a target='_blank' href='https://stackoverflow.com/questions/51956361/custom-css-file-for-readme-md-in-a-github-repo'>Custom css file for readme.md in a Github repo</a>
- <a target='_blank' href='https://gist.github.com/luigiMinardi/4574708d404cdf4fe0da7ac6fe2314db'>Github markdown colors (Using Tex and the github MathJax support)</a>
- <a target='_blank' href='https://en.wikibooks.org/wiki/LaTeX/Colors#Adding_the_color_package'>LaTeX/Colors</a>
- <a target='_blank' href='https://notionthings.com/2021/01/23/advanced-notion-formatting-using-katex-expressions/'>Advanced Notion Formatting Using KaTeX Expressions</a>

> [!CAUTION]
> - GFM 不支援 Tex 語法裡的 ```\colorbox``` (背景底色) 和 ```\fcolorbox``` (邊框顏色)

### Text Size

LaTex/KaTex 支援的 **Text Size** 有:
```LaTex
- $\tiny{\text{lorem ipsum 中文字}}$
- $\scriptsize{\text{lorem ipsum 中文字}}$
- $\footnotesize{\text{lorem ipsum 中文字}}$
- $\small{\text{lorem ipsum 中文字}}$
- $\normalsize{\text{lorem ipsum 中文字}}$
- $\large{\text{lorem ipsum 中文字}}$
- $\Large{\text{lorem ipsum 中文字}}$
- $\LARGE{\text{lorem ipsum 中文字}}$
- $\huge{\text{lorem ipsum 中文字}}$
- $\Huge{\text{lorem ipsum 中文字}}$
```
但 GFM 只支援其中的:

Size|看樣
--|--
**tiny** = **scriptsize**|$\tiny{\text{lorem ipsum 中文字}}$
**small**|$\small{\text{lorem ipsum 中文字}}$
**normalsize** (預設)|$\normalsize{\text{lorem ipsum 中文字}}$
**large**|$\large{\text{lorem ipsum 中文字}}$
**Large** = **LARGE** = **huge** = **Huge**|$\huge{\text{lorem ipsum 中文字}}$

> [!TIP]
> - Markdown 對文字的突顯效果只有: 粗體字 和 斜體字
> - 但粗體字在 中文字型 上的突顯效果很差, 所以選擇是:
>	- 加上配色 (color), 如:
>		- ```$\color{gold}{\text{lorem 中文 ipsum 字體}}$```
>		- $\color{gold}{\text{lorem 中文 ipsum 字體}}$
>	- 套用 Text Size, 但不建議...

### Font family

GFM-LaTex 不支援 **Sans Serif** 之外的字體, VSCode/KaTex 則有:

字型|語法|看樣
--|--|--
**Typewriter**|```$\texttt{lorem ipsum 中文 字體}$```|$\texttt{lorem ipsum 中文 字體}$
**Sans Serif** (預設)|```$\textsf{lorem ipsum 中文 字體}$```|$\textsf{lorem ipsum 中文 字體}$
**Roman**|```$\textrm{lorem ipsum 中文 字體}$```|$\textrm{lorem ipsum 中文 字體}$

目前 LaTex/KaTex 語法並沒有對中文字型的控制能力

### Hyper-Link and Image

- Hyper-link 簡單語法:
	```
	[說明文字](URL)
	如:
	[Markdown - Wiki](https://en.wikipedia.org/wiki/Markdown)
	```
	效果如下:

	[Markdown - Wiki](https://en.wikipedia.org/wiki/Markdown)

- Image 簡單語法:
	```
	![說明文字](位置)
  - 相對位置
	![image info](./pictures/image.png)
  - URL
	![system schema](https://server/group/jobs/blob/master/doc/systemDiagram.jpg)
	```

> [!IMPORTANT]
> - 使用 Markdown All in One 套件時, image 的位置預設會轉換成絕對位址
> - 要強制轉換成相對位置, 請改設定:
> 	- markdown.extension.print.**absoluteImgPath** 為 **false**

> [!TIP]
> - Hyper-link 語法會轉譯為 ```<a href='URL'>說明文字</a>```,
> - 如果希望在點擊時是: 自動另開新頁, 就得改用 HTML 語法:
> 	```
>	<a target='_blank' href='URL'>說明文字</a>
> 	```
>	即: 加入 **target='_blank'**

### Table

基本語法:
```
Heaer1|Header2|Header3|Header4
--|:--|:--:|--:
Item A|Left Aligned|Centralized|Right Aligned
123|Abc|def|567
```
效果如下:

Heaer1|Header2|Header3|Header4
--|:--|:--:|--:
Item A|Left Aligned|Centralized|Right Aligned
123|Abc|def|567

語法中, 表頭表身中間的分隔線用來指定對齊的方式:
- **:--** = 強迫靠左對齊, 等同預設的 **--**
- **:--:** = 強制置中
- **--:** = 強迫靠右對齊

### Task list

工作清單語法:
```
- [ ] A
- [x] b
- [ ] C
```
效果:
- [ ] A
- [x] b
- [ ] C

> [!IMPORTANT]
> 這是 GFM 和 VSCode 才支援的

### Code Block and Syntax Highlights

在 Code Block 裡使用 *TAB* (\\t) 字元, 容易因為 Render 不同而失去對齊的效果:
```sql
-- RDBMS..: SQLite, version 3
-- Table..: Blacklist
CREATE TABLE If NOT EXISTS [Blacklist] (
	[RecGUID]	INTEGER	NOT NULL PRIMARY KEY AUTOINCREMENT,
	[Activated]	BIT		DEFAULT (1) NOT NULL,
	--
	[Content]	VARCHAR	(255)	NOT NULL,
	[Remark]		NVARCHAR	(255)	NOT NULL,
	--
	[CreateUsrId]	NVARCHAR (50)	DEFAULT ('dba') NOT NULL,
	[CreateIPAdr]	NVARCHAR (32)	DEFAULT ('127.0.0.1') NOT NULL,
	[CreatePrgId]	NVARCHAR (50)	DEFAULT ('dba') NOT NULL,
	[CreateStamp]	VARCHAR	(30)	DEFAULT (strftime('%Y-%m-%d %H:%M:%f', 'now', 'localtime')) NOT NULL,
	[UpdateUsrId]	NVARCHAR (50)	DEFAULT ('dba') NOT NULL,
	[UpdateIPAdr]	NVARCHAR (32)	DEFAULT ('127.0.0.1') NOT NULL,
	[UpdatePrgId]	NVARCHAR (50)	DEFAULT ('dba') NOT NULL,
	[UpdateStamp]	VARCHAR	(30)	DEFAULT (strftime('%Y-%m-%d %H:%M:%f', 'now', 'localtime')) NOT NULL
);
CREATE UNIQUE	INDEX If NOT EXISTS [Blacklist_I01U] ON [Blacklist](RecGUID);
CREATE			INDEX If NOT EXISTS [Blacklist_I02X] ON [Blacklist](RecGUID, Activated, Content);
```
用 *空白* 字元才能確保版面對齊的效果:
```sql
-- RDBMS..: SQLite, version 3
-- Table..: Blacklist
CREATE TABLE If NOT EXISTS [Blacklist] (
   [RecGUID]   INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT,
   [Activated] BIT     DEFAULT (1) NOT NULL,
   --
   [Content] VARCHAR  (255) NOT NULL,
   [Remark]  NVARCHAR (255) NOT NULL,
   --
   [CreateUsrId] NVARCHAR (50) DEFAULT ('dba') NOT NULL,
   [CreateIPAdr] NVARCHAR (32) DEFAULT ('127.0.0.1') NOT NULL,
   [CreatePrgId] NVARCHAR (50) DEFAULT ('dba') NOT NULL,
   [CreateStamp] VARCHAR  (30) DEFAULT (strftime('%Y-%m-%d %H:%M:%f', 'now', 'localtime')) NOT NULL,
   [UpdateUsrId] NVARCHAR (50) DEFAULT ('dba') NOT NULL,
   [UpdateIPAdr] NVARCHAR (32) DEFAULT ('127.0.0.1') NOT NULL,
   [UpdatePrgId] NVARCHAR (50) DEFAULT ('dba') NOT NULL,
   [UpdateStamp] VARCHAR  (30) DEFAULT (strftime('%Y-%m-%d %H:%M:%f', 'now', 'localtime')) NOT NULL
);
CREATE UNIQUE INDEX If NOT EXISTS [Blacklist_I01U] ON [Blacklist](RecGUID);
CREATE        INDEX If NOT EXISTS [Blacklist_I02X] ON [Blacklist](RecGUID, Activated, Content);
```

> [!WARNING]
> 各家 Render (如: GFM vs. VSCode) 支援 *Code Block Syntax Highlights* 的函式庫各自不同, 所以突顯效果的套用結果也會不一樣!

### Math formula

語法範例:
```Tex
Inline math: $x^2$

Math block:

$$
\displaystyle
\left( \sum_{k=1}^n a_k b_k \right)^2
\leq
\left( \sum_{k=1}^n a_k^2 \right)
\left( \sum_{k=1}^n b_k^2 \right)
$$
```
效果如下:

Inline math: $x^2$

Math block:

$$
\displaystyle
\left( \sum_{k=1}^n a_k b_k \right)^2
\leq
\left( \sum_{k=1}^n a_k^2 \right)
\left( \sum_{k=1}^n b_k^2 \right)
$$

---
