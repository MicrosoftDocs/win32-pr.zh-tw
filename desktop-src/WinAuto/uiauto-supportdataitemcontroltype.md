---
title: DataItem 控制項類型
description: 本主題提供 DataItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- 消費者介面自動化，DataItem 控制項類型的支援
- 消費者介面自動化，DataItem 控制項類型
- 消費者介面自動化，DataItem 控制項類型的樹狀結構
- 消費者介面自動化，DataItem 控制項類型的屬性
- 消費者介面自動化，DataItem 控制項類型的控制項模式
- 消費者介面自動化，DataItem 控制項類型的事件
- 消費者介面自動化、大型清單和 DataItem 控制項類型
- 樹狀結構，DataItem 控制項類型
- properties、DataItem 控制項類型
- 控制項模式，DataItem 控制項類型
- events、DataItem 控制項類型
- 大型清單
- DataItem 控制項類型的支援
- DataItem 控制項類型
- 控制項類型，DataItem 控制項類型的樹狀結構
- 控制項類型，DataItem 控制項類型的控制項模式
- 控制項類型、大型清單和 DataItem 控制項類型
- 控制項類型，支援 DataItem
- 控制項類型，DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ec4612b43855578256d52bf6647b105ea666882cfe2f72dcdbf355559a7e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826311"
---
# <a name="dataitem-control-type"></a>DataItem 控制項類型

本主題提供 **DataItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

連絡人清單中的項目即是資料項目控制項的範例。 資料項目控制項包含與使用者相關的資訊。 由於包含更為豐富的資訊，這種控制項比簡單的清單項目複雜。

下列章節會定義 **DataItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有資料項目控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [在大型清單中使用 Dataitem](#working-with-dataitems-in-large-lists)
-   [必要的事件](#required-events)
-   [DataItem 控制項類型範例](#dataitem-control-type-example)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與資料項目控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的專案。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>DataItem
<ul>
<li>視情況而定 (0 個以上；可以結構化為階層)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataItem
<ul>
<li>視情況而定 (0 個以上；可以結構化為階層)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

資料格中資料項目 (Item) 的項目 (Element) 可裝載各種不同的物件，包括另一層資料項目，或是特定資料格項目 (Element) 如文字、影像或編輯控制項。 如果資料項目專案具有特定的物件角色，則元素應該公開為特定的控制項類型;例如，方格中可選取 [資料項目的專案類型控制項類型](uiauto-supportlistitemcontroltype.md) 。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 DataItem 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 資料項目控制項必須一律為內容。                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 資料項目控制項必須一律為控制項。                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | 請參閱備註。   | 如果控制項包含動態更新的狀態，則必須支援此屬性，以便在元素的狀態變更時，輔助技術可以接收更新。        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。   | 這個字串值可讓使用者知道項目所代表的物件為何。 範例包括 "Media File" 和 "Contact"。                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | 資料項目控制項沒有靜態文字標籤。                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應到 **DataItem** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「資料項目」。                                                              |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 資料項目控制項一律會包含主要文字專案，使用者會將它辨識為專案的識別碼。                                                                           |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有資料項目控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 如果資料項目目可展開或折迭以顯示和隱藏資訊，則必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | 相依 | 當可在空間中導覽專案的容器內有資料項目集合可供使用時，資料項目將會支援 [GridItem](uiauto-implementinggriditem.md) 控制項模式。                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | 相依 | 所有資料項目都支援當其資料容器的專案數目超過螢幕上可容納的專案時，能夠使用 [ScrollItem](uiauto-implementingscrollitem.md) 控制項模式來滾動查看。             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | 相依 | 選取資料項目的能力視內容而定。                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | 相依 | 如果資料項目包含在具有 header 專案的 [DataGrid](uiauto-supportdatagridcontroltype.md) 控制項類型中，它應該支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式。 |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | 相依 | 如果資料項目包含可迴圈的狀態，則它應該支援 [切換](uiauto-implementingtoggle.md) 控制項模式。                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | 相依 | 如果資料項目的主要文字是可編輯的，則必須支援 [值](uiauto-implementingvalue.md) 控制項模式。                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>在大型清單中使用 Dataitem

由於大型清單通常會在 UI 架構內虛擬化以協助效能，因此消費者介面自動化用戶端無法使用消費者介面自動化查詢功能來搜尋完整樹狀結構的內容，其方式與其他專案容器中的相同。 用戶端應該將專案滾動至 view (或展開控制項，以顯示所有可用的選項) ，然後再從資料項目存取完整的資訊集。

在資料項目的消費者介面自動化專案上呼叫 [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)時，Microsoft Windows 檔案總管會成功傳回，而且會將焦點設為數據項子樹中的編輯控制項。

## <a name="required-events"></a>必要的事件

下表列出資料項目目控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                                  |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | 如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。                 |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。         |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。       |
| [**UIA \_ItemStatusPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                            | 如果控制項支援 [**ItemStatus**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。        |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                 | 如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。                 |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                               | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。                   |



 

## <a name="dataitem-control-type-example"></a>DataItem 控制項類型範例

下圖說明清單視圖控制項中的 DataItem 控制項類型。

![具有 dataitem 控制項類型之清單視圖控制項的螢幕擷取畫面](images/dataitemxmpl.jpg)

與資料項目控制項相關之消費者介面自動化樹狀結構的控制項視圖和內容視圖如下所示。 每個自動化項目的控制項模式顯示在括號中。 **群組**"Contoso" 也是資料格主控制項方格的一部分。 如需更高層級方格結構的範例，請參閱 [DataGrid 控制項類型](uiauto-supportdatagridcontroltype.md)。



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
<td><ul>
<li>群組 &quot; Contoso &quot; (資料表、方格) 
<ul>
<li>DataItem &quot; 帳戶 Receivable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) 
<ul>
<li>映射 &quot; 帳戶 Receivable.doc&quot;</li>
<li>編輯 &quot; 名稱 &quot; (TableItem、GridItem、值 &quot; 帳戶 Receivable.doc&quot;) </li>
<li>修改的編輯 &quot; 日期 &quot; (TableItem、GridItem、VALUE &quot; 8/25/2006 3:29 PM &quot;) </li>
<li>編輯 &quot; 大小 &quot; (GridItem、TableItem、VALUE &quot; 11.0 KB &quot;) </li>
</ul></li>
<li>DataItem &quot; 帳戶 Payable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) 
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>群組 &quot; Contoso &quot; (資料表、方格) 
<ul>
<li>DataItem &quot; 帳戶 Receivable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) 
<ul>
<li>映射 &quot; 帳戶 Receivable.doc&quot;</li>
<li>編輯 &quot; 名稱 &quot; (TableItem、GridItem、值 &quot; 帳戶 Receivable.doc&quot;) </li>
<li>修改的編輯 &quot; 日期 &quot; (TableItem、GridItem、VALUE &quot; 8/25/2006 3:29 PM &quot;) </li>
<li>編輯 &quot; 大小 &quot; (GridItem、TableItem、VALUE &quot; 11.0 KB &quot;) </li>
</ul></li>
<li>DataItem &quot; 帳戶 Payable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) 
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

如果方格代表可選取專案的清單，則可以使用 [專案類型 [] 控制項類型](uiauto-supportlistitemcontroltype.md) 來公開對應的可選取 UI 元素，而不是 DataItem 控制項類型。 在上述範例中， **DataItem** 元素 ( 群組 ( "Contoso" ) 下的「帳戶 Receivable.doc」和「帳戶 ) Payable.doc」，可以藉由將它們公開為專案 **組合** 控制項類型來獲得改善，因為該類型已支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




