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
# <a name="grid-control-pattern"></a><span data-ttu-id="ba4d8-114">方格控制項模式</span><span class="sxs-lookup"><span data-stu-id="ba4d8-114">Grid Control Pattern</span></span>

<span data-ttu-id="ba4d8-115">描述執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="ba4d8-116">**方格** 控制項模式用來支援作為子專案集合之容器的控制項。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="ba4d8-117">這個專案的子系必須執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) ，並且在可依資料列和資料行進行往返的二維邏輯座標系統中進行組織。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="ba4d8-118">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ba4d8-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ba4d8-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="ba4d8-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ba4d8-121">**IGridProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="ba4d8-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="ba4d8-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba4d8-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ba4d8-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="ba4d8-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ba4d8-124">在執行 **方格** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="ba4d8-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ba4d8-125">格線座標是以零為基礎，具有左上角 (或右上角儲存格，視地區設定) 具有座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="ba4d8-126">如果資料格是空的，則仍然必須傳回 Microsoft 消費者介面自動化元素，才能支援該資料格的 [**IGridItemProvider：： ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="ba4d8-127">當子項目在方格中的配置類似不完全陣列 (請參閱以下範例)，就可能發生這種情形。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![具有空白座標的方格控制項範例](images/grid.png)

-   <span data-ttu-id="ba4d8-129">如果以邏輯方式將 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 視為格線，則仍需要具有單一專案的方格才能執行。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="ba4d8-130">方格中的子項目數為多少都沒關係。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="ba4d8-131">隱藏的資料列和資料行（視提供者的執行而定）可能會載入消費者介面自動化樹狀結構中，因此會反映在 [**IGridProvider：： RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) 和 [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="ba4d8-132">如果隱藏資料列和資料行未載入，則應不會列入計數。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="ba4d8-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 不會啟用方格的主動式操作;必須實行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 才能啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="ba4d8-134">使用 [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) 來接聽方格的結構化或版面配置變更，例如已新增、移除或合併的儲存格。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="ba4d8-135">您可以使用 [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) ，透過方格的專案或資料格追蹤遍歷。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="ba4d8-136">**IGridProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="ba4d8-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="ba4d8-137">執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="ba4d8-138">必要成員</span><span class="sxs-lookup"><span data-stu-id="ba4d8-138">Required members</span></span>                                        | <span data-ttu-id="ba4d8-139">成員類型</span><span class="sxs-lookup"><span data-stu-id="ba4d8-139">Member type</span></span> | <span data-ttu-id="ba4d8-140">備註</span><span class="sxs-lookup"><span data-stu-id="ba4d8-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ba4d8-141">**計數**</span><span class="sxs-lookup"><span data-stu-id="ba4d8-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="ba4d8-142">屬性</span><span class="sxs-lookup"><span data-stu-id="ba4d8-142">Property</span></span>    | <span data-ttu-id="ba4d8-143">無</span><span class="sxs-lookup"><span data-stu-id="ba4d8-143">None</span></span>  |
| [<span data-ttu-id="ba4d8-144">**ColumnCount**</span><span class="sxs-lookup"><span data-stu-id="ba4d8-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="ba4d8-145">屬性</span><span class="sxs-lookup"><span data-stu-id="ba4d8-145">Property</span></span>    | <span data-ttu-id="ba4d8-146">無</span><span class="sxs-lookup"><span data-stu-id="ba4d8-146">None</span></span>  |
| [<span data-ttu-id="ba4d8-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="ba4d8-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="ba4d8-148">方法</span><span class="sxs-lookup"><span data-stu-id="ba4d8-148">Method</span></span>      | <span data-ttu-id="ba4d8-149">無</span><span class="sxs-lookup"><span data-stu-id="ba4d8-149">None</span></span>  |



 

<span data-ttu-id="ba4d8-150">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="ba4d8-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba4d8-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba4d8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba4d8-152">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ba4d8-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ba4d8-153">GridItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="ba4d8-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="ba4d8-154">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="ba4d8-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ba4d8-155">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="ba4d8-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




