---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiCompon.vbs。 這個範例腳本可以用來列出 Windows Installer 資料庫中的元件。
ms.assetid: 4e6cc6f4-821a-4a10-a897-5c6aace1f702
title: 列出元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec396e66ed55d78131c74b85432b2f01829cdb5400fc5c00a6ced5725edadeae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129318"
---
# <a name="list-components"></a>列出元件

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiCompon.vbs。 這個範例腳本可以用來列出 Windows Installer 資料庫中的元件。

這個範例會示範如何在 [元件資料表](component-table.md)中使用不同的主要索引鍵。

此範例也會示範：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)。
-   [**OpenView 方法**](database-openview.md)、 [**TablePersistent 屬性**](database-tablepersistent.md)，以及 [**資料庫物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)。
-   [**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)。
-   [**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)（property）屬性（property）。

使用此範例需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiCompon.vbs \[ 資料庫 \] \[ 元件名稱的路徑\]**

指定 Windows Installer 資料庫的路徑。 指定元件的名稱。 此名稱必須列在 [元件資料表](component-table.md)的元件資料行中。 如果省略元件的名稱，則會列出所有的元件。 如果使用星號 (\*) 作為元件名稱，WiCompon.vbs 會列出所有元件的組合。 請注意，使用 CScript 而非 Wscript.echo，可以更妥善地顯示大型資料庫。

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



