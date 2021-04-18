---
description: 學習何時發生事件
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: 學習何時發生事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510178"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="b1131-103">學習何時發生事件</span><span class="sxs-lookup"><span data-stu-id="b1131-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="b1131-104">若要處理 DirectShow 事件，應用程式需要一種方法來找出佇列中的事件何時等候。</span><span class="sxs-lookup"><span data-stu-id="b1131-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="b1131-105">篩選圖形管理員提供兩種方式來執行此作業：</span><span class="sxs-lookup"><span data-stu-id="b1131-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="b1131-106">**視窗通知：** 每當有新的事件時，篩選圖形管理員就會將使用者定義的 Windows 訊息傳送至應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="b1131-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="b1131-107">**事件信號：** 如果佇列中有 DirectShow 事件，篩選圖形管理員會通知 Windows 事件，如果佇列是空的，則會重設事件。</span><span class="sxs-lookup"><span data-stu-id="b1131-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="b1131-108">應用程式可以使用這兩種技術。</span><span class="sxs-lookup"><span data-stu-id="b1131-108">An application can use either technique.</span></span> <span data-ttu-id="b1131-109">視窗通知通常更簡單。</span><span class="sxs-lookup"><span data-stu-id="b1131-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="b1131-110">**視窗通知**</span><span class="sxs-lookup"><span data-stu-id="b1131-110">**Window Notification**</span></span>

<span data-ttu-id="b1131-111">若要設定視窗通知，請呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) 方法，並指定私用訊息。</span><span class="sxs-lookup"><span data-stu-id="b1131-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="b1131-112">應用程式可以使用來自 WM 應用程式透過0xBFFF 的範圍中的訊息編號 \_ 作為私用訊息。</span><span class="sxs-lookup"><span data-stu-id="b1131-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="b1131-113">每當篩選圖形管理員在佇列中放置新的事件通知時，就會將此訊息張貼至指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="b1131-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="b1131-114">應用程式會從視窗的訊息迴圈內回應訊息。</span><span class="sxs-lookup"><span data-stu-id="b1131-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="b1131-115">下列程式碼範例顯示如何設定通知視窗。</span><span class="sxs-lookup"><span data-stu-id="b1131-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="b1131-116">此訊息是一般的 Windows 訊息，而且會與 DirectShow 事件通知佇列分開張貼。</span><span class="sxs-lookup"><span data-stu-id="b1131-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="b1131-117">這種方法的優點是大部分的應用程式都已執行訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="b1131-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="b1131-118">因此，您可以納入 DirectShow 事件處理，而不需要執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="b1131-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="b1131-119">下列程式碼範例顯示如何回應通知訊息的大綱。</span><span class="sxs-lookup"><span data-stu-id="b1131-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="b1131-120">如需完整的範例，請參閱 [回應事件](responding-to-events.md)。</span><span class="sxs-lookup"><span data-stu-id="b1131-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="b1131-121">由於事件通知和訊息迴圈都是非同步，因此在您的應用程式回應訊息時，佇列可能會包含一個以上的事件。</span><span class="sxs-lookup"><span data-stu-id="b1131-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="b1131-122">此外，如果事件變成無效，有時也可以從佇列中清除事件。</span><span class="sxs-lookup"><span data-stu-id="b1131-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="b1131-123">因此，在事件處理常式代碼中，呼叫 [**IAMMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 直到傳回失敗碼，表示佇列是空的。</span><span class="sxs-lookup"><span data-stu-id="b1131-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="b1131-124">釋放 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)指標之前，請使用 **Null** 指標呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)來取消事件通知。</span><span class="sxs-lookup"><span data-stu-id="b1131-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="b1131-125">在您的事件處理常式代碼中，檢查 **IMediaEventEx** 指標是否有效，然後再呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)。</span><span class="sxs-lookup"><span data-stu-id="b1131-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="b1131-126">這些步驟會防止可能發生的錯誤，在此情況下，應用程式會在發行 **IMediaEventEx** 指標之後接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="b1131-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="b1131-127">**事件信號**</span><span class="sxs-lookup"><span data-stu-id="b1131-127">**Event Signaling**</span></span>

<span data-ttu-id="b1131-128">篩選圖形管理員會保留手動重設事件，以反映事件佇列的狀態。</span><span class="sxs-lookup"><span data-stu-id="b1131-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="b1131-129">如果佇列包含暫止的事件通知，則篩選圖形管理員會發出手動重設事件的信號。</span><span class="sxs-lookup"><span data-stu-id="b1131-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="b1131-130">如果佇列是空的，則呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 方法會重設事件。</span><span class="sxs-lookup"><span data-stu-id="b1131-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="b1131-131">應用程式可以使用此事件來判斷佇列的狀態。</span><span class="sxs-lookup"><span data-stu-id="b1131-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="b1131-132">術語在此可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="b1131-132">The terminology can be confusing here.</span></span> <span data-ttu-id="b1131-133">手動重設事件是由 Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數所建立的事件種類;與 DirectShow 所定義的事件無關。</span><span class="sxs-lookup"><span data-stu-id="b1131-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="b1131-134">呼叫 [**IMediaEvent：： GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) 方法，以取得手動重設事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b1131-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="b1131-135">藉由呼叫 [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)之類的函式，等候事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="b1131-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="b1131-136">通知事件之後，請呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 來取得 DirectShow 事件。</span><span class="sxs-lookup"><span data-stu-id="b1131-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="b1131-137">下列程式碼範例說明此方法。</span><span class="sxs-lookup"><span data-stu-id="b1131-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="b1131-138">它會取得事件控制碼，然後以100毫秒的間隔等候事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="b1131-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="b1131-139">如果事件收到信號，就會呼叫 **GetEvent** ，並將事件程式碼和事件參數列印至主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="b1131-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="b1131-140">當執行 [**EC \_ 完成**](ec-complete.md) 事件（表示播放已完成）時，迴圈就會終止。</span><span class="sxs-lookup"><span data-stu-id="b1131-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="b1131-141">因為篩選圖形會在適當時自動設定或重設事件，所以您的應用程式不應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="b1131-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="b1131-142">此外，當您放開篩選圖形時，篩選圖形會關閉事件控制碼，因此請勿在該點之後使用事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="b1131-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
