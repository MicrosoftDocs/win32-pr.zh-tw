---
title: 行事曆控制項類型
description: 本主題提供行事曆控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 行事曆控制項可讓使用者輕鬆地判斷日期並選取其他日期。
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- 消費者介面自動化，行事曆控制項類型的支援
- 消費者介面自動化，行事曆控制項類型
- 消費者介面自動化，行事曆控制項類型的樹狀結構
- 消費者介面自動化，行事曆控制項類型的屬性
- 消費者介面自動化，行事曆控制項類型的控制項模式
- 消費者介面自動化，行事曆控制項類型的事件
- 樹狀結構，行事曆控制項類型
- 屬性、行事曆控制項類型
- 控制項模式，行事曆控制項類型
- 事件、行事曆控制項類型
- 行事曆控制項類型的支援
- Calendar 控制項類型
- 月曆控制項類型的控制項類型、樹狀結構
- 控制項類型、行事曆控制項類型的控制項模式
- 控制項類型、行事曆支援
- 控制項類型，行事曆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482944"
---
# <a name="calendar-control-type"></a>行事曆控制項類型

本主題提供行事 **曆** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 行事曆控制項可讓使用者輕鬆地判斷日期並選取其他日期。

下列章節會定義 **Calendar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有行事曆控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與行事曆控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>Calendar<ul><li>DataGrid<ul><li>標題 (0 或 1)<ul><li>HeaderItem (0 或7，數量取決於資料行中顯示多少天) </li></ul></li><li>ListItem (數量取決於要顯示多少天)</li><li>按鈕 (0 或 2；用於分頁月曆檢視)</li></ul></li></ul></li></ul> | <ul><li>Calendar<ul><li>ListItem (數量取決於要顯示多少天)</li></ul></li></ul> | 




 

月曆控制項可以在使用者介面中以許多不同的形式來表示。 唯一保證位於消費者介面自動化樹狀結構之控制項視圖中的控制項是資料格、標頭、標頭專案和清單專案控制項。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **Calendar** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendar** | 此值與所有使用者介面架構的值相同。                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 行事曆控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 行事曆控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。   | 這個屬性的值應該是文件控制項的標籤。 通常會使用文件的標題。                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應至行事 **曆** 控制項類型的當地語系化字串。 預設值為「行事曆」，代表 en-us 或英文 (美國) 。                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 行事曆控制項通常會從目前的日期取得其名稱。                                                                                                                                  |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有行事曆控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                        | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | 必要      | 行事曆控制項一律支援 [方格](uiauto-implementinggrid.md) 控制項模式，因為一個月內的天數是可流覽空間的專案。                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | 相依       | 大部分的月曆控制項都支援依頁面翻閱檢視。 建議使用 [滾動](uiauto-implementingscroll.md) 條控制項模式，以便支援分頁導覽。                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | 相依       | 大部分的行事曆控制項都會保留特定的日、月或年做為子項目的選取專案。 某些行事曆可供多重選取，且僅限單一選取。 具有可選取子項目的行事曆控制項應支援 [選取](uiauto-implementingselection.md) 控制項模式。                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | 必要      | 由於行事曆控制項的子樹中一律會有一個標頭，所以必須支援 [Table](uiauto-implementingtable.md) 控制項模式。                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | 否            | 因為專案無法直接在控制項上設定值，所以不需要為行事曆控制項設定 [值](uiauto-implementingvalue.md) 控制項模式。 如果特定日期與控制項相關聯，則應該透過 [選取](uiauto-implementingselection.md) 控制項模式來提供資訊。 |



 

## <a name="required-events"></a>必要的事件

下表列出行事曆控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                                                                                                              |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                                                                                     |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。             | 如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md)控制項模式的 [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。                                                                                             |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




