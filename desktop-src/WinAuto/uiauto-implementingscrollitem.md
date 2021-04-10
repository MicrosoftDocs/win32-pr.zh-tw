---
title: ScrollItem 控制項模式
description: 描述執行 IScrollItemProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- 消費者介面自動化，執行 ScrollItem 控制項模式
- 消費者介面自動化，ScrollItem 控制項模式
- 消費者介面自動化、IScrollItemProvider
- IScrollItemProvider
- 執行消費者介面自動化 ScrollItem 控制項模式
- ScrollItem 控制項模式
- 控制項模式，IScrollItemProvider
- 控制模式，消費者介面自動化執行 ScrollItem
- 控制項模式，ScrollItem
- 介面，IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183643"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="948ea-113">ScrollItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="948ea-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="948ea-114">描述執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="948ea-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="948ea-115">**ScrollItem** 控制項模式用來支援執行 [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)之容器的個別子控制項。</span><span class="sxs-lookup"><span data-stu-id="948ea-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="948ea-116">控制項的 **ScrollItem** 控制項模式是否存在，並不表示其容器或任何上階都必須執行 **滾動** 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="948ea-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="948ea-117">當容器執行的是 **滾動** 條控制項模式時， **ScrollItem** 控制項模式會作為子控制項與其容器之間的通道，以確保容器可以變更其區域內的目前可見內容 (或區域) ，以顯示子控制項。</span><span class="sxs-lookup"><span data-stu-id="948ea-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="948ea-118">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="948ea-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="948ea-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="948ea-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="948ea-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="948ea-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="948ea-121">**IScrollItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="948ea-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="948ea-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="948ea-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="948ea-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="948ea-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="948ea-124">在執行 **ScrollItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="948ea-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="948ea-125">不需要 [視窗](uiauto-supportwindowcontroltype.md) 或 **畫布** 控制項內所含的專案來執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="948ea-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="948ea-126">不過，您也必須公開 [**IUIAutomationElement：： CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (或 [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) 屬性的有效位置。</span><span class="sxs-lookup"><span data-stu-id="948ea-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="948ea-127">這可讓 Microsoft 消費者介面自動化用戶端應用程式使用容器上的 [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) 控制項模式方法來顯示子專案。</span><span class="sxs-lookup"><span data-stu-id="948ea-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="948ea-128">**IScrollItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="948ea-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="948ea-129">以下是執行 [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="948ea-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="948ea-130">必要成員</span><span class="sxs-lookup"><span data-stu-id="948ea-130">Required members</span></span>                                                    | <span data-ttu-id="948ea-131">成員類型</span><span class="sxs-lookup"><span data-stu-id="948ea-131">Member type</span></span> | <span data-ttu-id="948ea-132">備註</span><span class="sxs-lookup"><span data-stu-id="948ea-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="948ea-133">**ScrollIntoView**</span><span class="sxs-lookup"><span data-stu-id="948ea-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="948ea-134">方法</span><span class="sxs-lookup"><span data-stu-id="948ea-134">Method</span></span>      | <span data-ttu-id="948ea-135">無</span><span class="sxs-lookup"><span data-stu-id="948ea-135">None</span></span>  |



 

<span data-ttu-id="948ea-136">此控制項模式沒有任何相關聯的屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="948ea-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="948ea-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="948ea-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="948ea-138">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="948ea-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="948ea-139">選取控制項模式</span><span class="sxs-lookup"><span data-stu-id="948ea-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="948ea-140">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="948ea-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="948ea-141">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="948ea-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




