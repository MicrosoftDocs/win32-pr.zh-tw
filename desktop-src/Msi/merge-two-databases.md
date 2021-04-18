---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiMerge.vbs。 此範例腳本會將一個 Windows Installer 資料庫合併至另一個資料庫。 如需詳細資訊，請參閱合併和轉換。
ms.assetid: 31867082-7c1d-4530-a066-236d8ee5f023
title: 合併兩個資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0254cbe2bd0785b45d4ced3a16770023e617bc63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971616"
---
# <a name="merge-two-databases"></a>合併兩個資料庫

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiMerge.vbs。 此範例腳本會將一個 Windows Installer 資料庫合併至另一個資料庫。 如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)函式和 [**資料庫**](database-object.md)物件的 [**merge**](database-merge.md)方法無法用來合併安裝封裝中包含的模組。 它們不應該用來將 [合併模組](merge-modules.md) 合併成 Windows Installer 套件。 若要在安裝套件中包含合併模組，安裝套件的作者應遵循套用 [合併模組](applying-merge-modules.md) 主題中所述的指導方針。

此範例示範如何使用下列各項：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**OpenView 方法**](database-openview.md)
-   [**Merge 方法**](database-merge.md)
-   [](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)
-   [**Fetch 方法**](view-fetch.md)
-   [**View 物件**](view-object.md)
-   [](record-stringdata.md) [ **Record 物件** 的至 convertfrom-stringdata 屬性](record-object.md)

您必須擁有 Windows Script Host 的 CScript.exe 或 WScript.exe 版本，才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiMerge.vbs \[ 路徑指向匯 \] \[ 入資料庫 \] \[ 資料表名稱的資料庫路徑\]**

指定接收合併之 Windows Installer 資料庫的路徑。 指定要匯入至第一個資料庫的路徑。 您可以為資料表指定選擇性的名稱來保存合併錯誤。 如果未指定資料表名稱，安裝程式會使用名稱 \_ MergeErrors，並在顯示內容之後卸載資料表。

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



