<!-- title: ReadMe -->
# About me

## Markdown - github vs VSCode

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

## Markdown - Syntax Highlights

Using **TAB** (\\t) charater within Code Block:

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

Using Spaces instead of TAB charater within Code Block:

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

---


