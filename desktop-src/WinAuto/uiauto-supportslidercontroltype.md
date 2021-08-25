---
title: 滑杆控制項類型
description: 本主題提供滑杆控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- 消費者介面自動化，滑杆控制項類型的支援
- 消費者介面自動化，滑杆控制項類型
- 消費者介面自動化，滑杆控制項類型的樹狀結構
- 消費者介面自動化，滑杆控制項類型的屬性
- 消費者介面自動化，滑杆控制項類型的控制項模式
- 消費者介面自動化，滑杆控制項類型的事件
- 樹狀結構，滑杆控制項類型
- 屬性、滑杆控制項類型
- 控制項模式、滑杆控制項類型
- events、Slider 控制項類型
- 滑杆控制項類型的支援
- Slider 控制項類型
- 滑杆控制項類型的控制項類型、樹狀結構
- 控制項類型、滑杆控制項類型的控制項模式
- 控制項類型，支援滑杆
- 控制項類型，滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472874"
---
# <a name="slider-control-type"></a>滑杆控制項類型

本主題提供 **滑杆** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。

滑杆控制項是具有按鈕的複合控制項，可讓使用者設定數位範圍，或從一組專案中選取。

下列章節會定義 **滑杆** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有滑杆控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述滑杆控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>Slider<ul><li>按鈕 (2 或 4)</li><li>Thumb (1) </li><li>清單專案 (0 或更多) </li></ul></li></ul> | <ul><li>Slider<ul><li>清單專案 (0 或更多) </li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與滑杆控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 大部分的滑杆控制項都必須傳回 [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) 錯誤，因為滑杆控制項的整個周框控制項是由子控制項所佔用。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **滑桿** | 此值與所有架構的值相同。                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 滑杆控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 滑杆控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。 滑杆控制項 (按鈕和 thumb) 的子系不應取得焦點。 焦點應該一律保留在滑杆控制項本身。       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果有與控制項相關聯的靜態文字標籤，則此屬性必須公開該控制項的參考。 如果文字控制項是另一個控制項的子元件，則不會設定 **LabeledBy** 屬性。   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **滑杆** 控制項類型的當地語系化字串。 預設值為 "slider"，代表 en-us 或英文 (美國) 。                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 滑杆控制項的名稱通常會從靜態文字標籤產生。 如果沒有靜態文字標籤，則應用程式開發人員必須指派 **名稱** 的屬性值。                              |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有滑杆控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                          | 支援/值 | 備註                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | 相依       | 如果內容可以設定為數值範圍內的值，則滑杆應支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | 相依       | 如果內容代表一組不同選項中的一個值，則滑杆應支援 [選取](uiauto-implementingselection.md) 控制項模式。 支援選取控制項模式時，對應的選項必須公開為滑桿的一個或多個子清單項目。 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | 相依       | 如果內容代表一組離散選項中的一個值，則滑杆應支援 [值](uiauto-implementingvalue.md) 控制項模式。                                                                                                                                                     |



 

## <a name="required-events"></a>必要的事件

下表列出滑杆控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。        | 如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                       | 如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                  | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




