---
title: '>itemcontainer 控制項模式'
description: 描述執行 IItemContainerProvider 的方針和慣例，包括方法的相關資訊。 >itemcontainer 控制項模式用來支援專案虛擬化。
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- 消費者介面自動化，執行 >itemcontainer 控制項模式
- 消費者介面自動化，>itemcontainer 控制項模式
- 消費者介面自動化、IItemContainerProvider
- IItemContainerProvider
- 執行消費者介面自動化 >itemcontainer 控制項模式
- '>itemcontainer 控制項模式'
- 控制項模式，IItemContainerProvider
- 控制模式，消費者介面自動化執行 >itemcontainer
- 控制項模式，>itemcontainer
- 介面，IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55246abde51e7053bf0c3266ccbe9c2b080b2fe7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672659"
---
# <a name="itemcontainer-control-pattern"></a><span data-ttu-id="0ba0a-114">>itemcontainer 控制項模式</span><span class="sxs-lookup"><span data-stu-id="0ba0a-114">ItemContainer Control Pattern</span></span>

<span data-ttu-id="0ba0a-115">描述執行 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-115">Describes guidelines and conventions for implementing [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider), including information about methods.</span></span> <span data-ttu-id="0ba0a-116">**>itemcontainer** 控制項模式用來支援專案虛擬化。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-116">The **ItemContainer** control pattern is used to support item virtualization.</span></span>

<span data-ttu-id="0ba0a-117">包含大量子專案的控制項可以使用虛擬化來有效率地管理專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-117">Controls that contain a large number of child items can use virtualization to efficiently manage the items.</span></span> <span data-ttu-id="0ba0a-118">利用虛擬化，控制項在任何指定時間只會在記憶體中維護完整的資訊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-118">With virtualization, the control maintains full information in memory for only a subset of items at any given time.</span></span> <span data-ttu-id="0ba0a-119">通常，子集只會包含使用者目前可見的專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-119">Typically, the subset includes only those items that are currently visible to the user.</span></span> <span data-ttu-id="0ba0a-120">其餘虛擬化專案的完整資訊會保存在儲存體中，並載入記憶體中或已實現（例如，當使用者可以看到新專案時）。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-120">Full information about the remaining virtualized items is kept in storage and is loaded into memory, or realized, as the control needs it, for example, as new items become visible to the user.</span></span>

<span data-ttu-id="0ba0a-121">例如，下圖顯示包含上千個虛擬化專案的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-121">For example, the following diagram shows a list box that contains thousands of virtualized items.</span></span> <span data-ttu-id="0ba0a-122">因為控制項只會針對目前可見的子專案維護完整的資訊，所以提供者只能針對 100-127 的專案公開 Microsoft 消費者介面自動化元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-122">Because the control maintains full information only for the child items that are currently visible, the provider can expose Microsoft UI Automation elements only for items 100—127.</span></span>

![顯示清單方塊中已虛擬化且未虛擬化專案的圖表](images/virtualizeditems.jpg)

<span data-ttu-id="0ba0a-124">使用虛擬化的控制項代表一項挑戰，因為只會在消費者介面自動化樹狀結構中，以消費者介面自動化元素的形式完全提供 (的已解除虛擬化) 專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-124">Controls that use virtualization represent a challenge because only realized (de-virtualized) items are fully available as UI Automation elements in the UI Automation tree.</span></span> <span data-ttu-id="0ba0a-125">虛擬化專案不存在於樹狀結構中，因此無法使用這些專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-125">Virtualized items do not exist in the tree, so information about them is not available.</span></span>

