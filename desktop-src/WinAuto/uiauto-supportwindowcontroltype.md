---
title: Window 控制項類型
description: 本主題提供 Window 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- 消費者介面自動化，Window 控制項類型的支援
- 消費者介面自動化，Window 控制項類型
- 消費者介面自動化，Window 控制項類型的樹狀結構
- 消費者介面自動化，Window 控制項類型的屬性
- 消費者介面自動化，視窗控制項類型的控制項模式
- 消費者介面自動化，Window 控制項類型的事件
- 樹狀結構，視窗控制項類型
- 屬性、視窗控制項類型
- 控制項模式，視窗控制項類型
- 事件、視窗控制項類型
- 視窗控制項類型的支援
- Window 控制項類型
- 控制項類型，視窗控制項類型的樹狀結構
- 控制項類型，視窗控制項類型的控制項模式
- 控制項類型、視窗支援
- 控制項類型，視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422742381cd501d295e4cb7e354ca07e10c13360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301655"
---
# <a name="window-control-type"></a>Window 控制項類型

本主題提供 **Window** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

視窗控制項由視窗框架組成，而視窗框架包含子物件，如標題列、用戶端和其他物件。

下列章節會定義 **Window** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的視窗控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與 window 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>時間範圍</li>
</ul></td>
<td><ul>
<li>時間範圍</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與視窗控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 視窗控制項必須具有可點按的點，讓視窗變成已選取或未選取狀態。                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Window** | 此值與所有使用者介面架構的值相同。                                                                                                           |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 視窗控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 視窗控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | 視窗控制項沒有靜態視窗標籤。                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **視窗** 控制項類型的當地語系化字串。 預設值為 "window"，代表 en-us 或英文 (美國) 。                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 視窗控制項一律會包含主要視窗專案，此專案與使用者要建立為專案最多語義識別碼的關聯性。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出視窗控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                        | 支援/值 | 備註                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | 條件式   | 如果視窗可以停駐，就必須支援 [Dock](uiauto-implementingdock.md) 控制項模式。                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | 必要      | [轉換](uiauto-implementingtransform.md)控制項模式可讓視窗在螢幕上移動、調整大小或旋轉。  (不適用於 Windows Store 應用程式。 )  |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | 必要      | [視窗](uiauto-implementingwindow.md)控制項模式會啟用視窗的特定作業。                                                                      |



 

## <a name="required-events"></a>必要的事件

下表列出支援的 **視窗** 控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                                                                                                                           |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                                                                                                  |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                                                                                                |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                                |                                                                                                                                                                                                                           |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**UIA \_ 視窗 \_ WindowClosedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ 視窗 \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。             | 如果控制項支援 [Window](uiauto-implementingwindow.md)控制項模式的 [**WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate)屬性，就必須支援這個事件。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




