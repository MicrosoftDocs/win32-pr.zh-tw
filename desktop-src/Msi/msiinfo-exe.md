---
description: Msiinfo.exe 是一種命令列公用程式，它會使用資料庫函數和安裝程式函數來編輯或顯示資料庫的摘要資訊資料流程。
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851799"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe 是一種命令列公用程式，它會使用 [資料庫函數](database-functions.md) 和 [安裝程式函數](installer-functions.md) 來編輯或顯示資料庫的 [摘要資訊資料流程](summary-information-stream.md) 。

## <a name="syntax"></a>Syntax

**MsiInfo** *{database} \[ \[ /b \] /d \] {option} {data}*

-   資料庫不可以是唯讀資料庫。
-   如果沒有任何資料在選項之後，就會移除對應的屬性。
-   您可以在命令列上指定最多20個選項。 您可以多次指定相同的屬性。
-   如果資料包含空格，請使用引號來括住資料。 例如，例如/T 「MY TITLE」。

## <a name="command-line-options"></a>命令列選項

Msiinfo.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。 如需詳細資訊，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。



| 選項 | Description                                                                                                                                                                                                                                                                                                                                                      | 屬性識別碼        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| 無 | 如果未指定任何選項，則公用程式會顯示摘要資訊屬性的目前值。                                                                                                                                                                                                                                                      |                    |     |
| -b     | 顯示字串集區中每個字串的相關資訊。 如果同時使用-d，-b 選項才有效，而-b 必須在-d 選項之前。                                                                                                                                                                                                                 |                    |     |
| -d     | 顯示字串集區的相關資訊。 驗證字串集區，並提供資料庫之字碼頁的相關資訊。 請注意，資料庫的字碼頁與摘要資訊資料流程的字碼頁不同 (PID \_ 字碼頁) 。 此選項也會檢查每個字串，是否有資料庫的字碼頁中不正確字元。 |                    |     |
| -i     | 不適用。 保留的。                                                                                                                                                                                                                                                                                                                                        | PID \_ 字典    | 0   |
| -c     | 設定 [**字碼頁的摘要屬性**](codepage-summary.md)。                                                                                                                                                                                                                                                                                                  | PID \_ 字碼頁      | 1   |
| -t     | 設定 [**標題摘要屬性**](title-summary.md)。                                                                                                                                                                                                                                                                                                        | PID \_ 標題         | 2   |
| -j     | 設定 [ [**主體摘要] 屬性**](subject-summary.md)。                                                                                                                                                                                                                                                                                                    | 識別碼 PID \_ 主體    | 3   |
| -a     | 設定 [ [**作者摘要] 屬性**](author-summary.md)。                                                                                                                                                                                                                                                                                                      | PID \_ 作者        | 4   |
| -k     | 設定 [**關鍵字的摘要屬性**](keywords-summary.md)。                                                                                                                                                                                                                                                                                                  | PID \_ 關鍵字      | 5   |
| -o     | 設定 [**批註摘要屬性**](comments-summary.md)。                                                                                                                                                                                                                                                                                                  | PID \_ 批註      | 6   |
| -p     | 設定 [**範本摘要屬性**](template-summary.md)。                                                                                                                                                                                                                                                                                                  | PID \_ 範本      | 7   |
| -l     | 設定 [**上次儲存的摘要屬性**](last-saved-by-summary.md)。                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | 設定 [ [**修訂編號摘要] 屬性**](revision-number-summary.md)。                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | 不適用。 保留的。                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | 設定 [**最後列印的摘要屬性**](last-printed-summary.md)。 若要指定 year、month、day、hour、minute 和 second，請使用 "yyyy/mm/dd hh： mm： ss" 格式。 例如 "1997/06/20 03:25:59"。                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | 設定 [**建立時間/日期的摘要屬性**](create-time-date-summary.md)。 若要指定 year、month、day、hour、minute 和 second，請使用 "yyyy/mm/dd hh： mm： ss" 格式。 例如 "1997/06/20 03:25:59"。                                                                                                                                             | PID \_ 建立 \_ DTM   | 12  |
| -Q     | 設定 [**上次儲存的時間/日期摘要屬性**](last-saved-time-date-summary.md)。 若要指定 year、month、day、hour、minute 和 second，請使用 "yyyy/mm/dd hh： mm： ss" 格式。 例如 "1997/06/20 03:25:59"。                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | 設定 [ [**頁面計數摘要] 屬性**](page-count-summary.md)。                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | 設定 [**字數統計摘要屬性**](word-count-summary.md)。                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | 設定 [ [**字元計數] 摘要屬性**](character-count-summary.md)。                                                                                                                                                                                                                                                                                    | PID \_ >CHARCOUNT     | 16  |
|        | 不適用。 保留的。                                                                                                                                                                                                                                                                                                                                        | PID \_ 縮圖     | 17  |
| -n     | 設定 [**建立應用程式摘要屬性**](creating-application-summary.md)。                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | 設定 [**安全性摘要屬性**](security-summary.md)。                                                                                                                                                                                                                                                                                                  | PID \_ 安全性      | 19  |



 

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



