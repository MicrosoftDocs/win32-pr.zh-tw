---
title: Button 控制項類型
description: 本主題提供按鈕控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- 消費者介面自動化，Button 控制項類型的支援
- 消費者介面自動化，Button 控制項類型
- 消費者介面自動化，Button 控制項類型的樹狀結構
- 消費者介面自動化，Button 控制項類型的屬性
- 消費者介面自動化，Button 控制項類型的控制項模式
- 消費者介面自動化，Button 控制項類型的事件
- 樹狀結構，按鈕控制項類型
- 屬性，按鈕控制項類型
- 控制項模式，按鈕控制項類型
- 事件、按鈕控制項類型
- Button 控制項類型的支援
- Button 控制項類型
- 控制項類型、按鈕控制項類型的樹狀結構
- 控制項類型、按鈕控制項類型的控制項模式
- 控制項類型、支援按鈕
- 控制項類型，按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c080018e0fcaf8cd196204f80c61041d03fc1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478034"
---
# <a name="button-control-type"></a>Button 控制項類型

本主題提供 **按鈕** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。

按鈕是可供使用者互動的物件，能在對話方塊執行如 [確定] 和 [取消] 按鈕等動作。 按鈕控制項的公開方式很簡單，因為它對應的是使用者想要完成的單一命令。

下列章節會定義 **按鈕** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有按鈕控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述按鈕控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>Button<ul><li>影像 (0 個以上)</li><li>文字 (0 個以上)</li></ul></li></ul> | <ul><li>Button</li></ul> | 




 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與執行 **按鈕** 控制項 (類型的控制項（例如按鈕控制項) ）特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 按鈕控制項通常支援快速鍵，讓使用者能夠快速地從鍵盤執行按鈕所代表的動作。                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **按鈕** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | 解說文字應該會指出啟用按鈕的最終結果是什麼。 這通常是透過工具提示顯示的相同類型資訊。                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 按鈕控制項必須一律為內容。                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 按鈕控制項必須一律為控制項。                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | 按鈕控制項會自行將其內容設為標籤。                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應到 **按鈕** 控制項類型的當地語系化字串。 針對 en-us 或英文 (美國) ，預設值為 "button"。                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 按鈕控制項的名稱是用來加上標籤的文字。 只要使用影像來標記按鈕，就必須為按鈕的 [ **名稱** ] 屬性提供替代文字。                        |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有按鈕控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                  | 支援/值 | 備註                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | 請參閱備註。    | 當按鈕裝載為分割按鈕的子系時，子按鈕可以支援[ExpandCollapse](uiauto-implementingexpandcollapse.md)控制項模式，而不是叫[用或](uiauto-implementinginvoke.md)[切換](uiauto-implementingtoggle.md)控制項模式。 ExpandCollapse 控制項模式可用來開啟或關閉功能表，或與 button 元素相關聯的其他子結構。 |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | 請參閱備註。    | 所有按鈕都應該支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式或 [開關](uiauto-implementingtoggle.md) 控制項模式，但不能同時支援兩者。 當按鈕在要求使用者時執行命令時，必須支援 Invoke 控制項模式。 此命令對應於如「剪下」、「複製」、「貼上」或「刪除」等單一作業。                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | 請參閱備註。    | 所有按鈕都應該支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式或 [開關](uiauto-implementingtoggle.md) 控制項模式，但不能同時支援兩者。 如果按鈕可以迴圈處理最多三個狀態的一連串，則必須支援切換控制項模式。 這通常是指特定功能的開關切換。                                                                        |



 

## <a name="required-events"></a>必要的事件

下表列出按鈕控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | 如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。           |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。    | 如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




