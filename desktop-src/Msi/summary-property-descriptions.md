---
description: 下表說明安裝套件、轉換和修補程式的摘要屬性。
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: 摘要屬性描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb93e5881a25b6b79eef0fb0711acc1fec1b6666
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629541"
---
# <a name="summary-property-descriptions"></a>摘要屬性描述

下表說明安裝套件、轉換和修補程式的摘要屬性。 請注意，根據資料庫屬於安裝封裝、轉換或修補封裝，特定摘要屬性的意義可能會不同。 如需屬性識別碼、Pid 和類型的詳細資訊，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。

## <a name="installation-packages"></a>安裝套件



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>摘要屬性</th>
<th>此屬性在安裝資料庫中的意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>標題</strong></a></td>
<td>此檔案的描述做為安裝套件。 描述應該包含片語 &quot; <a href="about-the-installer-database.md">安裝資料庫</a>。&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>主體</strong></a></td>
<td>此封裝所安裝之產品的名稱。 這應該與 <a href="productname.md"><strong>ProductName</strong></a> 屬性中的名稱相同。</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>作者</strong></a></td>
<td>此產品的製造商名稱。 這應該與 [ <a href="manufacturer.md"><strong>製造商</strong></a> ] 屬性中的名稱相同。</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>關鍵字</strong></a></td>
<td>檔案瀏覽器可以用來對檔案進行關鍵字搜尋的關鍵字清單。 關鍵字應該包含 &quot; 安裝程式以及 &quot; 產品特定關鍵字。</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>評論</strong></a></td>
<td>包含片語： &quot; 此安裝程式資料庫包含安裝 <<em>產品名稱</em>所需的邏輯和資料 > 。&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>範本</strong></a> (必要) </td>
<td>與此安裝套件相容的平臺和語言。 請參閱語法的 <a href="template-summary.md"><strong>範本</strong></a> 。</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>上次儲存者</strong></a></td>
<td>資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式會在<a href="administrative-installation.md"><strong>系統管理安裝</strong></a>期間將此屬性設為<a href="logonuser.md"><strong>LogonUser</strong></a>屬性的值。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。</td>
</tr>
<tr class="even">
<td> (必要的<a href="revision-number-summary.md"><strong>修訂編號</strong></a>) </td>
<td>包含安裝程式套件的 <a href="package-codes.md">封裝程式碼</a> 。</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>前次列印時間</strong></a></td>
<td>可以設定為 <a href="administrative-installation.md">系統管理安裝</a> 期間的日期和時間，以在建立系統管理映射時錄製。</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>建立時間/日期</strong></a></td>
<td>此安裝程式資料庫的建立時間和日期。</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>上次儲存的時間/日期</strong></a></td>
<td>上次儲存安裝程式資料庫時的目前系統時間和日期。 一開始是 null。</td>
</tr>
<tr class="even">
<td>需要 (<a href="page-count-summary.md"><strong>頁面計數</strong></a>) </td>
<td>包含用來識別此安裝套件所需之最小安裝程式版本的值。 例如，如果封裝至少需要2.0 版的安裝程式，則此屬性應該設定為200的整數。
<blockquote>
[!Note]<br />
這個屬性的值必須是200或更高的<a href="64-bit-windows-installer-packages.md">64 位 Windows Installer 套件</a>。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>需要 (<a href="word-count-summary.md"><strong>字數統計</strong></a>) </td>
<td>來源檔案映射的類型。 儲存以取代標準計數屬性。 這個屬性是位欄位。 請參閱 [ <a href="word-count-summary.md"><strong>字數統計</strong></a> ] 主題以取得值。<br/> 從 Windows Vista 上的 Windows Installer 4.0 版開始，這個屬性會包含用來指定是否需要提高許可權的位。<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>字元計數</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>正在建立應用程式</strong></a></td>
<td>包含用來撰寫此安裝資料庫之軟體的名稱。</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>安全性</strong></a></td>
<td>這個屬性的值應該是2建議的唯讀。</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>字碼頁</strong></a></td>
<td>用來顯示摘要資訊的 ANSI 字碼頁數值。 在摘要資訊中設定任何字串屬性之前，必須先設定這個屬性。</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>轉換



