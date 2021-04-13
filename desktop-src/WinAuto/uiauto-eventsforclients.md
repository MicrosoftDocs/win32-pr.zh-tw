---
title: 訂閱消費者介面自動化事件
description: Microsoft 消費者介面自動化可讓用戶端訂閱感興趣的事件。 這項功能可讓您不需要持續輪詢系統中的 UI 元素，查看任何資訊、結構或狀態是否已變更，進而改善效能。
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- 用戶端，消費者介面自動化事件
- 用戶端，消費者介面自動化的事件
- 消費者介面自動化，用戶端的事件
- 消費者介面自動化，用戶端事件
- 消費者介面自動化，訂閱事件
- 消費者介面自動化，訂用帳戶方法
- 消費者介面自動化，程式碼範例
- 消費者介面自動化，範例
- 消費者介面自動化，範例
- 訂閱 UI 自動化事件
- 事件，消費者介面自動化訂用帳戶
- 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301059"
---
# <a name="subscribing-to-ui-automation-events"></a><span data-ttu-id="ec989-116">訂閱消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="ec989-116">Subscribing to UI Automation Events</span></span>

<span data-ttu-id="ec989-117">Microsoft 消費者介面自動化可讓用戶端訂閱感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="ec989-117">Microsoft UI Automation allows clients to subscribe to events of interest.</span></span> <span data-ttu-id="ec989-118">這項功能可讓您不需要持續輪詢系統中的 UI 元素，查看任何資訊、結構或狀態是否已變更，進而改善效能。</span><span class="sxs-lookup"><span data-stu-id="ec989-118">This capability improves performance by eliminating the need to continually poll the UI elements in the system to see if any information, structure, or state has changed.</span></span>

<span data-ttu-id="ec989-119">同時也因為能夠只接聽定義範圍內的事件，而改善效率。</span><span class="sxs-lookup"><span data-stu-id="ec989-119">Efficiency is also improved by the ability to listen for events only within a defined scope.</span></span> <span data-ttu-id="ec989-120">例如，用戶端可以接聽清單中專案、清單本身或整個對話方塊中的選取專案變更。</span><span class="sxs-lookup"><span data-stu-id="ec989-120">For example, a client can listen for selection changes on an item in a list, on the list itself, or on an entire dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="ec989-121">請勿假設所有可能的事件都是由消費者介面自動化提供者引發。</span><span class="sxs-lookup"><span data-stu-id="ec989-121">Do not assume that all possible events are raised by a UI Automation provider.</span></span> <span data-ttu-id="ec989-122">例如，並非所有屬性變更都會導致 Windows Forms 和 Microsoft Win32 控制項的標準 proxy 提供者引發事件。</span><span class="sxs-lookup"><span data-stu-id="ec989-122">For example, not all property changes cause events to be raised by the standard proxy providers for Windows Forms and Microsoft Win32 controls.</span></span>

 

