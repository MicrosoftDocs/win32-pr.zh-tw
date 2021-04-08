---
title: GridItem 控制項模式
description: 描述執行 IGridItemProvider 的方針和慣例，包括屬性的相關資訊。 GridItem 控制項模式用來支援執行 IGridProvider 之容器的個別子控制項。
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- 消費者介面自動化，執行 GridItem 控制項模式
- 消費者介面自動化，GridItem 控制項模式
- 消費者介面自動化、IGridItemProvider
- IGridItemProvider
- 執行消費者介面自動化 GridItem 控制項模式
- GridItem 控制項模式
- 控制項模式，IGridItemProvider
- 控制模式，消費者介面自動化執行 GridItem
- 控制項模式，GridItem
- 介面，IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672663"
---
# <a name="griditem-control-pattern"></a>GridItem 控制項模式

描述執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)的方針和慣例，包括屬性的相關資訊。 **GridItem** 控制項模式用來支援執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)之容器的個別子控制項。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IGridItemProvider** 的必要成員](#required-members-for-igriditemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **GridItem** 控制項模式時，請注意下列方針和慣例：

-   方格座標是以零起始，左上資料格座標為 (0, 0)。
-   合併的資料格會根據 Microsoft 消費者介面自動化提供者所定義的基礎錨定儲存格，報告其資料 [**列**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)和資料 [**行**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)屬性。 通常，它會是最上層或最左邊的資料列或資料行。
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 不提供方格的主動式操作，例如合併或分割儲存格。
-   執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 的控制項通常可以 (，也就是消費者介面自動化用戶端可以使用鍵盤移至連續的控制項) 。

## <a name="required-members-for-igriditemprovider"></a>**IGridItemProvider** 的必要成員

執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) 介面需要下列屬性。



| 必要成員                                                  | 成員類型 | 備註 |
|-------------------------------------------------------------------|-------------|-------|
| [**資料列**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | 屬性    | 無  |
| [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | 屬性    | 無  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | 屬性    | 無  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | 屬性    | 無  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | 屬性    | 無  |



 

此控制項模式沒有任何相關聯的方法或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[方格控制項模式](uiauto-implementinggrid.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




