---
title: DataGrid 控制項類型
description: 本主題提供 DataGrid 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- 消費者介面自動化，DataGrid 控制項類型的支援
- 消費者介面自動化，DataGrid 控制項類型
- DataGrid 控制項類型的消費者介面自動化、樹狀結構
- 消費者介面自動化，DataGrid 控制項類型的屬性
- 消費者介面自動化，DataGrid 控制項類型的控制項模式
- 消費者介面自動化，DataGrid 控制項類型的事件
- 樹狀結構，DataGrid 控制項類型
- properties、DataGrid 控制項類型
- 控制項模式、DataGrid 控制項類型
- events、DataGrid 控制項類型
- DataGrid 控制項類型的支援
- DataGrid 控制項類型
- DataGrid 控制項類型的控制項類型、樹狀結構
- 控制項類型，DataGrid 控制項類型的控制項模式
- 控制項類型，支援 DataGrid
- 控制項類型，DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932149"
---
# <a name="datagrid-control-type"></a>DataGrid 控制項類型

本主題提供 **DataGrid** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

**DataGrid** 控制項型別可讓使用者輕鬆地使用包含資料的專案或資料列中所呈現的自動化元素。 資料格控制項具有項目資料列和關於這些項目的資訊資料行。 Windows Vista Explorer 中的清單視圖控制項是支援 **DataGrid** 控制項類型的範例。

下列章節會定義 **DataGrid** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有資料格控制項，其中 UI framework/平臺會將控制項類型和控制項模式的消費者介面自動化支援整合。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [DataGrid 控制項類型範例](#datagrid-control-type-example)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與資料格控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>DataGrid
<ul>
<li>標頭 (0、1 或 2)
<ul>
<li>HeaderItem (行數或列數)</li>
</ul></li>
<li>DataItem (0 或以上;可以結構化在階層中) </li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 或以上;可以結構化在階層中) </li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **DataGrid** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 這個屬性的值必須一律為 **TRUE**。 這表示資料格控制項必須一律位於消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 這個屬性的值必須一律 **為 TRUE**。 這表示資料格控制項必須一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。   | 如果有靜態文字標籤，這個屬性必須公開該控制項的參考。                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應至 **DataGrid** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「資料方格」。                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 資料格控制項通常會從靜態文字標籤取得其 **Name** 屬性的值。 如果沒有靜態文字標籤，應用程式開發人員必須為 **Name** 屬性指派值。 **Name** 屬性的值絕對不能是編輯控制項的文字內容。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有資料格控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援  | 注意                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | 必要 | 資料格控制項本身一律支援 [方格](uiauto-implementinggrid.md) 控制項模式，因為它所包含的專案具有在方格中配置的中繼資料。 |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | 相依  | 資料格可捲動與否，會視內容以及是否有捲軸而定。                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | 相依  | 資料格可選取與否，視內容而定。                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | 相依  | 具有標頭的資料格控制項應支援 [Table](uiauto-implementingtable.md) 控制項模式。                                                                   |



 

資料格容器內的資料項目至少會支援：

-   [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式 (如果資料格可供選取) 
-   [ScrollItem](uiauto-implementingscrollitem.md) 控制項模式 (如果資料格為可滾動) 
-   [GridItem](uiauto-implementinggriditem.md) 控制項模式
-   [TableItem](uiauto-implementingtableitem.md) 控制項模式 (如果資料格有標頭) 

## <a name="required-events"></a>必要的事件

下表列出需要資料格控制項才能支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                                                          |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                                 |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。             | 如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式的 CurrentView 屬性，就必須支援這個事件。 |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                         |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>DataGrid 控制項類型範例

下圖說明可執行 **DataGrid** 控制項類型的清單視圖控制項。

![具有 datagrid 控制項類型之清單視圖控制項的螢幕擷取畫面](images/datagridxmpl.jpg)

以下顯示與清單視圖控制項相關之消費者介面自動化樹狀結構的控制項視圖和內容視圖。 每個自動化項目的控制項模式顯示在括號中。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>消費者介面自動化樹狀結構控制項視圖</th>
<th>消費者介面自動化樹狀結構-內容視圖</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataGrid (排序、資料表、選取專案、格線) 
<ul>
<li>標頭
<ul>
<li>HeaderItem &quot; Name &quot; (Invoke) </li>
<li>HeaderItem &quot; 修改日期 &quot; (叫用) </li>
<li>HeaderItem &quot; 大小 &quot; (叫用) </li>
</ul></li>
<li>群組 &quot; Contoso &quot; (TableItem、GridItem、SelectionItem、Table *、Grid*) 
<ul>
<li>DataItem &quot; 帳戶 Receivable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </li>
<li>DataItem &quot; 帳戶 Payable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </li>
</ul></li>
</ul></td>
<td>DataGrid (Table, Grid, Selection)
<ul>
<li>群組 &quot; Contoso &quot; (TableItem、GridItem、SelectionItem、Table *、Grid*) 
<ul>
<li>DataItem &quot; 帳戶 Receivable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </li>
<li>DataItem &quot; 帳戶 Payable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*上述範例顯示包含多個控制項層級的資料格。 **群組** ( "Contoso" ) 控制項包含兩個 **DataItem** 控制項 ( "accounts Receivable.doc" 和 "accounts Payable.doc" ) 。 **DataGrid** / **GridItem** 組與另一個層級的配對無關。 群組底下的 **DataItem** 控制項也可以公開為專案 **組合** 控制項 [類型](uiauto-supportlistitemcontroltype.md) ，讓它們更清楚地呈現為可選取的物件，而不是簡單的資料元素。 本範例不包含群組資料項目的子項目。 如需多個控制項層級的另一個範例，請參閱 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




