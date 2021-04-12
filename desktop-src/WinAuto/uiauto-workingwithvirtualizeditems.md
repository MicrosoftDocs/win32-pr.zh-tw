---
title: 使用虛擬化專案
description: 本主題說明如何使用 >itemcontainer 和 VirtualizedItem 控制項模式所提供的功能，來尋找和取得虛擬化專案的相關資訊。
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- 用戶端，消費者介面自動化虛擬化專案
- 用戶端，虛擬化專案
- 用戶端、控制項模式
- 用戶端，VirtualizedItem 控制項模式
- 用戶端，>itemcontainer 控制項模式
- 用戶端，消費者介面自動化 VirtualizedItem 控制項模式
- 用戶端，消費者介面自動化控制模式
- 用戶端，消費者介面自動化 >itemcontainer 控制項模式
- 消費者介面自動化，虛擬化專案
- 消費者介面自動化，控制項模式
- 消費者介面自動化，VirtualizedItem 控制項模式
- 消費者介面自動化，>itemcontainer 控制項模式
- VirtualizedItem 控制項模式
- '>itemcontainer 控制項模式'
- 控制項模式，VirtualizedItem
- 控制項模式，>itemcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301580"
---
# <a name="working-with-virtualized-items"></a><span data-ttu-id="ad11f-119">使用虛擬化專案</span><span class="sxs-lookup"><span data-stu-id="ad11f-119">Working with Virtualized Items</span></span>

<span data-ttu-id="ad11f-120">本主題說明如何使用 [>itemcontainer](uiauto-implementingitemcontainer.md) 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式所提供的功能，來尋找和取得虛擬化專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad11f-120">This topic describes how to use functionality provided by the [ItemContainer](uiauto-implementingitemcontainer.md) and [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control patterns to find and retrieve information about virtualized items.</span></span>

