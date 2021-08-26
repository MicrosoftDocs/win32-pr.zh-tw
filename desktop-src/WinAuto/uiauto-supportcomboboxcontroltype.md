---
title: ComboBox 控制項類型
description: 本主題提供 ComboBox 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- 消費者介面自動化，ComboBox 控制項類型的支援
- 消費者介面自動化，ComboBox 控制項類型
- 消費者介面自動化，ComboBox 控制項類型的樹狀結構
- 消費者介面自動化，ComboBox 控制項類型的屬性
- 消費者介面自動化，ComboBox 控制項類型的控制項模式
- 消費者介面自動化，ComboBox 控制項類型的事件
- 樹狀結構，ComboBox 控制項類型
- 屬性、ComboBox 控制項類型
- 控制項模式，ComboBox 控制項類型
- 事件、ComboBox 控制項類型
- ComboBox 控制項類型的支援
- ComboBox 控制項類型
- ComboBox 控制項類型的控制項類型、樹狀結構
- 控制項類型，ComboBox 控制項類型的控制項模式
- 控制項類型，支援 ComboBox
- 控制項類型，ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480104"
---
# <a name="combobox-control-type"></a>ComboBox 控制項類型

本主題提供 **ComboBox** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。 控制項的清單方塊部分會隨時顯示，或是只在使用者選取下拉式箭號 (這是按鈕) 時出現在控制項旁邊。 如果選取項目欄位是編輯控制項，使用者可以輸入不在清單中的資訊，否則使用者只能選取清單中的項目。

下列章節會定義 **ComboBox** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的下拉式方塊控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與下拉式方塊控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>ComboBox<ul><li>編輯 (0 或 1 個)</li><li>列出 (0 或 1) </li><li>清單項目 (子系清單；0 到多個)</li><li>按鈕 (1)</li></ul></li></ul> | <ul><li>ComboBox<ul><li>清單項目 (0 到多個)</li></ul></li></ul> | 




 

只有當下拉式方塊可以編輯為採用任何輸入（如同在 [ **執行** ] 對話方塊中的下拉式方塊的情況下）時，才需要在下拉式方塊的控制項視圖中編輯控制項。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **ComboBox** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | 下拉式方塊控制項的解說文字應解釋為何系統會詢問使用者如何從下拉式方塊中選擇一個選項。 文字類似於透過工具提示呈現的資訊。 例如，「選取項目以設定顯示器的解析度。」                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 下拉式方塊控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 下拉式方塊控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true       | 下拉式方塊控制項可以接收鍵盤焦點;不過，當消費者介面自動化用戶端將焦點設為下拉式方塊時，下拉式方塊子樹中的任何專案都可以接收焦點。                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 下拉式方塊控制項通常會有此屬性參考的靜態文字標籤。                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **ComboBox** 控制項類型的當地語系化字串。 預設值為「下拉式方塊」，適用于 en-us 或英文 (美國) 。                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 下拉式方塊控制項的名稱通常會從靜態文字標籤產生。 如果沒有靜態文字標籤，您必須為 [ **名稱** ] 屬性指派值。 當下拉式方塊的內容變更時，[ **名稱** ] 屬性不應包含下拉式方塊的目前內容或變更。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有下拉式方塊控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                                   | 支援  | 注意                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 必要 | 必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，因為下拉式方塊控制項一定要包含下拉式按鈕。                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | 相依  | 在下拉式方塊中顯示目前選取範圍。 [選取](uiauto-implementingselection.md)控制項模式的支援會委派給下拉式方塊下方的清單方塊，但不一定都可行。                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | 相依  | 如果下拉式方塊可以採用任意文字值，則必須支援 [值](uiauto-implementingvalue.md) 控制項模式。 此模式可讓您以程式設計方式設定下拉式方塊的字串內容。 如果不支援值控制項模式，使用者必須從下拉式方塊的子樹中的清單專案中選取。 |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | 永不    | 下拉式方塊中不會直接支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。 如果下拉式方塊中包含的清單方塊可以滾動，而且只有在畫面上看不到清單方塊時，才支援此功能。                                                                                                              |



 

## <a name="required-events"></a>必要的事件

下表列出支援的下拉式方塊控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                                | 備註                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                              |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                              | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                          | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                               | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




