---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiFeatur.vbs。
ms.assetid: 797cb383-22c0-42b4-82c1-d5bcc3a8bafb
title: 列出功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e166401b514f1beec9c14c74aba7ca0601f446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318999"
---
# <a name="list-features"></a>列出功能

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiFeatur.vbs。 此範例說明如何使用腳本來列出 Windows Installer 資料庫中的功能。 這個範例示範如何將暫存資料行新增至唯讀的 Windows Installer 資料庫。

此範例示範：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)
-   [**OpenView 方法**](database-openview.md)、 [**TablePersistent 屬性**](database-tablepersistent.md)，以及 [**資料庫物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)
-   [**FieldCount 屬性**](record-fieldcount.md)、 [**IntegerData 屬性**](record-integerdata.md)，以及 [**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)

使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiFeatur.vbs \[ 資料庫 \] \[ 功能名稱的路徑\]**

指定 Windows Installer 資料庫的路徑。 指定功能的名稱。 這必須列在 [功能資料表](feature-table.md)的 [功能] 資料行中。 如果省略功能的名稱，則會將所有功能列為功能樹狀目錄。 如果使用星號 (\*) 做為功能名稱，WiFeatur.vbs 會列出所有功能的組合。 請注意，使用 CScript 而非 Wscript.echo，可以更妥善地顯示大型資料庫。

如需詳細資訊，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md) ，以取得其他腳本範例。 針對不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



