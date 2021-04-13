---
title: 驗證常式
description: 本節說明 UI 協助工具檢查程式可以執行的驗證常式，以測試應用程式的協助工具實作為測試。
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300987"
---
# <a name="verification-routines"></a>驗證常式

本節說明 UI 協助工具檢查程式可以執行的驗證常式，以測試應用程式的協助工具實作為測試。



<table>
<thead>
<tr class="header">
<th>類別</th>
<th>常式傳回的值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>一致性</strong>$ {REMOVE} $<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>編譯驗證目標中所有可見的元素，並以標準螢幕讀取器向使用者宣告的順序，將這些專案顯示在 ListView 控制項中。</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>與 <strong>ScreenReader</strong>相同，但適用于 UIA 的執行。</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>導覽</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認目標的 UI 不太複雜，或無法使用標準鍵盤流覽來存取。</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認可以使用標準鍵盤流覽，以合理的邏輯方式連線到 UI 中的所有可設定的元素。</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Properties</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckRole</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 角色，且該控制項具有該角色所需的值。</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 狀態。</td>

</tr>
<tr class="odd">
<td><strong>CheckName</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 名稱。</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>確認指派給驗證目標中專案的存取金鑰在驗證目標內是唯一的。</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>確認 UI 中的每個可設定焦點專案都有周框，可用來做為點擊測試的目標。</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Tree</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>專案樹狀結構中的父系和子系關聯性一致且可預測。</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的 MSAA 父系。</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>UIA 屬性</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 名稱。</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認 UIA 目標 UI 中的元素時，不太複雜或無法使用標準鍵盤流覽。</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 狀態。</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>確認同輩元素沒有相同的存取和/或快速鍵。</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>確認 UI 中的每個可設定焦點 UIA 元素都有周框，可用來做為點擊測試的目標。</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 控制項類型。</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>UIA Tree</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>確認 UIA TreeWalker 可以流覽元素的子系。</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>確認 UI 中的每個可設定焦點元素都會報告有效的 UIA 父系。</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>確認同輩元素沒有相同的名稱： ControlType 組，也沒有相同的 AutomationId。</td>

</tr>
<tr class="odd">
<td>$ {ROWSPAN9} $<strong>ARIA Web 驗證</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>確認所有元素都具有有效的 ARIA 角色。 相關聯的 HTML 標籤和 ARIA 角色是有無效角色標示為錯誤的資訊元素。</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>確認具有輸入、按鈕、影像按鈕或地標角色的每個元素都有一個標籤。</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>確認具有滑杆或進度列角色的範圍控制項已定義適當的 ARIA 屬性。</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>確認元素（或至少一個子系）已定義 onkeydown/onkeypress。</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>確認資料表配置具有內含的摘要/th/aria describedby。</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>確認具有方格角色的非資料表專案具有方格>資料列的結構，>gridcell 有相關聯的屬性。</td>

</tr>
<tr class="odd">
<td><strong>CheckDataTable</strong></td>
<td>確認資料表的屬性。</td>

</tr>
<tr class="even">
<td><strong>CheckActiveDescendants</strong></td>
<td>確認已定義作用中子系的元素屬性。</td>

</tr>
<tr class="odd">
<td><strong>CheckElementsWithClickHandler</strong></td>
<td>使用按一下處理常式來確認專案的索引標籤索引。</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Web 驗證</strong>$ {REMOVE} $<br />
</td>
<td><strong>CheckHtml (Web) </strong></td>
<td>確認各種 HTML 特性，例如標頭、名稱、框架和標題。</td>
</tr>
<tr class="odd">
<td><strong>CheckName (Web) </strong></td>
<td>確認名稱特性，例如長度、無效字元和角色包含。</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web) </strong></td>
<td>確認不正確角色、應該具有值的角色，以及/或未執行的角色。</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 




