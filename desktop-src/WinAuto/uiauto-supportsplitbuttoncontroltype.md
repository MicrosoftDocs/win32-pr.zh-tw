---
title: SplitButton 控制項類型
description: 本主題提供 SplitButton 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- 消費者介面自動化，SplitButton 控制項類型的支援
- 消費者介面自動化，SplitButton 控制項類型
- 消費者介面自動化，SplitButton 控制項類型的樹狀結構
- 消費者介面自動化，SplitButton 控制項類型的屬性
- 消費者介面自動化，SplitButton 控制項類型的控制項模式
- 消費者介面自動化，SplitButton 控制項類型的事件
- 樹狀結構，SplitButton 控制項類型
- properties、SplitButton 控制項類型
- 控制項模式，SplitButton 控制項類型
- events、SplitButton 控制項類型
- SplitButton 控制項類型的支援
- SplitButton 控制項類型
- 控制項類型，SplitButton 控制項類型的樹狀結構
- 控制項類型，SplitButton 控制項類型的控制項模式
- 控制項類型，支援 SplitButton
- 控制項類型，SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674664"
---
# <a name="splitbutton-control-type"></a>SplitButton 控制項類型

本主題提供 **SplitButton** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

分割按鈕控制項可讓您在控制項上執行動作，以及展開控制項以查看其他可能執行的動作清單。

下列章節會定義 **SplitButton** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的分割按鈕控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [SplitButton 控制項類型範例](#splitbutton-control-type-example)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與分割按鈕控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>SplitButton
<ul>
<li>Image (0 或 1)</li>
<li>文字 (0 或 1)</li>
<li>按鈕 (1 或 2)
<ul>
<li>功能表 (0 或 1;顯示為支援 ExpandCollapse 模式之子按鈕的子按鈕) 
<ul>
<li>MenuItem (1 個以上)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>按鈕 (1 或 2)
<ul>
<li>MenuItem (1 個以上)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **SplitButton** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值           | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。      | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。      | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。      | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | 此值與所有使用者介面架構的值相同。                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。      | 說明文字可能指出啟動分割按鈕的結果，而這通常是透過工具提示顯示的相同類型資訊。                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true            | 分割按鈕控制項包含給使用者的資訊。                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true            | 使用者可以看到分割按鈕控制項。                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。      | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | 分割按鈕控制項沒有靜態文字標籤。                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。      | 對應到 **SplitButton** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「分割按鈕」。                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。      | 用來標示分割按鈕的文字。 每次使用影像來標示分割按鈕時，必須提供 [分割按鈕名稱] 屬性的替代文字。                              |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有分割按鈕控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援  | 注意                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 必要 | 因為分割按鈕一律具有展開選項清單的能力，所以必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | 必要 | 因為分割按鈕一律具有與 [**IInvokeProvider：： invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) 方法相關聯的預設動作，所以必須支援 [invoke](uiauto-implementinginvoke.md) 控制項模式。 |



 

## <a name="required-events"></a>必要的事件

下表列出需要支援分割按鈕控制項的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                            |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>SplitButton 控制項類型範例

下圖說明可實 **SplitButton** 控制項類型的控制項。

![顯示 splitbutton 控制項範例的螢幕擷取畫面](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>消費者介面自動化樹狀結構-控制項視圖</th>
<th>消費者介面自動化樹狀結構-內容視圖</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>SplitButton &quot; Name &quot; (Invoke，ExpandCollapse) 
<ul>
<li>按鈕 &quot; 更多選項 (叫用 &quot;) 
<ul>
<li>功能表
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton &quot; Name &quot; (Invoke，ExpandCollapse) 
<ul>
<li>按鈕 &quot; 更多選項 (叫用 &quot;) 
<ul>
<li>功能表
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




