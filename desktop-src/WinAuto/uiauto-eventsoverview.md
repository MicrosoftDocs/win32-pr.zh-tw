---
title: UI 自動化事件概觀
description: Microsoft 消費者介面自動化事件通知是輔助技術的主要功能，例如螢幕閱讀程式和螢幕放大鏡。
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- 消費者介面自動化，事件總覽
- 消費者介面自動化，事件類別目錄
- 消費者介面自動化，事件通知
- 事件通知
- 事件，類別
- 事件，事件通知
- 屬性變更事件
- 元素動作事件
- 結構變更事件
- 全域桌面變更事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315274"
---
# <a name="ui-automation-events-overview"></a><span data-ttu-id="df2a4-113">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="df2a4-113">UI Automation Events Overview</span></span>

<span data-ttu-id="df2a4-114">Microsoft 消費者介面自動化事件通知是輔助技術的主要功能，例如螢幕閱讀程式和螢幕放大鏡。</span><span class="sxs-lookup"><span data-stu-id="df2a4-114">Microsoft UI Automation event notification is a key feature for assistive technologies, such as screen readers and screen magnifiers.</span></span> <span data-ttu-id="df2a4-115">這些消費者介面自動化的用戶端會在 UI 中發生問題時追蹤消費者介面自動化提供者所引發的事件，並使用資訊來通知終端使用者。</span><span class="sxs-lookup"><span data-stu-id="df2a4-115">These UI Automation clients track events that are raised by UI Automation providers when something happens in the UI and use the information to notify end users.</span></span>

<span data-ttu-id="df2a4-116">藉由允許提供者應用程式選擇性地引發事件來改善效率，取決於是否有用戶端訂閱那些事件或完全沒有，前提是沒有用戶端正在接聽任何事件。</span><span class="sxs-lookup"><span data-stu-id="df2a4-116">Efficiency is improved by allowing provider applications to raise events selectively, depending on whether any clients are subscribed to those events, or not at all, if no clients are listening for any events.</span></span>

<span data-ttu-id="df2a4-117">UI 自動化事件分成下列類別。</span><span class="sxs-lookup"><span data-stu-id="df2a4-117">UI Automation events fall into the following categories.</span></span>



