---
title: DropTarget 控制項模式
description: 提供使用 IDropTargetProvider 來執行 DropTarget 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- 消費者介面自動化，執行 DropTarget 控制項模式
- 消費者介面自動化，DropTarget 控制項模式
- 消費者介面自動化、IDropTargetProvider
- IDropTargetProvider
- 執行消費者介面自動化 DropTarget 控制項模式
- DropTarget 控制項模式
- 控制項模式，IDropTargetProvider
- 控制模式，消費者介面自動化執行 DropTarget
- 控制項模式，DropTarget
- 介面，IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315670"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="4627a-113">DropTarget 控制項模式</span><span class="sxs-lookup"><span data-stu-id="4627a-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="4627a-114">提供使用 [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)來執行 **DropTarget** 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4627a-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="4627a-115">**DropTarget** 控制項模式是用來支援可作為拖放作業目標的控制項。</span><span class="sxs-lookup"><span data-stu-id="4627a-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="4627a-116">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="4627a-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="4627a-117">在執行 **DropTarget** 控制項模式時，請使用下列指導方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="4627a-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="4627a-118">當拖曳作業正在進行時，必須支援 **DropTarget** 模式。</span><span class="sxs-lookup"><span data-stu-id="4627a-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="4627a-119">即使未進行拖曳作業，也可以支援此功能。</span><span class="sxs-lookup"><span data-stu-id="4627a-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="4627a-120">[**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)屬性為必要項。</span><span class="sxs-lookup"><span data-stu-id="4627a-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="4627a-121">當目標有一個以上可能的卸載效果時，需要 [**IDropTargetProvider：:D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4627a-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="4627a-122">專案變更時，專案必須引發 **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) 和 **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) 屬性的屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4627a-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="4627a-123">**IDropTargetProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="4627a-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="4627a-124">執行 [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="4627a-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="4627a-125">必要成員</span><span class="sxs-lookup"><span data-stu-id="4627a-125">Required members</span></span>                                                                              | <span data-ttu-id="4627a-126">成員類型</span><span class="sxs-lookup"><span data-stu-id="4627a-126">Member type</span></span> | <span data-ttu-id="4627a-127">備註</span><span class="sxs-lookup"><span data-stu-id="4627a-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4627a-128">**DropTargetEffect**</span><span class="sxs-lookup"><span data-stu-id="4627a-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="4627a-129">屬性</span><span class="sxs-lookup"><span data-stu-id="4627a-129">Property</span></span>    | <span data-ttu-id="4627a-130">無</span><span class="sxs-lookup"><span data-stu-id="4627a-130">None</span></span>                                                                     |
| [<span data-ttu-id="4627a-131">**DropTargetEffects**</span><span class="sxs-lookup"><span data-stu-id="4627a-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="4627a-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4627a-132">Property</span></span>    | <span data-ttu-id="4627a-133">如果放置目標支援多個可能的卸載效果，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="4627a-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="4627a-134">**UIA \_ DropTarget \_ DragEnterEventId**</span><span class="sxs-lookup"><span data-stu-id="4627a-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="4627a-135">事件</span><span class="sxs-lookup"><span data-stu-id="4627a-135">Event</span></span>       | <span data-ttu-id="4627a-136">無</span><span class="sxs-lookup"><span data-stu-id="4627a-136">None</span></span>                                                                     |
| [<span data-ttu-id="4627a-137">**UIA \_ DropTarget \_ DragLeaveEventId**</span><span class="sxs-lookup"><span data-stu-id="4627a-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="4627a-138">事件</span><span class="sxs-lookup"><span data-stu-id="4627a-138">Event</span></span>       | <span data-ttu-id="4627a-139">無</span><span class="sxs-lookup"><span data-stu-id="4627a-139">None</span></span>                                                                     |
| [<span data-ttu-id="4627a-140">**UIA \_ DropTarget \_ DroppedEventId**</span><span class="sxs-lookup"><span data-stu-id="4627a-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="4627a-141">事件</span><span class="sxs-lookup"><span data-stu-id="4627a-141">Event</span></span>       | <span data-ttu-id="4627a-142">無</span><span class="sxs-lookup"><span data-stu-id="4627a-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="4627a-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="4627a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4627a-144">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4627a-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="4627a-145">拖曳控制項模式</span><span class="sxs-lookup"><span data-stu-id="4627a-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="4627a-146">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="4627a-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="4627a-147">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="4627a-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="4627a-148">消費者介面自動化的拖放支援</span><span class="sxs-lookup"><span data-stu-id="4627a-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 