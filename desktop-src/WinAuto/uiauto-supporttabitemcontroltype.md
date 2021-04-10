---
title: TabItem 控制項類型
description: 本主題提供 TabItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- 消費者介面自動化，TabItem 控制項類型的支援
- 消費者介面自動化，TabItem 控制項類型
- 消費者介面自動化，TabItem 控制項類型的樹狀結構
- 消費者介面自動化，TabItem 控制項類型的屬性
- 消費者介面自動化，TabItem 控制項類型的控制項模式
- 消費者介面自動化，TabItem 控制項類型的事件
- 樹狀結構，TabItem 控制項類型
- properties、TabItem 控制項類型
- 控制項模式，TabItem 控制項類型
- events、TabItem 控制項類型
- TabItem 控制項類型的支援
- TabItem 控制項類型
- 控制項類型，TabItem 控制項類型的樹狀結構
- 控制項類型，TabItem 控制項類型的控制項模式
- 控制項類型，支援 TabItem
- 控制項類型，TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183938"
---
# <a name="tabitem-control-type"></a>TabItem 控制項類型

本主題提供 **TabItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

索引標籤項目控制項是做為索引標籤控制項內的控制項，可選取要顯示在視窗中的特定頁面。

下列章節會定義 **TabItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的索引標籤專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與索引標籤專案控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>TabItem
<ul>
<li>Image (0 或 1)</li>
<li>Text</li>
<li>窗格
<ul>
<li>不同控制項 (0 或更多)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>TabItem
<ul>
<li>窗格
<ul>
<li>不同控制項 (0 或更多)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **TabItem** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值       | 注意                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。  | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。  | 包含整個控制項的最外層矩形。                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。  | 索引標籤項目控制項必須具有能讓項目成為選取項目的可點選的點。                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | 請參閱備註。  | 此屬性可做為相關聯索引標籤窗格的指標。 這在無法以索引標籤項目物件子系來裝載窗格時非常有用。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TabItem** | 此值與所有使用者介面架構的值相同。                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 索引標籤專案控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 索引標籤專案控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。  | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null        | 索引標籤項目控制項沒有靜態文字標籤。                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。  | 對應到 **TabItem** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「tab 專案」。       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。  | 索引標籤專案控制項自行加上標籤。                                                                                                          |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有索引標籤專案控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                 | 支援  | 注意                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | 必要 | 索引標籤專案控制項必須支援 [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern)。 |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | 永不    | 索引標籤專案控制項永遠不支援 [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)。             |



 

## <a name="required-events"></a>必要的事件

下表列出索引標籤專案控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                     | 備註                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。   |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                   | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。               | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




