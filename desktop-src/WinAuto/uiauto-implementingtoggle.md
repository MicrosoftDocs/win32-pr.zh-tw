---
title: 切換控制項模式
description: 描述執行 IToggleProvider 的方針和慣例，包括屬性和方法的相關資訊。 切換控制項模式是用來支援可在一組狀態之間迴圈的控制項，並在設定之後維護狀態。
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- 消費者介面自動化，執行切換控制項模式
- 消費者介面自動化，切換控制項模式
- 消費者介面自動化、IToggleProvider
- IToggleProvider
- 執行消費者介面自動化切換控制項模式
- 切換控制項模式
- 控制項模式，IToggleProvider
- 控制項模式，執行消費者介面自動化切換
- 控制項模式，切換
- 介面，IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372003"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="96b87-114">切換控制項模式</span><span class="sxs-lookup"><span data-stu-id="96b87-114">Toggle Control Pattern</span></span>

<span data-ttu-id="96b87-115">描述執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96b87-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="96b87-116">**切換** 控制項模式是用來支援可在一組狀態之間迴圈的控制項，並在設定之後維護狀態。</span><span class="sxs-lookup"><span data-stu-id="96b87-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="96b87-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="96b87-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="96b87-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="96b87-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="96b87-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="96b87-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="96b87-120">**IToggleProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="96b87-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="96b87-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="96b87-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="96b87-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="96b87-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="96b87-123">在執行 **切換** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="96b87-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="96b87-124">啟動時不會維持狀態的控制項（例如按鈕、工具列按鈕和超連結）必須改為執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 。</span><span class="sxs-lookup"><span data-stu-id="96b87-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="96b87-125">控制項必須依照下列順序，迴圈切換其切換狀態 ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) ： **ToggleState \_ On**、 **ToggleState \_ Off** 和（如果支援的話） **ToggleState \_ 不定**。</span><span class="sxs-lookup"><span data-stu-id="96b87-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="96b87-126">**切換** 不會提供設定狀態方法，因為在三個狀態的直接設定方面有問題，而不會迴圈其適當的 [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) 序列。</span><span class="sxs-lookup"><span data-stu-id="96b87-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="96b87-127">選項按鈕控制項不會執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)，因為它無法迴圈其有效狀態。</span><span class="sxs-lookup"><span data-stu-id="96b87-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="96b87-128">**IToggleProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="96b87-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="96b87-129">執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="96b87-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="96b87-130">必要成員</span><span class="sxs-lookup"><span data-stu-id="96b87-130">Required members</span></span>                                          | <span data-ttu-id="96b87-131">成員類型</span><span class="sxs-lookup"><span data-stu-id="96b87-131">Member type</span></span> | <span data-ttu-id="96b87-132">備註</span><span class="sxs-lookup"><span data-stu-id="96b87-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="96b87-133">**切換**</span><span class="sxs-lookup"><span data-stu-id="96b87-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="96b87-134">方法</span><span class="sxs-lookup"><span data-stu-id="96b87-134">Method</span></span>      | <span data-ttu-id="96b87-135">無</span><span class="sxs-lookup"><span data-stu-id="96b87-135">None</span></span>  |
| [<span data-ttu-id="96b87-136">**ToggleState**</span><span class="sxs-lookup"><span data-stu-id="96b87-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="96b87-137">屬性</span><span class="sxs-lookup"><span data-stu-id="96b87-137">Property</span></span>    | <span data-ttu-id="96b87-138">無</span><span class="sxs-lookup"><span data-stu-id="96b87-138">None</span></span>  |



 

<span data-ttu-id="96b87-139">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="96b87-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96b87-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="96b87-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b87-141">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="96b87-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="96b87-142">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="96b87-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="96b87-143">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="96b87-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




