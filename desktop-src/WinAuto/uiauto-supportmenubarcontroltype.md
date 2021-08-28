---
title: 功能表列控制項類型
description: 本主題提供 Microsoft 消費者介面自動化 MenuBar 控制項類型的支援相關資訊。
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- 消費者介面自動化，功能表列控制項類型的支援
- 消費者介面自動化，功能表列控制項類型
- 功能表列控制項類型消費者介面自動化、樹狀結構
- 消費者介面自動化，功能表列控制項類型的屬性
- 消費者介面自動化，功能表列控制項類型的控制項模式
- 消費者介面自動化，功能表列控制項類型的事件
- 樹狀結構，功能表列控制項類型
- properties、MenuBar 控制項類型
- 控制項模式、功能表列控制項類型
- events、MenuBar 控制項類型
- 功能表列控制項類型的支援
- 功能表列控制項類型
- 控制項類型、功能表列控制項類型的樹狀結構
- 控制項類型、功能表列控制項類型的控制項模式
- 控制項類型，支援功能表列
- 控制項類型，功能表列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558a734d69a9197b3e0a8d6c5655405074878bca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468155"
---
# <a name="menubar-control-type"></a>功能表列控制項類型

本主題提供 Microsoft 消費者介面自動化 **MenuBar** 控制項類型的支援相關資訊。

功能表列控制項是 **執行功能表列控制項類型** 的控制項範例。 功能表列可讓使用者啟用應用程式中所包含的命令和選項。

下列章節會定義 **功能表列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的功能表列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述功能表列控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>MenuBar<ul><li>MenuItem (1 個以上)</li><li>其他控制項 (0 個以上)</li></ul></li></ul> | <ul><li>不適用<ul><li>MenuItem (1 個以上)</li><li>其他控制項 (0 個以上)</li></ul></li></ul> | 




 

功能表列控制項一律會出現在 [內容視圖] 中，但不會顯示在內容視圖中，因為它通常不會將有意義的資訊傳遞給使用者 (除非應用程式包含一個以上的功能表列) 。

消費者介面自動化用戶端可以接聽 [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) 事件，以確保當 UI 進入功能表模式時，這些事件會持續收到通知。 當應用程式處於功能表模式時，可能會針對功能表導覽來捕捉所有鍵盤輸入 (例如，輸入 's ' 可能會叫用 [ **儲存** ] 功能表，而不是在應用程式工作區上輸入字元) 。 **UIA \_ MenuModeStartEventId** 事件必須在第一個 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)事件之前，以確保邏輯一致性。 [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)事件會遵循最後一個 [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)事件。 按一下功能表項目也可能會立即觸發 **UIA \_ MenuModeStartEventId** 事件，後面接著 **UIA \_ MenuOpenedEventId** 事件。

功能表列控制項可以在其結構內包含其他控制項，例如編輯控制項和下拉式方塊。 這些額外的控制項對應到控制項和內容檢視中列出的「其他控制項」。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **功能表列** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值       | 注意                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULL        | 功能表列通常不會有快速鍵。                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | "ALT"       | 按下 ALT 鍵通常應該會將焦點放在應用程式中的功能表列。                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。  | 這個屬性所公開的值必須包含所有內含的控制項。                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE       | 功能表列控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | 功能表列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true        | 因為功能表列控制項包含的控制項可接受鍵盤焦點，所以可設定鍵盤焦點。                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。  | 這個屬性的值取決於此控制項是否可在畫面上檢視。                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | 功能表列控制項通常沒有標籤。                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。  | 對應到 **功能表列** 控制項類型的當地語系化字串。 預設值為「功能表列」，適用于 en-us 或英文 (美國) 。                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。  | 除非應用程式有一個以上的功能表列，否則功能表列控制項不需要名稱。 如果應用程式中有一個以上的功能表列，請使用這個屬性來公開區分名稱，例如「格式化」或「大綱」。 |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | 相依     | 這個屬性會公開此功能表列控制項是水平或垂直。                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出功能表列控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 如果控制項可展開或折迭，則必須執行 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。 |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | 相依 | 如果控制項可以停駐在螢幕的不同部分，則必須執行 [Dock](uiauto-implementingdock.md) 控制項模式。   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | 相依 | 如果控制項可以調整大小、旋轉或移動，則必須執行 [轉換](uiauto-implementingtransform.md) 控制項模式。      |



 

## <a name="required-events"></a>必要的事件

下表列出支援的功能表列控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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

 

 




