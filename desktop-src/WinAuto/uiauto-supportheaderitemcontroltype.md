---
title: HeaderItem 控制項類型
description: 本主題提供 HeaderItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- 消費者介面自動化，HeaderItem 控制項類型的支援
- 消費者介面自動化，HeaderItem 控制項類型
- 消費者介面自動化，HeaderItem 控制項類型的樹狀結構
- 消費者介面自動化，HeaderItem 控制項類型的屬性
- 消費者介面自動化，HeaderItem 控制項類型的控制項模式
- 消費者介面自動化，HeaderItem 控制項類型的事件
- 樹狀結構，HeaderItem 控制項類型
- properties、HeaderItem 控制項類型
- 控制項模式，HeaderItem 控制項類型
- events、HeaderItem 控制項類型
- HeaderItem 控制項類型的支援
- HeaderItem 控制項類型
- 控制項類型，HeaderItem 控制項類型的樹狀結構
- 控制項類型，HeaderItem 控制項類型的控制項模式
- 控制項類型，支援 HeaderItem
- 控制項類型，HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6bbcd6d86e7401c3fa98d162e3aa273613dfd3a32705da891fc89d1f4ea003f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098208"
---
# <a name="headeritem-control-type"></a>HeaderItem 控制項類型

本主題提供 **HeaderItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

**HeaderItem** 控制項類型提供資料列或資料行的視覺標籤。

下列章節會定義 **HeaderItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的標題專案控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述標題專案控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的專案。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>HeaderItem</li>
</ul></td>
<td>(不適用)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **HeaderItem** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值          | 注意                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。     | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。     | 包含整個控制項的最外層矩形。                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。     | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **HeaderItem** | 此值與所有使用者介面架構的值相同。                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE          | 標題專案控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true           | 標題專案控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。     | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | 請參閱附註      | 這個屬性會提供依照標題項目之排序次序的相關資訊。                                                                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL           | 標題專案控制項沒有靜態文字標籤。                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。     | 對應到 **HeaderItem** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「標頭專案」。                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。     | 標題項目控制項一律自行設定標籤。                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有標題專案控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援 | 注意                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | 相依 | 如果可以按一下標頭專案控制項來排序資料，請執行 [Invoke](uiauto-implementinginvoke.md) 控制項模式。 |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | 相依 | 如果標頭專案控制項可以調整大小，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。            |



 

## <a name="required-events"></a>必要的事件

下表列出支援的標題專案控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | 如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。           |
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

 

 




