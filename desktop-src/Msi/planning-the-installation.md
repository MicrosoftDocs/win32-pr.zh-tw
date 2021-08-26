---
description: 將現有應用程式的安裝移到其他安裝技術 Windows Installer 時，安裝程式開發人員可能會使用現有安裝的來源和目標檔案映射來開始撰寫 Windows Installer 套件。
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: 規劃安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042358"
---
# <a name="planning-the-installation"></a>規劃安裝

將現有應用程式的安裝移到其他安裝技術 Windows Installer 時，安裝程式開發人員可能會使用現有安裝的來源和目標檔案映射來開始撰寫 Windows Installer 套件。 在來源和目標上組織檔案和其他資源的詳細計畫，也是針對新應用程式開發封裝的理想起點。

範例安裝套件會採用下列檔案，這些檔案會儲存在應用程式的來源位置，並將它們安裝到使用者電腦上的目標。



| 檔案         | 描述                               | 來源的路徑                                    | 目標路徑                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | 文字編輯器可執行檔。              | C： \\ 範例 \\ 記事本 \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Redpark.exe          |
| Readme.txt   | 資訊檔。                    | C： \\ 範例 \\ 記事本 \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Readme.txt           |
| Help.txt     | 協助手動                               | C： \\ 範例 \\ 記事本 \\Help.txt                     | 未安裝。 一律從來源執行。                  |
| Baseball.txt | 2000年的棒球遊戲排程。     | C： \\ 範例 \\ 記事本 \\ 事件 \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Baseball.txt |
| Football.txt | 年度2000的足球遊戲排程。     | C： \\ 範例 \\ 記事本 \\ 事件 \\Football.txt         | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Football.txt |
| Dance.txt    | Dance 年2000的效能。         | C： \\ 範例 \\ 記事本 \\ 事件 \\Dance.txt            | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Dance.txt      |
| Concert.txt  | 年度2000的音樂效能。         | C： \\ 範例 \\ 記事本 \\ 事件 \\Concert.txt          | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Concert.txt    |
| January.txt  | 2000年1月招生。       | C： \\ 範例 \\ 記事本網 \\ 關 \\January.txt            | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\January.txt    |
| NewYears.txt | 招生於2000年的新年度日。 | C： \\ 範例 \\ 記事本網 \\ 關 \\ 假日 \\NewYears.txt | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\NewYears.txt   |



 

此範例會在使用者的登錄下，將下列值寫入 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 記事本範例**。



| 名稱             | 值    |
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



 

此範例會安裝下列快速鍵。 在安裝過程中，您可以選取其中一個快捷方式作為公告的快捷方式，讓使用者可以視需要安裝棒球功能。



| 名稱      | 快捷方式位置                         | 快捷方式目標                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Redpark.exe          |
| sReadme   | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\Readme.txt           |
| 現成     | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ 範例 \\ 記事本 \\Help.txt       |
| sBaseball | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Baseball.txt |
| sFootball | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 運動 \\Football.txt |
| sDance    | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Dance.txt      |
| sConcert  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 藝術 \\Concert.txt    |
| sJanuary  | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\January.txt    |
| sNewYears | \[ProgramFilesFolder \] \\ Red \_ 公園 \\ 功能表\\ | \[ProgramFilesFolder \] \\ Red \_ 公園網 \\ 關 \\NewYears.txt   |



 

若要重現範例，請從建立第一個資料表中指定的來原始目錄結構開始。 您可以建立系統 Notepad.exe 檔案的複本，然後將此複本重新命名 Redpark.exe。 使用記事本編輯器來建立其餘的文字檔。 藉由撰寫安裝資料庫，即可新增目標的目錄結構、登錄值和快捷方式。

[繼續](importing-a-blank-database.md)

 

 



