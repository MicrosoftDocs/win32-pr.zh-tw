---
title: SelectionItem 控制項模式
description: 描述執行 ISelectionItemProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- 消費者介面自動化，執行 SelectionItem 控制項模式
- 消費者介面自動化，SelectionItem 控制項模式
- 消費者介面自動化、ISelectionItemProvider
- ISelectionItemProvider
- 執行消費者介面自動化 SelectionItem 控制項模式
- SelectionItem 控制項模式
- 控制項模式，ISelectionItemProvider
- 控制模式，消費者介面自動化執行 SelectionItem
- 控制項模式，SelectionItem
- 介面，ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966783"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="40ec9-113">SelectionItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="40ec9-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="40ec9-114">描述執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="40ec9-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="40ec9-115">**SelectionItem** 控制項模式用來支援控制項，這些控制項可作為執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)之容器控制項的個別可選取子專案。</span><span class="sxs-lookup"><span data-stu-id="40ec9-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="40ec9-116">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="40ec9-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="40ec9-117">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="40ec9-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="40ec9-118">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="40ec9-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="40ec9-119">**ISelectionItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="40ec9-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="40ec9-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="40ec9-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="40ec9-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="40ec9-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="40ec9-122">在執行 **SelectionItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="40ec9-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="40ec9-123">管理子控制項以執行 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)的單一選取控制項（例如 Windows 的 **顯示內容** 對話方塊中的 [**螢幕解析度**] 滑杆）應該會執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider);其子系應同時執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)和 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。</span><span class="sxs-lookup"><span data-stu-id="40ec9-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="40ec9-124">**ISelectionItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="40ec9-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="40ec9-125">執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) 介面需要下列屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="40ec9-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="40ec9-126">必要成員</span><span class="sxs-lookup"><span data-stu-id="40ec9-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="40ec9-127">成員類型</span><span class="sxs-lookup"><span data-stu-id="40ec9-127">Member type</span></span> | <span data-ttu-id="40ec9-128">備註</span><span class="sxs-lookup"><span data-stu-id="40ec9-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="40ec9-129">**AddToSelection**</span><span class="sxs-lookup"><span data-stu-id="40ec9-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="40ec9-130">方法</span><span class="sxs-lookup"><span data-stu-id="40ec9-130">Method</span></span>      | <span data-ttu-id="40ec9-131">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-131">None</span></span>  |
| [<span data-ttu-id="40ec9-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="40ec9-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="40ec9-133">屬性</span><span class="sxs-lookup"><span data-stu-id="40ec9-133">Property</span></span>    | <span data-ttu-id="40ec9-134">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-134">None</span></span>  |
| [<span data-ttu-id="40ec9-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="40ec9-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="40ec9-136">方法</span><span class="sxs-lookup"><span data-stu-id="40ec9-136">Method</span></span>      | <span data-ttu-id="40ec9-137">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-137">None</span></span>  |
| [<span data-ttu-id="40ec9-138">**選擇**</span><span class="sxs-lookup"><span data-stu-id="40ec9-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="40ec9-139">方法</span><span class="sxs-lookup"><span data-stu-id="40ec9-139">Method</span></span>      | <span data-ttu-id="40ec9-140">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-140">None</span></span>  |
| [<span data-ttu-id="40ec9-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="40ec9-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="40ec9-142">屬性</span><span class="sxs-lookup"><span data-stu-id="40ec9-142">Property</span></span>    | <span data-ttu-id="40ec9-143">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-143">None</span></span>  |
| [<span data-ttu-id="40ec9-144">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="40ec9-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="40ec9-145">事件</span><span class="sxs-lookup"><span data-stu-id="40ec9-145">Event</span></span>       | <span data-ttu-id="40ec9-146">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-146">None</span></span>  |
| [<span data-ttu-id="40ec9-147">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="40ec9-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="40ec9-148">事件</span><span class="sxs-lookup"><span data-stu-id="40ec9-148">Event</span></span>       | <span data-ttu-id="40ec9-149">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-149">None</span></span>  |
| [<span data-ttu-id="40ec9-150">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="40ec9-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="40ec9-151">事件</span><span class="sxs-lookup"><span data-stu-id="40ec9-151">Event</span></span>       | <span data-ttu-id="40ec9-152">無</span><span class="sxs-lookup"><span data-stu-id="40ec9-152">None</span></span>  |



 

<span data-ttu-id="40ec9-153">如果 [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)、 [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)或 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection)的結果是單一選取的專案，則應引發 **ElementSelected** 事件 ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) ; 否則，請將 **ElementAddedToSelection** (UIA SelectionItem ElementAddedToSelectionEventId) 或 **ElementRemovedFromSelection** (UIA SelectionItem ElementRemovedFromSelectionEventId) 事件適當。 [**\_ \_**](uiauto-event-ids.md) [**\_ \_**](uiauto-event-ids.md)</span><span class="sxs-lookup"><span data-stu-id="40ec9-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40ec9-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="40ec9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ec9-155">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="40ec9-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="40ec9-156">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="40ec9-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="40ec9-157">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="40ec9-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




