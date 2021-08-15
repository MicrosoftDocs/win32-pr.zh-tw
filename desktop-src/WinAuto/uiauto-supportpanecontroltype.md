---
title: 窗格控制項類型
description: 本主題提供窗格控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- 消費者介面自動化，窗格控制項類型的支援
- 消費者介面自動化，窗格控制項類型
- 窗格控制項類型的樹狀結構消費者介面自動化
- 消費者介面自動化，窗格控制項類型的屬性
- 消費者介面自動化，窗格控制項類型的控制項模式
- 消費者介面自動化，窗格控制項類型的事件
- 樹狀結構，窗格控制項類型
- 屬性，窗格控制項類型
- 控制項模式，窗格控制項類型
- 事件、窗格控制項類型
- 窗格控制項類型的支援
- Pane 控制項類型
- 控制項類型，窗格控制項類型的樹狀結構
- 控制項類型，窗格控制項類型的控制項模式
- 控制項類型，支援窗格
- 控制項類型，窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4a7225869c0752e65aece7e4eca00a416614315c8d5af810bdeb57d29aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825522"
---
# <a name="pane-control-type"></a>窗格控制項類型

本主題提供 **窗格** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。

**窗格** 控制項類型適用于具有不同內容的潛在可捲動區域。 它是用來表示框架或文件視窗內的物件。 使用者可以在窗格控制項和目前窗格的內容中流覽。 窗格控制項表示比 windows 或檔更低的群組層級，但在個別控制項上方。 使用者在窗格之間巡覽的方式是依照內容而定，可按下 TAB、F6 或 CTRL+TAB 鍵。

下列章節會定義 **窗格** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有窗格控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [窗格控制項類型範例](#pane-control-type-example)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與窗格控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>窗格</li>
</ul></td>
<td><ul>
<li>窗格</li>
</ul></td>
</tr>
</tbody>
</table>



 

窗格控制項一律會出現在控制項和內容視圖中。 如果物件只用于視覺呈現，請勿將版面設定物件公開為控制項或內容視圖中的窗格。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與窗格控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果特定的按鍵組合會讓焦點放在窗格中，則應該透過這個屬性公開該資訊。                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 這個屬性會公開窗格控制項之可點選的點，當按一下該點時，窗格就會取得焦點。                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **窗格**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | 窗格控制項的解說文字應解釋框架的用途，以及它與其他畫面格的關聯方式。 如果畫面格的目的和關聯性不清楚來自 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性的值，就必須提供描述。 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 窗格控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 窗格控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 窗格控制項通常沒有靜態標籤。 如果有靜態文字標籤，則標籤應透過這個屬性公開。                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應到 **窗格** 控制項類型的當地語系化字串。 預設值為 "pane"，代表 en-us 或英文 (美國) 。                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 這個屬性的值必須是清楚、精確且有意義的標題。                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出窗格控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援 | 注意                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | 相依 | 如果窗格控制項可以停駐，請執行停 [駐](uiauto-implementingdock.md) 控制項模式。                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | 相依 | 如果窗格控制項可以滾動，請執行 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | 相依 | 如果窗格控制項可以在螢幕上移動、調整大小或旋轉，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | 永不   | 如果專案需要執行 [視窗](uiauto-implementingwindow.md) 控制項模式，則控制項應以 [視窗](uiauto-supportwindowcontroltype.md) 控制項類型為基礎。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的窗格控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                            |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>窗格控制項類型範例

下圖說明可執行 **窗格** 控制項類型的控制項。

![顯示窗格控制項範例的螢幕擷取畫面](images/panexmpl.jpg)



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
<li>窗格
<ul>
<li>樹狀結構 (捲動模式)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>窗格
<ul>
<li>編輯 (捲軸模式) </li>
</ul></li>
</ul></td>
<td><ul>
<li>窗格
<ul>
<li>樹狀結構 (捲動模式)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>窗格
<ul>
<li>編輯 (捲軸模式) </li>
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

 

 




