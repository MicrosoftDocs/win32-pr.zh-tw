---
title: 停駐控制項模式
description: 描述執行 IDockProvider 的方針和慣例，包括屬性和方法的相關資訊。 Dock 控制項模式是用來公開停駐容器內控制項的停駐屬性。
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- 消費者介面自動化，實施 dock 控制項模式
- 消費者介面自動化，停駐控制項模式
- 消費者介面自動化、IDockProvider
- IDockProvider
- 執行消費者介面自動化 dock 控制項模式
- 停駐控制項模式
- 控制項模式，IDockProvider
- 控制模式，實施消費者介面自動化 dock
- 控制項模式，dock
- 介面，IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839875"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="ca830-114">停駐控制項模式</span><span class="sxs-lookup"><span data-stu-id="ca830-114">Dock Control Pattern</span></span>

<span data-ttu-id="ca830-115">描述執行 [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca830-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="ca830-116">**Dock** 控制項模式是用來公開停駐容器內控制項的停駐屬性。</span><span class="sxs-lookup"><span data-stu-id="ca830-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="ca830-117">停駐容器是一種控制項，可讓您依垂直和水平的相對位置排列子項目。</span><span class="sxs-lookup"><span data-stu-id="ca830-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="ca830-118">下圖顯示具有兩個子項目的停駐容器。</span><span class="sxs-lookup"><span data-stu-id="ca830-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="ca830-119">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="ca830-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![顯示具有兩個停駐子系之銜接容器的螢幕擷取畫面](images/dockxmpl.jpg)

<span data-ttu-id="ca830-121">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ca830-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ca830-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="ca830-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ca830-123">**IDockProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="ca830-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="ca830-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca830-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ca830-125">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="ca830-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ca830-126">在實施 **Dock** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="ca830-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ca830-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) 不會公開停駐容器的任何屬性，或停駐于停駐容器內目前控制項連續的控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="ca830-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="ca830-128">控制項會根據其目前的疊置順序，在彼此相對的位置停駐；疊置順序的位置愈高，控制項離停駐容器的指定邊緣就愈遠。</span><span class="sxs-lookup"><span data-stu-id="ca830-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="ca830-129">如果停駐容器可以調整大小，容器內的任何停駐控制項會再次對齊到原始停駐的相同邊緣。</span><span class="sxs-lookup"><span data-stu-id="ca830-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="ca830-130">停駐的控制項也會調整大小，以根據其 [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) 屬性的銜接行為填滿容器內的任何空間。</span><span class="sxs-lookup"><span data-stu-id="ca830-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="ca830-131">例如，如果指定了 **DockPosition \_ Top** ，則控制項的左邊和右邊將會展開以填滿任何可用的空間。</span><span class="sxs-lookup"><span data-stu-id="ca830-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="ca830-132">如果指定了 **DockPosition \_ Fill** ，則會展開控制項的四個邊來填滿任何可用的空間。</span><span class="sxs-lookup"><span data-stu-id="ca830-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="ca830-133">在多監視器系統上，控制項應停駐到目前監視器的左或右邊。</span><span class="sxs-lookup"><span data-stu-id="ca830-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="ca830-134">若不可行，則應停駐到最左邊監視器的左邊，或最右邊監視器的右邊。</span><span class="sxs-lookup"><span data-stu-id="ca830-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="ca830-135">**IDockProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="ca830-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="ca830-136">執行 [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="ca830-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="ca830-137">必要成員</span><span class="sxs-lookup"><span data-stu-id="ca830-137">Required members</span></span>                                                | <span data-ttu-id="ca830-138">成員類型</span><span class="sxs-lookup"><span data-stu-id="ca830-138">Member type</span></span> | <span data-ttu-id="ca830-139">備註</span><span class="sxs-lookup"><span data-stu-id="ca830-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ca830-140">**DockPosition**</span><span class="sxs-lookup"><span data-stu-id="ca830-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="ca830-141">屬性</span><span class="sxs-lookup"><span data-stu-id="ca830-141">Property</span></span>    | <span data-ttu-id="ca830-142">無</span><span class="sxs-lookup"><span data-stu-id="ca830-142">None</span></span>  |
| [<span data-ttu-id="ca830-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="ca830-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="ca830-144">方法</span><span class="sxs-lookup"><span data-stu-id="ca830-144">Method</span></span>      | <span data-ttu-id="ca830-145">無</span><span class="sxs-lookup"><span data-stu-id="ca830-145">None</span></span>  |



 

<span data-ttu-id="ca830-146">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="ca830-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca830-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca830-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca830-148">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ca830-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ca830-149">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="ca830-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ca830-150">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="ca830-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




