---
description: 本文描述如何回應篩選圖形中所發生的事件。
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: 回應事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510011"
---
# <a name="responding-to-events"></a><span data-ttu-id="85453-103">回應事件</span><span class="sxs-lookup"><span data-stu-id="85453-103">Responding to Events</span></span>

<span data-ttu-id="85453-104">本文描述如何回應篩選圖形中所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="85453-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="85453-105">事件通知的運作方式</span><span class="sxs-lookup"><span data-stu-id="85453-105">How Event Notification Works</span></span>

<span data-ttu-id="85453-106">當 DirectShow 應用程式正在執行時，事件可能會發生在篩選圖形內。</span><span class="sxs-lookup"><span data-stu-id="85453-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="85453-107">例如，篩選可能會遇到串流錯誤。</span><span class="sxs-lookup"><span data-stu-id="85453-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="85453-108">篩選器會藉由傳送事件（由事件程式碼和兩個事件參數組成）來警示篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="85453-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="85453-109">事件程式碼表示事件的類型，而事件參數則提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="85453-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="85453-110">參數的意義取決於事件代碼。</span><span class="sxs-lookup"><span data-stu-id="85453-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="85453-111">如需事件代碼的完整清單，請參閱 [事件通知碼](event-notification-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="85453-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="85453-112">某些事件會由篩選圖形管理員以無訊息方式處理，而不會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="85453-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="85453-113">其他事件則會放在應用程式的佇列上。</span><span class="sxs-lookup"><span data-stu-id="85453-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="85453-114">視應用程式而定，您可能需要處理各種不同的事件。</span><span class="sxs-lookup"><span data-stu-id="85453-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="85453-115">本文著重于三個非常常見的事件：</span><span class="sxs-lookup"><span data-stu-id="85453-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="85453-116">[**EC \_ 完成**](ec-complete.md)事件表示播放正常完成。</span><span class="sxs-lookup"><span data-stu-id="85453-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="85453-117">[**EC \_ USERABORT**](ec-userabort.md)事件表示使用者已中斷播放。</span><span class="sxs-lookup"><span data-stu-id="85453-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="85453-118">如果使用者關閉影片視窗，影片轉譯器就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="85453-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="85453-119">[**EC \_ ERRORABORT**](ec-errorabort.md)事件指出錯誤已導致播放暫停。</span><span class="sxs-lookup"><span data-stu-id="85453-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="85453-120">使用事件通知</span><span class="sxs-lookup"><span data-stu-id="85453-120">Using Event Notification</span></span>

<span data-ttu-id="85453-121">應用程式可以指示篩選圖形管理員在發生新事件時，將 Windows 訊息傳送至指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="85453-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="85453-122">這可讓應用程式在視窗的訊息迴圈內部回應。</span><span class="sxs-lookup"><span data-stu-id="85453-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="85453-123">首先，定義將傳送至應用程式視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="85453-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="85453-124">應用程式可以使用來自 WM 應用程式透過0xBFFF 的範圍中的訊息編號 \_ 作為私用訊息：</span><span class="sxs-lookup"><span data-stu-id="85453-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="85453-125">接下來，查詢 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面的篩選圖形管理員，然後呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) 方法：</span><span class="sxs-lookup"><span data-stu-id="85453-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="85453-126">這個方法會指定指定的視窗 (g \_ hwnd) 作為訊息的收件者。</span><span class="sxs-lookup"><span data-stu-id="85453-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="85453-127">在您建立篩選圖形之後，但在執行圖形之前，請呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="85453-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="85453-128">WM \_ GRAPHNOTIFY 是一般的 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="85453-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="85453-129">每當篩選圖形管理員將新事件放在事件佇列時，它就會將 WM \_ GRAPHNOTIFY 訊息張貼到指定的應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="85453-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="85453-130">訊息的 *lParam* 參數等於 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)中的第三個參數。</span><span class="sxs-lookup"><span data-stu-id="85453-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="85453-131">此參數可讓您使用訊息傳送實例資料。</span><span class="sxs-lookup"><span data-stu-id="85453-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="85453-132">視窗訊息的 *wParam* 參數一律為零。</span><span class="sxs-lookup"><span data-stu-id="85453-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="85453-133">在應用程式的 **WindowProc** 函式中，為 WM GRAPHNOTIFY 訊息新增 case 語句 \_ ：</span><span class="sxs-lookup"><span data-stu-id="85453-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="85453-134">在事件處理常式函式中，呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 方法，以從佇列中取出事件：</span><span class="sxs-lookup"><span data-stu-id="85453-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="85453-135">[**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)方法會捕獲事件程式碼和兩個事件參數。</span><span class="sxs-lookup"><span data-stu-id="85453-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="85453-136">第四個 **GetEvent** 參數會指定等待事件的時間長度（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="85453-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="85453-137">因為應用程式會呼叫此方法來回應 WM \_ GRAPHNOTIFY 訊息，所以事件已排入佇列。</span><span class="sxs-lookup"><span data-stu-id="85453-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="85453-138">因此，我們將超時值設定為零。</span><span class="sxs-lookup"><span data-stu-id="85453-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="85453-139">事件通知和訊息迴圈都是非同步，因此在您的應用程式回應訊息時，佇列可能會保留一個以上的事件。</span><span class="sxs-lookup"><span data-stu-id="85453-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="85453-140">此外，篩選圖形管理員可以從佇列中移除特定事件（如果它們變成無效）。</span><span class="sxs-lookup"><span data-stu-id="85453-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="85453-141">因此，您應該呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ，直到它傳回失敗碼，表示佇列是空的。</span><span class="sxs-lookup"><span data-stu-id="85453-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="85453-142">在此範例中，應用程式會藉由叫用應用程式定義的清除函式來回應 [**EC \_ COMPLETE**](ec-complete.md)、 [**ec \_ USERABORT**](ec-userabort.md)和 [**ec \_ ERRORABORT**](ec-errorabort.md) ，這會導致應用程式正常結束。</span><span class="sxs-lookup"><span data-stu-id="85453-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="85453-143">此範例會忽略兩個事件參數。</span><span class="sxs-lookup"><span data-stu-id="85453-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="85453-144">在您抓取事件之後，請呼叫 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) ，以取得與事件參數相關聯的任何可用資源。</span><span class="sxs-lookup"><span data-stu-id="85453-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="85453-145">請注意， [**EC \_ 完成**](ec-complete.md) 事件不會造成篩選圖形停止。</span><span class="sxs-lookup"><span data-stu-id="85453-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="85453-146">應用程式可以停止或暫停圖形。</span><span class="sxs-lookup"><span data-stu-id="85453-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="85453-147">如果您停止圖形，則篩選會釋出它們所持有的任何資源。</span><span class="sxs-lookup"><span data-stu-id="85453-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="85453-148">如果您暫停圖形，篩選準則會繼續保留資源。</span><span class="sxs-lookup"><span data-stu-id="85453-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="85453-149">此外，當影片轉譯器暫停時，它會顯示最新框架的靜態影像。</span><span class="sxs-lookup"><span data-stu-id="85453-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="85453-150">釋放 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)指標之前，請使用 **Null** 視窗控制碼來呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) ，以取消事件通知：</span><span class="sxs-lookup"><span data-stu-id="85453-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="85453-151">在 WM \_ GRAPHNOTIFY 訊息處理常式中，請先檢查 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 指標，再呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)：</span><span class="sxs-lookup"><span data-stu-id="85453-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="85453-152">這可防止應用程式在釋放指標之後收到事件通知時可能發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="85453-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85453-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="85453-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85453-154">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="85453-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="85453-155">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="85453-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



