---
title: ProgressBar 控制項類型
description: 本主題提供 ProgressBar 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- 消費者介面自動化，ProgressBar 控制項類型的支援
- 消費者介面自動化，ProgressBar 控制項類型
- 消費者介面自動化，ProgressBar 控制項類型的樹狀結構
- 消費者介面自動化，ProgressBar 控制項類型的屬性
- 消費者介面自動化，ProgressBar 控制項類型的控制項模式
- 消費者介面自動化，ProgressBar 控制項類型的事件
- 樹狀結構，ProgressBar 控制項類型
- properties、ProgressBar 控制項類型
- 控制項模式，ProgressBar 控制項類型
- events、ProgressBar 控制項類型
- ProgressBar 控制項類型的支援
- ProgressBar 控制項類型
- 控制項類型，ProgressBar 控制項類型的樹狀結構
- 控制項類型，ProgressBar 控制項類型的控制項模式
- 控制項類型，支援 ProgressBar
- 控制項類型，ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/06/2019
ms.locfileid: "104092487"
---
# <a name="progressbar-control-type"></a>ProgressBar 控制項類型

本主題提供 **ProgressBar** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

進度列控制項指出冗長作業的進度。 此控制項包含一個矩形，隨著作業的進度，會逐漸填滿系統的醒目提示色彩。

下列章節會定義 **ProgressBar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有進度列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

- [一般樹狀結構](#typical-tree-structure)
- [相關屬性](#relevant-properties)
- [必要的控制項模式](#required-control-patterns)
- [必要的事件](#required-events)
- [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與進度列控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>控制項檢視</th>
<th>內容檢視</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>ProgressBar</li>
</ul></td>
<td><ul>
<li>ProgressBar</li>
</ul></td>
</tr>
</tbody>
</table>

進度列控制項在消費者介面自動化樹狀結構的控制項或內容視圖中沒有任何子系。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與進度列特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。

| 使用者介面自動化屬性                                                                                              | 值           | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。      | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。      | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。      | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **進度列** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | 進度列控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | 進度列控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。      | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。      | 如果有靜態文字標籤，這個屬性必須公開該控制項的參考。                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。      | 對應到 **ProgressBar** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「進度列」。                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。      | 進度列控制項的名稱通常來自靜態文字標籤。 如果沒有靜態文字標籤，應用程式開發人員就必須公開 Name 屬性的值。                  |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出進度列控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                              | 支援/值 | 備註                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | 相依       | 使用數值範圍的進度列控制項必須執行 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。        |
| [**最小值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | 相依           | 這個屬性的值是控制項可以設定的最小值。 此值應小於 [**最大**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)值。                                                      |
| [**最大**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | 相依         | 這個屬性的值是控制項可以設定的最大值。 此值應大於 [**最小**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)值。                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | 這個屬性不是必要項，因為進度列控制項是唯讀的。                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | 這個屬性不是必要項，因為進度列控制項是唯讀的。                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | 相依       | 提供進度文字指示的進度列控制項必須執行實 [值](uiauto-implementingvalue.md) 控制項模式。 |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | 這個屬性的值一律為 **TRUE**。                                                                                            |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | 請參閱備註。    | 此屬性會公開進度列控制項的文字進度。                                                                          |



 

## <a name="required-events"></a>必要的事件

下表列出支援進度列所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。        | 如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。   |
| [**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。                  | 如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




