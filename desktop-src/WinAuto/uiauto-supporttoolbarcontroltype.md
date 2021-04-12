---
title: ToolBar 控制項類型
description: 本主題提供工具列控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 工具列控制項可讓使用者啟動應用程式內所含的命令和工具。
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- 消費者介面自動化，ToolBar 控制項類型的支援
- 消費者介面自動化，ToolBar 控制項類型
- 消費者介面自動化，工具列控制項類型的樹狀結構
- 消費者介面自動化，工具列控制項類型的屬性
- 消費者介面自動化，工具列控制項類型的控制項模式
- 消費者介面自動化，ToolBar 控制項類型的事件
- 樹狀結構，工具列控制項類型
- 屬性、工具列控制項類型
- 控制項模式、工具列控制項類型
- 事件、工具列控制項類型
- ToolBar 控制項類型的支援
- ToolBar 控制項類型
- 控制項類型、工具列控制項類型的樹狀結構
- 控制項類型、工具列控制項類型的控制項模式
- 控制項類型，支援工具列
- 控制項類型，工具列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372569"
---
# <a name="toolbar-control-type"></a>ToolBar 控制項類型

本主題提供 **工具列** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 工具列控制項可讓使用者啟動應用程式內所含的命令和工具。

下列章節會定義 **工具列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有工具列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與工具列控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>ToolBar
<ul>
<li>不同控制項 (0 或更多)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolBar
<ul>
<li>不同控制項 (0 或更多)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

工具列控制項可以在其子樹內包含任何類型的控制項。 通常包含按鈕、下拉式方塊與分割按鈕。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **工具列** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值       | 注意                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。  | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。  | 包含整個控制項的最外層矩形。                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。  | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **工具 欄** | 此值與所有使用者介面架構的值相同。                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 工具列控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 工具列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。  | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | 工具列控制項永遠沒有標籤。                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。  | 對應到 **ToolBar** 控制項類型的當地語系化字串。 預設值為 "tool bar" （適用于 en-us）或英文 (美國) 。                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 相依     | 除非在應用程式中使用一個以上的工具列控制項，否則它不需要名稱。 如果有一個以上的名稱，每個都必須有區別的名稱 (例如，「格式化」或「大綱」 ) 。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出 toolbar 控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | 相依 | 如果工具列可停駐在螢幕的不同部分，則必須支援 [Dock](uiauto-implementingdock.md) 控制項模式。                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 如果工具列可以展開和折迭以顯示更多專案，它必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。 |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | 相依 | 如果工具列可以調整大小、旋轉或移動，它必須支援 [轉換](uiauto-implementingtransform.md) 控制項模式。                          |



 

## <a name="required-events"></a>必要的事件

下表列出工具列控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                                  |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。         |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




