---
title: SynchronizedInput 控制項模式
description: 描述執行 ISynchronizedInputProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- 消費者介面自動化，執行 SynchronizedInput 控制項模式
- 消費者介面自動化，SynchronizedInput 控制項模式
- 消費者介面自動化、ISynchronizedInputProvider
- ISynchronizedInputProvider
- 執行消費者介面自動化 SynchronizedInput 控制項模式
- SynchronizedInput 控制項模式
- 控制項模式，ISynchronizedInputProvider
- 控制模式，消費者介面自動化執行 SynchronizedInput
- 控制項模式，SynchronizedInput
- 介面，ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984933"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="1955c-113">SynchronizedInput 控制項模式</span><span class="sxs-lookup"><span data-stu-id="1955c-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="1955c-114">描述執行 [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1955c-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="1955c-115">**SynchronizedInput** 控制項模式可讓 Microsoft 消費者介面自動化用戶端應用程式將滑鼠或鍵盤輸入導向至特定的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="1955c-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="1955c-116">此控制項模式通常用於自動化測試腳本，以將滑鼠或鍵盤輸入傳送至特定的使用者介面元素，然後確認專案收到輸入。</span><span class="sxs-lookup"><span data-stu-id="1955c-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="1955c-117">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="1955c-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1955c-118">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="1955c-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="1955c-119">**ISynchronizedInputProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="1955c-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="1955c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1955c-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="1955c-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="1955c-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="1955c-122">在執行 **SynchronizedInput** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="1955c-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="1955c-123">呼叫 [**ISynchronizedInputProvider：： StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) 方法時，消費者介面自動化提供者應該開始檢查指定類型的輸入，然後執行下列其中一個動作：</span><span class="sxs-lookup"><span data-stu-id="1955c-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="1955c-124">當針對元素找到相符的輸入時，提供者應該引發 [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1955c-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="1955c-125">當找到相符的輸入，但它到達不同的元素時，提供者應該引發 [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1955c-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="1955c-126">當找到不符的輸入時，提供者應該捨棄輸入並引發 [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1955c-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="1955c-127">如果消費者介面自動化提供者是針對目前專案以外的元素，則必須捨棄該輸入。</span><span class="sxs-lookup"><span data-stu-id="1955c-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="1955c-128">當專案接收到輸入時，或呼叫 [**ISynchronizedInputProvider：： Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) 方法時，提供者會停止檢查輸入並繼續正常執行。</span><span class="sxs-lookup"><span data-stu-id="1955c-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="1955c-129">如果提供者已在接聽輸入時呼叫 [**ISynchronizedInputProvider：： StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) ，則提供者應該傳回 [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1955c-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="1955c-130">**ISynchronizedInputProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="1955c-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="1955c-131">執行 [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) 介面需要下列屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="1955c-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="1955c-132">必要成員</span><span class="sxs-lookup"><span data-stu-id="1955c-132">Required members</span></span>                                                                         | <span data-ttu-id="1955c-133">成員類型</span><span class="sxs-lookup"><span data-stu-id="1955c-133">Member type</span></span> | <span data-ttu-id="1955c-134">備註</span><span class="sxs-lookup"><span data-stu-id="1955c-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1955c-135">**StartListening**</span><span class="sxs-lookup"><span data-stu-id="1955c-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="1955c-136">方法</span><span class="sxs-lookup"><span data-stu-id="1955c-136">Method</span></span>      | <span data-ttu-id="1955c-137">無</span><span class="sxs-lookup"><span data-stu-id="1955c-137">None</span></span>  |
| [<span data-ttu-id="1955c-138">**取消**</span><span class="sxs-lookup"><span data-stu-id="1955c-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="1955c-139">方法</span><span class="sxs-lookup"><span data-stu-id="1955c-139">Method</span></span>      | <span data-ttu-id="1955c-140">無</span><span class="sxs-lookup"><span data-stu-id="1955c-140">None</span></span>  |
| [<span data-ttu-id="1955c-141">**UIA \_ InputReachedTargetEventId**</span><span class="sxs-lookup"><span data-stu-id="1955c-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="1955c-142">事件</span><span class="sxs-lookup"><span data-stu-id="1955c-142">Event</span></span>       | <span data-ttu-id="1955c-143">無</span><span class="sxs-lookup"><span data-stu-id="1955c-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="1955c-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="1955c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1955c-145">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="1955c-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




