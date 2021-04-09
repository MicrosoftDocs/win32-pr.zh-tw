---
title: Menu 控制項類型
description: 本主題提供功能表控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- 消費者介面自動化，支援 Menu 控制項類型
- 消費者介面自動化，功能表控制項類型
- 消費者介面自動化，功能表控制項類型的樹狀結構
- 消費者介面自動化，功能表控制項類型的屬性
- 消費者介面自動化，功能表控制項類型的控制項模式
- 消費者介面自動化，Menu 控制項類型的事件
- 樹狀結構，功能表控制項類型
- 屬性，功能表控制項類型
- 控制項模式，功能表控制項類型
- 事件、功能表控制項類型
- Menu 控制項類型的支援
- 功能表控制項類型
- Menu 控制項類型的控制項類型、樹狀結構
- 控制項類型、功能表控制項類型的控制項模式
- 控制項類型，支援功能表
- 控制項類型，功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021340"
---
# <a name="menu-control-type"></a>Menu 控制項類型

本主題提供 **功能表** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。

功能表控制項可將命令和事件處理常式的關聯項目以階層方式組織。 在一般的 Microsoft Windows 應用程式中，功能表列會包含數個功能表按鈕 **(例如 [** 檔案]、[ **編輯**] 和 [ **視窗]**) ，而且每個功能表按鈕都會顯示功能表。 功能表又包含一組功能表項目 (例如 [開新檔案] **F:System.Windows.Automation.AutomationElementIdentifiers.IsEnabledProperty**、[開啟舊檔] **UI Automation Properties Overview** 和 [關閉檔案] **TLA#tla_win32**)，這些項目可展開顯示更多的功能表項目，或在按一下時可執行特定的動作。

下列章節會定義 **功能表** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有的功能表控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述功能表控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。



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
<li>功能表
<ul>
<li>MenuItem (1 或多個)</li>
</ul>
<ul>
<li>其他控制項 (0 個以上)</li>
</ul></li>
</ul></td>
<td><ul>
<li>功能表
<ul>
<li>MenuItem (1 或多個)</li>
</ul>
<ul>
<li>其他控制項 (0 個以上)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

功能表控制項一律會出現在 [控制台] 和 [消費者介面自動化] 樹狀結構的內容視圖中。 功能表控制項應該會出現在其資訊所參考的控制項底下。 消費者介面自動化用戶端可以接聽 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) ，以確保它們持續取得功能表控制項所傳達的資訊。 內容功能表控制項是特殊案例。 它們可能會顯示為桌面的子系或最上層應用程式視窗的子系。

Menu 控制項可以在其結構內包含其他控制項，例如編輯控制項和下拉式方塊。 這些額外的控制項會對應到控制項和內容視圖中上表所列的「其他控制項」。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **功能表** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                      | 值      | 注意                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **功能表**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | true       | 功能表控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | true       | 功能表控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | 典型的功能表控制項不預期有標籤。                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | Menu 控制項不需要設定 **name** 屬性，也可以與相關聯的控制項（例如開啟子功能表的功能表項目）有相同的名稱。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

功能表控制項類型沒有必要的控制項模式。

## <a name="required-events"></a>必要的事件

當功能表控制項出現在螢幕上時，必須引發 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) 事件。 **UIA \_ MenuOpenedEventId** 事件將包含控制項的文字。 當功能表從畫面上消失時，必須引發 [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) 事件。

下表列出支援的功能表控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                   | 備註                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。 |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                 | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。             | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




