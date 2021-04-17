---
title: VirtualizedItem 控制項模式
description: 描述執行 IVirtualizedItemProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- 消費者介面自動化，執行 VirtualizedItem 控制項模式
- 消費者介面自動化，VirtualizedItem 控制項模式
- 消費者介面自動化、IVirtualizedItemProvider
- IVirtualizedItemProvider
- 執行消費者介面自動化 VirtualizedItem 控制項模式
- VirtualizedItem 控制項模式
- 控制項模式，IVirtualizedItemProvider
- 控制模式，消費者介面自動化執行 VirtualizedItem
- 控制項模式，VirtualizedItem
- 介面，IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184172"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="987b6-113">VirtualizedItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="987b6-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="987b6-114">描述執行 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="987b6-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="987b6-115">**VirtualizedItem** 控制項模式用來支援虛擬化專案，這些專案是由 Microsoft 消費者介面自動化樹狀結構中的預留位置自動化元素所表示的專案。</span><span class="sxs-lookup"><span data-stu-id="987b6-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="987b6-116">虛擬化專案可以包含從支援 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式的控制項取出的專案，或是從支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式的控制項抓取的虛擬化内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="987b6-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="987b6-117">虛擬化專案的預留位置可能尚未載入所有消費者介面自動化屬性的資料，而且可能會傳回 [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) ，以回應無法使用的屬性查詢。</span><span class="sxs-lookup"><span data-stu-id="987b6-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="987b6-118">**VirtualizedItem** 控制項模式提供了一種方法，可讓您瞭解虛擬專案，讓專案可以使用完整資訊，而且可以在消費者介面自動化樹狀結構中建立專案的完整自動化專案。</span><span class="sxs-lookup"><span data-stu-id="987b6-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="987b6-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="987b6-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="987b6-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="987b6-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="987b6-121">**IVirtualizedItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="987b6-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="987b6-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="987b6-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="987b6-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="987b6-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="987b6-124">在執行 **VirtualizedItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="987b6-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="987b6-125">任何可以虛擬化消費者介面自動化預留位置專案都必須藉由公開 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)介面，支援 **VirtualizedItem** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="987b6-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="987b6-126">呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 時，預留位置物件必須使用其屬性和控制項模式的完整實作為更新。</span><span class="sxs-lookup"><span data-stu-id="987b6-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="987b6-127">當呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 時，提供者可以變更此分割區，讓虛擬化專案變成可供觀看。</span><span class="sxs-lookup"><span data-stu-id="987b6-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="987b6-128">不需要將專案帶入 view;不過，非虛擬化的專案應該支援 [**IScrollItemProvider：： ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) 方法。</span><span class="sxs-lookup"><span data-stu-id="987b6-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="987b6-129">**IVirtualizedItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="987b6-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="987b6-130">執行 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="987b6-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="987b6-131">必要成員</span><span class="sxs-lookup"><span data-stu-id="987b6-131">Required members</span></span>                                           | <span data-ttu-id="987b6-132">成員類型</span><span class="sxs-lookup"><span data-stu-id="987b6-132">Member type</span></span> | <span data-ttu-id="987b6-133">備註</span><span class="sxs-lookup"><span data-stu-id="987b6-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="987b6-134">**實現**</span><span class="sxs-lookup"><span data-stu-id="987b6-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="987b6-135">方法</span><span class="sxs-lookup"><span data-stu-id="987b6-135">Method</span></span>      | <span data-ttu-id="987b6-136">無</span><span class="sxs-lookup"><span data-stu-id="987b6-136">None</span></span>  |



 

<span data-ttu-id="987b6-137">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="987b6-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="987b6-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="987b6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="987b6-139">執行消費者介面自動化 >itemcontainer 控制項模式</span><span class="sxs-lookup"><span data-stu-id="987b6-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="987b6-140">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="987b6-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="987b6-141">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="987b6-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="987b6-142">使用虛擬化專案</span><span class="sxs-lookup"><span data-stu-id="987b6-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




