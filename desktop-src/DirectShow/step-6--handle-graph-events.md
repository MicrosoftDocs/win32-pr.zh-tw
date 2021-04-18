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
# <a name="step-6-handle-graph-events"></a>步驟6：處理圖形事件

本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟6。 完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。

當應用程式建立篩選圖形管理員的新實例時，應用程式會呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)。 這個方法會註冊應用程式視窗，以便從篩選圖形接收事件。


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



此值 `WM_GRAPH_EVENT` 為私用視窗訊息。 每當應用程式收到此訊息時，就會呼叫 `DShowPlayer::HandleGraphEvent` 方法。


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



`DShowPlayer::HandleGraphEvent` 方法會執行下列動作：

1.  在迴圈中呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ，以取得所有已排入佇列的事件。
2.   (*pfnOnGraphEvent*) 叫用回呼函數。
3.  呼叫 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) 來釋放與每個事件相關聯的資料。


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



下列程式碼顯示傳遞給的回呼函數 `DShowPlayer::HandleGraphEvent` 。 此函式會處理圖形事件的最小數目 ([**EC \_ COMPLETE**](ec-complete.md)、 [**ec \_ ERRORABORT**](ec-errorabort.md)和 [**EC \_ USERABORT**](ec-userabort.md)) ; 您可以擴充函數來處理其他事件。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 播放音訊/影片](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow 播放範例](directshow-playback-example.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> <dt>

[回應事件](responding-to-events.md)
</dt> </dl>

 

 



