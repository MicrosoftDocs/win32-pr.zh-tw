---
title: SemanticZoom 控制項類型
description: 本主題提供 SemanticZoom 控制項類型之消費者介面自動化支援的相關資訊。
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- 消費者介面自動化，SemanticZoom 控制項類型的支援
- 消費者介面自動化，SemanticZoom 控制項類型
- 消費者介面自動化，SemanticZoom 控制項類型的樹狀結構
- 消費者介面自動化，SemanticZoom 控制項類型的屬性
- 消費者介面自動化，SemanticZoom 控制項類型的控制項模式
- 消費者介面自動化，SemanticZoom 控制項類型的事件
- 樹狀結構，SemanticZoom 控制項類型
- properties、SemanticZoom 控制項類型
- 控制項模式，SemanticZoom 控制項類型
- events、SemanticZoom 控制項類型
- SemanticZoom 控制項類型的支援
- SemanticZoom 控制項類型
- 控制項類型，SemanticZoom 控制項類型的樹狀結構
- 控制項類型，SemanticZoom 控制項類型的控制項模式
- 控制項類型，支援 SemanticZoom
- 控制項類型，SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49609b7bc2b3958b6041bcf3a8c2c6442ce38501f95ff75a6c0f2145d497436f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825474"
---
# <a name="semanticzoom-control-type"></a>SemanticZoom 控制項類型

本主題提供 **SemanticZoom** 控制項類型之消費者介面自動化支援的相關資訊。

「語義縮放」是 Windows 8 引進的一項技術，可在單一視圖內呈現和導覽大型相關資料集或內容，例如相片專輯、應用程式清單或通訊錄。 語義縮放會使用兩種不同的分類模式（或 *縮放層級*）來組織和呈現內容。 低層級 (或 *放大*) 模式會以平面、「全功能」結構顯示專案;而高階 (或 *放大*) 模式會顯示群組中的專案，讓使用者可以快速流覽和流覽內容。 例如，縮放城市清單可能會變更為包含這些城市的州清單。 縮放程式清單可能會變更為邏輯程式群組清單。

如需語義縮放的詳細資訊（特別是用於 Windows Store 應用程式），請參閱[語義縮放的指導方針](/windows/uwp/controls-and-patterns/semantic-zoom)。

**SemanticZoom** 控制項類型的使用方式模型很不尋常，因為它主要是用來進行程式設計存取。 Microsoft 消費者介面自動化用戶端可以監視和操作語義縮放控制項，以控制清單的放大狀態。 未使用輔助技術的使用者通常會透過觸控手勢或鍵盤快速鍵直接操作語義縮放控制項。

下列章節會定義 **SemanticZoom** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的語義縮放控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式和屬性](#required-control-patterns-and-properties)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述 **SemanticZoom** 控制項類型之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>控制項檢視</th>
<th>內容檢視</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>List
<ul>
<li>[SemanticZoom]
<ul>
<li>ListItem (0 個以上)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>ListItem (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

或：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>控制項檢視</th>
<th>內容檢視</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>[SemanticZoom]
<ul>
<li>List
<ul>
<li>ListItem (0 個以上)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>ListItem (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與執行 **SemanticZoom** 控制項類型的控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>使用者介面自動化屬性</th>
<th>值</th>
<th>注意</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>包含整個控制項的最外層矩形。</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>如果清單控制項具有可點按的點 (可按一下以使清單取得焦點) 的點，則必須透過這個屬性公開該點。 如果 <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> 屬性的值為 <strong>TRUE</strong>，則嘗試取得此屬性會導致 <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> 錯誤。</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></td>
<td><strong>SemanticZoom</strong></td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></td>
<td>true</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></td>
<td>true</td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></td>
<td>FALSE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>如果有靜態文字標籤，這個屬性必須公開該控制項的參考。</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>對應到 <strong>SemanticZoom</strong> 控制項類型的當地語系化字串。 預設值為 &quot; &quot; En-us 或英文 (美國) 的語義縮放。
<blockquote>
[!Note]<br />
某些架構將此串連為 &quot; semanticzoom &quot; 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>請參閱備註。</td>
<td>空字串是可接受的，或是可以提供更有用的名稱，只要它不包含「語義比例」詞彙，這會讓控制項類型和名稱的組合混淆。</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>必要的控制項模式和屬性

下表列出所有語義縮放控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                  | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | 相依       | 語義縮放控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，允許啟用或停用縮放。 [**ToggleState \_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) 對應于 [一般]、[全部啟動] 狀態，而 [ [**ToggleState \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) ] 對應至 [高階]、[放大] 視圖。 |



 

## <a name="required-events"></a>必要的事件

下表列出需要語義縮放控制項才能支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。    |                                                                                                                            |



 

## <a name="remarks"></a>備註

如果 UI 具有切換語義縮放控制項行為的可見按鈕，此按鈕就不應該有 **SemanticZoom** 控制項類型。 這是可直覺化的，但 **SemanticZoom** 控制項類型是指縮放內容容器的特性，而不是控制縮放的按鈕。 您可以使用[切換](uiauto-implementingtoggle.md)控制項模式，以[按鈕](uiauto-supportbuttoncontroltype.md)控制項類型來表示 (這類按鈕。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

