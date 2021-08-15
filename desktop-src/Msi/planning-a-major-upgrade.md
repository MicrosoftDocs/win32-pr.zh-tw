---
description: 如果 Windows Installer 用於安裝和設定應用程式，則可透過安裝升級套件來處理該應用程式的後續升級。
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: 規劃主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377369"
---
# <a name="planning-a-major-upgrade"></a>規劃主要升級

如果 Windows Installer 用於安裝和設定應用程式，則可透過安裝升級套件來處理該應用程式的後續升級。 安裝程式開發人員可以選擇藉由修改原始安裝套件來撰寫升級套件。 下列升級範例說明此方法。

安裝原始產品 MNP2000，然後安裝升級套件，可為使用者提供產品 MNP2001 所需的下列檔案。



| 檔案          | 描述                                                    | 來源的路徑                                    | 目標路徑                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | 文字編輯器可執行檔。 先前的產品未變更。 | C： \\ 範例 \\ 記事本 \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Redpark.exe          |
| Readme.txt    | 資訊檔。 先前的產品未變更。         | C： \\ 範例 \\ 記事本 \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Readme.txt           |
| Help.txt      | 協助手動。 先前的產品未變更。                 | C： \\ 範例 \\ 記事本 \\Help.txt                     | 未安裝。 一律從來源執行。                  |
| Baseba01.txt  | 2001年的棒球遊戲排程。                          | C： \\ 範例 \\ 記事本 \\ 事件 \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Baseball.txt |
| Footba01.txt  | 年度2001的足球遊戲排程。                          | C： \\ 範例 \\ 記事本 \\ 事件 \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Football.txt |
| Basket01.txt  | 2001年的籃球遊戲排程。                        | C： \\ 範例 \\ 記事本 \\ 事件 \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Basket01.txt |
| Dance01.txt   | Dance 年2001的效能。                              | C： \\ 範例 \\ 記事本 \\ 事件 \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Dance.txt      |
| Concert01.txt | 年度2001的音樂效能。                              | C： \\ 範例 \\ 記事本 \\ 事件 \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Concert.txt    |
| Opera01.txt   | 年2001的 Opera 效能。                              | C： \\ 範例 \\ 記事本 \\ 事件 \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Opera01.txt    |
| Januar01.txt  | 2001年1月招生。                            | C： \\ 範例 \\ 記事本網 \\ 關 \\Januar01.txt           | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\January.txt    |
| NewYea01.txt  | 招生於2001年的新年度日。                      | C： \\ 範例 \\ 記事本網 \\ 關 \\ 假日 \\NewYea01.txt | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\NewYears.txt   |
| Memori01.txt  | 招生於2001年的紀念堂日。                       | C： \\ 範例 \\ 記事本網 \\ 關 \\ 假日 \\Memori01.txt | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\Memori01.txt   |



 

安裝升級套件會移除升級產品未使用的原始產品所安裝的所有功能。

例如，從 MNP2000 進行升級時，安裝會從使用者的電腦移除下列檔案：

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

安裝升級套件時，會在使用者的登錄中寫入下列值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **記事本範例**



| Name             | 值    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

升級會將舊的快捷方式更新為下列快速鍵。 在安裝過程中，您可以選取其中一個快捷方式作為公告的快捷方式，讓使用者可以視需要安裝棒球功能。



| Name        | 快捷方式位置                         | 快捷方式目標                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Redpark.exe            |
| sReadme     | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Readme.txt             |
| 現成       | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ 範例 \\ 記事本 \\Help.txt         |
| sBaseball   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Baseba01.txt   |
| sFootball   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Footba01.txt   |
| sBasketball | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Basketba01.txt |
| sDance      | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Dance01.txt      |
| sConcert    | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Concer01.txt     |
| sOpera      | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Opera01.txt      |
| sJanuary    | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\Januar01.txt     |
| sNewYears   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\NewYea01.txt     |
| sMemorial   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\Memori01.txt     |



 

當使用者卸載升級套件時，Windows Installer 會從使用者的電腦完全移除產品的所有版本。 使用者不會離開 MNP2000 或 MNP2001 的任何部分。

[繼續](importing-original-installation-database.md)

 

 



