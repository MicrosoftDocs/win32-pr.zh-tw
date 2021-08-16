---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiDiffDb.vbs。 此範例腳本會在兩個 Windows Installer 資料庫之間產生暫時的轉換檔案，並顯示轉換。
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: 查看兩個資料庫之間的差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb04ad6ed1ecaa9d4d5be73708c5edc7dc8c84c9fe230a3725f971d949d335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375911"
---
# <a name="view-differences-between-two-databases"></a>查看兩個資料庫之間的差異

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiDiffDb.vbs。 此範例腳本會在兩個 Windows Installer 資料庫之間產生暫時的轉換檔案，並顯示轉換。

此範例將示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**OpenView 方法**](database-openview.md)
-   [**SummaryInformation 屬性 (資料庫物件)**](database-summaryinformation.md)
-   [**將方法**](database-generatetransform.md)
-   [**ApplyTransform 方法**](database-applytransform.md)
-   [**資料庫物件**](database-object.md)
-   [](view-fetch.md) [ **View 物件** 的 Fetch 方法](view-object.md)
-   [**IsNull 屬性**](record-isnull.md)
-   [](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)
-   [\_TransformView 資料表](-transformview-table.md)

使用此範例需要 Windows 腳本主機的 CScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiDiffDb.vbs** *\[ 原始資料庫 \] \[ 路徑的軌跡，以修改 \] 資料庫*

指定原始 Windows Installer 資料庫的路徑。 指定已修改之資料庫的路徑。 範例腳本會顯示轉換。

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



