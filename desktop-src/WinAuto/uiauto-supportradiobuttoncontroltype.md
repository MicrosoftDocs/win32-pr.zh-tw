---
title: 選項按鈕控制項類型
description: 本主題提供 [選項按鈕] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- 消費者介面自動化，支援選項按鈕控制項類型
- 消費者介面自動化，選項按鈕控制項類型
- 消費者介面自動化，選項按鈕控制項類型的樹狀結構
- 消費者介面自動化，選項按鈕控制項類型的屬性
- 消費者介面自動化，選項按鈕控制項類型的控制項模式
- 消費者介面自動化，選項按鈕控制項類型的事件
- 樹狀結構，選項按鈕控制項類型
- 屬性，選項按鈕控制項類型
- 控制項模式，選項按鈕控制項類型
- 事件、選項按鈕控制項類型
- 選項按鈕控制項類型的支援
- RadioButton 控制項類型
- 選項按鈕控制項類型的控制項類型、樹狀結構
- 控制項類型，選項按鈕控制項類型的控制項模式
- 控制項類型，支援選項按鈕
- 控制項類型，選項按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674668"
---
# <a name="radiobutton-control-type"></a>選項按鈕控制項類型

本主題提供 [ **選項按鈕** ] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

選項按鈕包含一個圓形按鈕和應用程式定義的文字 (標籤)、圖示或點陣圖，其中會指出使用者可以藉由選取按鈕所進行的選擇。 應用程式通常會在群組方塊中使用選項按鈕，讓使用者選擇一組相關但彼此互斥的選項。 例如，應用程式可能會顯示一組選項按鈕，讓使用者可以針對用戶端區域所選取的文字選取偏好的格式。 使用者可以選取對應的選項按鈕，決定要靠左對齊、靠右對齊或置中對齊的格式。 使用者通常一次只能從一組選項按鈕選取一個選項。

> [!Note]  
> 按鈕的另一個控制項一般化，其中只有一個群組中的按鈕可以選取切換按鈕的內容。 某些 UI 架構會將選項按鈕視為特製化切換按鈕。

 

下列章節會定義 **選項按鈕** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有按鈕控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與選項按鈕控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

控制項檢視或內容檢視中沒有任何子系。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與執行 **單選** 按鈕控制項 (類型的控制項（例如按鈕控制項) ）特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值           | 注意                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。      | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。      | 包含整個控制項的最外層矩形。                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。      | 可點按的點必須在按下時，選取選項按鈕。                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true            | 選項按鈕控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true            | 選項按鈕控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。      | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | 選項按鈕控制項的內容會自行標示。                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。      | 對應至 **選項按鈕** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「選項按鈕」。 |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。      | 選項按鈕控制項的名稱是在維持選取狀態的按鈕旁邊顯示的文字。                      |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有選項按鈕控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                               | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | 必要      | 所有的選項按鈕控制項都必須支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，才能讓自己選取。                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | 請參閱備註。    | [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)屬性必須一律完成，讓消費者介面自動化用戶端可以判斷特定內容中的其他選項按鈕彼此之間的關聯。 針對 Microsoft Win32 版本的選項按鈕，不支援這個屬性，因為無法從該舊版 framework 取得這項資訊。 |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | 永不         | 選項按鈕一旦設定就無法循環其狀態。 選項按鈕上永遠不支援 [切換](uiauto-implementingtoggle.md) 控制項模式。                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>必要的事件

下表列出按鈕控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                     | 備註                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。   |                                                                                                                                |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                   | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。       |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。               | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。     |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>備註

選項按鈕表示一組對等選項按鈕之間的單一可選取選項。 在理想的情況下，選項按鈕應該有一個說明對等選項按鈕界限的群組元素。 不過，通常 UI 元素結構會隱含界限。 例如，功能表可能包含一組連續的選項按鈕，而不是功能表項目，或是一組出現在群組標籤之後，但可採取動作的元素（例如按鈕）之前的選項按鈕。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




