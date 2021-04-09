---
description: Windows Installer 會安裝和移除稱為 Windows Installer 元件的資源區塊。 如需詳細資訊，請參閱核心資料表群組和元件和功能。
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: 指定元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848187"
---
# <a name="specifying-components"></a>指定元件

Windows Installer 會安裝和移除稱為 [Windows Installer 元件](windows-installer-components.md)的資源區塊。 如需詳細資訊，請參閱 [核心資料表群組](core-tables-group.md) 和 [元件和功能](components-and-features.md)。

在本節中，您會將記事本範例所用元件的相關資訊，新增至您在匯[入空白資料庫](importing-a-blank-database.md)時所建立的[元件資料表](component-table.md)中。 如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md) 和 [定義安裝程式元件](defining-installer-components.md)。

「記事本」範例會使用八個元件來控制資源。



| 元件 | 資源                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 棒球  | Baseball.txt、sBaseball                                                                                               |
| 演唱會   | Concert.txt、sConcert                                                                                                 |
| 舞蹈     | Dance.txt、sDance                                                                                                     |
| 足球  | Football.txt、sFootball                                                                                               |
| Help      | Help.txt、現成                                                                                                       |
| 一月   | January.txt、sJanuary                                                                                                 |
| NewYears  | NewYears.txt、sNewYears                                                                                               |
| [記事本]   | Redpark.exe，Readme.txt，sReadme，sNotepad， **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Notepad Sample** |



 

每個元件都應該使用唯一的元件識別碼 [GUID](guid.md)來識別。 如果您要重現範例，請不要重複使用下表中的相同元件識別碼 Guid。 相反地，請使用 Guidgen.exe 之類的公用程式來為您的元件產生新的 Guid。

請確定您使用的 GUID 字串與 Windows Installer GUID 資料類型一致。 如需詳細資訊，請參閱 [變更元件程式碼](changing-the-component-code.md) ，以及 [元件規則是否中斷時會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)

使用 Orca 或其他資料庫編輯器，將下列資料輸入 MNP2000.msi 的空白 [元件資料表](component-table.md) 中。 請勿在範例的 [元件] 資料行中重複使用如下所示的 Guid。



| 元件 | ComponentId                            | 目錄\_ | 屬性 | 條件 | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| 棒球  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| 演唱會   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Concert.txt  |
| 舞蹈     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | ARTSDIR     | 2          |           | Dance.txt    |
| 足球  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Help      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| 一月   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| [記事本]   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

每個元件的來源和目標目錄都是由輸入目錄資料行中的值所指定 \_ 。 安裝程式會使用目錄資料表中的資訊來解析此目錄的位置。 安裝程式會使用 KeyPath 資料行中指定的金鑰路徑檔案來偵測每個元件。 在範例中會設定遠端執行屬性，讓元件可以從來源執行或在本機執行。

[繼續](specifying-files-and-file-attributes.md)

 

 



