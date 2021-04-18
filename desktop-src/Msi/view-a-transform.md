---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLstXfm.vbs。 這個腳本範例可以用來查看轉換檔。
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: 查看轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971196"
---
# <a name="view-a-transform"></a>查看轉換

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLstXfm.vbs。 這個腳本範例可以用來查看轉換檔。

此範例將示範如何使用：

-   [\_TransformView 資料表](-transformview-table.md)
-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**ApplyTransform 方法**](database-applytransform.md)
-   [**OpenView 方法**](database-openview.md)
-   [](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)
-   [**IsNull 屬性**](record-isnull.md)
-   [](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)

使用此範例需要 CScript.exe 版本的 Windows Script Host。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiLstXfm.vbs** *\[ 路徑參考要 \] \[ \] \[ 查看 \] 的轉換資料庫選項路徑*

指定參考 Windows Installer 資料庫的路徑。 指定要用來轉換所要查看之檔案的路徑清單。 清單中的每個路徑前面都有一個選擇性數值。 此值會指定要隱藏的一組錯誤條件。 您可以將這些值加在一起，以隱藏多個條件。 如果未指定數值選項，則會隱藏所有錯誤條件。 這份清單中的引數會以從左至右的循序執行，在命令列上顯示這些引數。



| 值 | 要隱藏的錯誤條件                   |
|-------|-----------------------------------------------|
| 1     | 加入已經存在的資料列。             |
| 2     | 正在刪除不存在的資料列。           |
| 4     | 加入已經存在的資料表。           |
| 8     | 正在刪除不存在的資料表。         |
| 16    | 正在更新不存在的資料列。           |
| 256   | 資料庫與轉換字碼頁不相符。 |



 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



