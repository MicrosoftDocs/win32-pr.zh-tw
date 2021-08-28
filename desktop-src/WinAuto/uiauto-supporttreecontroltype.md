---
title: 樹狀目錄控制項類型
description: 本主題提供樹狀結構控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- 消費者介面自動化，支援樹狀目錄控制項類型
- 消費者介面自動化，樹狀目錄控制項類型
- 消費者介面自動化，樹狀結構控制項類型的樹狀結構
- 消費者介面自動化，樹狀目錄控制項類型的屬性
- 消費者介面自動化，樹狀結構控制項類型的控制項模式
- 消費者介面自動化，樹狀目錄控制項類型的事件
- 樹狀結構，樹狀目錄控制項類型
- 屬性，樹狀目錄控制項類型
- 控制項模式，樹狀目錄控制項類型
- 事件，樹狀目錄控制項類型
- 樹狀目錄控制項類型的支援
- Tree 控制項類型
- 控制項類型，樹狀結構控制項類型的樹狀結構
- 控制項類型，樹狀結構控制項類型的控制項模式
- 控制項類型，支援樹狀結構
- 控制項類型，樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7ac6330428c2e79fca1e9a51d4ca0f7c63e8a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472844"
---
# <a name="tree-control-type"></a>樹狀目錄控制項類型

本主題提供 **樹狀結構** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。

**樹狀** 結構控制項類型用於其內容與節點階層具有相關性的容器，如同在 Windows 檔案總管的左窗格中顯示檔案和資料夾的方式。 每個節點都可能包含其他節點，稱為子節點。 父節點或包含子節點的節點可以顯示為展開或摺疊。 [**WC \_ TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)) 所識別的 Windows 樹狀檢視控制項 (是屬於 **樹狀結構** 控制項類型的控制項範例。

下列章節會定義 **樹狀** 結構控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。 消費者介面自動化需求適用于所有樹狀結構專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。

本主題包含下列各節。

-   [一般樹狀結構](#typical-tree-structure)
-   [相關屬性](#relevant-properties)
-   [必要的控制項模式](#required-control-patterns)
-   [必要的事件](#required-events)
-   [相關主題](#related-topics)

## <a name="typical-tree-structure"></a>一般樹狀結構

下表描述樹狀結構控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。 如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。




| 控制項檢視 | 內容檢視 | 
|--------------|--------------|
| <ul><li>樹狀結構<ul><li>DataItem (0 個以上)</li><li>TreeItem (0 個以上)<ul><li>TreeItem (0 個以上)<ul><li>...</li></ul></li></ul></li><li>捲軸 (0、1、2 個)</li></ul></li></ul> | <ul><li>樹狀結構<ul><li>DataItem (0 個以上)</li><li>TreeItem (0 個以上)<ul><li>TreeItem (0 個以上)<ul><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

消費者介面自動化樹狀結構的控制視圖包含：

-   容器內的許多專案中有零個 (專案可以根據) 的 [TreeItem](uiauto-supporttreeitemcontroltype.md) 或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。
-   0、1 或 2 個捲軸控制項

消費者介面自動化樹狀結構的內容視圖是由容器內的零或多個專案所組成 (專案可以) 的 [TreeItem](uiauto-supporttreeitemcontroltype.md) 或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型為基礎。

## <a name="relevant-properties"></a>相關屬性

下表列出消費者介面自動化屬性，其值或定義與 **樹狀結構** 控制項類型特別有關。 如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。



| 使用者介面自動化屬性                                                                                              | 值      | 注意                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | 請參閱備註。 | 這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | 請參閱備註。 | 包含整個控制項的最外層矩形。                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | 請參閱備註。 | 樹狀目錄控制項具有可點按的點，讓樹狀結構或樹狀結構中的其中一個專案接收焦點。 只有當您可以按一下樹狀結構中的位置，而不會造成選取專案或接收焦點時，樹狀目錄控制項才可以有可按一下的點。 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **樹狀結構**   | 此值與所有使用者介面架構的值相同。                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 樹狀目錄控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | 樹狀目錄控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | 請參閱備註。 | 如果控制項可接收鍵盤焦點，就必定支援此屬性。                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | 請參閱備註。 | 如果樹狀目錄控制項有與其相關聯的標籤，則此屬性會傳回該標籤的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 指標。 否則，屬性會傳回 null 參考。                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | 請參閱備註。 | 對應至 **樹狀結構** 控制項類型的當地語系化字串。 預設值為 "tree" （適用于 en-us）或英文 (美國) 。                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | 請參閱備註。 | 樹狀結構控制項的名稱屬性值通常取自於控制項的標籤文字。 如果沒有文字標籤，您必須提供這個屬性的值。                                                                                                                        |



 

## <a name="required-control-patterns"></a>必要的控制項模式

下表列出所有樹狀結構控制項都必須支援的消費者介面自動化控制項模式。 如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。



| 控制項模式/模式屬性                                             | 支援/值 | 備註                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | 相依       | 如果樹狀結構容器中的專案可以滾動，請執行 [滾動](uiauto-implementingscroll.md) 條控制項模式。                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | 相依       | 包含一組可選取專案的樹狀目錄控制項必須執行 [選取](uiauto-implementingselection.md) 控制項模式。 如果選取專案不會對使用者傳達有意義的資訊，則不需要執行此專案。 |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | 請參閱備註。    | 如果樹狀結構控制項支援多重選取 (大多數樹狀結構控制項並不支援多重選取)，即實作此屬性。                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | 請參閱備註。    | 如果控制項需要選取項目，則會公開此屬性的值。                                                                                                                                               |



 

## <a name="required-events"></a>必要的事件

下表列出所有樹狀結構控制項都必須支援的消費者介面自動化事件。 如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱



| 消費者介面自動化事件                                                                                                                                        | 備註                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                      |                                                                                                                            |
| [**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                      | 如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。   |
| [**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。                                  | 如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。 |
| [**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。   | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。 | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。           | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。     | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。       | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。               | 如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。           |
| [**UIA \_ 選取專案 \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | 如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化概觀](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 
