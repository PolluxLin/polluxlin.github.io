<!-- title: ReadMe -->
# Markdown study

- <a target='_blank' href='https://docs.github.com/en'>GitHub Doc</a>
- <a target='_blank' href='https://docs.github.com/en/get-started/writing-on-github'>Writing on GitHub</a>
- <a target='_blank' href='https://github.com/topics/profile-readme'>GitHub Profile ReadMe</a>
- <a target='_blank' href='https://github.com/abhisheknaiidu/awesome-github-profile-readme'>Awesome GitHub Profile ReadMe</a>
- <a target='_blank' href='https://code.visualstudio.com/docs/languages/markdown'>Markdown and Visual Studio Code</a>

## Markdown - GitHub vs VSCode

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

### Syntax Highlights

Using *TAB* (\\t) charater within Code Block:

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

Using *Spaces* instead of TAB charater within Code Block:

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

### CSS Style and Colors

GitHub Markdown 並不支援內嵌 CSS Style ! (VSCode 是支援的)

不能在 .md 裡放 ```<style></style>```
```html
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

In-line Style 也是不支援的
```
How about <span style='font-weight:900;'>In-Line Style</span> ?
```

How about <span style='font-weight:900;'>In-Line Style</span> ?

GitHub 會 *清除/去掉* CSS Style 裡不支援的內容, 結果就變成 Plain Text 格式.

#### LaTeX vs KaTex

得改用 <a target='_blank' href='https://en.wikibooks.org/wiki/LaTeX/Colors#Adding_the_color_package'>LaTeX/Colors</a> 語法. (VSCode + Markdown All in One 支援 <a target='_blank' href='https://katex.org/'>KaTex</a>)
```
github Markdown $\color{red}{DO\ NOT}$ support CSS Style !
$\tiny{\textsf{lorem ipsum 中文字}}$
$\textcolor{orange}{\textsf{lorem ipsum 中文字}}$
$\textcolor{#007bff}{\texttt{lorem ipsum 中文字}}$
$\color{#dc3545}{\text{lorem ipsum}}$
$\color{rgba(255,0,0,0.4)}{\text{lorem ipsum}}$
```
效果如下:

github Markdown $\color{red}{DO\ NOT}$ support CSS Style !

$\tiny{\textsf{lorem ipsum 中文字}}$

$\textcolor{orange}{\textsf{lorem ipsum 中文字}}$

$\textcolor{#007bff}{\texttt{lorem ipsum 中文字}}$

$\color{#dc3545}{\textrm{lorem ipsum}}$

$\color{rgba(255,0,0,0.4)}{\text{lorem ipsum}}$

> [!NOTE]
> - ```\textsf```, ```\textrm``` (指定字型) - GitHub 不支援
> - ```$\color{rgba(255,0,0,0.4)}{\text{lorem ipsum}}$``` 裡的 *rgba* - VSCode 不支援

相關的討論:
- <a target='_blank' href='https://stackoverflow.com/questions/11509830/how-to-add-color-to-githubs-readme-md-file'>How to add color to GitHub's README.md file</a>
- <a target='_blank' href='https://stackoverflow.com/questions/51956361/custom-css-file-for-readme-md-in-a-github-repo'>Custom css file for readme.md in a Github repo</a>
- <a target='_blank' href='https://gist.github.com/luigiMinardi/4574708d404cdf4fe0da7ac6fe2314db'>Github markdown colors (Using Tex and the github MathJax support)</a>

---
