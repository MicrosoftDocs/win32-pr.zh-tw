---
title: AppBar 控制項類型
description: 本主題提供 AppBar 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- 消費者介面自動化，AppBar 控制項類型的支援
- 消費者介面自動化，AppBar 控制項類型
- 消費者介面自動化，AppBar 控制項類型的控制項模式
- 控制項模式，AppBar 控制項類型
- AppBar 控制項類型的支援
- AppBar 控制項類型
- 控制項類型，AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472884"
---
# <a name="appbar-control-type"></a>AppBar 控制項類型

本主題提供 **AppBar** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

應用程式行是 UI 元素，可向使用者呈現導覽、命令和工具。 針對 Windows Store 應用程式，可以按 Windows 鍵 + Z 來顯示應用程式的應用程式列。

下列章節會定義 **AppBar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的事件](#required-events)
-   [相關事件](#relevant-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述 **AppBar** 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 **按鈕** 是 **AppBar** 中最常見的元素，但也可能會叫用應用程式動作的其他控制項。 **AppBar** 也可以有0個或多個分隔符號 (**分隔符號** 控制項類型) ，它會出現在控制項視圖中，以放置於其他控制項之間。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>按鈕 (0 個以上)</li><li>其他控制項 (0 個以上)</li></ul></li></ul> | <ul><li>不適用<ul><li>按鈕 (0 個以上)</li><li>其他控制項 (0 個以上)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與執行 **AppBar** 控制項類型的控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 這個屬性所公開的值必須包含所有內含的控制項。                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | 應用程式的工具列控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 應用程式橫條控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱附註  | 如果控制項可接收鍵盤焦點，就必定支援此屬性。 應用程式行內的控制項通常可以取得鍵盤焦點。                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。 | 這個屬性的值取決於此控制項是否可在畫面上檢視。                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | 應用程式行控制項通常沒有標籤。                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應到 **AppBar** 控制項類型的當地語系化字串。 預設值為 "app bar" （適用于 en-us）或英文 (美國) 。                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 除非應用程式有一個以上的應用程式行，否則應用程式行控制項不需要名稱。 如果應用程式中有一個以上的應用程式行，請使用此屬性來公開區分名稱，例如 "Top" 或 "底端"。 |



 

## <a name="required-events"></a>必要的事件

下表列出應用程式橫條控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>相關事件

下表列出與執行 **AppBar** 控制項類型，但不是絕對必要的控制項特別相關的消費者介面自動化事件。



| 消費者介面自動化事件                                                                                 | 備註                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | 當應用程式行控制項關閉時，平臺執行可能會引發此事件。 |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                            | 開啟應用程式行控制項時，平臺執行可能會引發此事件。 |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | 屬性變更的事件處理常式。                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> <dt>

**參考**
</dt> <dt>

[**AppBar XAML 控制項**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**WinJS. AppBar 物件**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
