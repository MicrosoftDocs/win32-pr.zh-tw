---
title: MultipleView 控制項模式
description: 描述執行 IMultipleViewProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- 消費者介面自動化，執行 MultipleView 控制項模式
- 消費者介面自動化，MultipleView 控制項模式
- 消費者介面自動化、IMultipleViewProvider
- IMultipleViewProvider
- 執行消費者介面自動化 MultipleView 控制項模式
- MultipleView 控制項模式
- 控制項模式，IMultipleViewProvider
- 控制模式，消費者介面自動化執行 MultipleView
- 控制項模式，MultipleView
- 介面，IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372333"
---
# <a name="multipleview-control-pattern"></a>MultipleView 控制項模式

描述執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)的方針和慣例，包括屬性和方法的相關資訊。 其他參考的連結列於主題的結尾。 **MultipleView** 控制項模式用來支援控制項，這些控制項可讓您在相同資訊或同一組子控制項的多個標記法之間切換。

可顯示多個視圖的控制項範例包括清單視圖 (可以將其內容顯示為縮圖。磚、圖示或詳細資料) 、Microsoft Excel 圖表 (圓形圖、線條、橫條圖、具有公式) 的儲存格值、Microsoft Word 檔 (一般、web 版面配置、列印配置、閱讀版面配置、大綱) 、Microsoft Outlook 行事曆 (年、月、周、日) 和 Microsoft Windows Media Player 的外觀。 支援哪些檢視會由控制項的開發人員決定，而且是每個控制項所特有。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IMultipleViewProvider** 的必要成員](#required-members-for-imultipleviewprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **MultipleView** 控制項模式時，請注意下列方針和慣例：

-   如果容器與提供目前視圖的控制項不同，則也應該在管理目前視圖的容器上執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) 。 例如，Windows 檔案總管包含目前資料夾內容的清單控制項，而控制項的視圖是從 Windows 檔案總管應用程式進行管理。
-   可以排序內容的控制項不視為支援多種檢視。
-   檢視集合在執行個體之間必須完全相同。
-   視圖名稱必須適合用於文字轉換語音、盲文和其他人類可讀取的應用程式。

## <a name="required-members-for-imultipleviewprovider"></a>**IMultipleViewProvider** 的必要成員

執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) 介面需要下列屬性和方法。



| 必要成員                                                            | 成員類型 | 備註 |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | 屬性    | 無  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | 方法      | 無  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | 方法      | 無  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[ExpandCollapse 控制項模式](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




