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
# <a name="griditem-control-pattern"></a><span data-ttu-id="e087f-114">GridItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="e087f-114">GridItem Control Pattern</span></span>

<span data-ttu-id="e087f-115">描述執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)的方針和慣例，包括屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e087f-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="e087f-116">**GridItem** 控制項模式用來支援執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)之容器的個別子控制項。</span><span class="sxs-lookup"><span data-stu-id="e087f-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="e087f-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="e087f-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="e087f-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="e087f-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e087f-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e087f-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="e087f-120">**IGridItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e087f-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="e087f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e087f-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="e087f-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e087f-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="e087f-123">在執行 **GridItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="e087f-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="e087f-124">方格座標是以零起始，左上資料格座標為 (0, 0)。</span><span class="sxs-lookup"><span data-stu-id="e087f-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="e087f-125">合併的資料格會根據 Microsoft 消費者介面自動化提供者所定義的基礎錨定儲存格，報告其資料 [**列**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)和資料 [**行**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)屬性。</span><span class="sxs-lookup"><span data-stu-id="e087f-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="e087f-126">通常，它會是最上層或最左邊的資料列或資料行。</span><span class="sxs-lookup"><span data-stu-id="e087f-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="e087f-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 不提供方格的主動式操作，例如合併或分割儲存格。</span><span class="sxs-lookup"><span data-stu-id="e087f-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="e087f-128">執行 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) 的控制項通常可以 (，也就是消費者介面自動化用戶端可以使用鍵盤移至連續的控制項) 。</span><span class="sxs-lookup"><span data-stu-id="e087f-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="e087f-129">**IGridItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e087f-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="e087f-130">執行 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) 介面需要下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e087f-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="e087f-131">必要成員</span><span class="sxs-lookup"><span data-stu-id="e087f-131">Required members</span></span>                                                  | <span data-ttu-id="e087f-132">成員類型</span><span class="sxs-lookup"><span data-stu-id="e087f-132">Member type</span></span> | <span data-ttu-id="e087f-133">備註</span><span class="sxs-lookup"><span data-stu-id="e087f-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="e087f-134">**資料列**</span><span class="sxs-lookup"><span data-stu-id="e087f-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="e087f-135">屬性</span><span class="sxs-lookup"><span data-stu-id="e087f-135">Property</span></span>    | <span data-ttu-id="e087f-136">無</span><span class="sxs-lookup"><span data-stu-id="e087f-136">None</span></span>  |
| [<span data-ttu-id="e087f-137">**Column**</span><span class="sxs-lookup"><span data-stu-id="e087f-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="e087f-138">屬性</span><span class="sxs-lookup"><span data-stu-id="e087f-138">Property</span></span>    | <span data-ttu-id="e087f-139">無</span><span class="sxs-lookup"><span data-stu-id="e087f-139">None</span></span>  |
| [<span data-ttu-id="e087f-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="e087f-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="e087f-141">屬性</span><span class="sxs-lookup"><span data-stu-id="e087f-141">Property</span></span>    | <span data-ttu-id="e087f-142">無</span><span class="sxs-lookup"><span data-stu-id="e087f-142">None</span></span>  |
| [<span data-ttu-id="e087f-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="e087f-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="e087f-144">屬性</span><span class="sxs-lookup"><span data-stu-id="e087f-144">Property</span></span>    | <span data-ttu-id="e087f-145">無</span><span class="sxs-lookup"><span data-stu-id="e087f-145">None</span></span>  |
| [<span data-ttu-id="e087f-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="e087f-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="e087f-147">屬性</span><span class="sxs-lookup"><span data-stu-id="e087f-147">Property</span></span>    | <span data-ttu-id="e087f-148">無</span><span class="sxs-lookup"><span data-stu-id="e087f-148">None</span></span>  |



 

<span data-ttu-id="e087f-149">此控制項模式沒有任何相關聯的方法或事件。</span><span class="sxs-lookup"><span data-stu-id="e087f-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e087f-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="e087f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e087f-151">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="e087f-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="e087f-152">方格控制項模式</span><span class="sxs-lookup"><span data-stu-id="e087f-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="e087f-153">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="e087f-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="e087f-154">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="e087f-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




