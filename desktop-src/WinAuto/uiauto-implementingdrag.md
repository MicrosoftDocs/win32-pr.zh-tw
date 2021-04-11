---
title: 拖曳控制項模式
description: 提供使用 IDragProvider 來執行拖曳控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。 拖曳控制項模式用來支援可拖曳的控制項，或具有可拖曳專案的控制項。
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- 消費者介面自動化，執行拖曳控制項模式
- 消費者介面自動化，拖曳控制項模式
- 消費者介面自動化、IDragProvider
- IDragProvider
- 執行消費者介面自動化拖曳控制項模式
- 拖曳控制項模式
- 控制項模式，IDragProvider
- 控制項模式，實施消費者介面自動化拖曳
- 控制項模式，拖曳
- 介面，IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023697"
---
# <a name="drag-control-pattern"></a><span data-ttu-id="45cd5-114">拖曳控制項模式</span><span class="sxs-lookup"><span data-stu-id="45cd5-114">Drag Control Pattern</span></span>

<span data-ttu-id="45cd5-115">提供使用 [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider)來執行 **拖曳** 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45cd5-115">Provides guidelines and conventions for implementing the **Drag** control pattern by using [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider), including information about properties and methods.</span></span> <span data-ttu-id="45cd5-116">**拖曳** 控制項模式用來支援可拖曳的控制項，或具有可拖曳專案的控制項。</span><span class="sxs-lookup"><span data-stu-id="45cd5-116">The **Drag** control pattern is used to support draggable controls, or controls with draggable items.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="45cd5-117">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="45cd5-117">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="45cd5-118">當您執行 **拖曳** 控制項模式時，請使用下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="45cd5-118">When implementing the **Drag** control pattern, use these guidelines and conventions:</span></span>

-   <span data-ttu-id="45cd5-119">[**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider)介面支援兩種不同的拖曳樣式：來源/目標樣式，以及僅限來源的樣式。</span><span class="sxs-lookup"><span data-stu-id="45cd5-119">The [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) interface supports two different dragging styles: the source/target style, and the source-only style.</span></span> <span data-ttu-id="45cd5-120">您必須選擇最適合拖放案例的樣式：</span><span class="sxs-lookup"><span data-stu-id="45cd5-120">You need to choose the style that works best for your drag-and-drop scenarios:</span></span>
    -   <span data-ttu-id="45cd5-121">**來源/目標樣式：** 每個可能的放置目標都是以實 [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) 介面的元素來表示。</span><span class="sxs-lookup"><span data-stu-id="45cd5-121">**Source/target style:** Each possible drop target is represented by an element that implements the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span> <span data-ttu-id="45cd5-122">在拖曳作業期間，Microsoft 消費者介面自動化的事件是來自正在拖曳的元素，以及從放置目標元素。</span><span class="sxs-lookup"><span data-stu-id="45cd5-122">During a drag operation, Microsoft UI Automation events originate from the element that is being dragged, and from the drop-target elements.</span></span>
    -   <span data-ttu-id="45cd5-123">**僅限來源樣式：** 卸載目標不會以消費者介面自動化元素表示。</span><span class="sxs-lookup"><span data-stu-id="45cd5-123">**Source-only style:** Drop targets are not represented by UI Automation elements.</span></span> <span data-ttu-id="45cd5-124">在拖曳作業期間，事件只源自于正在拖曳的元素。</span><span class="sxs-lookup"><span data-stu-id="45cd5-124">During a drag operation, events originate only from the element that is being dragged.</span></span>
