---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiUseXfm.vbs。 這個範例會示範如何使用腳本將轉換套用至 Windows Installer 資料庫。
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: 套用轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848975"
---
# <a name="apply-a-transform"></a>套用轉換

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiUseXfm.vbs。 這個範例會示範如何使用腳本將轉換套用至 Windows Installer 資料庫。

此範例示範如何使用

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**ApplyTransform 方法**](database-applytransform.md)
-   [](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)

您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**轉換檔案 \[ 選項之原始資料庫 \] \[ 路徑的 \] cscript WiUseXfm.vbs 路徑 \[\]**

指定 Windows Installer 資料庫的路徑。 指定轉換檔案的路徑。 如果省略轉換檔的路徑，則只會比較兩個資料庫。 第三個引數是選擇性的數值，指定要隱藏的一組錯誤條件。 將這些值加在一起，以隱藏多個條件。



| 值 | 要隱藏的錯誤條件                   |
|-------|-----------------------------------------------|
| 1     | 加入已經存在的資料列。             |
| 2     | 正在刪除不存在的資料列。           |
| 4     | 加入已經存在的資料表。           |
| 8     | 正在刪除不存在的資料表。         |
| 16    | 正在更新不存在的資料列。           |
| 256   | 資料庫與轉換字碼頁不相符。 |



 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



