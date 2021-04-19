---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiDialog.vbs。 此範例說明如何使用腳本來預覽 Windows Installer 資料庫中的對話方塊。
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: 預覽消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989455"
---
# <a name="preview-user-interface"></a>預覽消費者介面

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiDialog.vbs。 此範例說明如何使用腳本來預覽 Windows Installer 資料庫中的對話方塊。

此範例示範：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)、 [**CreateRecord 方法**](installer-createrecord.md)，以及 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [**OpenView 方法**](database-openview.md)和 [**資料庫物件**](database-object.md)的 [**EnableUIpreview 方法**](database-enableuipreview.md)
-   [**Execute 方法**](view-execute.md)和 [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)
-   [**至 convertfrom-stringdata 屬性**](record-stringdata.md) Propertyof [**記錄物件**](record-object.md)

此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。 若要使用此範例的 CScript.exe，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiDialog.vbs** *\[ 資料庫 \] \[ 對話方塊名稱 \] 的路徑*

指定 Windows Installer 資料庫的路徑。 指定對話方塊的名稱。 這個名稱必須列在 [對話方塊資料表](dialog-table.md)的對話方塊資料行中。 若要觀看佈告欄，請 [以控制項的](control-table.md) 名稱附加對話名稱，並將其附加至 [佈告欄資料表](billboard-table.md)中的佈告欄名稱。 如果未指定對話方塊，則會依序顯示對話方塊資料表中的所有對話方塊。

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