-   <span data-ttu-id="45cd5-125">[**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) 是唯讀介面，適用于監視拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="45cd5-125">[**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) is a read-only interface intended for monitoring drag operations.</span></span> <span data-ttu-id="45cd5-126">您無法使用它來控制拖曳作業。</span><span class="sxs-lookup"><span data-stu-id="45cd5-126">You cannot use it to control a drag operation.</span></span> <span data-ttu-id="45cd5-127">您可以藉由將滑鼠輸入傳送至控制項，將拖曳作業自動化。</span><span class="sxs-lookup"><span data-stu-id="45cd5-127">You can automate drag operations by sending mouse input to a control.</span></span>
-   <span data-ttu-id="45cd5-128">需要 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性。</span><span class="sxs-lookup"><span data-stu-id="45cd5-128">The [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property is required.</span></span>
-   <span data-ttu-id="45cd5-129">[**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)和 [**IDragProvider：:D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)屬性是僅限來源樣式的實作為必要屬性，且禁止來源/目標樣式的執行。</span><span class="sxs-lookup"><span data-stu-id="45cd5-129">The [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) and [**IDragProvider::DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) properties are required for a source-only style implementation, and prohibited for a source/target style implementation.</span></span> <span data-ttu-id="45cd5-130">在來源/目標樣式的執行中，可以查詢放置目標元素的卸載效果。</span><span class="sxs-lookup"><span data-stu-id="45cd5-130">In a source/target style implementation, drop-target elements can be queried for their drop effects.</span></span>
-   <span data-ttu-id="45cd5-131">[**IDragProvider：： GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)屬性工作表示拖曳多個專案。</span><span class="sxs-lookup"><span data-stu-id="45cd5-131">The [**IDragProvider::GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) property represents the dragging of multiple items.</span></span> <span data-ttu-id="45cd5-132">當使用者開始拖曳作業時，您必須建立新的消費者介面自動化專案，做為事件來源元素。</span><span class="sxs-lookup"><span data-stu-id="45cd5-132">When the user begins the drag operation, you need to create a new UI Automation element to serve as the event source element.</span></span> <span data-ttu-id="45cd5-133">這個新的元素會引發來源專案在來源/目標或僅限來源模式下引發的所有事件，但實際上不會拖曳的元素會引發任何事件。</span><span class="sxs-lookup"><span data-stu-id="45cd5-133">This new element fires all events that the source element would have fired in either the source/target or source-only mode, while none of the elements that are actually being dragged fire any events.</span></span> <span data-ttu-id="45cd5-134">當拖曳作業完成時，摧毀事件來源元素。</span><span class="sxs-lookup"><span data-stu-id="45cd5-134">When the drag operation is complete, destroy the event source element.</span></span>
-   <span data-ttu-id="45cd5-135">專案必須在變更時，引發 **DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) 和 **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) 屬性的屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="45cd5-135">The element must fire property-changed events for the **DropEffect** ([**UIA\_DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropEffects** ([**UIA\_DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span> <span data-ttu-id="45cd5-136">其他屬性的屬性變更事件是允許的，但可以從必要的 **DragStart** 中推斷 ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 、 **DragCancel** ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) ，以及 **DragComplete** ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。</span><span class="sxs-lookup"><span data-stu-id="45cd5-136">Property-changed events for the other properties are allowed, but can be inferred from the required **DragStart** ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)), **DragCancel** ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)), and **DragComplete** ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) events.</span></span>
-   

## <a name="required-members-for-idragprovider"></a><span data-ttu-id="45cd5-137">**IDragProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="45cd5-137">Required Members for **IDragProvider**</span></span>

