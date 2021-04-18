---
title: 消費者介面自動化的拖放支援
description: 本主題描述的控制項模式會公開專案拖放功能的相關資訊。
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- 消費者介面自動化，拖放支援
- 消費者介面自動化，拖曳模式總覽
- 消費者介面自動化，DropTarget 模式總覽
- 消費者介面自動化，拖放總覽
- 拖放模式，關於
- 拖曳控制項模式
- DropTarget 控制項模式
- 控制項模式，拖曳
- 控制項模式，DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965026"
---
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="d0c08-112">消費者介面自動化的拖放支援</span><span class="sxs-lookup"><span data-stu-id="d0c08-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="d0c08-113">Microsoft 消費者介面自動化定義兩種控制項模式，可支援拖放案例、 [拖曳](/windows/desktop/WinAuto/uiauto-implementingdrag) 控制項模式，以及 [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d0c08-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="d0c08-114">您可以針對可以拖曳的元素，以及可接收拖曳專案的專案 DropTarget 控制項模式，來執行拖曳控制項模式;也就是放置目標。</span><span class="sxs-lookup"><span data-stu-id="d0c08-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="d0c08-115">這兩個控制項模式會公開輔助技術可用於協助協助工具使用者完成拖放作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="d0c08-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="d0c08-116">拖曳樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="d0c08-117">來源/目標樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="d0c08-118">僅限來源的樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="d0c08-119">拖曳多個專案</span><span class="sxs-lookup"><span data-stu-id="d0c08-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="d0c08-120">拖放的用戶端介面</span><span class="sxs-lookup"><span data-stu-id="d0c08-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="d0c08-121">拖曳樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-121">Dragging Styles</span></span>

<span data-ttu-id="d0c08-122">當您針對可 [拖曳](/windows/desktop/WinAuto/uiauto-implementingdrag) 的元素執行拖曳控制項模式時，您必須決定要執行 *來源/目標* 拖曳樣式，還是要執行 *僅限來源* 的拖曳樣式。</span><span class="sxs-lookup"><span data-stu-id="d0c08-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="d0c08-123">來源/目標樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-123">Source/target Style</span></span>

<span data-ttu-id="d0c08-124">在拖放的來源/目標樣式中，拖曳的元素 (「來源」 ) ，而「目標」 )  (的放置目標元素則是相異的，且每個專案都會引發一組不同的事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="d0c08-125">以下是使用來源/目標樣式之拖曳操作的生命週期：</span><span class="sxs-lookup"><span data-stu-id="d0c08-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="d0c08-126">當使用者開始拖曳作業時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="d0c08-127">來源會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-128">來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="d0c08-129">目標會更新其 [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0c08-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="d0c08-130">當拖曳作業進入目的地區域時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="d0c08-131">目標會引發 System.windows.dragdrop.dragenter> ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="d0c08-132">當拖曳作業離開目的地區域時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="d0c08-133">目標會引發 DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="d0c08-134">當使用者放開非目標的拖曳專案時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="d0c08-135">來源會引發 DragCancel ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-136">來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="d0c08-137">當使用者在目標上放開拖曳的專案時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="d0c08-138">來源會引發 DragComplete ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-139">來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="d0c08-140">目標會設定 [**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性，以指出所發生的效果。</span><span class="sxs-lookup"><span data-stu-id="d0c08-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="d0c08-141">目標會引發已卸載的 ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="d0c08-142">來源與目標物件中的事件是密切相關的，但相異。</span><span class="sxs-lookup"><span data-stu-id="d0c08-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="d0c08-143">所要拖曳之內容的相關資料來自來源，而關於「發生什麼事」和「發生什麼事」的資料則來自于目標。</span><span class="sxs-lookup"><span data-stu-id="d0c08-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="d0c08-144">當拖曳作業正在進行時，拖曳的專案可以在作業完成之前，任意次數地拖曳至目的地區域。</span><span class="sxs-lookup"><span data-stu-id="d0c08-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="d0c08-145">任何需要更新其 [**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性的放置目標，都應該在該屬性上引發額外的屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="d0c08-146">僅限來源的樣式</span><span class="sxs-lookup"><span data-stu-id="d0c08-146">Source-only Style</span></span>

<span data-ttu-id="d0c08-147">僅限來源的拖曳樣式可讓提供者避免執行卸載目標。</span><span class="sxs-lookup"><span data-stu-id="d0c08-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="d0c08-148">未執行卸載目標有助於降低執行成本，但不會提供協助工具用戶端應用程式任何有關接收捨棄之物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="d0c08-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="d0c08-149">以下是使用僅限來源樣式之拖曳作業的生命週期：</span><span class="sxs-lookup"><span data-stu-id="d0c08-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="d0c08-150">當使用者開始拖曳作業時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="d0c08-151">來源會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-152">來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="d0c08-153">當拖曳作業進入目的地區域時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="d0c08-154">來源會將 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性設定為適當的值。</span><span class="sxs-lookup"><span data-stu-id="d0c08-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="d0c08-155">當拖曳作業離開目的地區域時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="d0c08-156">來源會將 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性設定為適當的值。</span><span class="sxs-lookup"><span data-stu-id="d0c08-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="d0c08-157">當使用者放開非目標的拖曳專案時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="d0c08-158">來源會引發 DragCancel ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-159">來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="d0c08-160">當使用者在目標上放開拖曳的專案時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="d0c08-161">來源會引發 DragComplete ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-162">來源會設定 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性，以指出卸載專案時所發生的效果。</span><span class="sxs-lookup"><span data-stu-id="d0c08-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="d0c08-163">拖曳多個專案</span><span class="sxs-lookup"><span data-stu-id="d0c08-163">Dragging Multiple Items</span></span>

<span data-ttu-id="d0c08-164">如果提供者所執行的拖放作業可讓使用者同時拖曳多個物件，則提供者會依照上一節所述，使用來源/目標或僅限來源的樣式，但差異較小。</span><span class="sxs-lookup"><span data-stu-id="d0c08-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="d0c08-165">當使用者開始拖曳作業時，提供者會建立主要來源元素，以代表正在拖曳的整組專案。</span><span class="sxs-lookup"><span data-stu-id="d0c08-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="d0c08-166">主要來源元素會代表一組拖曳的專案來引發所有事件;這些專案不會引發自己的任何事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="d0c08-167">當使用者開始拖曳作業時：</span><span class="sxs-lookup"><span data-stu-id="d0c08-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="d0c08-168">提供者會建立主要來源元素。</span><span class="sxs-lookup"><span data-stu-id="d0c08-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="d0c08-169">主要來源元素會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="d0c08-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="d0c08-170">主要來源元素會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d0c08-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="d0c08-171">主要來源元素會更新抓取專案的清單，以包含所有要拖曳的專案，讓 [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) 方法可以取得清單。</span><span class="sxs-lookup"><span data-stu-id="d0c08-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="d0c08-172">針對該點，主要來源專案會依照上一節所述，執行與來源元素相同的角色。</span><span class="sxs-lookup"><span data-stu-id="d0c08-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="d0c08-173">拖放的用戶端介面</span><span class="sxs-lookup"><span data-stu-id="d0c08-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="d0c08-174">消費者介面自動化用戶端應用程式會使用 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 和 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) 介面來存取 UI 元素的拖放資訊。</span><span class="sxs-lookup"><span data-stu-id="d0c08-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 