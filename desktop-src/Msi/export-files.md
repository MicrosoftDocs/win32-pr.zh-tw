---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiExport.vbs。
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: 匯出檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7cab882778bce6d84412f53987c65211f70f4a8a10b52836ad993d8e813304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044438"
---
# <a name="export-files"></a>匯出檔案

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiExport.vbs。 此範例示範如何撰寫腳本，以將資料表匯出至 Windows Installer 資料庫。 腳本範例會連接到 [**安裝程式**](installer-object.md) 物件、開啟資料庫，並將資料表匯出到封存檔案。

此範例將示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**Export 方法**](database-export.md)
-   [](database-openview.md) [**資料庫物件** 的 OpenView 方法](database-object.md)
-   [](view-fetch.md) [ **View 物件** 的 Fetch 方法](view-object.md)
-   [](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)

您將需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本，才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiExport.vbs \[ 路徑指向 \] \[ 資料夾 \] \[ 選項 \] \[ 資料表名稱清單的資料庫路徑\]**

指定要從中匯出資料表的安裝程式資料庫路徑。 指定要將匯出的封存檔案複製到其中的資料夾路徑。 列出要匯出的 [資料庫資料表](database-tables.md) 名稱（區分大小寫）。 指定 ' \* ' 以匯出所有資料表（包括 \_ SummaryInformation）。

您可以在命令列上的任何位置指定下列選項，在資料表名稱清單之前。



| 選項              | 描述                                            |
|---------------------|--------------------------------------------------------|
| 未指定任何選項 | 匯出的封存檔案的檔案名可能很長。      |
| /s                  | 強制匯出的封存檔案具有簡短的檔案名。 |



 

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



