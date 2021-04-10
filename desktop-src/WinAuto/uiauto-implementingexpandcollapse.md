---
title: ExpandCollapse 控制項模式
description: 描述執行 IExpandCollapseProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- 消費者介面自動化，執行 ExpandCollapse 控制項模式
- 消費者介面自動化，ExpandCollapse 控制項模式
- 消費者介面自動化、IExpandCollapseProvider
- IExpandCollapseProvider
- 執行消費者介面自動化 ExpandCollapse 控制項模式
- ExpandCollapse 控制項模式
- 控制項模式，IExpandCollapseProvider
- 控制模式，消費者介面自動化執行 ExpandCollapse
- 控制項模式，ExpandCollapse
- 介面，IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021212"
---
# <a name="expandcollapse-control-pattern"></a><span data-ttu-id="64402-113">ExpandCollapse 控制項模式</span><span class="sxs-lookup"><span data-stu-id="64402-113">ExpandCollapse Control Pattern</span></span>

<span data-ttu-id="64402-114">描述執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="64402-114">Describes guidelines and conventions for implementing [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="64402-115">**ExpandCollapse** 控制項模式是用來支援以視覺化方式展開以顯示更多內容和折迭以隱藏內容的控制項。</span><span class="sxs-lookup"><span data-stu-id="64402-115">The **ExpandCollapse** control pattern is used to support controls that visually expand to display more content and collapse to hide content.</span></span>

<span data-ttu-id="64402-116">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="64402-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="64402-117">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="64402-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="64402-118">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="64402-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="64402-119">**IExpandCollapseProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="64402-119">Required Members for **IExpandCollapseProvider**</span></span>](#required-members-for-iexpandcollapseprovider)
-   [<span data-ttu-id="64402-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="64402-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="64402-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="64402-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="64402-122">在執行 **ExpandCollapse** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="64402-122">When implementing the **ExpandCollapse** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="64402-123">匯總控制項（以提供 UI 擴充/折迭功能的子物件所建立）必須支援 **ExpandCollapse** 控制項模式，而其子項目則否。</span><span class="sxs-lookup"><span data-stu-id="64402-123">Aggregate controls, built with child objects that provide the UI with expand/collapse functionality, must support the **ExpandCollapse** control pattern whereas their child elements do not.</span></span> <span data-ttu-id="64402-124">例如，下拉式方塊控制項是使用清單方塊、按鈕和編輯控制項的組合所建立，但它只是必須支援 **ExpandCollapse** 控制項模式的父下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="64402-124">For example, a combo box control is built with a combination of list box, button, and edit controls, but it is only the parent combo box that must support the **ExpandCollapse** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="64402-125">例外狀況是功能表控制項，這是個別功能表項目物件的匯總。</span><span class="sxs-lookup"><span data-stu-id="64402-125">An exception is the menu control, which is an aggregate of individual menu item objects.</span></span> <span data-ttu-id="64402-126">功能表項目物件可以支援 **ExpandCollapse** 控制項模式，但是父功能表控制項則不能。</span><span class="sxs-lookup"><span data-stu-id="64402-126">The menu item objects can support the **ExpandCollapse** control pattern, but the parent menu control cannot.</span></span> <span data-ttu-id="64402-127">樹狀結構和樹狀目錄專案控制項會套用類似的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="64402-127">A similar exception applies to the tree and tree item controls.</span></span>

     

-   <span data-ttu-id="64402-128">當控制項的 [**IExpandCollapseProvider：： ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) 設定為 **ExpandCollapseState \_ LeafNode** 時，控制項的任何 **ExpandCollapse** 功能目前為非使用中狀態，而且可以使用此控制項模式取得的唯一資訊是 **ExpandCollapseState**。</span><span class="sxs-lookup"><span data-stu-id="64402-128">When the [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) of a control is set to **ExpandCollapseState\_LeafNode**, any **ExpandCollapse** functionality is currently inactive for the control and the only information that can be obtained using this control pattern is the **ExpandCollapseState**.</span></span> <span data-ttu-id="64402-129">如果後續新增任何子物件，則會啟用 **ExpandCollapseState** 變更和 **ExpandCollapse** 功能。</span><span class="sxs-lookup"><span data-stu-id="64402-129">If any child objects are subsequently added, the **ExpandCollapseState** changes and **ExpandCollapse** functionality is activated.</span></span>
-   <span data-ttu-id="64402-130">[**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) 只是指直屬子物件的可見度;它不會參考所有子系物件的可見度。</span><span class="sxs-lookup"><span data-stu-id="64402-130">[**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) refers to the visibility of immediate child objects only; it does not refer to the visibility of all descendant objects.</span></span>
-   <span data-ttu-id="64402-131">[**IExpandCollapseProvider：： Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) 和 [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) 功能是控制項特定的。</span><span class="sxs-lookup"><span data-stu-id="64402-131">[**IExpandCollapseProvider::Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) and [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) functionality is control-specific.</span></span> <span data-ttu-id="64402-132">以下是此行為的範例：</span><span class="sxs-lookup"><span data-stu-id="64402-132">The following are examples of this behavior.</span></span>
    -   <span data-ttu-id="64402-133">Office 個人功能表可以是三個狀態的功能表項目 ( 「展開」、「折迭」和「PartiallyExpanded」 ) 其中控制項指定在呼叫 [**展開**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)[**或折迭時要**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)採用的狀態。</span><span class="sxs-lookup"><span data-stu-id="64402-133">The Office Personal Menu can be a three-state menu item ("Expanded", "Collapsed" and "PartiallyExpanded") where the control specifies the state to adopt when [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) or [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) is called.</span></span>
    -   <span data-ttu-id="64402-134">在樹狀目錄專案上呼叫 [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) 可能會顯示所有子系或只顯示立即的子系。</span><span class="sxs-lookup"><span data-stu-id="64402-134">Calling [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) on a tree item may display all descendants or only immediate children.</span></span>
    -   <span data-ttu-id="64402-135">如果呼叫控制項的 [**展開**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)[**或折**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)迭維持其子系的狀態，則應該傳送可見度變更事件，而不是狀態變更事件。</span><span class="sxs-lookup"><span data-stu-id="64402-135">If calling [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) or [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) on a control maintains the state of its descendants, a visibility change event should be sent, not a state change event.</span></span> <span data-ttu-id="64402-136">如果父控制項在折迭時不維持其子系的狀態，控制項可能會損毀所有不再可見的子系，並引發終結的事件;或者，它可能會變更每個子代的 [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) ，並引發可見度變更事件。</span><span class="sxs-lookup"><span data-stu-id="64402-136">If the parent control does not maintain the state of its descendants when collapsed, the control may destroy all the descendants that are no longer visible and raise a destroyed event; or it may change the [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) for each descendant and raise a visibility change event.</span></span>
-   <span data-ttu-id="64402-137">為了保證導覽，在 Microsoft 消費者介面自動化樹狀結構 (中，不論其父系 [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)為何，都需要有適當的可見度狀態) 的物件。</span><span class="sxs-lookup"><span data-stu-id="64402-137">To guarantee navigation, it is desirable for an object to be in the Microsoft UI Automation tree (with appropriate visibility state) regardless of its parents [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate).</span></span> <span data-ttu-id="64402-138">如果子系是依需求產生的，則它們可能只會在第一次顯示時出現在消費者介面自動化樹狀結構中，或只在顯示時出現。</span><span class="sxs-lookup"><span data-stu-id="64402-138">If descendants are generated on demand, they may only appear in the UI Automation tree after being displayed for the first time or only while they are visible.</span></span>

## <a name="required-members-for-iexpandcollapseprovider"></a><span data-ttu-id="64402-139">**IExpandCollapseProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="64402-139">Required Members for **IExpandCollapseProvider**</span></span>

<span data-ttu-id="64402-140">執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) 介面需要下列屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="64402-140">The following properties, methods, and events are required for implementing the [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) interface.</span></span>



| <span data-ttu-id="64402-141">必要成員</span><span class="sxs-lookup"><span data-stu-id="64402-141">Required members</span></span>                                                                                    | <span data-ttu-id="64402-142">成員類型</span><span class="sxs-lookup"><span data-stu-id="64402-142">Member type</span></span> | <span data-ttu-id="64402-143">備註</span><span class="sxs-lookup"><span data-stu-id="64402-143">Notes</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [<span data-ttu-id="64402-144">**ExpandCollapseState**</span><span class="sxs-lookup"><span data-stu-id="64402-144">**ExpandCollapseState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | <span data-ttu-id="64402-145">屬性</span><span class="sxs-lookup"><span data-stu-id="64402-145">Property</span></span>    | <span data-ttu-id="64402-146">無</span><span class="sxs-lookup"><span data-stu-id="64402-146">None</span></span>                                                                   |
| [<span data-ttu-id="64402-147">**展開**</span><span class="sxs-lookup"><span data-stu-id="64402-147">**Expand**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | <span data-ttu-id="64402-148">方法</span><span class="sxs-lookup"><span data-stu-id="64402-148">Method</span></span>      | <span data-ttu-id="64402-149">無</span><span class="sxs-lookup"><span data-stu-id="64402-149">None</span></span>                                                                   |
| [<span data-ttu-id="64402-150">**摺疊**</span><span class="sxs-lookup"><span data-stu-id="64402-150">**Collapse**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | <span data-ttu-id="64402-151">方法</span><span class="sxs-lookup"><span data-stu-id="64402-151">Method</span></span>      | <span data-ttu-id="64402-152">無</span><span class="sxs-lookup"><span data-stu-id="64402-152">None</span></span>                                                                   |
| [<span data-ttu-id="64402-153">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="64402-153">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="64402-154">事件</span><span class="sxs-lookup"><span data-stu-id="64402-154">Event</span></span>       | <span data-ttu-id="64402-155">此控制項沒有相關聯的事件;使用這個一般事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="64402-155">This control has no associated events; use this generic event handler.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="64402-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="64402-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64402-157">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="64402-157">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="64402-158">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="64402-158">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="64402-159">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="64402-159">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




