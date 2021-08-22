---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiMakCab.vbs。 此範例示範如何使用腳本從 Windows Installer 資料庫產生檔案封包。
ms.assetid: 26671cb9-a200-4520-8b52-4cff3f71a2f2
title: 產生檔案封包
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca9e30822d0683aa09dc015ec2fd98d1f598c70e0fd63fd00f66a6bcdf3edf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581488"
---
# <a name="generate-file-cabinet"></a>產生檔案封包

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiMakCab.vbs。 此範例示範如何使用腳本從 Windows Installer 資料庫產生檔案封包。

此範例示範：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)和 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [**Commit 方法**](database-commit.md)、 [**OpenView 方法**](database-openview.md)和 [**SummaryInformation 屬性 (**](database-summaryinformation.md)資料庫 [**物件的**](database-object.md)資料庫物件) 
-   [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)、 [**Execute 方法**](view-execute.md)和 [**Modify 方法**](view-modify.md)
-   [**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)和 [**IntegerData 屬性**](record-integerdata.md)
-   [**Dataadapter.doaction 方法**](session-doaction.md)、 [**Property 屬性 (session 物件)**](session-session.md)，以及 [**session 物件**](session-object.md)的 [**Mode 屬性**](session-mode.md)

您將需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本，才能使用此範例。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiMakCab.vbs \[ 資料庫 \] \[ 基底名稱 \] \[ 選擇性來源位置的路徑\]**

為了產生封包，Makecab.exe 必須在路徑上。 Makecab.exe 公用程式包含在[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。 請注意，此範例不會更新 [媒體資料表](media-table.md) 來處理多個封包。 若要取代內嵌的封包，請包含選項：/R/C/U/E

指定安裝程式資料庫的路徑。 這必須位於來源樹狀結構的根目錄。 為產生的封包檔指定區分大小寫的基底名稱。 如果來源類型為壓縮，則會在根目錄開啟所有檔案。 您可以在命令列上的任何位置指定下列選項。



| 選項              | 描述                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 未指定任何選項 |                                                                                                                                           |
| /C                  | 執行壓縮。 如果未指定/C，WiMakCab.vbs 只會產生 DDF 檔案。                                                        |
| /L                  | 使用 LZX 壓縮而非 MSZIP                                                                                                      |
| /F                  | 將封包大小限制為 1.44 MB 的磁片大小，而不是 CD-ROM                                                                              |
| /U                  | 更新資料庫以參考產生的封包                                                                                    |
| /E                  | 在安裝程式套件中將封包檔內嵌為數據流                                                                               |
| /S                  | 在檔案資料表中使用依目錄排序的序號                                                                             |
| /R                  | 還原為非封包安裝，如果指定了/E，請移除封包 (/R 選項會移除壓縮的 SummaryInfo 屬性 15 & 2)  |



 

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



