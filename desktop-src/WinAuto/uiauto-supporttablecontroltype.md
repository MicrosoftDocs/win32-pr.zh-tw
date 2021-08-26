---
title: Table 控制項類型
description: 本主題提供 Microsoft 消費者介面自動化 Table 控制項類型支援的相關資訊。
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- 消費者介面自動化，支援 Table 控制項類型
- 消費者介面自動化，Table 控制項類型
- 消費者介面自動化，Table 控制項類型的樹狀結構
- 消費者介面自動化，Table 控制項類型的屬性
- 消費者介面自動化，資料表控制項類型的控制項模式
- 消費者介面自動化，Table 控制項類型的事件
- 樹狀結構，資料表控制項類型
- properties、Table 控制項類型
- 控制項模式，資料表控制項類型
- events、Table 控制項類型
- Table 控制項類型的支援
- Table 控制項類型
- 控制項類型，資料表控制項類型的樹狀結構
- 控制項類型，資料表控制項類型的控制項模式
- 控制項類型，支援資料表
- 控制項類型，資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470075"
---
# <a name="table-control-type"></a>Table 控制項類型

本主題提供 Microsoft 消費者介面自動化 **Table** 控制項類型支援的相關資訊。

資料表控制項包含文字的資料列和資料行，以及選擇性的資料列標頭和資料行標頭。

下列章節會定義 **資料表** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有資料表控制項，其中 UI 架構/平臺會將控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述與資料表控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>資料表<ul><li>文字 (0 或 1)</li><li>標頭 (0 或更多) </li><li>不同控制項 (0 或更多)</li></ul></li></ul> | <ul><li>資料表<ul><li>文字 (1 或更多) </li><li>不同控制項 (0 或更多)</li></ul></li></ul> | 




 

如果資料表控制項具有資料列或資料行標頭，就必須在消費者介面自動化樹狀結構的控制項視圖中公開這些標頭。 內容視圖不需要公開此資訊，因為它可以使用 [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)存取。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與資料表控制項特別相關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 如果有週框即受支援。 如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **資料表**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | 請參閱備註。 | 如果此資料表是由其他使用者介面項目 (例如保留資料表描述的文字項目) 所標註，則 DescribedBy 屬性應公開對文字控制項之自動化項目的參考。           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | 請參閱備註。 | 如需更多有關資料表用途的詳細資料，請透過此屬性公開（如果 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性未充分說明）。      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Table 控制項必須一律出現在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Table 控制項必須一律出現在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果有靜態文字標籤，則此屬性應公開對控制項之自動化項目的參考。                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **Table** 控制項類型的當地語系化字串。 預設值為 "table" 代表 en-us 或英文 (美國) 。                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | Table 控制項通常會從靜態文字標籤取得其名稱的值。 如果沒有靜態文字標籤，則專案必須指派名稱屬性，該屬性必須永遠可用來說明資料表的用途。 |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有資料表控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式                                         | 支援                     | 注意                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | 必要                    | 因為資料表控制項包含在方格中顯示的專案，所以它一律支援 [方格](uiauto-implementinggrid.md) 控制項模式。                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | 需要有子物件 | 資料表的內建物件應同時支援 [GridItem](uiauto-implementinggriditem.md) 和 [TableItem](uiauto-implementingtableitem.md) 控制項模式。 除非資料表是另一個資料表的一部分，否則資料表本身不需要支援 GridItem 或 TableItem 控制項模式。  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | 必要                    | Table 控制項一律可以有與內容相關聯的標頭。                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | 需要有子物件 | 資料表的內建物件應同時支援 [GridItem](uiauto-implementinggriditem.md) 和 [TableItem](uiauto-implementingtableitem.md) 控制項模式。 除非此資料表是另一個資料表的一部份，否則資料表本身不需要支援 GridItem 或 TableItem 控制項模式。 |



 

## <a name="required-events"></a>必要的事件

下表列出支援資料表控制項所需的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



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

 

 