<span data-ttu-id="ec989-123">如需更廣泛的消費者介面自動化事件查看，請參閱 [消費者介面自動化事件總覽](uiauto-eventsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ec989-123">For a broader view of UI Automation events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="ec989-124">在執行事件處理常式之前，您應該先熟悉 [瞭解執行緒問題](uiauto-threading.md)中所述的執行緒問題。</span><span class="sxs-lookup"><span data-stu-id="ec989-124">Before implementing an event handler, you should be familiar with the threading issues described in [Understanding Threading Issues](uiauto-threading.md).</span></span>

 

<span data-ttu-id="ec989-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ec989-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ec989-126">註冊事件處理常式</span><span class="sxs-lookup"><span data-stu-id="ec989-126">Registering Event Handlers</span></span>](#registering-event-handlers)
-   [<span data-ttu-id="ec989-127">範例</span><span class="sxs-lookup"><span data-stu-id="ec989-127">Examples</span></span>](#examples)
-   [<span data-ttu-id="ec989-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec989-128">Related topics</span></span>](#related-topics)

## <a name="registering-event-handlers"></a><span data-ttu-id="ec989-129">註冊事件處理常式</span><span class="sxs-lookup"><span data-stu-id="ec989-129">Registering Event Handlers</span></span>

<span data-ttu-id="ec989-130">用戶端應用程式會使用下列其中一個 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 方法，藉由註冊事件處理常式來訂閱特定種類的事件。</span><span class="sxs-lookup"><span data-stu-id="ec989-130">Client applications subscribe to events of a particular kind by registering an event handler, using one of the following [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) methods.</span></span>



| <span data-ttu-id="ec989-131">訂用帳戶方法</span><span class="sxs-lookup"><span data-stu-id="ec989-131">Subscription Method</span></span>                                                                                                                                                                                                | <span data-ttu-id="ec989-132">事件類型</span><span class="sxs-lookup"><span data-stu-id="ec989-132">Event Type</span></span>       | <span data-ttu-id="ec989-133">回呼介面</span><span class="sxs-lookup"><span data-stu-id="ec989-133">Callback Interface</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec989-134">**AddFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-134">**AddFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | <span data-ttu-id="ec989-135">焦點變更</span><span class="sxs-lookup"><span data-stu-id="ec989-135">Focus change</span></span>     | [<span data-ttu-id="ec989-136">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-136">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| <span data-ttu-id="ec989-137">[**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)、 [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)</span><span class="sxs-lookup"><span data-stu-id="ec989-137">[**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)</span></span> | <span data-ttu-id="ec989-138">屬性變更</span><span class="sxs-lookup"><span data-stu-id="ec989-138">Property change</span></span>  | [<span data-ttu-id="ec989-139">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-139">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [<span data-ttu-id="ec989-140">**AddStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-140">**AddStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | <span data-ttu-id="ec989-141">結構變更</span><span class="sxs-lookup"><span data-stu-id="ec989-141">Structure change</span></span> | [<span data-ttu-id="ec989-142">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-142">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [<span data-ttu-id="ec989-143">**AddNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-143">**AddNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | <span data-ttu-id="ec989-144">通知</span><span class="sxs-lookup"><span data-stu-id="ec989-144">Notification</span></span>     | [<span data-ttu-id="ec989-145">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-145">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [<span data-ttu-id="ec989-146">**AddAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-146">**AddAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | <span data-ttu-id="ec989-147">其他事件</span><span class="sxs-lookup"><span data-stu-id="ec989-147">Other events</span></span>     | [<span data-ttu-id="ec989-148">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-148">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

<span data-ttu-id="ec989-149">當用戶端將所有子系的事件處理常式加入 (Treescope.children 下階) 時，消費者介面自動化只針對子樹的根目錄新增一個處理常式，而處理常式會接聽所有子代。 [**\_**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)</span><span class="sxs-lookup"><span data-stu-id="ec989-149">When a client adds an event handler for all descendants ([**TreeScope\_Descendants**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), UI Automation adds only one handler for the root of sub-tree, and the handler listens across all descendents.</span></span> <span data-ttu-id="ec989-150">消費者介面自動化不會以遞迴方式加入事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-150">UI Automation does not add event handlers recursively.</span></span>

<span data-ttu-id="ec989-151">當用戶端呼叫 [**IUIAutomation：： RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) 方法時消費者介面自動化會從用戶端進程中移除所有事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-151">When a client calls the [**IUIAutomation::RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) method, UI Automation removes all event handlers from the client process.</span></span>

<span data-ttu-id="ec989-152">若要接收和處理事件，您可以執行公開回呼介面的事件處理物件，而且您必須呼叫事件註冊方法（例如 [**IUIAutomation：： AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler)）來註冊物件。</span><span class="sxs-lookup"><span data-stu-id="ec989-152">To receive and handle events, you implement an event-handling object that exposes a callback interface, and you must register the object by calling an event registration method such as [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler).</span></span> <span data-ttu-id="ec989-153">回呼介面具有單一方法;當處理事件時，消費者介面自動化會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec989-153">The callback interface has a single method; UI Automation calls this method when the event is processed.</span></span>

<span data-ttu-id="ec989-154">在關機時，或當應用程式不再需要消費者介面自動化事件時，消費者介面自動化用戶端應該呼叫下列一或多個 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 方法。</span><span class="sxs-lookup"><span data-stu-id="ec989-154">On shutdown, or when UI Automation events are no longer of interest to the application, UI Automation clients should call one or more of the following [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) methods.</span></span>

> [!Note]  
> <span data-ttu-id="ec989-155">消費者介面自動化用戶端不應該使用多個執行緒來新增或移除事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-155">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="ec989-156">如果在相同的用戶端進程中新增或移除一個事件處理常式，可能會導致未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="ec989-156">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

 



| <span data-ttu-id="ec989-157">方法</span><span class="sxs-lookup"><span data-stu-id="ec989-157">Method</span></span>                                                                                                | <span data-ttu-id="ec989-158">描述</span><span class="sxs-lookup"><span data-stu-id="ec989-158">Description</span></span>                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec989-159">**RemoveAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-159">**RemoveAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | <span data-ttu-id="ec989-160">取消註冊使用 [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-160">Unregisters an event handler that was registered by using [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).</span></span>                                                                                                                                  |
| [<span data-ttu-id="ec989-161">**RemoveFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-161">**RemoveFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | <span data-ttu-id="ec989-162">取消註冊使用 [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-162">Unregisters an event handler that was registered by using [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).</span></span>                                                                                                                              |
| [<span data-ttu-id="ec989-163">**RemovePropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-163">**RemovePropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | <span data-ttu-id="ec989-164">取消註冊使用 [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) 或 [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-164">Unregisters an event handler that was registered by using [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span> |
| [<span data-ttu-id="ec989-165">**RemoveStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-165">**RemoveStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | <span data-ttu-id="ec989-166">取消註冊使用 [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-166">Unregisters an event handler that was registered by using [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).</span></span>                                                                                                                      |
| [<span data-ttu-id="ec989-167">**RemoveNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="ec989-167">**RemoveNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | <span data-ttu-id="ec989-168">取消註冊 weas 使用 [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-168">Unregisters an event handler that weas registered by using [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).</span></span>                                                                                                                            |
| [<span data-ttu-id="ec989-169">**RemoveAllEventHandlers**</span><span class="sxs-lookup"><span data-stu-id="ec989-169">**RemoveAllEventHandlers**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | <span data-ttu-id="ec989-170">移除註冊所有已註冊的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-170">Unregisters all registered event handlers.</span></span>                                                                                                                                                                                                                                      |



 

<span data-ttu-id="ec989-171">在取消訂閱處理常式之後，如果事件同時與取消訂閱事件的要求同時收到，就可能會將事件傳遞至事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="ec989-171">It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, if the event is received simultaneously with the request to unsubscribe the event.</span></span> <span data-ttu-id="ec989-172">最佳作法是遵循元件物件模型 (COM) 標準，並避免在其參考計數達到零時終結事件處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="ec989-172">The best practice is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count has reached zero.</span></span> <span data-ttu-id="ec989-173">在取消訂閱事件之後立即終結事件處理常式，可能會在延遲傳遞事件時導致存取違規。</span><span class="sxs-lookup"><span data-stu-id="ec989-173">Destroying an event handler immediately after unsubscribing for events may result in an access violation if an event is delivered late.</span></span>

## <a name="examples"></a><span data-ttu-id="ec989-174">範例</span><span class="sxs-lookup"><span data-stu-id="ec989-174">Examples</span></span>

<span data-ttu-id="ec989-175">如需示範如何處理消費者介面自動化事件的程式碼範例，請參閱 [如何執行事件處理常式](uiauto-howto-implement-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="ec989-175">For code examples that show how to handle UI Automation events, see [How to Implement Event Handlers](uiauto-howto-implement-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec989-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec989-176">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ec989-177">**概念**</span><span class="sxs-lookup"><span data-stu-id="ec989-177">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ec989-178">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="ec989-178">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="ec989-179">瞭解執行緒問題</span><span class="sxs-lookup"><span data-stu-id="ec989-179">Understanding Threading Issues</span></span>](uiauto-threading.md)
</dt> </dl>

 

 




