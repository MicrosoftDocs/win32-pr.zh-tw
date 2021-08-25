---
title: 標題控制項類型
description: 本主題提供標題控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- 消費者介面自動化，標題控制項類型的支援
- 消費者介面自動化，標題控制項類型
- 消費者介面自動化，標題控制項類型的樹狀結構
- 消費者介面自動化，標題控制項類型的屬性
- 消費者介面自動化，適用于標題控制項類型的控制項模式
- 消費者介面自動化，標題控制項類型的事件
- 樹狀結構，標題控制項類型
- 屬性、標題控制項類型
- 控制項模式，標題控制項類型
- 事件，標題控制項類型
- 標題控制項類型的支援
- Header 控制項類型
- 控制項類型，標題控制項類型的樹狀結構
- 控制項類型，標題控制項類型的控制項模式
- 控制項類型，支援標頭
- 控制項類型，標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482506"
---
# <a name="header-control-type"></a>標題控制項類型

本主題提供 **標題** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

標題控制項可為資料列或資料行資訊的標籤提供視覺容器。

下列章節會定義 **標題** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的標頭控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述標題控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>標頭<ul><li>HeaderItem (1 個以上)</li></ul></li></ul> | (不適用) | 




 

標題控制項在消費者介面自動化樹狀結構的控制視圖中一律會有一或多個子系。

標題控制項在消費者介面自動化樹狀結構的內容視圖中有零個子系。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與標題控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值                                                            | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。                                                       | 這個屬性的值在應用程式中的所有控制項之間必須是唯一的。                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。                                                       | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。                                                       | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **標頭**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE                                                            | 標題控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true                                                             | 標題控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。                                                       | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | 標題控制項沒有靜態標籤。                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。                                                       | 預設值為 "header"，代表 en-us 或英文 (美國) 。                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。                                                       | 如果有一個以上的資料列標題或資料行標題，標題控制項就需要名稱。 如此可識別標題內的資訊。                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_水準** 或 **OrientationType \_ 垂直** | 這個屬性的值會公開標題控制項的位置，也就是它是否為數據列標頭， (**OrientationType \_ 水準**) 或資料行標頭 (**OrientationType \_ 垂直**) 。                 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出標題控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援 | 注意                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | 相依 | 如果標頭控制項可以調整大小，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的標題控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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

 

 




