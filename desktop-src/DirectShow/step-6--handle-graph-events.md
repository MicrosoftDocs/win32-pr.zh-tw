---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟6。
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 步驟6：處理圖形事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971533"
---
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="eb523-103">步驟6：處理圖形事件</span><span class="sxs-lookup"><span data-stu-id="eb523-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="eb523-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟6。</span><span class="sxs-lookup"><span data-stu-id="eb523-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="eb523-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="eb523-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="eb523-106">當應用程式建立篩選圖形管理員的新實例時，應用程式會呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)。</span><span class="sxs-lookup"><span data-stu-id="eb523-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="eb523-107">這個方法會註冊應用程式視窗，以便從篩選圖形接收事件。</span><span class="sxs-lookup"><span data-stu-id="eb523-107">This method registers the application window to receive events from the filter graph.</span></span>


```C++
    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="eb523-108">此值 `WM_GRAPH_EVENT` 為私用視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="eb523-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="eb523-109">每當應用程式收到此訊息時，就會呼叫 `DShowPlayer::HandleGraphEvent` 方法。</span><span class="sxs-lookup"><span data-stu-id="eb523-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="eb523-110">`DShowPlayer::HandleGraphEvent` 方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="eb523-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="eb523-111">在迴圈中呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ，以取得所有已排入佇列的事件。</span><span class="sxs-lookup"><span data-stu-id="eb523-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="eb523-112"> (*pfnOnGraphEvent*) 叫用回呼函數。</span><span class="sxs-lookup"><span data-stu-id="eb523-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="eb523-113">呼叫 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) 來釋放與每個事件相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="eb523-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



<span data-ttu-id="eb523-114">下列程式碼顯示傳遞給的回呼函數 `DShowPlayer::HandleGraphEvent` 。</span><span class="sxs-lookup"><span data-stu-id="eb523-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="eb523-115">此函式會處理圖形事件的最小數目 ([**EC \_ COMPLETE**](ec-complete.md)、 [**ec \_ ERRORABORT**](ec-errorabort.md)和 [**EC \_ USERABORT**](ec-userabort.md)) ; 您可以擴充函數來處理其他事件。</span><span class="sxs-lookup"><span data-stu-id="eb523-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="eb523-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb523-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb523-117">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="eb523-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="eb523-118">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="eb523-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="eb523-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="eb523-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="eb523-120">回應事件</span><span class="sxs-lookup"><span data-stu-id="eb523-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



