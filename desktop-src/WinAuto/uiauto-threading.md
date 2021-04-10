---
title: 瞭解執行緒問題
description: 本主題說明 Microsoft 消費者介面自動化用戶端的常見執行緒案例，並說明如何避免用戶端不正確地使用執行緒時可能發生的問題。
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- 用戶端，消費者介面自動化執行緒問題
- 用戶端，執行緒問題
- 用戶端，事件處理常式執行緒模型
- 用戶端，消費者介面自動化事件處理常式執行緒模型
- 用戶端，消費者介面自動化親和性
- 用戶端、親和性
- 消費者介面自動化，執行緒問題
- 消費者介面自動化，事件處理常式執行緒模型
- 消費者介面自動化，親和性
- 執行緒問題
- 事件處理常式執行緒模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023529"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="de9a4-114">瞭解執行緒問題</span><span class="sxs-lookup"><span data-stu-id="de9a4-114">Understanding Threading Issues</span></span>

<span data-ttu-id="de9a4-115">本主題說明 Microsoft 消費者介面自動化用戶端的常見執行緒案例，並說明如何避免用戶端不正確地使用執行緒時可能發生的問題。</span><span class="sxs-lookup"><span data-stu-id="de9a4-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="de9a4-116">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="de9a4-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="de9a4-117">消費者介面自動化和 UI 執行緒</span><span class="sxs-lookup"><span data-stu-id="de9a4-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="de9a4-118">事件處理常式的執行緒模型</span><span class="sxs-lookup"><span data-stu-id="de9a4-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="de9a4-119">64位 Windows 上的 COM 單元親和性</span><span class="sxs-lookup"><span data-stu-id="de9a4-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="de9a4-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="de9a4-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="de9a4-121">消費者介面自動化和 UI 執行緒</span><span class="sxs-lookup"><span data-stu-id="de9a4-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="de9a4-122">由於消費者介面自動化使用 Windows 訊息的方式，因此當用戶端應用程式嘗試在 UI 執行緒上與其本身的 UI 互動時，就會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="de9a4-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="de9a4-123">這些衝突可能會導致效能變慢，或甚至導致應用程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="de9a4-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="de9a4-124">如果您的用戶端應用程式要與桌面上的所有元素互動，包括它自己的 UI，您應該從個別的執行緒進行所有的消費者介面自動化呼叫。</span><span class="sxs-lookup"><span data-stu-id="de9a4-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="de9a4-125">這包括尋找元素，例如使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 或 [**IUIAutomationElement：： FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) 方法，以及使用控制項模式。</span><span class="sxs-lookup"><span data-stu-id="de9a4-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="de9a4-126">這個執行緒不應該擁有任何視窗，而且應該是元件物件模型 (COM) 多執行緒的單元 (MTA) 模型執行緒， (使用 **COINIT \_ 多執行緒** 旗標呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)來初始化 COM。 ) </span><span class="sxs-lookup"><span data-stu-id="de9a4-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="de9a4-127">您可以安全地在消費者介面自動化事件處理常式中進行消費者介面自動化呼叫，因為在非 UI 執行緒上一律會呼叫事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="de9a4-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="de9a4-128">不過，在訂閱可能源自用戶端應用程式 UI 的事件時，您必須在非 UI 執行緒上呼叫 [**IUIAutomation：： AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)或相關的方法， (也應該是) 的 MTA 執行緒。</span><span class="sxs-lookup"><span data-stu-id="de9a4-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="de9a4-129">在相同執行緒上移除事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="de9a4-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="de9a4-130">消費者介面自動化用戶端不應該使用多個執行緒來新增或移除事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="de9a4-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="de9a4-131">如果在相同的用戶端進程中新增或移除一個事件處理常式，可能會導致未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="de9a4-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="de9a4-132">事件處理常式的執行緒模型</span><span class="sxs-lookup"><span data-stu-id="de9a4-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="de9a4-133">消費者介面自動化的用戶端應該針對可執行事件處理常式的執行緒使用 COM MTA 執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="de9a4-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="de9a4-134">使用單一執行緒的單元 (STA) 模型可能會造成問題，例如防止用戶端從執行緒移除事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="de9a4-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="de9a4-135">64位 Windows 上的 COM 單元親和性</span><span class="sxs-lookup"><span data-stu-id="de9a4-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="de9a4-136">根據 COM 規格，遠端物件的存留期是由呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數以建立物件的單元存留期來控管。</span><span class="sxs-lookup"><span data-stu-id="de9a4-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="de9a4-137">當原始的單元關閉時，也會釋放遠端物件。</span><span class="sxs-lookup"><span data-stu-id="de9a4-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="de9a4-138">針對消費者介面自動化用戶端，此 COM 行為可能表示32位專案所使用的 UIAutomationCore.dll) 所建立的遠端32/64 協助程式 (的存留期，是由建立元素之執行緒的單位存留期所控管。</span><span class="sxs-lookup"><span data-stu-id="de9a4-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="de9a4-139">如果消費者介面自動化用戶端將專案封送處理至另一個執行緒，則當原始的單元關閉時，該專案可能會失效。</span><span class="sxs-lookup"><span data-stu-id="de9a4-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="de9a4-140">消費者介面自動化的用戶端應該在使用封送處理的自動化專案時攔截錯誤，以正常方式處理這些問題。</span><span class="sxs-lookup"><span data-stu-id="de9a4-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="de9a4-141">具有64位元素的32位消費者介面自動化用戶端可能會發生相同的問題。</span><span class="sxs-lookup"><span data-stu-id="de9a4-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de9a4-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="de9a4-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="de9a4-143">**概念**</span><span class="sxs-lookup"><span data-stu-id="de9a4-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de9a4-144">取得 UI 自動化項目</span><span class="sxs-lookup"><span data-stu-id="de9a4-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="de9a4-145">訂閱消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="de9a4-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="de9a4-146">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="de9a4-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="de9a4-147">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="de9a4-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="de9a4-148">資訊： OLE 執行緒模型的描述和運作方式</span><span class="sxs-lookup"><span data-stu-id="de9a4-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 