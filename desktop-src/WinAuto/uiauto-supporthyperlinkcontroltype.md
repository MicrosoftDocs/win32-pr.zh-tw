---
title: Hyperlink 控制項類型
description: 本主題提供超連結控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- 消費者介面自動化，支援 Hyperlink 控制項類型
- 消費者介面自動化，超連結控制項類型
- 消費者介面自動化，超連結控制項類型的樹狀結構
- 消費者介面自動化，超連結控制項類型的屬性
- 消費者介面自動化，超連結控制項類型的控制項模式
- 消費者介面自動化，超連結控制項類型的事件
- 樹狀結構，超連結控制項類型
- 屬性，超連結控制項類型
- 控制項模式，超連結控制項類型
- 事件，超連結控制項類型
- Hyperlink 控制項類型的支援
- Hyperlink 控制項類型
- 控制項類型，超連結控制項類型的樹狀結構
- 控制項類型，超連結控制項類型的控制項模式
- 控制項類型，支援超連結
- 控制項類型，超連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673075"
---
# <a name="hyperlink-control-type"></a>Hyperlink 控制項類型

本主題提供 **超連結** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

超連結控制項可建立連結，讓使用者在同一個頁面中或從一個頁面流覽至另一個頁面。

下列章節會定義 **超連結** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有超連結控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述超連結控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>Hyperlink</li>
</ul></td>
<td><ul>
<li>Hyperlink</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與超連結控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值         | 注意                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。    | 這個屬性的值在應用程式中的所有控制項之間必須是唯一的。                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。    | 包含整個控制項的最外層矩形。                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。    | 如果按一下滑鼠指標，超連結控制項的可按點必須是啟動超連結的點。                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **超連結** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 此超連結控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 此超連結控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。    | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。    | 如果有靜態文字標籤，這個屬性必須公開該控制項的參考。                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。    | 對應至 **超連結** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的 [超連結]。 |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。    | 超連結控制項的名稱是顯示在畫面上以加上底線的文字。                                                  |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出超連結控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                  | 支援/值                | 備註                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | 必要                     | 所有超連結控制項都必須支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式。                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | 相依                      | 當連結包含可供使用者使用且有意義的資訊時，超連結控制項應支援 [值](uiauto-implementingvalue.md) 控制項模式。                                                                              |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | 例如，"https://www..." | 網際網路或內部網路位址的 URL 是超連結的範例，其中包含對使用者有意義的資訊。 不過，程式設計連結只對應用程式有意義，因此不建議用於 **Value** 屬性。 |



 

## <a name="required-events"></a>必要的事件

下表列出超連結控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>備註

Hyperlink 控制項類型應該只套用至物件，當按下時，就會導致導覽。它不應該套用至超連結的容器。 例如，只有影像地圖內可按的「作用點」才會有 **超連結** 控制項類型。 文字欄位或檔容器中的超連結也是如此。 在此情況下，只有超連結文字或影像應該有 **超連結** 控制項類型，而不是容器。

[文字](uiauto-implementingtextandtextrange.md)控制項模式非常適合用來支援文字或檔元素中的內嵌超連結。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