| 摘要屬性                                              | 轉換中這個屬性的意義                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標題**](title-summary.md)                                | 這個檔案做為轉換的描述。 描述應該包含「[轉換](database-transforms.md)」這個片語。                                                                                                                                                                     |
| [**主體**](subject-summary.md)                            | 原始安裝套件所安裝的產品名稱。 這應該與原始安裝套件中的 [主旨 [**摘要**](subject-summary.md) ] 屬性值相同。                                                                                            |
| [**作者**](author-summary.md)                              | 此轉換的製造商名稱。                                                                                                                                                                                                                                                   |
| [**關鍵字**](keywords-summary.md)                          | 檔案瀏覽器可以用來對檔案進行關鍵字搜尋的關鍵字清單。 關鍵字應該包含「安裝程式」，以及產品特定的關鍵字。                                                                                                                             |
| [**評論**](comments-summary.md)                          | 包含片語：「此轉換包含安裝 <*產品名稱*> 所需的邏輯和資料。」                                                                                                                                                                                     |
| [**範本**](template-summary.md) (必要)                | 與此轉換相容的平臺和語言版本。 如果沒有任何限制，此值可以保留空白。 只能為轉換指定一種語言。 如需語法的詳細資訊，請參閱 [**範本**](template-summary.md)。                                |
| [**上次儲存者**](last-saved-by-summary.md)                | 在資料庫轉換之後， (s 的平臺和語言識別項) 。 新資料庫中的 [ [**範本摘要**](template-summary.md) ] 屬性應該設定為相同的值。                                                                                              |
|  (必要的 [**修訂編號**](revision-number-summary.md))  | 新的和原始產品的產品代碼 Guid 和版本清單，以及升級程式碼 GUID。 清單會以分號分隔，如下所示。 *原始產品-程式碼原始-版本*;*新產品程式碼新產品-版本*; *升級-程式碼*<br/>                       |
| [**前次列印時間**](last-printed-summary.md)                  | Null                                                                                                                                                                                                                                                                                              |
| [**建立時間/日期**](create-time-date-summary.md)          | 建立轉換的時間和日期。                                                                                                                                                                                                                                                 |
| [**上次儲存的時間/日期**](last-saved-time-date-summary.md)  | 儲存轉換時目前的系統時間和日期。 一開始是 null。                                                                                                                                                                                                             |
| 需要 ([**頁面計數**](page-count-summary.md))            | 值，用來指出處理轉換所需的最低安裝程式版本。 此值應該設定為屬於用來產生轉換之資料庫的兩個 [**頁面計數**](page-count-summary.md) 屬性值的最大值。                                 |
| 需要 ([**字數統計**](word-count-summary.md))            | Null                                                                                                                                                                                                                                                                                              |
| [**字元計數**](character-count-summary.md)            | 摘要資訊資料流程的這個部分分成 2 16 位單字。 上方文字包含 [*轉換驗證旗標*](t-gly.md)。 下方的單字包含 [*轉換錯誤條件旗標*](t-gly.md)。 |
| [**正在建立應用程式**](creating-application-summary.md)  | 包含用來建立此轉換之軟體的名稱。                                                                                                                                                                                                                                  |
| [**安全性**](security-summary.md)                          | 這個屬性的值應該是4強制的唯讀。                                                                                                                                                                                                                                      |
| [**字碼頁**](codepage-summary.md)                          | 用來顯示摘要資訊的 ANSI 字碼頁數值。 必須先設定這個屬性，才能在摘要資訊中設定任何字串屬性。                                                                                                                    |



 

## <a name="patch-packages"></a>修補套件



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>摘要屬性</th>
<th>修補程式套件中這個屬性的意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>標題</strong></a></td>
<td>此檔案作為修補封裝的描述。 描述應該包含片語： &quot; <a href="patch-packages.md">Patch</a>。&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>主體</strong></a></td>
<td>包含產品名稱之修補程式的描述。</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>作者</strong></a></td>
<td>Patch 封裝的製造商名稱。</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>關鍵字</strong></a></td>
<td>以分號分隔的修補程式來源清單。</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>評論</strong></a></td>
<td>包含片語： &quot; 此修補套裝程式含安裝 <<em>產品名稱</em>所需的邏輯和資料 > 。&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>範本</strong></a> (必要) </td>
<td>以分號分隔的產品代碼清單，可接受此修補程式。</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>上次儲存者</strong></a></td>
<td>以分號分隔的轉換 substorage 名稱清單（以這個修補程式套用的順序排列）。</td>
</tr>
<tr class="even">
<td> (必要的<a href="revision-number-summary.md"><strong>修訂編號</strong></a>) </td>
<td>包含修補程式的 GUID 修補程式碼。 之後可能會有修補程式的程式碼 Guid 清單，這些修補程式會在套用此修補程式時移除。 系統會串連修補程式碼，而不使用分隔符號分隔清單中的 Guid。
<blockquote>
[!Note]<br />
如果 patch 套件包含 <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> 資料表，修補程式不會移除目前修補程式的 GUID 之後所列的修補程式。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>前次列印時間</strong></a></td>
<td>Null</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>建立時間/日期</strong></a></td>
<td>建立修補檔案的時間和日期。</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>上次儲存的時間/日期</strong></a></td>
<td>儲存修補程式套件時的目前系統時間和日期。 此值一開始是 null。</td>
</tr>
<tr class="even">
<td>需要 (<a href="page-count-summary.md"><strong>頁面計數</strong></a>) </td>
<td>Null</td>
</tr>
<tr class="odd">
<td>需要 (<a href="word-count-summary.md"><strong>字數統計</strong></a>) </td>
<td>包含值，指出安裝修補程式所需的最小 Windows Installer 版本。 文字計數值為4的 patch 需要 Windows Installer 3.0 版或更高版本，才能套用修補程式。 值為3表示需要 Windows Installer 版本2.0 或更高版本。 值為2表示需要 Windows Installer 版本1.2 或更高版本。 預設值為 1。</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>字元計數</strong></a></td>
<td>Null</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>正在建立應用程式</strong></a></td>
<td>用來建立修補程式的軟體名稱。</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>安全性</strong></a></td>
<td>這個屬性的值應該是4強制的唯讀。</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>字碼頁</strong></a></td>
<td>用來顯示摘要資訊的 ANSI 字碼頁數值。 在摘要資訊中設定任何字串屬性之前，必須先設定這個屬性。</td>
</tr>
</tbody>
</table>



 

 

 




