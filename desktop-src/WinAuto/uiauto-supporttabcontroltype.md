---
title: 索引標籤控制項類型
description: 本主題提供索引標籤控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- 消費者介面自動化，支援索引標籤控制項類型
- 消費者介面自動化，索引標籤控制項類型
- 消費者介面自動化，索引標籤控制項類型的樹狀結構
- 消費者介面自動化，索引標籤控制項類型的屬性
- 消費者介面自動化、索引標籤控制項類型的控制項模式
- 消費者介面自動化，索引標籤控制項類型的事件
- 樹狀結構，索引標籤控制項類型
- 屬性，索引標籤控制項類型
- 控制項模式，索引標籤控制項類型
- 事件，索引標籤控制項類型
- 支援索引標籤控制項類型
- Tab 控制項類型
- 控制項類型，索引標籤控制項類型的樹狀結構
- 控制項類型，索引標籤控制項類型的控制項模式
- 控制項類型，支援 Tab
- 控制項類型，Tab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a83263db87a68e258598ea46ca903af2ddb39c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482494"
---
# <a name="tab-control-type"></a>索引標籤控制項類型

本主題提供 **選項卡** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

「索引標籤控制項」類似於筆記本裡的分隔頁或檔案櫃中的標籤。 藉由使用索引標籤控制項，應用程式可以定義視窗或對話方塊中同一個區域的多個頁面。

下列章節會定義 **選項卡** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的索引標籤控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與索引標籤控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>索引標籤<ul><li>TabItem (1 個以上)</li><li>捲軸 (0 或 1 個)<ul><li>按鈕 (0 或 2 個)</li></ul></li></ul></li></ul> | <ul><li>索引標籤<ul><li>TabItem (1 個以上)</li></ul></li></ul> | 




 

索引標籤控制項根據 [TabItem](uiauto-supporttabitemcontroltype.md) 控制項類型，有子消費者介面自動化專案。 當索引標籤專案分組時 (例如 Microsoft Office 應用程式中) **選項卡** 控制項類型也可以裝載 **群組** 索引標籤專案的群組控制項類型，如下列樹狀結構所示。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>索引標籤<ul><li>TabItem (1 個以上)</li><li>Group (0 個以上)<ul><li>TabItem (0 個以上)</li></ul></li><li>捲軸 (0 或 1 個)<ul><li>按鈕 (0 或 2 個)</li></ul></li></ul></li></ul> | <ul><li>索引標籤<ul><li>TabItem (1 個以上)</li><li>Group (0 個以上)<ul><li>TabItem (0 個以上)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與索引標籤控制項特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 否         | 索引標籤控制項沒有可點按的點。                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tab**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 索引標籤控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 索引標籤控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true       | 索引標籤控制項類型必須能夠接收鍵盤焦點。 一般而言，消費者介面自動化用戶端會在索引標籤控制項上呼叫 [**IUIAutomationElement：： SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) ，其中一個專案會將鍵盤焦點轉送至索引標籤控制項。 部分索引標籤容器可以接收焦點，而無須將焦點設在容器的其中一個項目。 |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 索引標籤控制項通常會有透過此屬性公開的靜態文字標籤。                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **選項卡** 控制項類型的當地語系化字串。 預設值為 "tab" 代表 en-us 或英文 (美國) 。                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 索引標籤控制項很少需要 **名稱** 屬性。                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。 | 此索引標籤控制項必須一律指出是水平或垂直放置。                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有索引標籤控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                             | 支援/值 | 備註                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | 必要      | 所有的索引標籤控制項都必須支援 [選取](uiauto-implementingselection.md) 控制項模式。                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | true          | 索引標籤控制項一律需要選取某個項目。                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | 索引標籤控制項一律是單一選取容器。                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | 相依       | 如果索引標籤控制項具有可讓一組索引標籤專案通過滾動的 widget，則必須支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的索引標籤控制項消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




