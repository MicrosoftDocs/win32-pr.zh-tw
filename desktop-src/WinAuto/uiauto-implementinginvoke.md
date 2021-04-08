---
title: Invoke 控制項模式
description: 描述執行 IInvokeProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- 消費者介面自動化，執行調用控制項模式
- 消費者介面自動化，叫用控制項模式
- 消費者介面自動化、IInvokeProvider
- IInvokeProvider
- 執行消費者介面自動化叫用控制項模式
- 叫用控制項模式
- 控制項模式，IInvokeProvider
- 控制項模式，執行消費者介面自動化叫用
- 控制項模式，Invoke
- 介面，IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839807"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="e57b2-113">Invoke 控制項模式</span><span class="sxs-lookup"><span data-stu-id="e57b2-113">Invoke Control Pattern</span></span>

<span data-ttu-id="e57b2-114">描述執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e57b2-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="e57b2-115">叫 **用控制項模式** 是用來支援在啟用時不會維持狀態的控制項，而是會起始或執行單一明確的動作。</span><span class="sxs-lookup"><span data-stu-id="e57b2-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="e57b2-116">維護狀態的控制項（例如核取方塊和選項按鈕）必須改為分別執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) 和 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) 。</span><span class="sxs-lookup"><span data-stu-id="e57b2-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="e57b2-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="e57b2-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="e57b2-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="e57b2-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e57b2-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e57b2-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="e57b2-120">**IInvokeProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e57b2-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="e57b2-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e57b2-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="e57b2-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="e57b2-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="e57b2-123">在實作為 **Invoke** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="e57b2-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="e57b2-124">如果不是透過另一個控制項模式提供者來公開相同的行為，則控制項會執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 。</span><span class="sxs-lookup"><span data-stu-id="e57b2-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="e57b2-125">例如，如果控制項的 [**IUIAutomationInvokePattern：： Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) 方法執行的動作與 [**IUIAutomationExpandCollapsePattern：： Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) 或 [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) 方法相同，則控制項不應執行 **IInvokeProvider**。</span><span class="sxs-lookup"><span data-stu-id="e57b2-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="e57b2-126">通常按一下、按兩下或按 ENTER、使用預先定義的鍵盤快速鍵，或其他按鈕組合，就可以叫用控制項。</span><span class="sxs-lookup"><span data-stu-id="e57b2-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="e57b2-127">叫用 **的事件 (** UIA 叫用 [**\_ \_ InvokedEventId**](uiauto-event-ids.md)) 事件會在已啟動的控制項上引發，而控制項已啟用 (做為回應，以執行其相關聯的動作) 。</span><span class="sxs-lookup"><span data-stu-id="e57b2-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="e57b2-128">在可能的情況下，應該是在控制項完成該動作並返回，且沒有發生封鎖時才會引發該事件。</span><span class="sxs-lookup"><span data-stu-id="e57b2-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="e57b2-129">在下列情況 **下，必須** 先引發叫用的事件 (UIA 叫用 **\_ \_ InvokedEventId**) ，才能在下列案例中提供 **Invoke** 要求：</span><span class="sxs-lookup"><span data-stu-id="e57b2-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="e57b2-130">無法或不適合等待至動作完成。</span><span class="sxs-lookup"><span data-stu-id="e57b2-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="e57b2-131">動作需要使用者互動。</span><span class="sxs-lookup"><span data-stu-id="e57b2-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="e57b2-132">動作費時，且會導致發出呼叫的用戶端長時間凍結。</span><span class="sxs-lookup"><span data-stu-id="e57b2-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="e57b2-133">如果叫用控制項有顯著的副作用，則應該透過 **HelpText** 屬性來公開這些副作用。</span><span class="sxs-lookup"><span data-stu-id="e57b2-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="e57b2-134">例如，即使 [**IUIAutomationInvokePattern：： invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) 未與選取專案相關聯， **invoke** 仍可能造成另一個控制項被選取。</span><span class="sxs-lookup"><span data-stu-id="e57b2-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="e57b2-135">停留 (或滑鼠停留) 效果通常不會構成叫用 **的事件。**</span><span class="sxs-lookup"><span data-stu-id="e57b2-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="e57b2-136">不過，執行動作 (而不是造成視覺效果) 以停留狀態為基礎的控制項，應該支援叫用 **控制項模式** 。</span><span class="sxs-lookup"><span data-stu-id="e57b2-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="e57b2-137">如果控制項的叫用是與滑鼠相關的副作用所造成的，便會將這個實作視為協助工具問題。</span><span class="sxs-lookup"><span data-stu-id="e57b2-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="e57b2-138">叫用控制項和選擇項目不同。</span><span class="sxs-lookup"><span data-stu-id="e57b2-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="e57b2-139">但是，依據控制項而定，叫用某些控制項可能會有造成此項目受到選取的副作用。</span><span class="sxs-lookup"><span data-stu-id="e57b2-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="e57b2-140">例如，在 [我的檔] 資料夾中叫用 Microsoft Word 檔案清單專案時，會選取該專案並開啟檔。</span><span class="sxs-lookup"><span data-stu-id="e57b2-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="e57b2-141">元素可能會在叫用時立即從 Microsoft 消費者介面自動化樹狀結構中消失。</span><span class="sxs-lookup"><span data-stu-id="e57b2-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="e57b2-142">要求事件回呼所提供的項目資訊，可能會因此而失敗。</span><span class="sxs-lookup"><span data-stu-id="e57b2-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="e57b2-143">建議的解決方法是預先擷取快取的資訊。</span><span class="sxs-lookup"><span data-stu-id="e57b2-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="e57b2-144">控制項可以實作多個控制項模式。</span><span class="sxs-lookup"><span data-stu-id="e57b2-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="e57b2-145">例如，Microsoft Excel 工具列上的 [ **填滿色彩** ] 控制項可同時實作為 Invoke 和 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="e57b2-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="e57b2-146">ExpandCollapse 控制項模式會公開功能表 **，而叫用控制項模式** 會以選擇的色彩填滿現用選取範圍。</span><span class="sxs-lookup"><span data-stu-id="e57b2-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="e57b2-147">**IInvokeProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="e57b2-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="e57b2-148">以下是執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="e57b2-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="e57b2-149">必要成員</span><span class="sxs-lookup"><span data-stu-id="e57b2-149">Required members</span></span>                                | <span data-ttu-id="e57b2-150">成員類型</span><span class="sxs-lookup"><span data-stu-id="e57b2-150">Member type</span></span> | <span data-ttu-id="e57b2-151">備註</span><span class="sxs-lookup"><span data-stu-id="e57b2-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e57b2-152">**調用**</span><span class="sxs-lookup"><span data-stu-id="e57b2-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="e57b2-153">方法</span><span class="sxs-lookup"><span data-stu-id="e57b2-153">Method</span></span>      | <span data-ttu-id="e57b2-154">**Invoke** 是非同步呼叫，必須在不封鎖的情況下立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e57b2-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="e57b2-155">對於叫用時直接或間接啟動強制回應對話方塊的控制項，此行為尤其重要。</span><span class="sxs-lookup"><span data-stu-id="e57b2-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="e57b2-156">任何引發事件的使用者介面自動化用戶端都會維持封鎖的狀態，直到強制回應對話方塊關閉為止。</span><span class="sxs-lookup"><span data-stu-id="e57b2-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="e57b2-157">此控制項模式沒有任何相關聯的屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="e57b2-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e57b2-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="e57b2-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e57b2-159">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="e57b2-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="e57b2-160">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="e57b2-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="e57b2-161">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="e57b2-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="e57b2-162">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="e57b2-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





