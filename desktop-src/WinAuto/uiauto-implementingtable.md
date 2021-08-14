---
title: Table 控制項模式
description: 描述執行 ITableProvider 的方針和慣例，包括屬性和方法的相關資訊。 Table 控制項模式用來支援作為子專案集合之容器的控制項。
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- 消費者介面自動化，執行 Table 控制項模式
- 消費者介面自動化，Table 控制項模式
- 消費者介面自動化、ITableProvider
- ITableProvider
- 執行消費者介面自動化 Table 控制項模式
- Table 控制項模式
- 控制項模式，ITableProvider
- 控制模式，執行消費者介面自動化資料表
- 控制項模式，資料表
- 介面，ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb484245ee7c2f982ca6c5624ad108a0c75a4721ba7f6cbdf7a8af8ee2d91881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324127"
---
# <a name="table-control-pattern"></a>Table 控制項模式

描述執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)的方針和慣例，包括屬性和方法的相關資訊。 **Table** 控制項模式用來支援作為子專案集合之容器的控制項。

容器元素的子系必須執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) ，並且在可依資料列和資料行進行往返的二維邏輯座標系統中進行組織。 此控制項模式類似于 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ，因為任何控制項執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) 也都必須為每個子項目公開一個資料行和/或資料列標頭關聯性。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ITableProvider** 的必要成員](#required-members-for-itableprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **Table** 控制項模式時，請注意下列方針和慣例：

-   存取個別資料格的內容是透過二維邏輯座標系統或 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)所需的並存執行所提供的陣列。
-   資料行或資料列標頭可以包含在資料表物件中，也可以是與資料表物件建立關係的個別標頭物件。
-   資料行和資料列標頭可同時包含主要標頭和任何支援的標頭。
    > [!Note]  
    > 在使用者定義了 **First name** 資料行的 Microsoft Excel 試算表中，此概念會變得很明顯。 此資料行現在有兩個標頭，包括使用者所定義的 **名字** 標頭，以及該應用程式所指派之資料行的英數位元。

     

-   請參閱 [方格控制項模式](uiauto-implementinggrid.md) 以取得相關格線功能。

    下圖顯示具有複雜資料行標頭的資料表。

    ![具有複雜資料行標頭的資料表](images/uia-valuepattern-colorpicker.jpg)

    下圖顯示具有不明確 [**ITableProvider：：之 roworcolumnmajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) 屬性的資料表。

    ![具有不明確之 roworcolumnmajor 屬性的資料表](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>**ITableProvider** 的必要成員

執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) 介面需要下列屬性和方法。



| 必要成員                                                   | 成員類型 | 附註 |
|--------------------------------------------------------------------|-------------|-------|
| [**之 roworcolumnmajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | 屬性    | 無  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | 方法      | 無  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[TableItem 控制項模式](uiauto-implementingtableitem.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




