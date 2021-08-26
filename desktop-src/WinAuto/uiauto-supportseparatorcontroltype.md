---
title: 分隔符號控制項類型
description: 本主題提供分隔符號控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- 消費者介面自動化、分隔符號控制項類型的支援
- 消費者介面自動化、分隔符號控制項類型
- 消費者介面自動化，分隔符號控制項類型的樹狀結構
- 消費者介面自動化，分隔符號控制項類型的屬性
- 消費者介面自動化，分隔符號控制項類型的控制項模式
- 消費者介面自動化，分隔符號控制項類型的事件
- 樹狀結構、分隔符號控制項類型
- 屬性、分隔符號控制項類型
- 控制項模式、分隔符號控制項類型
- 事件、分隔符號控制項類型
- 分隔符號控制項類型的支援
- Separator 控制項類型
- 控制項類型、分隔符號控制項類型的樹狀結構
- 控制項類型、分隔符號控制項類型的控制項模式
- 控制項類型，支援分隔符號
- 控制項類型，分隔符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0685f21565a6252febfadad115c8edf10990995c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477714"
---
# <a name="separator-control-type"></a>分隔符號控制項類型

本主題提供 **分隔符號** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

分隔符號控制項是用來以視覺方式將空間分隔成兩個區域。 例如，分隔符號控制項可以是定義視窗中兩個窗格的分隔線。 如果分隔符號是可移動的，控制項就應公開為控制項類型 Thumb。

下列章節會定義 **分隔符號** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的分隔符號控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與分隔符號控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>Separator</li></ul> | <ul><li><strong>分隔符號</strong>控制項類型永遠不會有內容。</li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與分隔符號控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值         | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。    | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。    | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。    | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Separator** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | 分隔符號控制項絕不會是內容。                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 分隔符號控制項必須一律是控制項。                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。    | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | 分隔符號控制項沒有靜態標籤。                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。    | 對應至 **分隔符號** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「分隔符號」。                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""            | 分隔符號控制項不需要 **Name** 屬性。                                                                                                                                          |



 

## <a name="required-control-patterns"></a>必要的控制項模式

分隔符號控制項不必支援任何控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。

## <a name="required-events"></a>必要的事件

下表列出需要分隔符號控制項的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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

 

 




