---
title: 清單控制項類型
description: 本主題提供清單控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- 消費者介面自動化，清單控制項類型的支援
- 消費者介面自動化，清單控制項類型
- 消費者介面自動化，清單控制項類型的樹狀結構
- 消費者介面自動化，清單控制項類型的屬性
- 消費者介面自動化，清單控制項類型的控制項模式
- 消費者介面自動化，清單控制項類型的事件
- 樹狀結構，清單控制項類型
- 屬性，清單控制項類型
- 控制項模式，清單控制項類型
- 事件，清單控制項類型
- 清單控制項類型的支援
- List 控制項類型
- 控制項類型，清單控制項類型的樹狀結構
- 控制項類型，清單控制項類型的控制項模式
- 控制項類型，支援清單
- 控制項類型，清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a493418750bff1932fe933340b3eb2cb05829e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372124"
---
# <a name="list-control-type"></a>清單控制項類型

本主題提供 **清單** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

**清單** 控制項類型提供一種方式來組織一般群組或專案群組，並允許使用者選取其中一個或多個專案。 **清單** 控制項類型對其可能包含的子項目類型有鬆散的限制。 這可讓使用者介面自動化提供者支援選取範圍容器的已知項目。

下列章節會定義 **清單** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有清單控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式和屬性](#required-control-patterns-and-properties)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與清單控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<td>包含對應控制項的項目。</td>
<td>從樹狀結構中移除多餘的資訊，讓輔助技術能使用對使用者有意義的最小資訊集。</td>
</tr>
<tr class="even">
<td><ul>
<li>List
<ul>
<li>DataItem (0 個以上)</li>
<li>ListItem (0 個以上)</li>
<li>Group (0 個以上)</li>
<li>ScrollBar (0、1 或 2 個)</li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>DataItem (0 個以上)</li>
<li>ListItem (0 個以上)</li>
<li>Group (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

針對實作清單控制項類型的控制項 (例如清單控制項)，其控制項檢視包含：

-   清單控制項 [內的零](uiauto-supportlistitemcontroltype.md) 或多個專案 (專案可以根據專案清單或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型) 
-   清單控制項中零個以上的群組控制項
-   0、1 或 2 個捲軸控制項

針對實作清單控制項類型的控制項 (例如清單控制項)，其內容檢視包含：

-   清單控制項 [內的零](uiauto-supportlistitemcontroltype.md) 或多個專案 (專案可以根據專案清單或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型) 
-   清單控制項中零個以上的群組

除了集中成群組的項目，清單控制項所包含的項目不能有階層式關聯性。 如果專案在消費者介面自動化樹狀結構中有子系，則清單容器應以 [樹狀結構](uiauto-supporttreecontroltype.md) 控制項類型為基礎。

清單控制項中可選取的專案將可從清單控制項之消費者介面自動化樹狀結構中的下階取得。 清單控制項內的所有項目都必須屬於相同的選取群組。 清單中可選取的專案應該 [公開為專案](uiauto-supportlistitemcontroltype.md) 清單 (而不是 [DataItem](uiauto-supportdataitemcontroltype.md)) 控制項類型。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **清單** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果清單控制項具有可點按的點 (可按一下以使清單取得焦點) 的點，則必須透過這個屬性公開該點。 如果 [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性的值為 **TRUE**，則嘗試抓取此屬性會導致 [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) 錯誤。                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **清單**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | 清單控制項的說明文字應解釋為什麼會要求使用者從清單選擇選項。 例如，「從此清單選取項目將會設定顯示器的解析度。」                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 清單控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 清單控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果有靜態文字標籤，那麼這個屬性必須公開該控制項的參考。                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應到 **清單** 控制項類型的當地語系化字串。 預設值為 "list" 代表 en-us 或英文 (美國) 。                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 清單控制項的 [ **名稱** ] 屬性的值應傳達要求使用者從中選取的選項類別。 此屬性通常會從靜態文字標籤取得其名稱。 如果沒有靜態文字標籤，應用程式開發人員必須公開 **Name** 屬性的值。<br/> 清單控制項唯一不需要此屬性的情況是，當控制項用於其他控制項的樹狀子目錄時。<br/> |



 

## <a name="required-control-patterns-and-properties"></a>必要的控制項模式和屬性

下表列出所有清單控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                             | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | 相依       | 當每個專案都必須提供方格導覽時，請執行 [方格](uiauto-implementinggrid.md) 控制項模式。                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | 相依       | 如果控制項可以支援容器中專案的多個視圖，請執行 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式。                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | 相依       | 如果容器中的專案是可滾動的，請執行 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | 相依       | 如果控制項支援支援選取的清單控制項類型，則在控制項所包含的專案之間維持選取狀態時，控制項必須執行 [選取](uiauto-implementingselection.md) 控制項模式。 如果無法選取控制項內的專案，則可以使用 [群組](uiauto-supportgroupcontroltype.md) 控制項類型。 |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | 相依       | 清單控制項可以是單一或多重選擇容器。                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | 相依       | 清單控制項不一定需要選取某個項目。                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | 永不         | **清單** 控制項類型永遠不支援 [Table](uiauto-implementingtable.md)控制項模式。 如果控制項需要支援此控制項模式，則控制項應以 [DataGrid](uiauto-supportdatagridcontroltype.md) 控制項類型為基礎。                                                                                                             |



 

## <a name="required-events"></a>必要的事件

下表列出支援的清單控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                              |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。     |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | 如果子專案的版面配置可以變更，控制項就必須支援這個事件。                                            |
| [**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。             | 如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。             |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | 如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





