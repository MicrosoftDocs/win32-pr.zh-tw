---
title: 標題列控制項類型
description: 本主題提供標題列控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 標題列控制項代表視窗中的標題或標題列。
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- 消費者介面自動化，標題控制項類型的支援
- 消費者介面自動化，標題列控制項類型
- 消費者介面自動化，標題列控制項類型的樹狀結構
- 消費者介面自動化，標題列控制項類型的屬性
- 消費者介面自動化，標題列控制項類型的控制項模式
- 消費者介面自動化，標題列控制項類型的事件
- 樹狀結構，標題控制項類型
- 屬性、標題列控制項類型
- 控制項模式、標題列控制項類型
- 事件、標題列控制項類型
- 標題列控制項類型的支援
- 標題列控制項類型
- 控制項類型，標題列控制項類型的樹狀結構
- 控制項類型，標題列控制項類型的控制項模式
- 控制項類型，支援標題列
- 控制項類型，標題列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e3d3ed0c4a3abc995afab7aec4aa89d02542e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473354"
---
# <a name="titlebar-control-type"></a>標題列控制項類型

本主題提供 **標題列** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 標題列控制項代表視窗中的標題或標題列。

下列章節會定義 **標題列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的標題列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述標題列控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>標題列<ul><li>功能表 (0 或 1 個)</li><li>按鈕 (0 個以上)</li></ul></li></ul> |  (不適用;標題列控制項沒有內容)  | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **標題列** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 這個屬性所公開的值必須包含所有內含的控制項。                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **標題列** | 此值與所有使用者介面架構的值相同。                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE        | 標題列控制項絕不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 標題列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | 標題列控制項永遠不會有鍵盤焦點。                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 相依      | 標題列控制項會根據畫面上是否可見來傳回值。                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。   | 標題列控制項通常沒有標籤。                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應到標題列控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「標題列」。                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | 標題列不是內容;其文字資訊會以父視窗的名稱來公開。                                                                                                     |



 

## <a name="required-control-patterns"></a>必要的控制項模式

**標題列** 控制項類型不需要支援任何控制項模式。 它的功能是透過[window 控制項類型](uiauto-supportwindowcontroltype.md)上的[window](uiauto-implementingwindow.md)控制項模式來公開。

## <a name="required-events"></a>必要的事件

下表列出支援的標題列控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




