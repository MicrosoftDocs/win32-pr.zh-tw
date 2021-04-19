---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstScr.vbs。 此範例腳本示範 Windows Installer 腳本檢視器。
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: 查看安裝程式腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979021"
---
# <a name="view-installer-script"></a>查看安裝程式腳本

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstScr.vbs。 此範例腳本示範 Windows Installer 腳本檢視器。

此範例將示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [**安裝程式**](installer-object.md)物件的 [**LastErrorRecord**](installer-lasterrorrecord.md)方法
-   [**資料庫**](database-object.md)物件的 [**OpenView**](database-openview.md)方法
-   [**View**](view-object.md)物件的 [**Fetch**](view-fetch.md)方法
-   [**FormatText**](record-formattext.md) 方法
-   [**FieldCount**](record-fieldcount.md) 屬性
-   [**Record**](record-object.md)物件的 [**至 convertfrom-stringdata**](record-stringdata.md)屬性
-   [\_TransformView 資料表](-transformview-table.md)

使用此範例需要 CScript.exe 版本的 Windows Script Host。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

*\[ Windows Installer 執行腳本 \] 的* **cscript WiLstScr.vbs** 路徑

指定安裝程式執行腳本的路徑。

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



