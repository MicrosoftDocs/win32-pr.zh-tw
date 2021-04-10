---
title: UI 自動化控制項模式概觀
description: 控制項模式是介面執行，可將控制項功能的特定層面公開給 Microsoft 消費者介面自動化用戶端應用程式。
ms.assetid: fdac2b9f-916a-495a-b187-c4d8086319ff
keywords:
- 消費者介面自動化，控制項模式總覽
- 消費者介面自動化，動態控制項模式
- 控制項模式，關於
- 控制項模式，元件
- 控制項模式，用戶端
- 控制項模式、提供者
- 控制項模式，動態
- 控制項模式，介面
- 介面、控制項模式
- 用戶端、控制項模式
- 動態控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51abcfd316f5ab892155cf248d5473bd4e387227
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092848"
---
# <a name="ui-automation-control-patterns-overview"></a>UI 自動化控制項模式概觀

*控制項模式* 是介面執行，可將控制項功能的特定層面公開給 Microsoft 消費者介面自動化用戶端應用程式。 用戶端會使用透過控制項模式所公開的屬性和方法，以抓取控制項特定功能的相關資訊，或操作控制項行為的特定層面。 例如，呈現表格式介面的控制項會使用 [方格](uiauto-implementinggrid.md) 控制項模式來公開資料表中的資料列和資料行數目，以及讓用戶端從資料表中取出專案。

消費者介面自動化使用控制項模式來表示常見的控制項行為。 例如，您可以針對可以叫用的控制項（例如按鈕），以及具有捲軸的控制項（例如清單方塊、清單視圖或下拉式方塊）的[滾動](uiauto-implementingscroll.md)控制項模式，使用[Invoke](uiauto-implementinginvoke.md)控制項模式。 由於每個控制項模式都代表不同的功能，因此可以結合控制項模式來描述特定控制項所支援的完整功能集。

> [!Note]  
> 您可以使用子控制項來建立匯總控制項，以提供父項所公開之功能的使用者介面，而父系應該執行通常與其子控制項相關聯的所有控制項模式。 然後相同的控制項模式便不需要由子控制項所實作。

 

本主題包含下列幾節：

