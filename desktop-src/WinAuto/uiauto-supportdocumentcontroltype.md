---
title: 檔控制項類型
description: 本主題提供檔控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- 消費者介面自動化，檔控制項類型的支援
- 消費者介面自動化，檔控制項類型
- 消費者介面自動化，Document 控制項類型的樹狀結構
- 消費者介面自動化，Document 控制項類型的屬性
- 消費者介面自動化，檔控制項類型的控制項模式
- 消費者介面自動化，Document 控制項類型的事件
- 樹狀結構，檔控制項類型
- 屬性，檔控制項類型
- 控制項模式，檔控制項類型
- 事件，檔控制項類型
- Document 控制項類型的支援
- Document 控制項類型
- 控制項類型，檔控制項類型的樹狀結構
- 控制項類型，檔控制項類型的控制項模式
- 控制項類型，支援檔
- 控制項類型，檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb068e5b2d69c3b7ac180b65436888ca550b1db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467795"
---
# <a name="document-control-type"></a>檔控制項類型

本主題提供 **檔** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

控制項可讓使用者檢視和操作多個頁面的文字。 不同于僅支援簡單的未格式化文字的編輯控制項，document 控制項可以裝載豐富樣式和格式化的文字。

下列章節會定義 **檔** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有檔控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與檔控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>文件<ul><li>不定</li></ul></li></ul> | <ul><li>文件<ul><li>不定</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與檔控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值        | 注意                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。   | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。   | 包含整個控制項的最外層矩形。                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。   | 文件具有可按的點，它會使文件容器中其中一個項目的文件具有焦點。                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **文件** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 檔控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | 檔控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。   | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。   | 這個屬性的值應該是文件控制項的標籤。 通常會使用文件的標題。                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。   | 對應至 **檔** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「檔」。            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。   | Document 控制項通常會從載入它的檔案名中取得其名稱。 這通常會顯示在包含視窗或框架標題。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出檔控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                  | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | 相依       | 文件控制項的跨越範圍可能大於檢視區的跨越範圍。 如果內容為可滾動的，則控制項應支援 [滾動](uiauto-implementingscroll.md) 控制項模式。                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | 必要      | 所有檔控制項都必須支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式。                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | 相依       | 雖然消費者介面自動化用戶端可以使用 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 取得檔的文字資訊，但是它們需要 [值](uiauto-implementingvalue.md) 控制項模式來設定內部值。 只有透過值控制項模式才能使用簡單的文字專案。 |



 

## <a name="required-events"></a>必要的事件

下表列出檔控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | 如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。     |
| [**UIA \_ 文字 \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                       | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




