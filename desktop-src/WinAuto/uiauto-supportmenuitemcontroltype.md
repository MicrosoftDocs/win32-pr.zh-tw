---
title: MenuItem 控制項類型
description: 本主題提供 MenuItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- 消費者介面自動化，MenuItem 控制項類型的支援
- 消費者介面自動化，MenuItem 控制項類型
- 消費者介面自動化，MenuItem 控制項類型的樹狀結構
- 消費者介面自動化，MenuItem 控制項類型的屬性
- 消費者介面自動化，MenuItem 控制項類型的控制項模式
- 消費者介面自動化，MenuItem 控制項類型的事件
- 樹狀結構，MenuItem 控制項類型
- 屬性，MenuItem 控制項類型
- 控制項模式、MenuItem 控制項類型
- events、MenuItem 控制項類型
- MenuItem 控制項類型的支援
- MenuItem 控制項類型
- MenuItem 控制項類型的控制項類型、樹狀結構
- 控制項類型，MenuItem 控制項類型的控制項模式
- 控制項類型，支援 MenuItem
- 控制項類型，MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482507"
---
# <a name="menuitem-control-type"></a>MenuItem 控制項類型

本主題提供 **MenuItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

功能表控制項可將命令和事件處理常式的關聯項目以階層方式組織。 在一般的 Windows 應用程式中，功能表列會包含數個功能表項目 (例如 [檔案]、[**編輯**] 和 [**視窗) ]** **，而** 每個功能表項目會顯示功能表。 功能表又包含一組功能表項目 (例如 [開新檔案] 、[開啟舊檔] 和 [關閉檔案] )，這些項目可展開顯示更多的功能表項目，或在按一下時可執行特定的動作。

下列章節會定義 **MenuItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的功能表項目控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [舊版問題](#legacy-issues)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與功能表項目控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>MenuItem 的「說明」<ul><li>[說明] 功能表項目的功能表 (子功能表) <ul><li>MenuItem 的「說明主題」</li><li>MenuItem 的「關於記事本」</li></ul></li></ul></li></ul> | <ul><li>MenuItem 的「說明」<ul><li>MenuItem 的「說明主題」</li><li>MenuItem 的「關於記事本」</li></ul></li></ul> | 




 

功能表項目控制項的控制項視圖具有上面所示的消費者介面自動化樹狀結構。 請注意，已新增功能表 **欄上的** [說明] 功能表項目來更清楚地說明此結構。

針對內容視圖，消費者介面自動化樹狀目錄中不存在 **功能表** ，因為它不會將有意義的資訊傳遞給使用者。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **MenuItem** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。 如果已知專案在使用者介面的不同實例之間是一致的，則配置功能表項目的 **AutomationId** 屬性。 如果功能表項目動態填入且不可預測，請將 **AutomationId** 屬性保留空白。 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 功能表項目控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 功能表項目控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應至 **MenuItem** 控制項類型的當地語系化字串。 預設值為「功能表項目」，適用于 en-us 或英文 (美國) 。                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | 功能表項目控制項的名稱是用來加上標籤的文字。                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出功能表項目控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 如果可以展開或折迭控制項，請執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)。                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | 相依 | 如果控制項執行單一動作或命令，請執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)。                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | 相依 | 如果控制項是用來從功能表項目中的選項清單中選取，請執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。 |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | 相依 | 如果控制項代表可以開啟或關閉的選項，請執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)。                       |



 

## <a name="required-events"></a>必要的事件

下表列出支援的功能表項目控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                                  |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。 |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | 如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。                 |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。         |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。       |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                 | 如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。                 |



 

## <a name="legacy-issues"></a>舊版問題

若為 Microsoft Win32 功能表項目，只有在選取功能表項目時才支援 [切換](uiauto-implementingtoggle.md) 控制項模式，而您可以透過程式設計方式判斷是否需要切換控制項模式的支援。 因為 Win32 功能表項目不會公開是否可以進行檢查，所以不檢查功能表項目時，就會支援 Invoke 控制項模式。 除了支援切換控制項模式所需的功能表項目之外，也一律支援 Invoke 控制項模式。 如此一來，當功能表項目未核取時，用戶端就不[](uiauto-implementinginvoke.md)會混淆 (當功能表項目未核取時，) 不會再于檢查時再支援該模式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




