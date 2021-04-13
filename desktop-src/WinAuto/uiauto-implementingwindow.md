---
title: 視窗控制項模式
description: 描述執行 IWindowProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。 Window 控制項模式支援在傳統 GUI 內提供基本視窗功能的控制項。
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- 消費者介面自動化，執行視窗控制項模式
- 消費者介面自動化、視窗控制項模式
- 消費者介面自動化、IWindowProvider
- IWindowProvider
- 執行消費者介面自動化 Window 控制項模式
- 視窗控制項模式
- 控制項模式，IWindowProvider
- 控制項模式，執行消費者介面自動化視窗
- 控制項模式，視窗
- 介面，IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311343"
---
# <a name="window-control-pattern"></a><span data-ttu-id="028be-114">視窗控制項模式</span><span class="sxs-lookup"><span data-stu-id="028be-114">Window Control Pattern</span></span>

<span data-ttu-id="028be-115">描述執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="028be-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="028be-116">**Window** 控制項模式支援在傳統 GUI 內提供基本視窗功能的控制項。</span><span class="sxs-lookup"><span data-stu-id="028be-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="028be-117">必須執行此控制項模式的控制項範例包括最上層應用程式視窗、多重文件介面 (MDI) 子視窗、可調整大小的分割窗格控制項、強制回應對話方塊和氣球說明視窗。</span><span class="sxs-lookup"><span data-stu-id="028be-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="028be-118">如需實作此控制項模式的控制項範例，請參閱 [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="028be-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="028be-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="028be-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="028be-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="028be-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="028be-121">**IWindowProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="028be-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="028be-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="028be-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="028be-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="028be-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="028be-124">在執行 **Window** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="028be-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="028be-125">為了支援使用 Microsoft 消費者介面自動化修改視窗大小和螢幕位置的功能，除了 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)以外，控制項還必須執行 [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) 。</span><span class="sxs-lookup"><span data-stu-id="028be-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="028be-126">包含標題列的控制項和可讓控制項移動、調整大小、最大化、最小化或關閉的標題列元素，通常都必須執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)。</span><span class="sxs-lookup"><span data-stu-id="028be-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="028be-127">工具提示快顯視窗和下拉式方塊或功能表下拉式清單等控制項通常不會執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)。</span><span class="sxs-lookup"><span data-stu-id="028be-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="028be-128">氣球說明視窗與基本工具提示快顯視窗的差異在於布建類似視窗的 [ **關閉** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="028be-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="028be-129">[**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)不支援全螢幕模式，因為它是應用程式特有的功能，而不是一般的視窗行為。</span><span class="sxs-lookup"><span data-stu-id="028be-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="028be-130">**IWindowProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="028be-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="028be-131">執行 [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) 介面需要下列屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="028be-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="028be-132">必要成員</span><span class="sxs-lookup"><span data-stu-id="028be-132">Required members</span></span>                                                                            | <span data-ttu-id="028be-133">成員類型</span><span class="sxs-lookup"><span data-stu-id="028be-133">Member type</span></span> | <span data-ttu-id="028be-134">備註</span><span class="sxs-lookup"><span data-stu-id="028be-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="028be-135">**WindowInteractionState**</span><span class="sxs-lookup"><span data-stu-id="028be-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="028be-136">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-136">Property</span></span>    | <span data-ttu-id="028be-137">不保證是 **WindowInteractionState \_ ReadyForUserInteraction**</span><span class="sxs-lookup"><span data-stu-id="028be-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="028be-138">**IsModal**</span><span class="sxs-lookup"><span data-stu-id="028be-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="028be-139">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-139">Property</span></span>    | <span data-ttu-id="028be-140">無</span><span class="sxs-lookup"><span data-stu-id="028be-140">None</span></span>                                                                        |
| [<span data-ttu-id="028be-141">**IsTopmost**</span><span class="sxs-lookup"><span data-stu-id="028be-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="028be-142">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-142">Property</span></span>    | <span data-ttu-id="028be-143">無</span><span class="sxs-lookup"><span data-stu-id="028be-143">None</span></span>                                                                        |
| [<span data-ttu-id="028be-144">**CanMaximize**</span><span class="sxs-lookup"><span data-stu-id="028be-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="028be-145">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-145">Property</span></span>    | <span data-ttu-id="028be-146">無</span><span class="sxs-lookup"><span data-stu-id="028be-146">None</span></span>                                                                        |
| [<span data-ttu-id="028be-147">**CanMinimize**</span><span class="sxs-lookup"><span data-stu-id="028be-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="028be-148">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-148">Property</span></span>    | <span data-ttu-id="028be-149">無</span><span class="sxs-lookup"><span data-stu-id="028be-149">None</span></span>                                                                        |
| [<span data-ttu-id="028be-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="028be-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="028be-151">屬性</span><span class="sxs-lookup"><span data-stu-id="028be-151">Property</span></span>    | <span data-ttu-id="028be-152">無</span><span class="sxs-lookup"><span data-stu-id="028be-152">None</span></span>                                                                        |
| [<span data-ttu-id="028be-153">**關閉**</span><span class="sxs-lookup"><span data-stu-id="028be-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="028be-154">方法</span><span class="sxs-lookup"><span data-stu-id="028be-154">Method</span></span>      | <span data-ttu-id="028be-155">無</span><span class="sxs-lookup"><span data-stu-id="028be-155">None</span></span>                                                                        |
| [<span data-ttu-id="028be-156">**SetVisualState**</span><span class="sxs-lookup"><span data-stu-id="028be-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="028be-157">方法</span><span class="sxs-lookup"><span data-stu-id="028be-157">Method</span></span>      | <span data-ttu-id="028be-158">無</span><span class="sxs-lookup"><span data-stu-id="028be-158">None</span></span>                                                                        |
| [<span data-ttu-id="028be-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="028be-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="028be-160">方法</span><span class="sxs-lookup"><span data-stu-id="028be-160">Method</span></span>      | <span data-ttu-id="028be-161">無</span><span class="sxs-lookup"><span data-stu-id="028be-161">None</span></span>                                                                        |
| [<span data-ttu-id="028be-162">**UIA \_ 視窗 \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="028be-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="028be-163">事件</span><span class="sxs-lookup"><span data-stu-id="028be-163">Event</span></span>       | <span data-ttu-id="028be-164">無</span><span class="sxs-lookup"><span data-stu-id="028be-164">None</span></span>                                                                        |
| [<span data-ttu-id="028be-165">**UIA \_ 視窗 \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="028be-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="028be-166">事件</span><span class="sxs-lookup"><span data-stu-id="028be-166">Event</span></span>       | <span data-ttu-id="028be-167">無</span><span class="sxs-lookup"><span data-stu-id="028be-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="028be-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="028be-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="028be-169">**概念**</span><span class="sxs-lookup"><span data-stu-id="028be-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="028be-170">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="028be-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="028be-171">UI 自動化用戶端的控制項模式對應</span><span class="sxs-lookup"><span data-stu-id="028be-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="028be-172">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="028be-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




