---
title: ToolTip 控制項類型
description: 本主題提供工具提示控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 工具提示控制項是包含文字的快顯視窗。
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- 消費者介面自動化，工具提示控制項類型的支援
- 消費者介面自動化，工具提示控制項類型
- 消費者介面自動化，工具提示控制項類型的樹狀結構
- 消費者介面自動化，工具提示控制項類型的屬性
- 消費者介面自動化，工具提示控制項類型的控制項模式
- 消費者介面自動化，工具提示控制項類型的事件
- 樹狀結構，工具提示控制項類型
- 屬性，工具提示控制項類型
- 控制項模式，工具提示控制項類型
- events、ToolTip 控制項類型
- ToolTip 控制項類型的支援
- ToolTip 控制項類型
- 工具提示控制項類型的控制項類型、樹狀結構
- 控制項類型、工具提示控制項類型的控制項模式
- 控制項類型，支援工具提示
- 控制項類型，工具提示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673071"
---
# <a name="tooltip-control-type"></a>ToolTip 控制項類型

本主題提供 **工具提示** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 工具提示控制項是包含文字的快顯視窗。

下列章節會定義 **工具提示** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有工具提示控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與工具提示控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>ToolTip
<ul>
<li>文字 (0 個以上)</li>
<li>影像 (0 個以上)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolTip</li>
</ul></td>
</tr>
</tbody>
</table>



 

只有當工具提示控制項可以接收鍵盤焦點時，才會出現在消費者介面自動化樹狀結構的內容視圖中。 否則，您可以從工具提示所參考專案上的 [**IUIAutomationElement：： CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (或 [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) 屬性取得所有工具提示資訊。

工具提示應該會出現在其資訊所參考的控制項下方。 用戶端必須接聽 [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) ，以確保它們持續取得工具提示中包含的資訊。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **工具提示** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值       | 注意                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。  | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。  | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。  | 可點按的點應該是可關閉控制項的工具提示部分。 某些工具提示沒有這種功能，也不會有可點按的點。                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | 相依     | 如果工具提示控制項可以接收鍵盤焦點，則它必須出現在樹狀結構的內容視圖中。 如果只是文字，則會從引發它的控制項以 [**IUIAutomationElement：： CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (或 [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) 屬性的形式提供。 |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | 對        | 工具提示控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。  | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | 工具提示控制項的內容一律會自行加上標籤。                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。  | 對應到工具提示控制項類型的當地語系化字串。 預設值為 "tooltip"，適用于 en-us 或英文 (美國) 。                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。  | 工具提示控制項的名稱是顯示在工具提示中的文字。                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出工具提示控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                   | 支援 | 注意                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | 相依 | 為了提供更好的協助工具，工具提示控制項可以支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，雖然不是必要的。 當文字有豐富的樣式和屬性 (例如色彩、粗體和斜體) 時，這種文字控制項模式相當有用。 |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | 相依 | 您可以按一下 UI 專案來關閉的工具提示，必須支援 [視窗](uiauto-implementingwindow.md) 控制項模式，才能自動關閉。                                                                                                                 |



 

## <a name="required-events"></a>必要的事件

當工具提示控制項出現在螢幕上時，必須引發 [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) 事件。 此事件會包含工具提示本身之消費者介面自動化專案的參考。

下表列出支援工具提示控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                            | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。          |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                          | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                    |                                                                                                                            |
| [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)                                                          | 如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ 視窗 \_ WindowClosedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。           |
| [**UIA \_ 視窗 \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。           |
| [**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




