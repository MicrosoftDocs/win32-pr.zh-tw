---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiSubStg.vbs。
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: 管理 Substorages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320567"
---
# <a name="manage-substorages"></a>管理 Substorages

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiSubStg.vbs。 這個範例會示範如何使用腳本來管理 Windows Installer 資料庫中的 substorages。 轉換可以新增至現有的 Windows Installer 資料庫做為 substorage。

此範例將示範如何使用：

-   [\_儲存體資料表](-storages-table.md)
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

**cscript WiSubStg.vbs \[ 路徑指向檔案 \] \[ 選項的資料庫路徑 \] \[ \] \[ substorage 名稱\]**

指定 Windows Installer 資料庫的路徑，以新增或移除 substorage。 指定要新增為 substorage 的轉換或資料庫檔案的路徑。 若要列出 Windows Installer 資料庫中的 substorages，請省略這個檔案的路徑。 您可以指定選擇性的 substorage 名稱，如果省略此名稱，substorage 名稱就會預設為檔案名。

您可以指定下列選項。



| 選項              | Description                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| 未指定任何選項 | 將 substorage 新增至 Windows Installer 資料庫。                                                 |
| /d                  | 移除 substorage。 此選項旗標後面必須接著要移除的 substorage 名稱。 |



 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

請注意， [當地語系化範例](a-localization-example.md) 示範如何將 [自訂轉換內嵌為 Substorage](embedding-customization-transforms-as-substorage.md)。

 

 



