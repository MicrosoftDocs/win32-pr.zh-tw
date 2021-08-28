---
title: TreeItem 控制項類型
description: 本主題提供 TreeItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- 消費者介面自動化，TreeItem 控制項類型的支援
- 消費者介面自動化，TreeItem 控制項類型
- 消費者介面自動化，TreeItem 控制項類型的樹狀結構
- 消費者介面自動化，TreeItem 控制項類型的屬性
- 消費者介面自動化，TreeItem 控制項類型的控制項模式
- 消費者介面自動化，TreeItem 控制項類型的事件
- 樹狀結構，TreeItem 控制項類型
- properties、TreeItem 控制項類型
- 控制項模式，TreeItem 控制項類型
- events、TreeItem 控制項類型
- TreeItem 控制項類型的支援
- TreeItem 控制項類型
- 控制項類型，TreeItem 控制項類型的樹狀結構
- 控制項類型，TreeItem 控制項類型的控制項模式
- 控制項類型，支援 TreeItem
- 控制項類型，TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07f55ab6d9df8af46253a2428964bdf4ded64c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482924"
---
# <a name="treeitem-control-type"></a>TreeItem 控制項類型

本主題提供 **TreeItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

**TreeItem** 控制項類型代表樹狀結構容器內的節點。 每個節點都可能包含其他節點，稱為「子節點」。 父節點或包含子節點的節點可以顯示為展開或摺疊。

下列章節會定義 **TreeItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有樹狀結構專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述樹狀結構專案控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>TreeItem<ul><li>核取方塊 (0 或 1)</li><li>Image (0 或 1)</li><li>按鈕 (0 或 1)</li><li>TreeItem (0 個以上)</li></ul></li></ul> | <ul><li>TreeItem<ul><li>TreeItem (0 個以上)</li></ul></li></ul> | 




 

樹狀結構專案控制項在消費者介面自動化樹狀結構的內容視圖中可以有零或多個樹狀目錄專案子系。 如果樹狀結構專案控制項的功能超出下列控制項模式所公開的功能，則控制項應以 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型為基礎。

折迭樹狀結構專案在展開和可見之前都不會出現在控制項視圖或內容視圖中， (或可滾動) 。

控制項檢視可以包含控制項的額外詳細資訊，包括相關的影像或按鈕。 例如，大綱模式中的項目可能包含展開或摺疊大綱的影像以及按鈕。 這些詳細資料物件不會出現在內容視圖中，因為該資訊已經以父樹狀結構專案表示。

滾動畫面的樹狀目錄專案會同時出現在消費者介面自動化樹狀結構的控制項和內容視圖中，且 [**IUIAutomationElement：： CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (或 [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) 屬性必須設定為 **TRUE**。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **TreeItem** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 這個屬性必須傳回導致樹狀目錄專案變更選取狀態或成為焦點的位置。                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | 此值與所有使用者介面架構的值相同。                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | 樹狀目錄專案控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | 樹狀目錄專案控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。   | 這個屬性會指出樹狀目錄專案控制項是否會在螢幕上向外滾動。                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | 請參閱備註。   | 如果控制項包含動態更新的狀態，則必須支援此屬性，以便在元素的狀態變更時，輔助技術可以接收更新。 |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。   | 如果樹狀結構專案控制項使用視覺化圖示來指出是特定類型的專案，就必須支援這個屬性，而且必須指定專案類型。                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | 樹狀結構項目控制項會自行設定標籤。                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應到 TreeItem 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「樹狀專案」。                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 此屬性會公開每個樹狀結構項目控制項顯示的文字。                                                                                                                          |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有樹狀專案控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                                  | 支援/值                     | 備註                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | 必要                          | 所有樹狀目錄專案都必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，因為所有專案都可以展開或折迭。                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | 已展開、已摺疊或分葉節點 | 當樹狀目錄專案未展開或折迭時，它們就是分葉節點。                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | 相依                           | 如果樹狀結構專案可以執行命令，請執行 [Invoke](uiauto-implementinginvoke.md) 控制項模式。                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | 相依                           | 如果樹狀結構容器支援[滾動](uiauto-implementingscroll.md)條控制項模式，請執行[ScrollItem](uiauto-implementingscrollitem.md)控制項模式。                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | 相依                           | 如果有可能會在使用者返回樹狀結構容器時維持作用中的選取範圍，請執行 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。 |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | 必要                          | 這個屬性會針對容器內的所有專案公開相同的容器。                                                                                                                      |



 

## <a name="required-events"></a>必要的事件

下表列出樹狀專案控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                                |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 |                                                                                                                                |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | 如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。               |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。       |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。     |
| [**UIA \_ItemStatusPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                            | 如果控制項支援 [**ItemStatus**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。      |
| [**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                     | 如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                                        |                                                                                                                                |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                 | 如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。               |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                               | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。                 |



 

## <a name="remarks"></a>備註

如果樹狀結構專案有子系外框節點以外的子項目，則提供者必須謹慎且清楚地處理子物件資訊。 在消費者介面自動化中，樹狀結構本身會處理樹狀結構。 藉由有一或多個非外框節點的子系，兩者之間的差異和實際的子外框節點會變得很明確。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




