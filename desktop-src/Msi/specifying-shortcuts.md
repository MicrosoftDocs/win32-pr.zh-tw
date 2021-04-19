---
description: 安裝資料庫的快捷方式資料表和相關資料表會保存安裝快捷方式所需的資訊。 請參閱「程式資訊資料表」群組和編輯安裝程式快捷方式。
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: 指定快速鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974405"
---
# <a name="specifying-shortcuts"></a>指定快速鍵

安裝資料庫的 [快捷方式資料表](shortcut-table.md) 和相關資料表會保存安裝快捷方式所需的資訊。 請參閱「 [程式資訊資料表」群組](program-information-tables-group.md) 和 [編輯安裝程式快捷方式](editing-installer-shortcuts.md)。

在本節中，您會新增資訊，以指定「記事本」範例的公告和非公告快捷方式。

使用您的資料庫編輯器開啟 MNP2000.msi，並在快捷方式資料表中輸入下列資料。

[快速鍵資料表](shortcut-table.md)



| 快速鍵  | 目錄\_ | Name         | 元件\_ | 目標             | 引數 | 描述 | 熱鍵 | 圖示\_         | >iconindex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | 棒球    | 棒球           |           |             |        | orca \_icon.exe |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | 演唱會     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | 舞蹈       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | 足球    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| 現成     | MENUDIR     | Help.txt     | Help        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | 一月     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | [記事本]     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | [記事本]     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

範例安裝需要啟用針對棒球功能所公告的快捷方式安裝。 這需要在快捷方式資料表的圖示資料行中，指定圖示資料表的索引鍵 \_ 。 基於此範例的目的，您可以複製 Windows Installer SDK 所提供的 Orca 資料庫編輯器圖示。 從 Orca.msi 匯出 [圖示資料表](icon-table.md) ，然後使用 Orca 或其他合併工具，將此資料表合併到 MNP2000.msi 資料庫中。 Orca 也會在包含 MNP2000.msi 的目錄中建立名為 Icon 的目錄，並將圖示二進位資料檔案 orca \_icon.exe ibd。 請參閱圖示表格中的資料行。 在 Orca 中觀看時，已完成的圖示資料表看起來應該如下所示。

[圖示表](icon-table.md)



| Name           | 資料            |
|----------------|-----------------|
| orca \_icon.exe | \[Binary Data\] |



 

[繼續](specifying-properties.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編輯安裝程式快捷方式](editing-installer-shortcuts.md)
</dt> </dl>

 

 



