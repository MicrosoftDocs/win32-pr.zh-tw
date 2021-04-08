---
title: CheckBox 控制項類型
description: 本主題提供 [CheckBox] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- 消費者介面自動化，CheckBox 控制項類型的支援
- 消費者介面自動化，CheckBox 控制項類型
- 消費者介面自動化，CheckBox 控制項類型的樹狀結構
- 消費者介面自動化，CheckBox 控制項類型的屬性
- 消費者介面自動化，CheckBox 控制項類型的控制項模式
- 消費者介面自動化，CheckBox 控制項類型的事件
- 樹狀結構，CheckBox 控制項類型
- 屬性，CheckBox 控制項類型
- 控制項模式，CheckBox 控制項類型
- 事件，CheckBox 控制項類型
- CheckBox 控制項類型的支援
- CheckBox 控制項類型
- CheckBox 控制項類型的控制項類型、樹狀結構
- 控制項類型，CheckBox 控制項類型的控制項模式
- 控制項類型，支援核取方塊
- 控制項類型，核取方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839968"
---
# <a name="checkbox-control-type"></a>CheckBox 控制項類型

本主題提供 [ **CheckBox]** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

核取方塊是用來表示狀態的物件，使用者可與之互動以循環狀態。 對使用者來說，核取方塊會顯示成二元 (是/否) 或 (開/關) 選項或三元 (開、關、未定) 選項。

下列章節會定義 **CheckBox** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有核取方塊控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [DefaultAction](#defaultaction)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與核取方塊控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>CheckBox</li>
</ul></td>
<td><ul>
<li>CheckBox</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **CheckBox** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 這個屬性的值必須一律為 **TRUE**。 這表示核取方塊控制項必須一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 這個屬性的值必須一律為 **TRUE**。 這表示核取方塊控制項必須一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | 核取方塊控制項為自我標記。                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應至 **CheckBox** 控制項類型的當地語系化字串。 針對 en-us 或英文 (美國) ，預設值為 [核取方塊]。                                                                                                                                            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 核取方塊控制項的 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (或 [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) 屬性的值是在維持切換狀態的方塊旁邊顯示的文字。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有核取方塊控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                  | 支援/值 | 備註                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | 必要      | 核取方塊支援 [切換](uiauto-implementingtoggle.md) 控制項模式，可讓您透過程式設計的方式，在其內部狀態中迴圈執行核取方塊。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的核取方塊控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。    |                                                                                                                            |



 

## <a name="defaultaction"></a>DefaultAction

核取方塊的預設動作是使選項按鈕成為焦點，並切換其目前的狀態。 如先前所述，核取方塊會顯示二進位 (Yes/No 或 On/Off) 決策給使用者，或第三 (On、Off、不定) 。 如果核取方塊是二元的，那麼預設動作就會讓「開」狀態變成「關」，或是「關」狀態變成「開」。 在第三個核取方塊中，預設動作會依相同順序迴圈查看核取方塊的狀態，就像使用者已傳送連續的滑鼠點給控制項一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