-   [使用者介面自動化控制項模式元件](#ui-automation-control-pattern-components)
-   [提供者和用戶端中的控制項模式](#control-patterns-in-providers-and-clients)
-   [動態控制項模式](#dynamic-control-patterns)
-   [控制項模式和相關介面](#control-patterns-and-related-interfaces)
-   [相關主題](#related-topics)

## <a name="ui-automation-control-pattern-components"></a>使用者介面自動化控制項模式元件

控制項模式支援方法、屬性、事件和關聯性，這是定義控制項中可用之離散功能所需的關聯性。

-   這些方法可以讓使用者介面自動化用戶端操作此控制項。
-   屬性和事件提供控制項功能和狀態的相關資訊。
-   消費者介面自動化專案與其父系、子系和同級之間的關聯性描述消費者介面自動化樹狀目錄中的元素結構。

控制項模式與控制項相關聯的控制項，類似于介面與元件物件模型 (COM) 物件的關聯方式。 在 COM 中，您可以查詢物件來詢問它所支援的介面，然後使用這些介面來存取功能。 在消費者介面自動化中，用戶端可以詢問控制項支援何種控制項模式，然後透過支援的控制項模式所公開的屬性、方法、事件和結構，與控制項互動。

## <a name="control-patterns-in-providers-and-clients"></a>提供者和用戶端中的控制項模式

消費者介面自動化提供者會執行控制項模式介面，以公開控制項所支援之特定功能的適當行為。 這些介面不會直接公開給用戶端，但消費者介面自動化核心會用來執行另一組用戶端介面。 例如，提供者會透過 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)公開滾動功能來消費者介面自動化，並消費者介面自動化透過 [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern)將功能公開給用戶端。

## <a name="dynamic-control-patterns"></a>動態控制項模式

有些控制項不一定支援一組相同的控制項模式。 例如，多行編輯控制項只會在其包含的文字行數超過可顯示在其可見區域中的行時，才會啟用垂直捲動。 移除足夠的文字，因而不再需要捲動之後，捲動便會停用。 在此範例中，會根據編輯方塊中的文字數量，以動態方式支援 [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) 。

## <a name="control-patterns-and-related-interfaces"></a>控制項模式和相關介面

下表描述消費者介面自動化控制項模式。 此表格也會列出用來執行控制項模式的提供者介面，以及用來存取它們的用戶端介面。



| Name                                                          | 提供者介面                                                      | 用戶端介面                                                                              | Description                                                                                                                                                                                                                     |
|---------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [註釋](uiauto-implementingannotation.md)               | [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)           | [**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern)           | 用來公開檔中注釋的屬性，例如，連接到檔文字之邊界中的批註。                                                                                           |
| [Dock](uiauto-implementingdock.md)                           | [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                           | [**IUIAutomationDockPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdockpattern)                           | 用於可停駐在停駐容器中的控制項，例如工具列或工具調色板。                                                                                                                            |
| [拖曳](/windows/desktop/WinAuto/uiauto-implementingdrag)                       | [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider)                           | [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern)                           | 用於支援可拖曳的控制項，或者含有可拖曳項目的控制項。                                                                                                                                                           |
| [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget)           | [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider)               | [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)               | 用於支援可成為拖放作業目標的控制項。                                                                                                                                                   |
| [ExpandCollapse](uiauto-implementingexpandcollapse.md)       | [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)       | [**IUIAutomationExpandCollapsePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationexpandcollapsepattern)       | 用於可展開或折迭的控制項（例如，應用程式中的功能表項目，例如 [檔案] 功能表）。                                                                                                          |
| [方格](uiauto-implementinggrid.md)                           | [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                           | [**IUIAutomationGridPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationgridpattern)                           | 用於支援格線功能的控制項，例如調整大小和移至指定的儲存格，例如 Windows 檔案總管中的大型圖示視圖，或 Microsoft Office Word 中的簡單資料表。                               |
| [GridItem](uiauto-implementinggriditem.md)                   | [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)                   | [**IUIAutomationGridItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationgriditempattern)                   | 用於方格中有儲存格的控制項。 個別資料格應支援 GridItem 模式，例如 Windows 檔案總管詳細資料檢視中的每個資料格。                                                                   |
| [調用](uiauto-implementinginvoke.md)                       | [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                       | [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)                       | 用於可叫用的控制項，例如按鈕。                                                                                                                                                                         |
| [ItemContainer](uiauto-implementingitemcontainer.md)         | [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)         | [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern)         | 用於可包含其他專案的控制項。                                                                                                                                                                                 |
| [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) | [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) | [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) | 用來公開 Microsoft Active Accessibility 屬性和方法，以消費者介面自動化用戶端。                                                                                                                                  |
| [MultipleView](uiauto-implementingmultipleview.md)           | [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)           | [**IUIAutomationMultipleViewPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationmultipleviewpattern)           | 用於可在同一組資訊、資料或子系的多個標記法之間切換的控制項，例如，可在縮圖、磚、圖示、清單或詳細資料檢視中使用資料的清單視圖控制項。 |
| [ObjectModel](uiauto-implementingobjectmodel.md)             | [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)         | [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern)             | 用於公開對於文件基本物件模型的指標。 此控制項模式可讓用戶端從消費者介面自動化元素流覽至基礎物件模型。                                          |
| [RangeValue](uiauto-implementingrangevalue.md)               | [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)               | [**IUIAutomationRangeValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationrangevaluepattern)               | 用於具有值範圍的控制項。 例如，顯示年份的微調控制項的範圍可能是 1900-2010，而顯示月份的微調控制項的範圍則是 1-12。                     |
| [捲動](uiauto-implementingscroll.md)                       | [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                       | [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern)                       | 用於可在有更多資訊時滾動的控制項，而不能在控制項的可見區域中顯示。                                                                                                     |
| [ScrollItem](uiauto-implementingscrollitem.md)               | [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)               | [**IUIAutomationScrollItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollitempattern)               | 用於在清單中具有個別專案的控制項，例如，下拉式方塊控制項中的清單控制項。                                                                                                        |
| [選取範圍](uiauto-implementingselection.md)                 | [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                 | [**IUIAutomationSelectionPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionpattern)                 | 用於選取容器控制項，例如清單方塊和下拉式方塊。                                                                                                                                                 |
| [SelectionItem](uiauto-implementingselectionitem.md)         | [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)         | [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern)         | 用於選取容器控制項 (例如清單方塊及下拉式方塊) 中的個別項目。                                                                                                                                  |
| [試算表](uiauto-implementingspreadsheet.md)             | [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)         | [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern)         | 用於公開試算表或其他以格線為基礎的文件的內容。 執行試算表控制項模式的控制項也應該執行方格控制項模式。                                              |
| [SpreadsheetItem](uiauto-implementingspreadsheetitem.md)     | [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) | [**IUIAutomationSpreadsheetItemPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) | 用於公開試算表或其他以格線為基礎的文件中儲存格的屬性。 實 SpreadsheetItem 控制項模式的控制項也應執行 GridItem 控制項模式。                          |
| [樣式](/windows/desktop/WinAuto/uiauto-implementingstyles)                   | [**IStylesProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-istylesprovider)                   | [**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern)                   | 用於說明含有特定樣式、填滿色彩、填滿圖樣或形狀的 UI 元素。                                                                                                                                    |
| [SynchronizedInput](uiauto-implementingsynchronizedinput.md) | [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) | [**IUIAutomationSynchronizedInputPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationsynchronizedinputpattern) | 用於接受鍵盤或滑鼠輸入的控制項。                                                                                                                                                                          |
| [資料表](uiauto-implementingtable.md)                         | [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                         | [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)                         | 用於具有方格和標頭資訊的控制項。                                                                                                                                                                      |
| [TableItem](uiauto-implementingtableitem.md)                 | [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)                 | [**IUIAutomationTableItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtableitempattern)                 | 用於表格中的項目。                                                                                                                                                                                                      |
| [Text](uiauto-implementingtextandtextrange.md)               | [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                           | [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern)                           | 用於公開文字資訊的編輯控制項及文件。                                                                                                                                                           |
| TextEdit                                                      | [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)               | [**IUIAutomationTextEditPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtexteditpattern)                   | 用於以程式設計方式修改文字的編輯控制項，例如執行自動校正或啟用輸入組合的控制項。                                                                                     |
| [TextChild](textchild-control-pattern.md)                    | [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)            | [**IUIAutomationTextChildPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextchildpattern)             | 用於存取最接近元素且支援 Text 控制項模式的上階。                                                                                                                                            |
| [TextRange](uiauto-implementingtextandtextrange.md)          | [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)                 | [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)                               | 用於從以文字為基礎的控制項（例如編輯控制項和檔）抓取文字內容、文字屬性和内嵌物件。                                                                                        |
| [切換](uiauto-implementingtoggle.md)                       | [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                       | [**IUIAutomationTogglePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtogglepattern)                       | 用於可以切換狀態的控制項，例如核取方塊和 checkable 功能表項目。                                                                                                                            |
| [轉換](uiauto-implementingtransform.md)                 | [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)                 | [**IUIAutomationTransformPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtransformpattern)                 | 用於可以調整大小、移動和旋轉的控制項。 轉換控制項模式通常使用於設計工具、表單、圖形編輯器，以及繪圖應用程式。                                                 |
| [值](uiauto-implementingvalue.md)                         | [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                         | [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern)                         | 用於其值不在指定範圍內的控制項（例如，日期時間選擇器）。                                                                                                                |
| [VirtualizedItem](uiauto-implementingvirtualizeditem.md)     | [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)     | [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)     | 用於使用虛擬清單中專案的控制項。                                                                                                                                                                       |
| [Window](uiauto-implementingwindow.md)                       | [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)                       | [**IUIAutomationWindowPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationwindowpattern)                       | 用於 windows。 範例包括最上層的應用程式視窗、多重文件介面 (MDI) 子視窗和對話方塊。                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行消費者介面自動化控制項模式](uiauto-implementinguiautocontrolpatterns.md)
</dt> <dt>

[UI 自動化用戶端的控制項模式對應](uiauto-controlpatternmapping.md)
</dt> </dl>

 

 