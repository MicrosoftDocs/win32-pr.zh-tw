---
title: Thumb 控制項類型
description: 本主題提供有關 Microsoft 消費者介面自動化 Thumb 控制項類型支援的相關資訊。
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- 消費者介面自動化，Thumb 控制項類型的支援
- 消費者介面自動化，Thumb 控制項類型
- 消費者介面自動化，Thumb 控制項類型的樹狀結構
- 消費者介面自動化，Thumb 控制項類型的屬性
- 消費者介面自動化、Thumb 控制項類型的控制項模式
- 消費者介面自動化，Thumb 控制項類型的事件
- 樹狀結構，Thumb 控制項類型
- properties、Thumb 控制項類型
- 控制項模式、Thumb 控制項類型
- 事件、Thumb 控制項類型
- Thumb 控制項類型的支援
- Thumb 控制項類型
- 控制項類型，Thumb 控制項類型的樹狀結構
- 控制項類型、Thumb 控制項類型的控制項模式
- 控制項類型，支援 Thumb
- 控制項類型、Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372570"
---
# <a name="thumb-control-type"></a>Thumb 控制項類型

本主題提供有關 Microsoft 消費者介面自動化 **Thumb** 控制項類型支援的相關資訊。

Thumb 控制項提供移動 (或拖曳) 控制項的功能 (如捲軸按鈕)，或是調整控制項大小的功能 (如會調整 Widget 大小的視窗)。 請注意，thumb 控制項不會提供拖放功能。 Thumb 控制項可以接收滑鼠焦點，而不是鍵盤焦點。 控制項開發人員必須正確實作控制項，使其能夠適當運作 (可供拖曳或調整大小)。

下列章節會定義 **Thumb** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的 thumb 控制項，UI 架構/平臺會將控制項類型和控制項模式的消費者介面自動化支援全部整合在一起。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述的是與 thumb 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>Thumb</li>
</ul></td>
<td>(不適用)</td>
</tr>
</tbody>
</table>



 

Thumb 控制項不會出現在內容視圖中，因為它們只會在使用滑鼠操作時存在。 它們是由 thumb 控制項容器支援的另一個控制項模式（例如 [滾動](uiauto-implementingscroll.md) 條控制項模式、 [轉換](uiauto-implementingtransform.md) 控制項模式或 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式）所公開。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 thumb 控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | Thumb 控制項之可見工作區內的某個點。                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **拇指**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Thumb 控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Thumb 控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。 如果 thumb 控制項是用來做為視窗大小調整視窗或窗格的「控制手柄」物件，就可以接收焦點。 滑杆或捲軸中的 thumb 控制項絕對不會收到焦點。 |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Thumb 控制項一律沒有標籤。                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **Thumb** 控制項類型的當地語系化字串。 預設值為 "thumb"，代表 en-us 或英文 (美國) 。                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | 由於 thumb 控制項無法在消費者介面自動化樹狀結構的內容視圖中使用，因此不需要名稱。                                                                                                                                        |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出 thumb 控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援  | 注意                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | 必要 | 使畫面上的 Thumb 控制項可以移動。 由於 thumb 控制項通常無法調整大小或旋轉，因此 [轉換](uiauto-implementingtransform.md) 控制項模式主要支援 [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) 函數。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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

 

 




