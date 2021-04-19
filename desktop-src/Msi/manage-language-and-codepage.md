---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiLangID.vbs。
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: 管理語言和字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996968"
---
# <a name="manage-language-and-codepage"></a>管理語言和字碼頁

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiLangID.vbs。 此範例說明如何使用腳本來存取套件的語言資訊和字碼頁。 如需詳細資訊，請參閱 (Windows Installer) [當地語系化 Windows Installer 封裝](localizing-a-windows-installer-package.md) 和 [字碼頁處理 ](code-page-handling-windows-installer-.md)。

此範例將示範如何使用：

-   [**(安裝程式物件) 的 OpenDatabase 方法**](installer-opendatabase.md)
-   [**CreateRecord 方法**](installer-createrecord.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)
-   [**OpenView 方法**](database-openview.md)
-   資料庫物件的 [**SummaryInformation 屬性 (資料庫物件)**](database-summaryinformation.md) [](database-object.md)

使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiLangID.vbs \[ 資料庫 \] \[ 關鍵字 \] \[ 值的路徑\]**

指定 Windows Installer 資料庫的路徑。 若要變更值，請指定下列其中一個關鍵字，並在後面加上新值。 如果未指定任何值，此範例會傳回目前的值。



| 關鍵字      | 描述                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **套件**  | 資料庫所支援的語言版本。 如需詳細資訊，請參閱 [**範本摘要**](template-summary.md) 屬性。                                                               |
| **產品**  | 安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。 如需詳細資訊，請參閱 [**ProductLanguage**](productlanguage.md) 屬性。 |
| **Codepage** | 字串集區的單一 ANSI 字碼頁。 如需詳細資訊，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。                                       |



 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 針對不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

如需詳細資訊，請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md) 和 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。

 

 



