---
description: 資料表的檔案群組包含所有與檔案相關的 Windows Installer 資料表。
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: 檔案資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f8a73aa46b202d184356c14ff12da9ce9ce9880b009418e922b252cc35bc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142900"
---
# <a name="file-tables-group"></a>檔案資料表群組

![檔案資料表群組](images/filegrp.png)

如需此圖表的詳細資訊，請參閱 [實體關聯性圖表圖例](entity-relationship-diagram-legend.md)。

安裝程式套件開發人員應該考慮在將應用程式分解成 [元件和功能](components-and-features.md) 之後，以及擴展 [核心資料表群組](core-tables-group.md)之後，填入資料表的檔案資料表群組。 檔案資料表群組包含所有屬於安裝的檔案，而且這些檔案大部分都列在檔案 [資料表](file-table.md)中。 [目錄資料表](directory-table.md)未顯示在圖中，但與檔案資料表群組密切相關。 目錄資料表提供安裝的目錄結構。

資料表的檔案群組包含與檔案相關的所有資料表。

-   [File 資料表](file-table.md)會列出屬於安裝的檔案。 檔案資料表中未列出的檔案包含 [媒體] 表格中所列的磁片檔案。 因為每個檔案都屬於某個元件，所以檔案資料表在元件資料表中有外部索引鍵。
-   [RemoveFile 資料表](removefile-table.md)包含[RemoveFiles 動作](removefiles-action.md)要移除的檔案清單。
-   [字型表](font-table.md)會列出要向系統註冊的字型檔案。
-   [SelfReg 資料表](selfreg-table.md)會列出自行註冊之安裝的模組檔案。
-   [媒體資料表](media-table.md)會列出屬於安裝的來源媒體和磁片。
-   [BindImage 資料表](bindimage-table.md)會列出系結至可執行檔所匯入之 dll 的檔案。
-   [MoveFile 資料表](movefile-table.md)會指定在安裝期間要移動的檔案。
-   [DuplicateFile 資料表](duplicatefile-table.md)會指定在安裝期間複製的檔案。
-   [IniFile 資料表](inifile-table.md)會列出 .ini 檔案，以及應用程式必須在檔案中設定的資訊。
-   [RemoveIniFile 資料表](removeinifile-table.md)包含應用程式從 .ini 檔案中刪除所需的資訊。
-   [環境資料表](environment-table.md)是用來設定環境變數的值。
-   [圖示表格](icon-table.md)提供在產品公告中複製到檔案的圖示資訊。
-   [FileSFPCatalog 資料表](filesfpcatalog-table.md)會將指定的檔案與系統檔案保護類別目錄檔案產生關聯。

    **Windows Vista、Windows Server 2003 和 Windows XP：** 不支援。

-   [SFPCatalog 資料表](sfpcatalog-table.md)包含系統檔案保護目錄。

    **Windows Vista、Windows Server 2003 和 Windows XP：** 不支援。

-   [MsiFileHash 資料表](msifilehash-table.md)是用來儲存 Windows Installer 封裝所提供之原始程式檔的128位雜湊。

 

 



