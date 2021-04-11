---
title: 方格控制項模式
description: 描述執行 IGridProvider 的方針和慣例，包括屬性和方法的相關資訊。 方格控制項模式用來支援作為子專案集合之容器的控制項。
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- 消費者介面自動化，執行方格控制項模式
- 消費者介面自動化，方格控制項模式
- 消費者介面自動化、IGridProvider
- IGridProvider
- 執行消費者介面自動化方格控制項模式
- 方格控制項模式
- 控制項模式，IGridProvider
- 控制項模式，執行消費者介面自動化方格
- 控制項模式，方格
- 介面，IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021211"
---
# <a name="grid-control-pattern"></a>方格控制項模式

描述執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)的方針和慣例，包括屬性和方法的相關資訊。 **方格** 控制項模式用來支援作為子專案集合之容器的控制項。

這個專案的子系必須執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) ，並且在可依資料列和資料行進行往返的二維邏輯座標系統中進行組織。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IGridProvider** 的必要成員](#required-members-for-igridprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **方格** 控制項模式時，請注意下列方針和慣例：

-   格線座標是以零為基礎，具有左上角 (或右上角儲存格，視地區設定) 具有座標 (0，0) 。
-   如果資料格是空的，則仍然必須傳回 Microsoft 消費者介面自動化元素，才能支援該資料格的 [**IGridItemProvider：： ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) 屬性。 當子項目在方格中的配置類似不完全陣列 (請參閱以下範例)，就可能發生這種情形。

    ![具有空白座標的方格控制項範例](images/grid.png)

-   如果以邏輯方式將 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 視為格線，則仍需要具有單一專案的方格才能執行。 方格中的子項目數為多少都沒關係。
-   隱藏的資料列和資料行（視提供者的執行而定）可能會載入消費者介面自動化樹狀結構中，因此會反映在 [**IGridProvider：： RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) 和 [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) 屬性中。 如果隱藏資料列和資料行未載入，則應不會列入計數。
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 不會啟用方格的主動式操作;必須實行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 才能啟用此功能。
-   使用 [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) 來接聽方格的結構化或版面配置變更，例如已新增、移除或合併的儲存格。
-   您可以使用 [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) ，透過方格的專案或資料格追蹤遍歷。

## <a name="required-members-for-igridprovider"></a>**IGridProvider** 的必要成員

執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 介面需要下列屬性和方法。



| 必要成員                                        | 成員類型 | 備註 |
|---------------------------------------------------------|-------------|-------|
| [**計數**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | 屬性    | 無  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | 屬性    | 無  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[GridItem 控制項模式](uiauto-implementinggriditem.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 




