---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiSumInf.vbs。 此範例腳本可用來管理 Windows Installer 封裝的摘要資訊串流。
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: 管理摘要資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5ad72ee4f308831077ec2f732b92a70f407c560b204d10f2d3db63d1bb9bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926968"
---
# <a name="manage-summary-information"></a>管理摘要資訊

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiSumInf.vbs。 此範例腳本可用來管理 Windows Installer 封裝的[摘要資訊串流](summary-information-stream.md)。

此範例將示範如何使用：

-   [**SummaryInformation 屬性 (安裝程式物件)**](installer-summaryinformation.md)
-   [](installer-lasterrorrecord.md) [**安裝程式物件** 的 LastErrorRecord 方法](installer-object.md)

使用此範例需要 Windows 腳本主機的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiSumInf.vbs \[ 資料庫 \] \[ 屬性 = 值的路徑\]**

指定 Windows Installer 資料庫的路徑。 如果未指定其他引數，腳本會列出封裝的所有摘要屬性。 使用 format Property = value，指定要更新的摘要屬性和值清單。 您可以透過如下所示的名稱或 PID 值來指定屬性。 日期和時間欄位使用目前的地區設定格式，或 "Now" 或 "Date"。 如需詳細資訊，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。



| PID | 名稱        | 描述                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | 摘要資訊中文字字串的 ANSI 字碼頁。 如需詳細資訊，請參閱 [**字碼頁摘要**](codepage-summary.md) 屬性。                                                                                                                                                           |
| 2   | 標題       | Windows Installer 封裝的類型。 如需詳細資訊，請參閱 [**標題摘要屬性**](title-summary.md)。                                                                                                                                                                                    |
| 3   | 主旨     | 完整的產品名稱。 如需詳細資訊，請參閱 [**主題摘要屬性**](subject-summary.md)。                                                                                                                                                                                               |
| 4   | 作者      | 建立者，通常是廠商名稱。 如需詳細資訊，請參閱 [**作者摘要屬性**](author-summary.md)。                                                                                                                                                                                     |
| 5   | 關鍵字    | 檔案瀏覽器所使用的關鍵字清單。 如需詳細資訊，請參閱 [**關鍵字摘要屬性**](keywords-summary.md)。                                                                                                                                                                       |
| 6   | 註解    | 封裝用途或使用的描述。 如需詳細資訊，請參閱 [**批註摘要屬性**](comments-summary.md)。                                                                                                                                                                       |
| 7   | 範本    | 支援的平臺和語言。 如需詳細資訊，請參閱 [**範本摘要屬性**](template-summary.md)。                                                                                                                                                                              |
| 8   | LastAuthor  | 僅由安裝程式設定。 如需詳細資訊，請參閱 [**上次儲存的摘要屬性**](last-saved-by-summary.md)。                                                                                                                                                                            |
| 9   | 修訂版    | 封裝程式碼 GUID。 如需詳細資訊，請參閱 [**修訂編號摘要屬性**](revision-number-summary.md)。                                                                                                                                                                                |
| 11  | 印刷     | 安裝映射的日期和時間。 如需詳細資訊，請參閱 [**上次列印的摘要屬性**](last-printed-summary.md)。                                                                                                                                                                    |
| 12  | 建立時間     | 封裝建立的日期和時間。 如需詳細資訊，請參閱 [**建立時間/日期摘要屬性**](create-time-date-summary.md)。                                                                                                                                                              |
| 13  | 已儲存       | 上次修改封裝的日期和時間。 如需詳細資訊，請參閱 [**上次儲存的時間/日期摘要屬性**](last-saved-time-date-summary.md)。                                                                                                                                             |
| 14  | 頁面       | 此封裝所需 Windows Installer 的最小版本。 如需詳細資訊，請參閱 [**頁面計數摘要屬性**](page-count-summary.md)。                                                                                                                                             |
| 15  | 的話       | 來源檔案映射的類型。 如需詳細資訊，請參閱 [**字數統計摘要屬性**](word-count-summary.md)。從 Windows Vista 和 Windows Server 2008 上的 Windows Installer 4.0 版開始，這個屬性會包含用來指定是否需要提升許可權的位。<br/> |
| 16  | Characters  | 僅用於轉換。 [**字元計數**](character-count-summary.md)。                                                                                                                                                                                                                    |
| 18  | 應用程式 | 與此檔案相關聯的應用程式，也就是「Windows Installer」。 如需詳細資訊，請參閱 [**建立應用程式摘要屬性**](creating-application-summary.md)。                                                                                                                        |
| 19  | 安全性    | 安全性設定。 如需詳細資訊，請參閱 [**安全性摘要屬性**](security-summary.md)。                                                                                                                                                                                               |



 

如需其他腳本範例，請參閱[Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows 腳本主機的範例公用程式，請參閱[Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 