<span data-ttu-id="45cd5-138">執行 [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="45cd5-138">The following properties and methods are required for implementing the [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) interface.</span></span>



| <span data-ttu-id="45cd5-139">必要成員</span><span class="sxs-lookup"><span data-stu-id="45cd5-139">Required members</span></span>                                                                        | <span data-ttu-id="45cd5-140">成員類型</span><span class="sxs-lookup"><span data-stu-id="45cd5-140">Member type</span></span> | <span data-ttu-id="45cd5-141">備註</span><span class="sxs-lookup"><span data-stu-id="45cd5-141">Notes</span></span>                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="45cd5-142">**IsGrabbed**</span><span class="sxs-lookup"><span data-stu-id="45cd5-142">**IsGrabbed**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | <span data-ttu-id="45cd5-143">屬性</span><span class="sxs-lookup"><span data-stu-id="45cd5-143">Property</span></span>    | <span data-ttu-id="45cd5-144">無</span><span class="sxs-lookup"><span data-stu-id="45cd5-144">None</span></span>                                                                          |
| [<span data-ttu-id="45cd5-145">**DropEffect**</span><span class="sxs-lookup"><span data-stu-id="45cd5-145">**DropEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | <span data-ttu-id="45cd5-146">屬性</span><span class="sxs-lookup"><span data-stu-id="45cd5-146">Property</span></span>    | <span data-ttu-id="45cd5-147">僅限來源樣式的執行所需。</span><span class="sxs-lookup"><span data-stu-id="45cd5-147">Required for an implementation of the source-only style.</span></span>                      |
| [<span data-ttu-id="45cd5-148">**DropEffects**</span><span class="sxs-lookup"><span data-stu-id="45cd5-148">**DropEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | <span data-ttu-id="45cd5-149">屬性</span><span class="sxs-lookup"><span data-stu-id="45cd5-149">Property</span></span>    | <span data-ttu-id="45cd5-150">如果抓取專案有一個以上可能的卸載效果，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="45cd5-150">Required if there is more than one possible drop effect for the grabbed item.</span></span> |
| [<span data-ttu-id="45cd5-151">**GetGrabbedItems**</span><span class="sxs-lookup"><span data-stu-id="45cd5-151">**GetGrabbedItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | <span data-ttu-id="45cd5-152">方法</span><span class="sxs-lookup"><span data-stu-id="45cd5-152">Method</span></span>      | <span data-ttu-id="45cd5-153">多重專案拖曳作業的必要專案。</span><span class="sxs-lookup"><span data-stu-id="45cd5-153">Required for a multiple-item drag operation.</span></span>                                  |
| [<span data-ttu-id="45cd5-154">**UIA \_ 拖曳 \_ DragStartEventId**</span><span class="sxs-lookup"><span data-stu-id="45cd5-154">**UIA\_Drag\_DragStartEventId**</span></span>](uiauto-event-ids.md)       | <span data-ttu-id="45cd5-155">事件</span><span class="sxs-lookup"><span data-stu-id="45cd5-155">Event</span></span>       | <span data-ttu-id="45cd5-156">無</span><span class="sxs-lookup"><span data-stu-id="45cd5-156">None</span></span>                                                                          |
| [<span data-ttu-id="45cd5-157">**UIA \_ 拖曳 \_ DragCancelEventId**</span><span class="sxs-lookup"><span data-stu-id="45cd5-157">**UIA\_Drag\_DragCancelEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="45cd5-158">事件</span><span class="sxs-lookup"><span data-stu-id="45cd5-158">Event</span></span>       | <span data-ttu-id="45cd5-159">無</span><span class="sxs-lookup"><span data-stu-id="45cd5-159">None</span></span>                                                                          |
| [<span data-ttu-id="45cd5-160">**UIA \_ 拖曳 \_ DragCompleteEventId**</span><span class="sxs-lookup"><span data-stu-id="45cd5-160">**UIA\_Drag\_DragCompleteEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="45cd5-161">事件</span><span class="sxs-lookup"><span data-stu-id="45cd5-161">Event</span></span>       | <span data-ttu-id="45cd5-162">無</span><span class="sxs-lookup"><span data-stu-id="45cd5-162">None</span></span>                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="45cd5-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="45cd5-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45cd5-164">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="45cd5-164">Control Types and their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="45cd5-165">DropTarget 控制項模式</span><span class="sxs-lookup"><span data-stu-id="45cd5-165">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[<span data-ttu-id="45cd5-166">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="45cd5-166">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="45cd5-167">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="45cd5-167">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="45cd5-168">消費者介面自動化的拖放支援</span><span class="sxs-lookup"><span data-stu-id="45cd5-168">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 