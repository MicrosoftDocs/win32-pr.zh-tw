---
title: 微調控制項類型
description: 本主題提供微調控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- 消費者介面自動化，微調控制項類型的支援
- 消費者介面自動化，微調控制項類型
- 微調控制項類型的樹狀結構消費者介面自動化
- 消費者介面自動化，微調控制項類型的屬性
- 消費者介面自動化，微調控制項類型的控制項模式
- 消費者介面自動化，微調控制項類型的事件
- 樹狀結構，微調控制項類型
- 屬性、微調控制項類型
- 控制項模式，微調控制項類型
- 事件、微調控制項類型
- 微調控制項類型的支援
- Spinner 控制項類型
- 微調控制項類型的控制項類型、樹狀結構
- 控制項類型，微調控制項類型的控制項模式
- 控制項類型，支援微調
- 控制項類型，微調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674667"
---
# <a name="spinner-control-type"></a>微調控制項類型

本主題提供 **微調** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

微調控制項可用來選取某個範圍的項目或數字。

下列章節會定義 **微調** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有 UI 架構/平臺整合控制項類型和控制項模式消費者介面自動化支援的微調控制項。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述在支援 **RangeValue** 和 **選取** 控制項模式時，與微調控制項相關的消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。

**RangeValue 控制項模式**



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
<li>Spinner
<ul>
<li>編輯 (0 或 1 個)</li>
<li>按鈕 (2 個)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Selection 控制項模式**



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
<li>Spinner
<ul>
<li>編輯 (0 或 1 個)</li>
<li>按鈕 (2 個)</li>
<li>清單專案 (0 或更多) </li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner
<ul>
<li>ListItem (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

若要確保「控制視圖」子樹中的兩個按鈕可以透過自動化測試控管來辨別，請適當地將 **ScrollAmount \_ SmallIncrement** 或 [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) 值指派給 **AutomationId** 屬性。 針對某些執行，相關聯的編輯控制項可能是微調控制項的對等。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與微調控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值       | 注意                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。  | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。  | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。  | 微調控制項可點選的點會將焦點置於控制項的編輯部分。                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spinner** | 此值與所有架構的值相同。                                                                                                                                                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 微調控制項必須一律為內容。                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 微調控制項必須一律為控制項。                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。  | 如果控制項可接收鍵盤焦點，就必定支援此屬性。 微調控制項很少會取得焦點，但在這種情況下，焦點應該留在微調控制項本身，而不是子按鈕。 使用者應該可以使用向上鍵和向下鍵來執行所有滾動動作。 |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。  | 微調控制項有靜態文字標籤。                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。  | 對應至 **微調** 控制項類型的當地語系化字串。 針對 en-us 或英文 (美國) ，預設值為 "微調"。                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。  | 微調控制項的名稱通常來自靜態文字標籤。                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有微調控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                         | 支援/值 | 備註                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | 相依       | 橫跨數值範圍的微調控制項可以支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | 相依       | 具有要選取之專案清單的微調控制項，必須支援 [選取](uiauto-implementingselection.md) 控制項模式。 |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | 微調控制項一律是單一選擇容器。                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | 相依       | 橫跨一組 descrete 選項或數位的微調控制項可以支援 [值](uiauto-implementingvalue.md) 控制項模式。    |



 

## <a name="required-events"></a>必要的事件

下表列出微調控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。        | 如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_Selection \_ InvalidatedEventId**](uiauto-event-ids.md) 屬性變更事件。               | 如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                  | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




