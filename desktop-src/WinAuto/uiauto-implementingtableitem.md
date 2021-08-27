---
title: TableItem 控制項模式
description: 描述執行 ITableItemProvider 的方針和慣例，包括方法的相關資訊。 TableItem 控制項模式用來支援執行 ITableProvider 之容器的子控制項。
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- 消費者介面自動化，執行 TableItem 控制項模式
- 消費者介面自動化，TableItem 控制項模式
- 消費者介面自動化、ITableItemProvider
- ITableItemProvider
- 執行消費者介面自動化 TableItem 控制項模式
- TableItem 控制項模式
- 控制項模式，ITableItemProvider
- 控制模式，消費者介面自動化執行 TableItem
- 控制項模式，TableItem
- 介面，ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098268"
---
# <a name="tableitem-control-pattern"></a>TableItem 控制項模式

描述執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)的方針和慣例，包括方法的相關資訊。 **TableItem** 控制項模式用來支援執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)之容器的子控制項。

個別資料格功能的存取是由 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)的必要並存執行所提供。 此控制項模式類似于 **IGridItemProvider** ，因為任何控制項執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) 都必須以程式設計方式公開個別資料格與其資料列和資料行資訊之間的關聯性。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ITableItemProvider** 的必要成員](#required-members-for-itableitemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **TableItem** 控制項模式時，請注意下列方針和慣例：

-   如需相關的格線專案功能，請參閱 [GridItem 控制項模式](uiauto-implementinggriditem.md)。

## <a name="required-members-for-itableitemprovider"></a>**ITableItemProvider** 的必要成員

以下是執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) 介面的必要方法。



| 必要成員                                                               | 成員類型 | 備註 |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | 方法      | 無  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | 方法      | 無  |



 

此控制項模式沒有任何相關聯的屬性或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[Table 控制項模式](uiauto-implementingtable.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




