---
title: '[類型] 控制項類型'
description: 本主題提供 [內容類型] 的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- 消費者介面自動化，支援代表類型控制項類型
- 消費者介面自動化，[類型] 控制項類型
- 消費者介面自動化，[類型] 控制項類型的樹狀結構
- 消費者介面自動化，[類型] 控制項類型的屬性
- 消費者介面自動化，[組合] 控制項類型的控制項模式
- 消費者介面自動化，[代表] 控制項類型的事件
- 樹狀結構、[類型] 控制項類型
- properties、[類型] 控制項類型
- 控制項模式、[類型] 控制項類型
- 事件、[類型] 控制項類型
- 支援 [類型] 控制項類型
- '[類型] 控制項類型'
- 控制項類型，[類型] 控制項類型的樹狀結構
- 控制項類型，類型群組控制項類型的控制項模式
- 控制項類型、支援代表
- 控制項類型，[類型]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483194"
---
# <a name="listitem-control-type"></a>[類型] 控制項類型

本主題 **提供 [內容** 類型] 的 Microsoft 消費者介面自動化支援相關資訊。

清單 **專案控制項是執行 [專案** ] 控制項類型的控制項範例。

下列各節會定義必要的消費者介面自動化樹狀結構、屬性、控制項模式，以及 [類型 **] 控制項類型** 的事件。 消費者介面自動化需求適用于所有的清單專案控制項，使用者介面架構/平臺會將控制項類型和控制項模式的消費者介面自動化支援全部整合起來。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與清單專案控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的專案。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>ListItem<ul><li>影像 (0 個以上)</li><li>文字 (0 個以上)</li><li>編輯 (0 個以上)</li></ul></li></ul> | <ul><li>ListItem</li></ul> | 




 

消費者介面自動化樹狀結構之內容視圖內清單專案控制項的子系必須一律顯示零個子系。 如果控制項的結構是讓其他專案包含在清單專案下，則應該遵循 [TreeItem](uiauto-supporttreeitemcontroltype.md) 控制項類型的消費者介面自動化支援需求。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義 **與 [清單** ] 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。 如果已知專案在使用者介面的不同實例之間是一致的，則配置清單專案的 **AutomationId** 屬性。 如果清單專案是動態填入且不可預測的，請將 **AutomationId** 屬性保留空白。                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 這個屬性的值應包含清單項目的影像區域和文字內容。                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 相依      | 如果清單控制項具有可點按的點 (可按一下以使清單取得焦點) 的點，則必須透過這個屬性公開該點。 如果清單控制項完全由子系列表專案所涵蓋，則會傳回 [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) 錯誤，指出用戶端必須向清單控制項內的專案詢問可點按的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | 此值與所有使用者介面架構的值相同。                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。   | 清單控制項的說明文字應解釋，為什麼會要求使用者從選項清單中選擇選項，而這通常也是透過工具提示顯示的資訊類型。 例如，「選取專案以設定監視器的顯示解析度」。                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | 清單控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | 清單控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果容器可以接受鍵盤輸入，則此屬性值應為 **TRUE**。                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 相依      | 這個屬性必須傳回值，以指出清單專案目前是否已在執行 [滾動](uiauto-implementingscroll.md) 控制項模式的父容器內進行查看。                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | 相依      | 如果控制項包含動態更新的狀態，則必須支援此屬性，以便在元素的狀態變更時，輔助技術可以接收更新。                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | 相依      | 表示基礎物件的清單項目控制項應公開此屬性。 這些清單項目控制項通常會有相關聯的圖示，可讓使用者將控制項與基礎物件建立關聯。                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。   | 如果有靜態文字標籤，那麼這個屬性必須公開該控制項的參考。                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應 **至 [輸入** ] 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「清單專案」。                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 清單專案控制項的 [名稱] 屬性值來自專案的文字標籤。                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有清單專案控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 如果專案可以操作來顯示或隱藏資訊，則必須實 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | 相依 | 如果清單容器內支援專案對專案空間流覽，而且容器排列在資料列和資料行中，則必須執行 [GridItem](uiauto-implementinggriditem.md) 控制項模式。                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | 相依 | 如果專案具有可在其上執行的命令（與選取的不同），則必須執行叫 [用控制項模式](uiauto-implementinginvoke.md) 。 這通常是與按兩下清單項目控制項相關聯的動作。 範例將從 Windows 檔案總管開機檔案，或在 Microsoft Windows Media Player 中播放音樂檔案。        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | 相依 | 如果清單專案包含在可滾動的容器內，則必須執行 [ScrollItem](uiauto-implementingscrollitem.md) 控制項模式。                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | 相依 | 支援選取專案的清單專案控制項必須執行 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。 這可讓清單項目控制項傳遞已選取的訊息。                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | 相依 | 如果清單專案是 checkable 的，且動作不會執行選取狀態變更，則必須實作為 [切換](uiauto-implementingtoggle.md) 控制項模式。                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | 相依 | 如果可以編輯專案，則必須實 [值](uiauto-implementingvalue.md) 控制項模式。 變更清單專案控制項將會導致 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 和 [**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性的值變更。 |



 

## <a name="required-events"></a>必要的事件

下表列出清單專案控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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



 

## <a name="remarks"></a>備註

如果容器裝載清單專案，則流覽的主要方法應該會移至清單專案。 透過清單導覽將焦點放在子項目上，可能會對使用者和協助工具工具造成混淆。 如果容器裝載專案的垂直清單，按向上鍵和向下鍵可流覽專案，但是按向右鍵和向左鍵可流覽至焦點專案的子項目，例如清單欄或 UI 子項目。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




