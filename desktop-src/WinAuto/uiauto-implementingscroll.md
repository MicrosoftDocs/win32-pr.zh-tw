---
title: 捲軸控制項模式
description: 描述執行 IScrollProvider 的方針和慣例，包括屬性和方法的相關資訊。 捲軸控制項模式用來支援做為子物件集合之可滾動容器的控制項。
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- 消費者介面自動化，執行捲軸控制項模式
- 消費者介面自動化、捲軸控制項模式
- 消費者介面自動化、IScrollProvider
- IScrollProvider
- 執行消費者介面自動化捲軸控制項模式
- 捲軸控制項模式
- 控制項模式，IScrollProvider
- 控制項模式，執行消費者介面自動化捲軸
- 控制項模式、捲軸
- 介面，IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674315"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="e9e0c-114">捲軸控制項模式</span><span class="sxs-lookup"><span data-stu-id="e9e0c-114">Scroll Control Pattern</span></span>

<span data-ttu-id="e9e0c-115">描述執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="e9e0c-116">**滾動** 條控制項模式用來支援做為子物件集合之可滾動容器的控制項。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="e9e0c-117">控制項不一定要使用捲軸來支援滾動功能（雖然通常會這樣做）。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="e9e0c-118">下圖顯示不使用捲軸的滾動控制項。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="e9e0c-119">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![顯示沒有捲軸之滾動控制項的螢幕擷取畫面](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="e9e0c-121">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e9e0c-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e9e0c-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="e9e0c-123">**IScrollProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e9e0c-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="e9e0c-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9e0c-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="e9e0c-125">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e9e0c-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="e9e0c-126">在實行 **Scroll** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="e9e0c-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="e9e0c-127">此控制項的子系必須執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="e9e0c-128">容器控制項的捲軸不支援 **滾動** 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="e9e0c-129">它們必須改為支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="e9e0c-130">若捲動是以百分比為單位，則與捲動刻度相關的所有值或數量必須標準化為 0 到 100 之間的範圍。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="e9e0c-131">[**IScrollProvider：： HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)屬性和 [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)屬性與 **IsEnabled** 屬性無關。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="e9e0c-132">如果 [**IScrollProvider：： HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) 屬性為 **FALSE**，則 [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) 屬性應設定為 100 (100% ) 而 [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) 屬性應設定為 **UIA \_ ScrollPatternNoScroll** (-1) 。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="e9e0c-133">同樣地，如果 [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) 屬性為 **FALSE**，則 [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) 屬性應該設定為 100 (100% ) 而 [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) 屬性應設定為 **UIA \_ ScrollPatternNoScroll** (-1) 。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="e9e0c-134">這可讓 Microsoft 消費者介面自動化用戶端在 [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) 方法中使用這些屬性值，同時避免在用戶端不感興趣的方向啟動時，才會發生競爭情況。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="e9e0c-135">[**IScrollProvider：： HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent)屬性是地區設定特有的。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="e9e0c-136">將 **HorizontalScrollPercent** 設定為100時，必須將控制項的滾動位置設定為對等語言的最右邊位置，例如從左至右讀取的英文。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="e9e0c-137">或者，如果是由右至左的阿拉伯文語言，將 **HorizontalScrollPercent** 設定為100，就必須將滾動位置設定為最左邊的位置。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="e9e0c-138">**IScrollProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e9e0c-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="e9e0c-139">執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="e9e0c-140">必要成員</span><span class="sxs-lookup"><span data-stu-id="e9e0c-140">Required members</span></span>                                                                  | <span data-ttu-id="e9e0c-141">成員類型</span><span class="sxs-lookup"><span data-stu-id="e9e0c-141">Member type</span></span> | <span data-ttu-id="e9e0c-142">備註</span><span class="sxs-lookup"><span data-stu-id="e9e0c-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="e9e0c-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="e9e0c-144">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-144">Property</span></span>    | <span data-ttu-id="e9e0c-145">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-145">None</span></span>  |
| [<span data-ttu-id="e9e0c-146">**VerticalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="e9e0c-147">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-147">Property</span></span>    | <span data-ttu-id="e9e0c-148">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-148">None</span></span>  |
| [<span data-ttu-id="e9e0c-149">**HorizontalViewSize**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="e9e0c-150">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-150">Property</span></span>    | <span data-ttu-id="e9e0c-151">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-151">None</span></span>  |
| [<span data-ttu-id="e9e0c-152">**VerticalViewSize**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="e9e0c-153">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-153">Property</span></span>    | <span data-ttu-id="e9e0c-154">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-154">None</span></span>  |
| [<span data-ttu-id="e9e0c-155">**HorizontallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="e9e0c-156">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-156">Property</span></span>    | <span data-ttu-id="e9e0c-157">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-157">None</span></span>  |
| [<span data-ttu-id="e9e0c-158">**VerticallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="e9e0c-159">屬性</span><span class="sxs-lookup"><span data-stu-id="e9e0c-159">Property</span></span>    | <span data-ttu-id="e9e0c-160">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-160">None</span></span>  |
| [<span data-ttu-id="e9e0c-161">**捲動**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="e9e0c-162">方法</span><span class="sxs-lookup"><span data-stu-id="e9e0c-162">Method</span></span>      | <span data-ttu-id="e9e0c-163">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-163">None</span></span>  |
| [<span data-ttu-id="e9e0c-164">**SetScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="e9e0c-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="e9e0c-165">方法</span><span class="sxs-lookup"><span data-stu-id="e9e0c-165">Method</span></span>      | <span data-ttu-id="e9e0c-166">無</span><span class="sxs-lookup"><span data-stu-id="e9e0c-166">None</span></span>  |



 

<span data-ttu-id="e9e0c-167">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="e9e0c-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9e0c-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9e0c-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9e0c-169">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="e9e0c-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="e9e0c-170">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="e9e0c-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="e9e0c-171">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="e9e0c-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




