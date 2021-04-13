---
title: Text 控制項類型
description: 本主題提供 Text 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- 消費者介面自動化，文字控制項類型的支援
- 消費者介面自動化，文字控制項類型
- 消費者介面自動化，Text 控制項類型的樹狀結構
- 消費者介面自動化，Text 控制項類型的屬性
- 消費者介面自動化，文字控制項類型的控制項模式
- 消費者介面自動化，Text 控制項類型的事件
- 樹狀結構，文字控制項類型
- 屬性，文字控制項類型
- 控制項模式，文字控制項類型
- events、Text 控制項類型
- Text 控制項類型的支援
- Text 控制項類型
- 控制項類型，文字控制項類型的樹狀結構
- 控制項類型，文字控制項類型的控制項模式
- 控制項類型，支援文字
- 控制項類型，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301428"
---
# <a name="text-control-type"></a>Text 控制項類型

本主題提供 **Text** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

文字控制項是代表螢幕上某段文字的基本使用者介面專案。

下列章節會定義 **Text** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的樹狀目錄控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述文字控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>Text</li>
</ul></td>
<td><ul>
<li>Text (如果內容)</li>
</ul></td>
</tr>
</tbody>
</table>



 

控制項可以單獨用來當做標籤或當做表單上的靜態文字。 它也可以包含在下列其中一個專案的結構內：

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

文字控制項可能不會出現在消費者介面自動化樹狀結構的內容視圖中，因為文字通常是透過另一個控制項的 [ **名稱** ] 屬性來顯示。 例如，用來為下拉式方塊控制項加上標籤的文字，會透過控制項的 [ **名稱** ] 屬性來公開。 因為下拉式方塊控制項位於消費者介面自動化樹狀結構的內容視圖中，所以不需要有文字控制項。 如果有内嵌物件（例如超連結），則文字控制項在內容視圖中可能會有子系。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與文字控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | 相依    | 如果文字控制項包含未在另一個控制項的名稱屬性中公開的資訊，則為內容。                                                                                                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 文字控制項必須一律為控制項。                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | 文字控制項沒有靜態文字標籤。                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **文字** 控制項類型的當地語系化字串。 預設值為 "text" 代表 en-us 或英文 (美國) 。                                                                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 文字控制項的名稱可以是它所顯示的文字。 但是，如果控制項也支援 [文字](uiauto-implementingtextandtextrange.md) 模式，且文字很廣泛，請不要使用全文檢索內容作為 **名稱** 值。 請改為提供較短的 **名稱** 值，其衍生自您的控制項的其他屬性。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出文字控制項必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援 | 注意                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | 相依 | 如果文字控制項包含在資料表控制項中，則必須支援 [GridItem](uiauto-implementinggriditem.md) 控制項模式。                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | 相依 | 如果文字控制項包含在資料表控制項中，則必須支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式。                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | 相依 | 文字應該支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，以提供更好的協助工具;不過，這不是必要的。 當文字有豐富的樣式和屬性 (例如色彩、粗體和斜體) 時，這種文字控制項模式相當有用。 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | 永不   | 文字控制項永遠不支援 [值](uiauto-implementingvalue.md) 控制項模式。 如果文字是可編輯的，則為 [編輯](uiauto-supporteditcontroltype.md) 控制項類型。                                                                                    |



 

## <a name="required-events"></a>必要的事件

下表列出文字控制項必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)                                                 | 如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




