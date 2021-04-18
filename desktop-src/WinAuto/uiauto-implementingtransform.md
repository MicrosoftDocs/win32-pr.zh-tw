---
title: 轉換控制項模式
description: 描述執行 ITransformProvider 和 ITransformProvider2 的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- 消費者介面自動化，執行轉換控制項模式
- 消費者介面自動化，轉換控制項模式
- 消費者介面自動化、ITransformProvider
- ITransformProvider
- 執行消費者介面自動化轉換控制項模式
- 轉換控制項模式
- 控制項模式，ITransformProvider
- 控制模式，實施消費者介面自動化轉換
- 控制項模式，轉換
- 介面，ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508028"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="eae56-113">轉換控制項模式</span><span class="sxs-lookup"><span data-stu-id="eae56-113">Transform Control Pattern</span></span>

<span data-ttu-id="eae56-114">描述執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 和 [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2)的指導方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eae56-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="eae56-115">轉換控制項模式用來支援可在二維空間內移動、調整大小或旋轉的控制項。</span><span class="sxs-lookup"><span data-stu-id="eae56-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="eae56-116">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="eae56-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="eae56-117">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="eae56-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eae56-118">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="eae56-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="eae56-119">**ITransformProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="eae56-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="eae56-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="eae56-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="eae56-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="eae56-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="eae56-122">在執行 **轉換** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="eae56-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="eae56-123">此控制項模式的支援不限於桌面上的物件。</span><span class="sxs-lookup"><span data-stu-id="eae56-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="eae56-124">若容器物件的子項可以自由在容器的範圍內移動、調整大小或旋轉，則這些子項也必須支援此控制項模式。</span><span class="sxs-lookup"><span data-stu-id="eae56-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="eae56-125">如果物件最後在螢幕上的位置完全在其容器的座標以外，而鍵盤或滑鼠存取不到的話，就無法移動、調整大小或旋轉物件 (例如，最上層的視窗移離螢幕，或是子物件移到容器檢視區範圍以外的地方)。</span><span class="sxs-lookup"><span data-stu-id="eae56-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="eae56-126">在這種情況下，物件會放置到最接近所要求螢幕座標的地方，其上方或左方座標會覆寫成容器範圍內的座標。</span><span class="sxs-lookup"><span data-stu-id="eae56-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="eae56-127">針對多監視器系統，若物件移動、調整大小或旋轉後的位置完全超出合併桌面螢幕座標的範圍，物件就會移至主要監視器上最接近所要求座標的位置。</span><span class="sxs-lookup"><span data-stu-id="eae56-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="eae56-128">所有參數和屬性值都是絕對值，不受地區設定影響。</span><span class="sxs-lookup"><span data-stu-id="eae56-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="eae56-129">**ITransformProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="eae56-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="eae56-130">執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="eae56-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="eae56-131">必要成員</span><span class="sxs-lookup"><span data-stu-id="eae56-131">Required members</span></span>                                         | <span data-ttu-id="eae56-132">成員類型</span><span class="sxs-lookup"><span data-stu-id="eae56-132">Member type</span></span> | <span data-ttu-id="eae56-133">備註</span><span class="sxs-lookup"><span data-stu-id="eae56-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="eae56-134">**CanMove**</span><span class="sxs-lookup"><span data-stu-id="eae56-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="eae56-135">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-135">Property</span></span>    | <span data-ttu-id="eae56-136">無</span><span class="sxs-lookup"><span data-stu-id="eae56-136">None</span></span>  |
| [<span data-ttu-id="eae56-137">**Graphicswindow.canresize**</span><span class="sxs-lookup"><span data-stu-id="eae56-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="eae56-138">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-138">Property</span></span>    | <span data-ttu-id="eae56-139">無</span><span class="sxs-lookup"><span data-stu-id="eae56-139">None</span></span>  |
| [<span data-ttu-id="eae56-140">**CanRotate**</span><span class="sxs-lookup"><span data-stu-id="eae56-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="eae56-141">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-141">Property</span></span>    | <span data-ttu-id="eae56-142">無</span><span class="sxs-lookup"><span data-stu-id="eae56-142">None</span></span>  |
| [<span data-ttu-id="eae56-143">**移動**</span><span class="sxs-lookup"><span data-stu-id="eae56-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="eae56-144">方法</span><span class="sxs-lookup"><span data-stu-id="eae56-144">Method</span></span>      | <span data-ttu-id="eae56-145">無</span><span class="sxs-lookup"><span data-stu-id="eae56-145">None</span></span>  |
| [<span data-ttu-id="eae56-146">**調整大小**</span><span class="sxs-lookup"><span data-stu-id="eae56-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="eae56-147">方法</span><span class="sxs-lookup"><span data-stu-id="eae56-147">Method</span></span>      | <span data-ttu-id="eae56-148">無</span><span class="sxs-lookup"><span data-stu-id="eae56-148">None</span></span>  |
| [<span data-ttu-id="eae56-149">**旋轉**</span><span class="sxs-lookup"><span data-stu-id="eae56-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="eae56-150">方法</span><span class="sxs-lookup"><span data-stu-id="eae56-150">Method</span></span>      | <span data-ttu-id="eae56-151">無</span><span class="sxs-lookup"><span data-stu-id="eae56-151">None</span></span>  |



 

<span data-ttu-id="eae56-152">執行 [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 介面需要下列其他屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="eae56-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="eae56-153">必要成員</span><span class="sxs-lookup"><span data-stu-id="eae56-153">Required members</span></span>                                              | <span data-ttu-id="eae56-154">成員類型</span><span class="sxs-lookup"><span data-stu-id="eae56-154">Member type</span></span> | <span data-ttu-id="eae56-155">備註</span><span class="sxs-lookup"><span data-stu-id="eae56-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="eae56-156">**CanZoom**</span><span class="sxs-lookup"><span data-stu-id="eae56-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="eae56-157">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-157">Property</span></span>    | <span data-ttu-id="eae56-158">無</span><span class="sxs-lookup"><span data-stu-id="eae56-158">None</span></span>  |
| [<span data-ttu-id="eae56-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="eae56-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="eae56-160">方法</span><span class="sxs-lookup"><span data-stu-id="eae56-160">Method</span></span>      | <span data-ttu-id="eae56-161">無</span><span class="sxs-lookup"><span data-stu-id="eae56-161">None</span></span>  |
| [<span data-ttu-id="eae56-162">**ZoomByUnit**</span><span class="sxs-lookup"><span data-stu-id="eae56-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="eae56-163">方法</span><span class="sxs-lookup"><span data-stu-id="eae56-163">Method</span></span>      | <span data-ttu-id="eae56-164">無</span><span class="sxs-lookup"><span data-stu-id="eae56-164">None</span></span>  |
| [<span data-ttu-id="eae56-165">**ZoomLevel**</span><span class="sxs-lookup"><span data-stu-id="eae56-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="eae56-166">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-166">Property</span></span>    | <span data-ttu-id="eae56-167">無</span><span class="sxs-lookup"><span data-stu-id="eae56-167">None</span></span>  |
| [<span data-ttu-id="eae56-168">**ZoomMaximum**</span><span class="sxs-lookup"><span data-stu-id="eae56-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="eae56-169">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-169">Property</span></span>    | <span data-ttu-id="eae56-170">無</span><span class="sxs-lookup"><span data-stu-id="eae56-170">None</span></span>  |
| [<span data-ttu-id="eae56-171">**ZoomMinimum**</span><span class="sxs-lookup"><span data-stu-id="eae56-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="eae56-172">屬性</span><span class="sxs-lookup"><span data-stu-id="eae56-172">Property</span></span>    | <span data-ttu-id="eae56-173">無</span><span class="sxs-lookup"><span data-stu-id="eae56-173">None</span></span>  |



 

<span data-ttu-id="eae56-174">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="eae56-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eae56-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="eae56-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eae56-176">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="eae56-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="eae56-177">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="eae56-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="eae56-178">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="eae56-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 