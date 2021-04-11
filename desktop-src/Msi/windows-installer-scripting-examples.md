---
description: Windows Installer 開發人員的 Windows SDK 元件包含 VBScript 檔案，這些檔案會說明如何使用 Windows Installer automation 介面來修改 Windows Installer 套件。
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Installer 腳本範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944475"
---
# <a name="windows-installer-scripting-examples"></a>Windows Installer 腳本範例

[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)包含 VBScript 檔案，這些檔案會說明如何使用 Windows Installer automation 介面來修改 Windows Installer 套件。

Microsoft Corporation 不支援本主題中所識別的腳本範例，而只提供這些範例做為可能有用的參考。 執行這些範例需要 Windows Script Host。 如需 Windows Script Host 的詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 的 [Windows Script host](/previous-versions//9bbdkx3k(v=vs.85)) 一節。



| 指令檔範例 | Description                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [列出產品、屬性、功能和元件](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [匯入檔案](import-files.md)                                                                            |
| WiExport.vbs       | [匯出檔案](export-files.md)                                                                            |
| WiSubStg.vbs       | [管理 Substorages](manage-substorages.md)                                                                |
| WiStream.vbs       | [管理二進位資料流程](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [合併兩個資料庫](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [產生轉換](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [套用轉換](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | 只 (CSCRIPT 來[查看轉換](view-a-transform.md))                                                      |
| WiDiffDb.vbs       | [在兩個資料庫之間查看](view-differences-between-two-databases.md) (CSCRIPT 的差異)          |
| WiLstScr.vbs       | [View Installer 腳本](view-installer-script.md) (CSCRIPT only)                                            |
| WiSumInf.vbs       | [管理摘要資訊](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [管理原則設定](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [管理語言和字碼頁](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [將 Unicode 檔案複製到 Ansi 檔案](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [管理檔案大小和版本](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [產生檔案封包](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [執行 SQL 語句](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [將 ANSI 檔案複製到資料庫欄位](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [列出元件](list-components.md)                                                                      |
| WiFeatur.vbs       | [列出功能](list-features.md)                                                                          |
| WiDialog.vbs       | [預覽消費者介面](preview-user-interface.md)                                                        |



 

所有這些腳本都會顯示描述其命令列引數的說明畫面。 若要在 Windows 中顯示 [說明] 畫面，請按兩下該檔案。 若要從命令列顯示說明畫面，請輸入？ 作為第一個引數，或輸入較少的引數。 腳本會傳回值0表示成功，1表示叫用說明，如果發生失敗，則為2。

這些範例需要 Windows Script Host 才能執行。 Windows Script Host 實際上是兩個主機：

-   CScript.exe 是可讓您從命令提示字元執行腳本的版本，並提供命令列參數來設定腳本屬性。
-   WScript.exe 是 Windows Script Host 的版本，可讓您從 Windows 執行腳本。 如需詳細資訊，請參閱 Windows SDK 中的 [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) 一節。

Makecab.exe 公用程式隨附于 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中的修補範例。

如需 WMI 的詳細資訊，請參閱搭配 [使用 Windows Installer 與 wmi](using-windows-installer-with-wmi.md)。

 

 
