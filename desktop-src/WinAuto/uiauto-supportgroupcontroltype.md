---
title: 群組控制項類型
description: 本主題提供有關 Microsoft 消費者介面自動化 Group 控制項類型支援的資訊。
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- 消費者介面自動化，支援 Group 控制項類型
- 消費者介面自動化，Group 控制項類型
- 消費者介面自動化，群組控制項類型的樹狀結構
- 消費者介面自動化，群組控制項類型的屬性
- 消費者介面自動化，群組控制項類型的控制項模式
- 消費者介面自動化，群組控制項類型的事件
- 樹狀結構，群組控制項類型
- 屬性，群組控制項類型
- 控制項模式，群組控制項類型
- 事件、群組控制項類型
- 群組控制項類型的支援
- Group 控制項類型
- 控制項類型，群組控制項類型的樹狀結構
- 控制項類型，群組控制項類型的控制項模式
- 控制項類型，支援群組
- 控制項類型，群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477744"
---
# <a name="group-control-type"></a>群組控制項類型

本主題提供有關 Microsoft 消費者介面自動化 **Group** 控制項類型支援的資訊。

群組控制項代表階層內的節點。 **組合** 控制項類型會在消費者介面自動化樹狀結構中建立分隔，讓群組在一起的專案在消費者介面自動化樹狀結構內具有邏輯除法。

下列章節會定義 **Group** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的群組控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與群組控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>Group<ul><li>0 個以上的控制項</li></ul></li></ul> | <ul><li>Group<ul><li>0 個以上的控制項</li></ul></li></ul> | 




 

群組控制項通常包含子樹 [中的控制項](uiauto-supportlistitemcontroltype.md)類型消費者介面自動化支援，包括專案組合、 [TreeItem](uiauto-supporttreeitemcontroltype.md)和 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。 因為群組控制項是泛型容器，所以在樹狀結構中的群組控制項下可以有任何類型的控制項。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與群組控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **群組**  |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 此群組控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 此群組控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 群組控制項通常會自行設定標籤。 在這些情況下，會傳回 **Null**。 如果群組具有靜態文字標籤，則會傳回標籤作為 **LabeledBy** 屬性的值。                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **組合** 控制項類型的當地語系化字串。 預設值為 "group"，代表 en-us 或英文 (美國) 。                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 群組控制項通常會從控制項的標籤文字取得名稱。                                                                                                                     |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出 **群組** 控制項類型所需的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援 | 注意                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 相依 | 可以用來顯示或隱藏資訊的群組控制項，必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。 |



 

## <a name="required-events"></a>必要的事件

下表列出需要支援群組控制項的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                                                  |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式控制項模式，就必須支援這個事件。 |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                         |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。                       |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                 | 如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




