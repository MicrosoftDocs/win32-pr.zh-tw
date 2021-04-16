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
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104550397"
---
# <a name="table-control-pattern"></a><span data-ttu-id="68a75-114">Table 控制項模式</span><span class="sxs-lookup"><span data-stu-id="68a75-114">Table Control Pattern</span></span>

<span data-ttu-id="68a75-115">描述執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68a75-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="68a75-116">**Table** 控制項模式用來支援作為子專案集合之容器的控制項。</span><span class="sxs-lookup"><span data-stu-id="68a75-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="68a75-117">容器元素的子系必須執行 [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) ，並且在可依資料列和資料行進行往返的二維邏輯座標系統中進行組織。</span><span class="sxs-lookup"><span data-stu-id="68a75-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="68a75-118">此控制項模式類似于 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ，因為任何控制項執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) 也都必須為每個子項目公開一個資料行和/或資料列標頭關聯性。</span><span class="sxs-lookup"><span data-stu-id="68a75-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="68a75-119">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="68a75-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="68a75-120">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="68a75-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="68a75-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="68a75-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="68a75-122">**ITableProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="68a75-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="68a75-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="68a75-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="68a75-124">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="68a75-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="68a75-125">在執行 **Table** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="68a75-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="68a75-126">存取個別資料格的內容是透過二維邏輯座標系統或 [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)所需的並存執行所提供的陣列。</span><span class="sxs-lookup"><span data-stu-id="68a75-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="68a75-127">資料行或資料列標頭可以包含在資料表物件中，也可以是與資料表物件建立關係的個別標頭物件。</span><span class="sxs-lookup"><span data-stu-id="68a75-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="68a75-128">資料行和資料列標頭可同時包含主要標頭和任何支援的標頭。</span><span class="sxs-lookup"><span data-stu-id="68a75-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="68a75-129">此概念在 Microsoft Excel 試算表中變得很明顯，其中使用者已定義 **名字** 資料行。</span><span class="sxs-lookup"><span data-stu-id="68a75-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="68a75-130">此資料行現在有兩個標頭，包括使用者所定義的 **名字** 標頭，以及該應用程式所指派之資料行的英數位元。</span><span class="sxs-lookup"><span data-stu-id="68a75-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="68a75-131">請參閱 [方格控制項模式](uiauto-implementinggrid.md) 以取得相關格線功能。</span><span class="sxs-lookup"><span data-stu-id="68a75-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="68a75-132">下圖顯示具有複雜資料行標頭的資料表。</span><span class="sxs-lookup"><span data-stu-id="68a75-132">The following image shows a table with complex column headers.</span></span>

    ![具有複雜資料行標頭的資料表](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="68a75-134">下圖顯示具有不明確 [**ITableProvider：：之 roworcolumnmajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) 屬性的資料表。</span><span class="sxs-lookup"><span data-stu-id="68a75-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![具有不明確之 roworcolumnmajor 屬性的資料表](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="68a75-136">**ITableProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="68a75-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="68a75-137">執行 [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="68a75-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="68a75-138">必要成員</span><span class="sxs-lookup"><span data-stu-id="68a75-138">Required members</span></span>                                                   | <span data-ttu-id="68a75-139">成員類型</span><span class="sxs-lookup"><span data-stu-id="68a75-139">Member type</span></span> | <span data-ttu-id="68a75-140">備註</span><span class="sxs-lookup"><span data-stu-id="68a75-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="68a75-141">**之 roworcolumnmajor**</span><span class="sxs-lookup"><span data-stu-id="68a75-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="68a75-142">屬性</span><span class="sxs-lookup"><span data-stu-id="68a75-142">Property</span></span>    | <span data-ttu-id="68a75-143">無</span><span class="sxs-lookup"><span data-stu-id="68a75-143">None</span></span>  |
| [<span data-ttu-id="68a75-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="68a75-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="68a75-145">方法</span><span class="sxs-lookup"><span data-stu-id="68a75-145">Method</span></span>      | <span data-ttu-id="68a75-146">無</span><span class="sxs-lookup"><span data-stu-id="68a75-146">None</span></span>  |
| [<span data-ttu-id="68a75-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="68a75-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="68a75-148">方法</span><span class="sxs-lookup"><span data-stu-id="68a75-148">Method</span></span>      | <span data-ttu-id="68a75-149">無</span><span class="sxs-lookup"><span data-stu-id="68a75-149">None</span></span>  |



 

<span data-ttu-id="68a75-150">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="68a75-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68a75-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="68a75-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="68a75-152">**概念**</span><span class="sxs-lookup"><span data-stu-id="68a75-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68a75-153">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="68a75-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="68a75-154">TableItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="68a75-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="68a75-155">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="68a75-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="68a75-156">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="68a75-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