-   [<span data-ttu-id="ad11f-121">虛擬化總覽</span><span class="sxs-lookup"><span data-stu-id="ad11f-121">Overview of Virtualization</span></span>](#overview-of-virtualization)
-   [<span data-ttu-id="ad11f-122">控制項如何支援虛擬化</span><span class="sxs-lookup"><span data-stu-id="ad11f-122">How a Control Supports Virtualization</span></span>](#how-a-control-supports-virtualization)
-   [<span data-ttu-id="ad11f-123">用戶端如何尋找和實現虛擬化專案</span><span class="sxs-lookup"><span data-stu-id="ad11f-123">How Clients Find and Realize Virtualized Items</span></span>](#how-clients-find-and-realize-virtualized-items)
-   [<span data-ttu-id="ad11f-124">範例</span><span class="sxs-lookup"><span data-stu-id="ad11f-124">Example</span></span>](#example)
-   [<span data-ttu-id="ad11f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad11f-125">Related topics</span></span>](#related-topics)

## <a name="overview-of-virtualization"></a><span data-ttu-id="ad11f-126">虛擬化總覽</span><span class="sxs-lookup"><span data-stu-id="ad11f-126">Overview of Virtualization</span></span>

<span data-ttu-id="ad11f-127">包含大量子專案的控制項可以使用虛擬化來有效率地管理專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-127">Controls that contain a large number of child items can use virtualization to efficiently manage the items.</span></span> <span data-ttu-id="ad11f-128">利用虛擬化，控制項在任何指定時間只會在記憶體中維護完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad11f-128">With virtualization, the control maintains full information in memory for only a subset of items at any given time.</span></span> <span data-ttu-id="ad11f-129">通常，子集只會包含使用者目前可見的專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-129">Typically, the subset includes only those items that are currently visible to the user.</span></span> <span data-ttu-id="ad11f-130">其餘虛擬化專案的完整資訊會保存在儲存體中，並載入記憶體中或已實現（例如，當使用者可以看到新專案時）。</span><span class="sxs-lookup"><span data-stu-id="ad11f-130">Full information about the remaining virtualized items is kept in storage and is loaded into memory, or realized, as the control needs it, for example, as new items become visible to the user.</span></span>

<span data-ttu-id="ad11f-131">使用虛擬化的控制項代表一項挑戰，因為只有在消費者介面自動化樹狀目錄中，以 Microsoft 消費者介面自動化專案的形式來提供正式的專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-131">Controls that use virtualization represent a challenge because only realized items are fully available as Microsoft UI Automation elements in the UI Automation tree.</span></span> <span data-ttu-id="ad11f-132">虛擬化專案不存在於樹狀結構中，因此用戶端無法使用這些專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad11f-132">Virtualized items do not exist in the tree, so information about them is not available to clients.</span></span> <span data-ttu-id="ad11f-133">為了抓取虛擬化專案的相關資訊，用戶端需要一種方式來強制消費者介面自動化傳遞要求，以實現控制項的專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-133">To retrieve information about virtualized items, clients need a way to force UI Automation to pass the request to realize the items to the control.</span></span> <span data-ttu-id="ad11f-134">在瞭解專案之後，消費者介面自動化可以為它們建立消費者介面自動化元素。</span><span class="sxs-lookup"><span data-stu-id="ad11f-134">After the items have been realized, UI Automation can create UI Automation elements for them.</span></span> <span data-ttu-id="ad11f-135">消費者介面自動化包含兩種可讓用戶端使用虛擬化專案的控制項模式： [>itemcontainer](uiauto-implementingitemcontainer.md) 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md)。</span><span class="sxs-lookup"><span data-stu-id="ad11f-135">UI Automation includes two control patterns to enable clients to work with virtualized items: [ItemContainer](uiauto-implementingitemcontainer.md) and [VirtualizedItem](uiauto-implementingvirtualizeditem.md).</span></span>

## <a name="how-a-control-supports-virtualization"></a><span data-ttu-id="ad11f-136">控制項如何支援虛擬化</span><span class="sxs-lookup"><span data-stu-id="ad11f-136">How a Control Supports Virtualization</span></span>

<span data-ttu-id="ad11f-137">任何可以包含虛擬化專案的控制項都必須支援 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ad11f-137">Any control that can contain virtualized items must support the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern.</span></span> <span data-ttu-id="ad11f-138">此外，任何可以虛擬化的專案都必須支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ad11f-138">Further, any item that can be virtualized must support the [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control pattern.</span></span> <span data-ttu-id="ad11f-139">>itemcontainer 和 VirtualizedItem 控制項模式所公開的功能，可透過 [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) 和 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面供用戶端存取。</span><span class="sxs-lookup"><span data-stu-id="ad11f-139">The functionality that is exposed by the ItemContainer and VirtualizedItem control patterns is accessible to clients through the [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) and [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) interfaces.</span></span>

## <a name="how-clients-find-and-realize-virtualized-items"></a><span data-ttu-id="ad11f-140">用戶端如何尋找和實現虛擬化專案</span><span class="sxs-lookup"><span data-stu-id="ad11f-140">How Clients Find and Realize Virtualized Items</span></span>

<span data-ttu-id="ad11f-141">用戶端可以使用 [**IUIAutomationItemContainerPattern：： FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) 方法，根據特定屬性的值來搜尋容器中的子專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-141">Clients can use the [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) method to search for child items in the container based on the value of a particular property.</span></span> <span data-ttu-id="ad11f-142">方法也可以取出容器中的第一個專案，或在指定專案之後的專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-142">The method can also retrieve the first item in the container or the item that follows the specified item.</span></span> <span data-ttu-id="ad11f-143">如果找到相符的子專案， **FindItemByProperty** 會抓取專案的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面。</span><span class="sxs-lookup"><span data-stu-id="ad11f-143">If a matching child item is found, the **FindItemByProperty** retrieves an [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the item.</span></span> <span data-ttu-id="ad11f-144">但是，如果子專案已虛擬化，則 **IUIAutomationElement** 介面是預留位置。</span><span class="sxs-lookup"><span data-stu-id="ad11f-144">However, if the child item is virtualized, the **IUIAutomationElement** interface is a placeholder.</span></span> <span data-ttu-id="ad11f-145">當用戶端嘗試使用 **IUIAutomationElement** 介面來取出屬性值或呼叫尚未提供的方法時，就會發生 [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md)錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad11f-145">The [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) error occurs when the client attempts to use the **IUIAutomationElement** interface to retrieve property values or call methods that are not yet available.</span></span> <span data-ttu-id="ad11f-146">您可以透過預留位置取得哪些屬性或方法，取決於控制項的執行。</span><span class="sxs-lookup"><span data-stu-id="ad11f-146">Which properties or methods are available through a placeholder depends on the control implementation.</span></span> <span data-ttu-id="ad11f-147">預留位置的唯一需求是支援 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面。</span><span class="sxs-lookup"><span data-stu-id="ad11f-147">The only requirement for a placeholder is to support the [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) interface.</span></span>

<span data-ttu-id="ad11f-148">[**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md)錯誤是指用戶端可能會虛擬化專案的指示。</span><span class="sxs-lookup"><span data-stu-id="ad11f-148">The [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) error is an indication to the client that an item may be virtualized.</span></span> <span data-ttu-id="ad11f-149">用戶端應藉由取得專案的 [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) 介面來回應，然後藉由呼叫 [**IUIAutomationVirtualizedItemPattern：：認識**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) 方法來實現專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-149">The client should respond by retrieving the [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) interface for the item, and then realizing the item by calling the [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) method.</span></span> <span data-ttu-id="ad11f-150">如果成功，則 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面可完全正常運作，並提供所有適當的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad11f-150">If this succeeds, the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface is fully functional with all appropriate properties available.</span></span>

<span data-ttu-id="ad11f-151">視控制項的執行而定，呼叫 [**IUIAutomationVirtualizedItemPattern：：意識**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) 可能會導致控制項將專案滾動到視圖中。</span><span class="sxs-lookup"><span data-stu-id="ad11f-151">Depending on the control implementation, calling [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) may cause the control to scroll the item into view.</span></span> <span data-ttu-id="ad11f-152">不過，用戶端不應該依賴專案滾動或變成可見的專案。</span><span class="sxs-lookup"><span data-stu-id="ad11f-152">However, a client should not rely on the item scrolling into view or made visible.</span></span> <span data-ttu-id="ad11f-153">為了確保可以看見專案，用戶端可以使用 [**IUIAutomationScrollItemPattern：： ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) 方法。</span><span class="sxs-lookup"><span data-stu-id="ad11f-153">To ensure that the item is visible, the client can use the [**IUIAutomationScrollItemPattern::ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) method.</span></span>

## <a name="example"></a><span data-ttu-id="ad11f-154">範例</span><span class="sxs-lookup"><span data-stu-id="ad11f-154">Example</span></span>

<span data-ttu-id="ad11f-155">如需示範如何使用消費者介面自動化的虛擬化支援的程式碼範例，請參閱 [如何取出虛擬化專案](uiauto-howto-retrieve-virtualized-item.md)。</span><span class="sxs-lookup"><span data-stu-id="ad11f-155">For example code that shows how to use the UI Automation support for virtualization, see [How to Retrieve a Virtualized Item](uiauto-howto-retrieve-virtualized-item.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad11f-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad11f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad11f-157">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="ad11f-157">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




