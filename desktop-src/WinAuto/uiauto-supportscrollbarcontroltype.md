---
title: 捲軸控制項類型
description: 本主題提供捲軸控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- 消費者介面自動化、捲軸控制項類型的支援
- 消費者介面自動化、捲軸控制項類型
- 消費者介面自動化、捲軸控制項類型的樹狀結構
- 消費者介面自動化、捲軸控制項類型的屬性
- 消費者介面自動化、捲軸控制項類型的控制項模式
- 消費者介面自動化、捲軸控制項類型的事件
- 樹狀結構、捲軸控制項類型
- 屬性、捲軸控制項類型
- 控制項模式、捲軸控制項類型
- 事件、捲軸控制項類型
- 捲軸控制項類型的支援
- 捲軸控制項類型
- 控制項類型、捲軸控制項類型的樹狀結構
- 控制項類型、捲軸控制項類型的控制項模式
- 控制項類型、捲軸支援
- 控制項類型、捲軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a25d0398ca8e094e1dbec5e06eb725f3e9d7edbb5c193fdc3699e166b118142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413368"
---
# <a name="scrollbar-control-type"></a>捲軸控制項類型

本主題提供 **捲軸** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

捲軸控制項可讓使用者捲動視窗或項目容器內的內容。 此控制項是由一組按鈕和 thumb 控制項所組成。

下列章節會定義 **捲軸** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有捲軸控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述捲軸控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>ScrollBar
<ul>
<li>按鈕 (0、2或 4) </li>
<li>Thumb (0 或 1) </li>
</ul></li>
</ul></td>
<td>不適用。  (捲軸控制項沒有內容。 ) </td>
</tr>
</tbody>
</table>



 

捲軸控制項可以有零到五個子系。 因為子樹有一個以上的按鈕控制項，所以元素必須將特定的 [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) 值設定為每個專案，才能讓自動化測試控管可以找到它們。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與捲軸控制項特別相關。 請注意，捲軸控制項永遠沒有內容;它的功能是透過 [滾動](uiauto-implementingscroll.md) 條控制項模式來公開的，此模式在滾動的容器上受到支援。

如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值         | 注意                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。    | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。    | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | 捲軸控制項沒有可點選的點。                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ScrollBar** | 此值與所有架構的值相同。 作為滑杆運作的捲軸必須使用 [滑杆](uiauto-supportslidercontroltype.md) 控制項類型。                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | 捲軸控制項不是內容項目。 如果捲軸是獨立控制項，則必須滿足 [滑杆](uiauto-supportslidercontroltype.md)控制項類型，並傳回 [**IUIAutomationElement：： CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (或 [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) 屬性的 [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) 。 |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 捲軸控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。    | 如果控制項可接收鍵盤焦點，就必定支援此屬性。 捲軸控制項很少會取得焦點，但在此情況下，焦點應該留在捲軸控制項本身，而不是子按鈕或 thumb。 使用者應該能夠使用向上箭號和向下箭號， (或向右箭號和向下箭號) 按鍵，或 PAGE UP 和 PAGE DOWN 鍵來執行所有滾動動作。                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | 捲軸沒有標籤。                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。    | 對應到 **捲軸** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「捲軸」。                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | 捲軸控制項沒有 content 元素，而且不需要設定 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性。                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。    | 捲軸控制項必須一律公開其水平或垂直的方向。                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有捲軸控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。

> [!Note]  
> 使用捲軸作為僅限滑鼠操作的控制項時，不支援控制項模式。 如果用來作為應用程式內的滑杆控制項，則必須提供 [滑杆](uiauto-supportslidercontroltype.md) 控制項類型給它。

 



| 控制項模式                                           | 支援 | 注意                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | 相依 | 只有在具有捲軸的容器不支援[滾動](uiauto-implementingscroll.md)條控制項模式時，才需要支援[RangeValue](uiauto-implementingrangevalue.md)控制項模式。 |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | 永不   | 捲軸不直接支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                                                                                                     |



 

## <a name="required-events"></a>必要的事件

下表列出捲軸控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 附註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。        | 如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




