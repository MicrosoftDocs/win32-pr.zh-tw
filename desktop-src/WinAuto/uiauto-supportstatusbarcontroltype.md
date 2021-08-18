---
title: 狀態列控制項類型
description: 本主題提供關於狀態列控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- 消費者介面自動化，支援狀態列控制項類型
- 消費者介面自動化，狀態列控制項類型
- 消費者介面自動化，狀態列控制項類型的樹狀結構
- 消費者介面自動化，狀態列控制項類型的屬性
- 消費者介面自動化，狀態列控制項類型的控制項模式
- 消費者介面自動化，狀態列控制項類型的事件
- 樹狀結構，狀態列控制項類型
- 屬性、狀態列控制項類型
- 控制項模式、狀態列控制項類型
- 事件、狀態列控制項類型
- 狀態列控制項類型的支援
- StatusBar 控制項類型
- 控制項類型，狀態列控制項類型的樹狀結構
- 控制項類型，狀態列控制項類型的控制項模式
- 控制項類型，支援狀態列
- 控制項類型，狀態列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52f3f04db86a8c8ff0e9cad9a3938a17e996e8210960912c3abc5039468e178
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614248"
---
# <a name="statusbar-control-type"></a>狀態列控制項類型

本主題提供關於 **狀態列** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

狀態列控制項可以顯示多項資訊：在應用程式的視窗中檢視的物件、物件的元件，或是與物件的作業相關的內容資訊。

下列章節會定義 **狀態列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有狀態列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表說明與狀態列控制項相關的消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>StatusBar
<ul>
<li>編輯 (0 個以上)</li>
<li>進度列 (0 個以上)</li>
<li>影像 (0 個以上)</li>
<li>按鈕 (0 個以上)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>編輯 (0 個以上)</li>
<li>進度列 (0 個以上)</li>
<li>影像 (0 個以上)</li>
<li>按鈕 (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與狀態列控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值         | 注意                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。    | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。    | 狀態列的週框必須框住其中所有控制項。                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。    | 如果有週框即受支援。 如果周框內有一些區域無法按下，且專案執行特製化的點擊測試，請覆寫這個專案，並提供可點按的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 狀態列控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | 狀態列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 相依       | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | 相依       | 如果目前看不到狀態列控制項，此屬性將會傳回 TRUE。                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | 狀態列控制項通常沒有標籤。                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。    | 對應到 **狀態列** 控制項類型的當地語系化字串。 預設值為 en-us 或英文 (美國) 的「狀態列」。                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。    | 除非應用程式使用一個以上的狀態列，否則狀態列不需要名稱。 在此情況下，請將每個條碼與名稱（例如「網際網路狀態」或「應用程式狀態」）加以區別。                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | 相依       | 指出控制項方向的值：水準或垂直。                                                                                                                                               |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出狀態列控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                               | 支援  | 注意                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | 選擇性 | 狀態列控制項應支援 [方格](uiauto-implementinggrid.md) 控制項模式，以便監視和輕鬆參考個別的元件以取得資訊。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援的狀態列控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                   |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 **IsEnabled** 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 **IsOffscreen** 屬性，就必須支援這個事件。 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>備註

建議您在狀態列中使用編輯控制項做為子格線元素。 使用編輯控制項可讓您使用 [專案名稱] 和 [值] 屬性，更輕鬆地將 status 欄位的用途與其值產生關聯。 因為文字控制項不應支援 **值** 控制項模式，所以不應該當做子格線元素使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




