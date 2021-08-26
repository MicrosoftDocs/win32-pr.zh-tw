---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiImport.vbs。 此範例示範如何撰寫腳本，以將資料表匯入 Windows Installer 資料庫。
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: 匯入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc67cc3f698d1268a5ce08fe1e4c76b86a425216396fa168b0e8e6dc8a3f91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043858"
---
# <a name="import-files"></a>匯入檔案

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiImport.vbs。 此範例示範如何撰寫腳本，以將資料表匯入 Windows Installer 資料庫。

腳本會連接到 [**安裝程式**](installer-object.md) 物件、開啟資料庫、處理檔案清單，並在關閉資料庫之前認可變更。

此範例將示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**Import 方法**](database-import.md)
-   [](database-commit.md) [ **Database 物件** 的 Commit 方法](database-object.md)

您將需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本，才能使用此範例。 若要使用 CScript.exe 執行此範例，請在命令提示字元中使用下列語法。

**cscript WiImport.vbs \[ 路徑指向 \] \[ 資料夾 \] \[ 選項 \] \[ 保存檔案清單的資料庫路徑**\]

如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[ \] 。此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

指定要建立之 Windows 安裝程式資料庫的路徑，或要接收匯入之資料表的路徑。 指定包含要匯入之資料表保存檔案的資料夾路徑。 列出正在匯入的封存檔案名稱。 萬用字元檔案名（例如 \* idt）可以用來匯入多個檔案。

您可以在檔案清單前的命令列上的任何位置指定下列選項。



| 選項              | 描述                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| 未指定任何選項 | 從指定的資料夾將資料表封存檔案清單匯入 Windows Installer 資料庫。                                |
| /c                  | 建立 Windows Installer 資料庫，然後從指定的資料夾將資料表封存檔案清單匯入至新的資料庫。 |



 

如需詳細資訊，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)，以取得其他腳本範例。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

請注意， [當地語系化範例](a-localization-example.md) 也會示範如何匯 [入當地語系化的錯誤和 ActionText 資料表](importing-localized-error-and-actiontext-tables.md)。

 

 