<span data-ttu-id="0ba0a-126">為了提供虛擬化專案的相關資訊，提供者會執行公開 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)介面的 **>itemcontainer** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-126">To provide information about virtualized items, providers implement the **ItemContainer** control pattern, which exposes the [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) interface.</span></span> <span data-ttu-id="0ba0a-127">[**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)方法會根據特定屬性的值（例如 **Name**、 **AutomationId** 或 **IsSelected**）來尋找子專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-127">The [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) method finds child items based on the value of a particular property, such as **Name**, **AutomationId**, or **IsSelected**.</span></span> <span data-ttu-id="0ba0a-128">如果專案已虛擬化， **FindItemByProperty** 會抓取專案的消費者介面自動化預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-128">If an item is virtualized, **FindItemByProperty** retrieves a UI Automation placeholder element for the item.</span></span> <span data-ttu-id="0ba0a-129">預留位置元素是 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面的實作為支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-129">A placeholder element is an implementation of the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface that supports only the [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control pattern.</span></span>

<span data-ttu-id="0ba0a-130">[**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize)方法可讓用戶端要求實現虛擬化專案，藉此公開專案的完整消費者介面自動化專案，讓所有必要的屬性和模式都可以使用。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-130">The [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) method enables a client to request that a virtualized item be realized, thereby exposing a full UI Automation element for the item so that all required properties and patterns are available.</span></span>

<span data-ttu-id="0ba0a-131">雖然 **>itemcontainer** 控制項模式的主要目的是要支援虛擬化的容器案例，但它可以由任何可依名稱抓取子專案的容器來執行，而不論容器是否使用虛擬化。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-131">Although the primary purpose of the **ItemContainer** control pattern is to support virtualized container scenarios, it can be implemented by any container that retrieves child items by name, regardless of whether the container uses virtualization.</span></span>

<span data-ttu-id="0ba0a-132">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0ba0a-133">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="0ba0a-133">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="0ba0a-134">IItemContainerProvider 的必要成員</span><span class="sxs-lookup"><span data-stu-id="0ba0a-134">Required Members for IItemContainerProvider</span></span>](#required-members-for-iitemcontainerprovider)
-   [<span data-ttu-id="0ba0a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ba0a-135">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="0ba0a-136">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="0ba0a-136">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="0ba0a-137">在執行 **>itemcontainer** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="0ba0a-137">When implementing the **ItemContainer** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="0ba0a-138">任何可以包含虛擬化專案的控制項都必須支援 **>itemcontainer** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-138">Any control that can contain virtualized items must support the **ItemContainer** control pattern.</span></span> <span data-ttu-id="0ba0a-139">任何支援根據屬性值抓取專案的容器都可以支援此模式，不論容器是否使用虛擬化。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-139">Any container that supports the retrieval of items based on a property value can support this pattern, regardless of whether the container uses virtualization.</span></span>
-   <span data-ttu-id="0ba0a-140">當容器已虛擬化時，其他控制項模式（例如 [選取專案](uiauto-implementingselection.md)、 [資料表](uiauto-implementingtable.md)和 [方格](uiauto-implementinggrid.md) ）可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-140">When a container is virtualized, other controls patterns such as [Selection](uiauto-implementingselection.md), [Table](uiauto-implementingtable.md), and [Grid](uiauto-implementinggrid.md) can be affected.</span></span> <span data-ttu-id="0ba0a-141">例如， [**ISelectionProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) 方法可能只支援位於視口中的元素，或僅支援目前未虛擬化的選取專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-141">For example, the [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) method may support only elements that are in the viewport, or only selected elements that are currently not virtualized.</span></span>
-   <span data-ttu-id="0ba0a-142">[滾動](uiauto-implementingscroll.md)條控制項模式應該不會受到虛擬化的影響。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-142">The [Scroll](uiauto-implementingscroll.md) control pattern should be unaffected by virtualization.</span></span>
-   <span data-ttu-id="0ba0a-143">虛擬化專案沒有可用的專案計數或索引資訊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-143">No item count or index information is available for virtualized items.</span></span> <span data-ttu-id="0ba0a-144">如有必要，虛擬化控制項可以使用 **DescribedBy** 或 **ItemStatus** 屬性來提供此資訊。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-144">A virtualized control can use the **DescribedBy** or the **ItemStatus** property to provide this information, if necessary.</span></span>
-   <span data-ttu-id="0ba0a-145">控制項開發人員應記錄併發布所有消費者介面自動化屬性的詳細資料，以及使用虛擬化所影響的控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-145">Control developers should document and publish details of all UI Automation properties and control patterns affected by the use of virtualization.</span></span> <span data-ttu-id="0ba0a-146">雖然 >itemcontainer 和 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式提供基本支援，但它們可能不支援某些虛擬化行為。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-146">Although the ItemContainer and [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control patterns offer basic support, they may not support some virtualization behaviors.</span></span>

<span data-ttu-id="0ba0a-147">下列指導方針和需求適用于 [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 方法。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-147">The following guidelines and requirements apply to the [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) method.</span></span>

-   <span data-ttu-id="0ba0a-148">雖然並非必要，但 Microsoft 強烈建議 [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 支援 **Name**、 **AutomationId** 和 **IsSelected** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-148">While not required, Microsoft highly recommends that [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) support the **Name**, **AutomationId**, and **IsSelected** properties.</span></span>
-   <span data-ttu-id="0ba0a-149">如果需要跨越多個物件來尋找相符的物件， [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)可能會變慢。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-149">[**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) can be slow if it needs to traverse multiple objects to find a matching one.</span></span>
-   <span data-ttu-id="0ba0a-150">您可以重複呼叫 [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) ，以依序尋找專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-150">[**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) can be called repeatedly to find items in sequence.</span></span> <span data-ttu-id="0ba0a-151">只要每個專案只傳回一次，專案就可以依任何順序排列。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-151">The items can be in any order as long as each item is returned only once.</span></span>
-   <span data-ttu-id="0ba0a-152">[**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 可實作為只尋找出現在消費者介面自動化樹狀結構的控制項或內容視圖中的元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-152">[**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) may be implemented to find only those elements that appear in the control or content view of the UI Automation tree.</span></span> <span data-ttu-id="0ba0a-153">可以略過只出現在原始視圖中的專案，以避免將多個只代表「專案」一部分的元素，提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-153">Elements that appear only in raw view can be skipped to avoid retrieving multiple elements that represent only a portion of an "item" to the user.</span></span>
-   <span data-ttu-id="0ba0a-154">當搜尋準則符合虛擬化專案時，提供者可以傳回支援 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-154">When the search criteria matches a virtualized item, the provider can return a placeholder element that supports the [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control pattern.</span></span> <span data-ttu-id="0ba0a-155">下列指導方針適用于預留位置元素：</span><span class="sxs-lookup"><span data-stu-id="0ba0a-155">The following guidelines apply to placeholder elements:</span></span>
    -   <span data-ttu-id="0ba0a-156">抓取虛擬化專案的預留位置專案時，不能造成 UI 變更。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-156">Retrieving a placeholder element for a virtualized item must not cause UI changes.</span></span>
    -   <span data-ttu-id="0ba0a-157">預留位置元素必須是其他子專案的對等專案， (需要有結構變更的事件) 。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-157">The placeholder element must be a peer of other child elements (a structure-changed event is required).</span></span>
    -   <span data-ttu-id="0ba0a-158">在可能的情況下，提供者可以建立完整的 automation 元素，而不是預留位置。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-158">When possible, the provider can create a full automation element instead of a placeholder.</span></span>
-   <span data-ttu-id="0ba0a-159">當搜尋準則符合非虛擬化專案時，提供者必須傳回實際的元素，而不是預留位置。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-159">When the search criteria matches a non-virtualized element, the provider must return the actual element, not a placeholder.</span></span>
-   <span data-ttu-id="0ba0a-160">如果找不到任何專案， [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 應該將 *pFound* 參數設定為 **Null** ，並傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-160">When no item is found, [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) should set the *pFound* parameter to **NULL** and return **S\_OK**.</span></span>
-   <span data-ttu-id="0ba0a-161">當 *propertyId* 參數是0時，提供者應該在 *pStartAfter* 之後傳回下一個專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-161">When the *propertyId* parameter is 0, the provider should return the next item after *pStartAfter*.</span></span>
-   <span data-ttu-id="0ba0a-162">如果 *pStartAfter* 參數為 **Null** ，而 *propertyId* 為0，則提供者應該傳回容器中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-162">If the *pStartAfter* parameter is **NULL** and *propertyId* is 0, the provider should return the first item in the container.</span></span>
-   <span data-ttu-id="0ba0a-163">當 *propertyId* 參數是0時，會忽略 value 參數。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-163">When the *propertyId* parameter is 0, the value parameter is ignored.</span></span>

<span data-ttu-id="0ba0a-164">下列指導方針和需求適用于消費者介面自動化樹狀結構中虛擬化專案的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-164">The following guidelines and requirements apply to placeholder elements for virtualized items in the UI Automation tree.</span></span>

-   <span data-ttu-id="0ba0a-165">雖然我們鼓勵提供者為預留位置元素支援更多屬性和控制項模式，但是只需要 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-165">Although providers are encouraged to support more properties and control patterns for a placeholder element, only the [VirtualizedItem](uiauto-implementingvirtualizeditem.md) control pattern is required.</span></span>
-   <span data-ttu-id="0ba0a-166">當再次呼叫 [**IItemContainerProvider：： FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) 時，提供者可能會使先前的預留位置元素失效。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-166">The provider can invalidate a previous placeholder element when [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) is called again.</span></span> <span data-ttu-id="0ba0a-167"> (如果用戶端需要瞭解預留位置元素，就應該立即這麼做;否則，如果再次呼叫 **FindItemByProperty** ，或因為任何原因而改變，則元素可能會失效。 ) </span><span class="sxs-lookup"><span data-stu-id="0ba0a-167">(If a client needs to realize the placeholder element, it should do so immediately; otherwise, the element can be invalidated if **FindItemByProperty** is called again or if the viewport changes for whatever reason.)</span></span>
-   <span data-ttu-id="0ba0a-168">UI 動作（例如滾動或調整大小）可能會導致容器的視口變更，而且會顯示一組新的子專案。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-168">UI actions such as scrolling or resizing can cause the viewport of the container to change and a new set of child items to become visible.</span></span> <span data-ttu-id="0ba0a-169">在此情況下，消費者介面自動化樹狀結構中可能無法使用先前抓取的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-169">In this case, previously-retrieved placeholder elements may not be available in the UI Automation tree.</span></span>
-   <span data-ttu-id="0ba0a-170">提供者不應虛擬化 UI 元素，這些專案可在容器物件的元件區中使用。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-170">The provider should not virtualize UI elements that are available on-screen in the viewport of the container object.</span></span>

## <a name="required-members-for-iitemcontainerprovider"></a><span data-ttu-id="0ba0a-171">IItemContainerProvider 的必要成員</span><span class="sxs-lookup"><span data-stu-id="0ba0a-171">Required Members for IItemContainerProvider</span></span>

<span data-ttu-id="0ba0a-172">以下是執行 [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-172">The following method is required for implementing the [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) interface.</span></span>



| <span data-ttu-id="0ba0a-173">必要成員</span><span class="sxs-lookup"><span data-stu-id="0ba0a-173">Required members</span></span>                                                               | <span data-ttu-id="0ba0a-174">成員類型</span><span class="sxs-lookup"><span data-stu-id="0ba0a-174">Member type</span></span> | <span data-ttu-id="0ba0a-175">備註</span><span class="sxs-lookup"><span data-stu-id="0ba0a-175">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="0ba0a-176">**FindItemByProperty**</span><span class="sxs-lookup"><span data-stu-id="0ba0a-176">**FindItemByProperty**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | <span data-ttu-id="0ba0a-177">方法</span><span class="sxs-lookup"><span data-stu-id="0ba0a-177">Method</span></span>      | <span data-ttu-id="0ba0a-178">無</span><span class="sxs-lookup"><span data-stu-id="0ba0a-178">None</span></span>  |



 

<span data-ttu-id="0ba0a-179">**>itemcontainer** 控制項模式沒有相關聯的屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="0ba0a-179">The **ItemContainer** control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ba0a-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ba0a-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ba0a-181">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0ba0a-181">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="0ba0a-182">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="0ba0a-182">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0ba0a-183">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="0ba0a-183">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="0ba0a-184">VirtualizedItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="0ba0a-184">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




