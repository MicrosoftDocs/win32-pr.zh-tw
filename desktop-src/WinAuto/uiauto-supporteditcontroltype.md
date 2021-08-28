---
title: 編輯控制項類型
description: 本主題提供編輯控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- 消費者介面自動化，編輯控制項類型的支援
- 消費者介面自動化，編輯控制項類型
- 消費者介面自動化，編輯控制項類型的樹狀結構
- 消費者介面自動化，編輯控制項類型的屬性
- 消費者介面自動化，編輯控制項類型的控制項模式
- 消費者介面自動化，編輯控制項類型的事件
- 樹狀結構，編輯控制項類型
- 屬性、編輯控制項類型
- 控制項模式，編輯控制項類型
- 事件，編輯控制項類型
- 編輯控制項類型的支援
- Edit 控制項類型
- 控制項類型，編輯控制項類型的樹狀結構
- 控制項類型，編輯控制項類型的控制項模式
- 控制項類型，支援編輯
- 控制項類型，編輯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476131"
---
# <a name="edit-control-type"></a>編輯控制項類型

本主題提供 **編輯** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

本主題提供編輯控制項類型之使用者介面自動化支援的相關資訊。

下列章節會定義編輯控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有編輯控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述編輯控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>編輯</li></ul> | <ul><li>編輯</li></ul> | 




 

執行 **編輯** 控制項類型的控制項在消費者介面自動化樹狀結構的控制項視圖中一律會有零個捲軸，因為這是單行控制項。 在某些配置案例中，單行文字可能會換行。 **編輯** 控制項類型只適用于少量的文字。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與編輯控制項特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 編輯控制項必須有可點選的點，當使用者按一下滑鼠時，會將輸入焦點置於控制項的編輯部分。                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **編輯**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 此編輯控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | 編輯控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | 請參閱備註。 | 包含密碼的編輯控制項上必須設定為 **TRUE** 。 如果編輯控制項包含密碼內容，則螢幕助讀程式可使用這個屬性來判斷在使用者輸入密碼時，是否應讀出所按的按鍵。                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果有與控制項相關聯的靜態文字標籤，則此屬性必須公開該控制項的參考。 如果文字控制項是另一個控制項的子元件，則不會設定 **LabeledBy** 屬性。                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應到 **編輯** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的 [編輯]。                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 編輯控制項的名稱通常是從靜態文字標籤產生的。 如果沒有靜態文字標籤，則應用程式開發人員必須指派 **名稱** 的屬性值。 **Name** 屬性絕不能包含編輯控制項的文字內容。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出編輯控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                              | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | 相依       | 所有採用數位範圍的編輯控制項都必須公開 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。                                                                                                                                                                                                                                                                                       |
| [**最小值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | 請參閱備註。    | 這個屬性必須是編輯控制項內容可以設定的最小值。                                                                                                                                                                                                                                                                                                                     |
| [**最大值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | 請參閱備註。    | 這個屬性必須是編輯控制項內容可以設定的最大值。                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | 請參閱備註。    | 這個屬性必須指定該值可以設定的小數位數。 如果編輯控制項只接受整數， **SmallChange** 屬性值必須是1。 如果編輯控制項接受從1.0 到2.0 的範圍，則 **SmallChange** 屬性值必須是0.1。 如果編輯控制項接受從1.00 到2.00 的範圍，則 **SmallChange** 屬性值必須是0.001。                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | 編輯控制項無須公開這個屬性。                                                                                                                                                                                                                                                                                                                                                      |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | 請參閱備註。    | 這個屬性會指出編輯控制項的數值內容。 在 [ [**最小**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) 值] 和 [ [**最大**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) 值] 屬性指定的範圍內，消費者介面自動化用戶端設定更精確的值時，[ [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) ] 屬性會自動四捨五入至最接近的接受值。 |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | 必要      | 所有編輯控制項都必須支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，因為輔助技術用戶端必須一律提供詳細的資訊。                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | 相依       | 所有採用字串的編輯控制項都必須公開 [值](uiauto-implementingvalue.md) 控制項模式。                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | 請參閱備註。    | 您必須設定此屬性，以指出控制項是否可以透過程式設計方式設定值，或可由使用者編輯。                                                                                                                                                                                                                                                                                |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | 請參閱備註。    | 此屬性包含編輯控制項的文字內容。 如果 [ [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) ] 屬性設定為 [ **TRUE**]，則查詢 [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) 屬性必須傳回錯誤。                                                                                                                      |



 

## <a name="required-events"></a>必要的事件

下表列出需要支援編輯控制項的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                                |                                                                                                                            |
| [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                             | 如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 編輯控制項不支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      | 如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ 文字 \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    | 如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                                      | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="remarks"></a>備註

編輯控制項可以當做唯讀文字欄位使用，不支援選取或編輯文字。 這類編輯控制項的行為就像是具有特定名稱和值的欄位物件。

如果編輯控制項包含預留位置文字 (例如，提示橫幅) ，除非使用者可以編輯文字，然後重複使用做為預留位置文字，否則應該將文字當做 **HelpText** 屬性使用。 例如，開啟新索引標籤時，Windows Internet Explorer 位址列包含文字 "about： tab"。 這並不 **HelpText** ，因為它是程式設計的位址，可供使用者使用或編輯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