| <span data-ttu-id="df2a4-118">事件類別目錄</span><span class="sxs-lookup"><span data-stu-id="df2a4-118">Event Category</span></span>        | <span data-ttu-id="df2a4-119">Description</span><span class="sxs-lookup"><span data-stu-id="df2a4-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df2a4-120">屬性變更</span><span class="sxs-lookup"><span data-stu-id="df2a4-120">Property change</span></span>       | <span data-ttu-id="df2a4-121">當消費者介面自動化元素或控制項模式上的屬性變更時引發。</span><span class="sxs-lookup"><span data-stu-id="df2a4-121">Raised when a property on UI Automation element or control pattern changes.</span></span> <span data-ttu-id="df2a4-122">例如，如果用戶端需要監視應用程式的核取方塊控制項，則可以註冊來接聽 [**IUIAutomationTogglePattern：： CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) 屬性上的屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="df2a4-122">For example, if a client needs to monitor an application check box control, it can register to listen for a property change event on the [**IUIAutomationTogglePattern::CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) property.</span></span> <span data-ttu-id="df2a4-123">當選取或取消選取核取方塊控制項時，提供者會引發事件，而且用戶端可視需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="df2a4-123">When the check box control is checked or unchecked, the provider raises the event and the client can act as necessary.</span></span> |
| <span data-ttu-id="df2a4-124">項目動作</span><span class="sxs-lookup"><span data-stu-id="df2a4-124">Element action</span></span>        | <span data-ttu-id="df2a4-125">當使用者或程式設計活動的 UI 結果變更時引發，例如，按一下按鈕或透過 [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)叫用時。</span><span class="sxs-lookup"><span data-stu-id="df2a4-125">Raised when a change in the UI results from end user or programmatic activity, for example, when a button is clicked or invoked through [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="df2a4-126">結構變更</span><span class="sxs-lookup"><span data-stu-id="df2a4-126">Structure change</span></span>      | <span data-ttu-id="df2a4-127">當消費者介面自動化樹狀結構的結構變更時引發。</span><span class="sxs-lookup"><span data-stu-id="df2a4-127">Raised when the structure of the UI Automation tree changes.</span></span> <span data-ttu-id="df2a4-128">當新的 UI 項目顯示、隱藏或從桌面上移除時，結構會變更。</span><span class="sxs-lookup"><span data-stu-id="df2a4-128">The structure changes when new UI items become visible, hidden, or removed on the desktop.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="df2a4-129">全域桌面變更</span><span class="sxs-lookup"><span data-stu-id="df2a4-129">Global desktop change</span></span> | <span data-ttu-id="df2a4-130">發生用戶端感興趣的全域動作時 (例如，焦點從一個項目移到另一個項目時，或當視窗關閉時) 引發。</span><span class="sxs-lookup"><span data-stu-id="df2a4-130">Raised when actions of global interest to the client occur, such as when the focus shifts from one element to another, or when a window closes.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="df2a4-131">通知</span><span class="sxs-lookup"><span data-stu-id="df2a4-131">Notification</span></span>          | <span data-ttu-id="df2a4-132">當應用程式呼叫 [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) 函式時引發。</span><span class="sxs-lookup"><span data-stu-id="df2a4-132">Raised when an app calls the [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) function.</span></span> <span data-ttu-id="df2a4-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) 表示通知的類型。</span><span class="sxs-lookup"><span data-stu-id="df2a4-133">[**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indicates the type of the notification.</span></span>                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="df2a4-134">某些事件並不一定表示 UI 的狀態已經變更。</span><span class="sxs-lookup"><span data-stu-id="df2a4-134">Some events do not necessarily mean that the state of the UI has changed.</span></span> <span data-ttu-id="df2a4-135">例如，如果使用者索引標籤是文字輸入欄位，然後按一下按鈕來更新欄位，則會引發 UIA 的 [**\_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md) 事件，即使使用者未實際變更文字也是一樣。</span><span class="sxs-lookup"><span data-stu-id="df2a4-135">For example, if the user tabs to a text entry field, and then clicks a button to update the field, a [**UIA\_Text\_TextChangedEventId**](uiauto-event-ids.md) event is raised, even if the user did not actually change the text.</span></span> <span data-ttu-id="df2a4-136">在處理事件時，用戶端應用程式可能需要在採取動作之前檢查是否有任何實際變更。</span><span class="sxs-lookup"><span data-stu-id="df2a4-136">When processing an event, it may be necessary for a client application to check whether anything has actually changed before taking action.</span></span>

<span data-ttu-id="df2a4-137">即使 UI 的狀態未變更，也可能引發下列事件。</span><span class="sxs-lookup"><span data-stu-id="df2a4-137">The following events may be raised even when the state of the UI has not changed.</span></span>

-   <span data-ttu-id="df2a4-138">[**UIA \_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (取決於已變更的屬性) </span><span class="sxs-lookup"><span data-stu-id="df2a4-138">[**UIA\_AutomationPropertyChangedEventId**](uiauto-event-ids.md) (depending on the property that has changed)</span></span>
-   [<span data-ttu-id="df2a4-139">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="df2a4-139">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="df2a4-140">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="df2a4-140">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)
-   [<span data-ttu-id="df2a4-141">**UIA \_ 文字 \_ TextChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="df2a4-141">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)

<span data-ttu-id="df2a4-142">如需所有消費者介面自動化事件的說明，請參閱 [事件識別碼](uiauto-event-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="df2a4-142">For a description of all UI Automation events, see [Event Identifiers](uiauto-event-ids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df2a4-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="df2a4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df2a4-144">訂閱消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="df2a4-144">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> </dl>

 

 