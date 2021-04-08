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
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672384"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="bdf65-114">TableItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="bdf65-114">TableItem Control Pattern</span></span>

<span data-ttu-id="bdf65-115">描述執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bdf65-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="bdf65-116">**TableItem** 控制項模式用來支援執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)之容器的子控制項。</span><span class="sxs-lookup"><span data-stu-id="bdf65-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="bdf65-117">個別資料格功能的存取是由 [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)的必要並存執行所提供。</span><span class="sxs-lookup"><span data-stu-id="bdf65-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="bdf65-118">此控制項模式類似于 **IGridItemProvider** ，因為任何控制項執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) 都必須以程式設計方式公開個別資料格與其資料列和資料行資訊之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="bdf65-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="bdf65-119">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="bdf65-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="bdf65-120">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="bdf65-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bdf65-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="bdf65-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="bdf65-122">**ITableItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="bdf65-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="bdf65-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdf65-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="bdf65-124">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="bdf65-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="bdf65-125">在執行 **TableItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="bdf65-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="bdf65-126">如需相關的格線專案功能，請參閱 [GridItem 控制項模式](uiauto-implementinggriditem.md)。</span><span class="sxs-lookup"><span data-stu-id="bdf65-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="bdf65-127">**ITableItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="bdf65-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="bdf65-128">以下是執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="bdf65-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="bdf65-129">必要成員</span><span class="sxs-lookup"><span data-stu-id="bdf65-129">Required members</span></span>                                                               | <span data-ttu-id="bdf65-130">成員類型</span><span class="sxs-lookup"><span data-stu-id="bdf65-130">Member type</span></span> | <span data-ttu-id="bdf65-131">備註</span><span class="sxs-lookup"><span data-stu-id="bdf65-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="bdf65-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="bdf65-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="bdf65-133">方法</span><span class="sxs-lookup"><span data-stu-id="bdf65-133">Method</span></span>      | <span data-ttu-id="bdf65-134">無</span><span class="sxs-lookup"><span data-stu-id="bdf65-134">None</span></span>  |
| [<span data-ttu-id="bdf65-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="bdf65-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="bdf65-136">方法</span><span class="sxs-lookup"><span data-stu-id="bdf65-136">Method</span></span>      | <span data-ttu-id="bdf65-137">無</span><span class="sxs-lookup"><span data-stu-id="bdf65-137">None</span></span>  |



 

<span data-ttu-id="bdf65-138">此控制項模式沒有任何相關聯的屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="bdf65-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdf65-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdf65-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bdf65-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="bdf65-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bdf65-141">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="bdf65-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="bdf65-142">Table 控制項模式</span><span class="sxs-lookup"><span data-stu-id="bdf65-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="bdf65-143">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="bdf65-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="bdf65-144">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="bdf65-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




