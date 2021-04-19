---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiStream.vbs。
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: 管理二進位資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980459"
---
# <a name="manage-binary-streams"></a>管理二進位資料流程

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiStream.vbs。 這個範例會示範如何使用腳本來管理 Windows Installer 資料庫中的二進位資料流程。 範例可以用來將壓縮的檔案封包輸入至資料庫。 這個範例會示範 Windows Installer 資料庫中[ \_ 資料流程資料表](-streams-table.md)的作業。

此範例也會示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [**CreateRecord 方法**](installer-createrecord.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**OpenView 方法**](database-openview.md)
-   [](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)
-   [**Fetch 方法**](view-fetch.md)
-   [**Modify 方法**](view-modify.md)
-   [](view-execute.md) [ **View 物件** 的 Execute 方法](view-object.md)
-   [**至 convertfrom-stringdata 屬性**](record-stringdata.md)
-   [](record-setstream.md) [ **Record 物件** 的 SetStream 方法](record-object.md)

您將需要 CScript.exe 或 WScript.exe 版本的 Windows Script Host 才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令列。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiStream.vbs \[ 路徑指向檔案 \] \[ \] \[ 選項 \] \[ 資料流程名稱的資料庫路徑\]**

指定接收資料流程之 Windows Installer 資料庫的路徑。 指定包含資料流程資料之二進位檔案的路徑。 若要列出安裝程式資料庫中的資料流程，請省略此路徑。 您可以指定選擇性的資料流程名稱，如果省略，則會預設為檔案名。

您可以指定下列選項。



| 選項              | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| 未指定任何選項 | 將資料流程新增至 Windows Installer 資料庫。                                                 |
| /d                  | 移除資料流程。 此選項旗標後面必須接著要移除之 substorage 的名稱。 |



 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



