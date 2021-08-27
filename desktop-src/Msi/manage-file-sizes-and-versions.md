---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiFilVer.vbs。 此範例會示範如何使用腳本來報告或更新檔案版本、大小和語言資訊。
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: 管理檔案大小和版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dcb5bec9b7fd24d7171efed9295479e56d979a3f7aa69352f2231d409417f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629039"
---
# <a name="manage-file-sizes-and-versions"></a>管理檔案大小和版本

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiFilVer.vbs。 此範例會示範如何使用腳本來報告或更新檔案版本、大小和語言資訊。

此範例也會顯示 Windows Installer 動作、如何存取 Windows Installer 資料庫，以及如何使用下列各項：

-   [](installer-opendatabase.md) [**安裝程式物件** 的 OpenDatabase 方法](installer-object.md)
-   [**FileAttributes**](installer-fileattributes.md) 屬性
-   [**Get-filehash**](installer-filehash.md) 方法
-   [**FileVersion**](installer-fileversion.md) 方法
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**資料庫. OpenView**](database-openview.md) 方法
-   [](database-summaryinformation.md) [ **Database 物件** 的 SummaryInformation 屬性](database-object.md)
-   [**Dataadapter.doaction**](session-doaction.md) 方法
-   [**Session. 屬性**](session-session.md)
-   [**Session**](session-sourcepath.md) 屬性
-   Session 物件的 [**session. Mode**](session-mode.md)屬性 [](session-object.md)
-   [**至 convertfrom-stringdata**](record-stringdata.md) 屬性
-   [](record-integerdata.md) [ **Record 物件** 的 IntegerData 屬性](record-object.md)

使用此範例需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令：

**cscript WiFilVer.vbs \[ 資料庫 \] \[ 選擇性來源位置的路徑\]**

也請注意下列事項：

-   如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。
-   若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。
-   此範例會傳回值 0 (零) 表示成功，1 (一個) （如果叫用說明），而如果腳本失敗，則為 2 (兩個) 。

指定您要更新的 Windows Installer 資料庫（必須位於原始程式檔根目錄）。 不過，您可以在不同的位置指定資料庫的來源。 如果來源是壓縮的，則會在根目錄開啟所有檔案。

您可以在命令列上的任何位置指定下列選項。



| 選項                | Description                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| *未指定任何選項* | 顯示資料庫的檔案資訊。                                            |
| /U                    | 從來源更新資料庫中的檔案大小、版本和語言資訊。 |



 

如需詳細資訊，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)和[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



