---
description: 本文描述如何回應篩選圖形中所發生的事件。
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: 回應事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb0325af2e216a3679d3e15a293aa6bfe1c100f2271d089e982b295df791130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050558"
---
# <a name="responding-to-events"></a>回應事件

本文描述如何回應篩選圖形中所發生的事件。

## <a name="how-event-notification-works"></a>事件通知的運作方式

當 DirectShow 的應用程式正在執行時，事件可能會發生在篩選圖形內。 例如，篩選可能會遇到串流錯誤。 篩選準則會透過傳送事件（包含事件代碼和兩個事件參數）來警示篩選 Graph 管理員。 事件程式碼表示事件的類型，而事件參數則提供其他資訊。 參數的意義取決於事件代碼。 如需事件代碼的完整清單，請參閱 [事件通知碼](event-notification-codes.md)。

某些事件會由篩選 Graph 管理員以無訊息方式處理，而不會通知應用程式。 其他事件則會放在應用程式的佇列上。 視應用程式而定，您可能需要處理各種不同的事件。 本文著重于三個非常常見的事件：

-   [**EC \_ 完成**](ec-complete.md)事件表示播放正常完成。
-   [**EC \_ USERABORT**](ec-userabort.md)事件表示使用者已中斷播放。 如果使用者關閉影片視窗，影片轉譯器就會傳送此事件。
-   [**EC \_ ERRORABORT**](ec-errorabort.md)事件指出錯誤已導致播放暫停。

## <a name="using-event-notification"></a>使用事件通知

應用程式可以指示篩選 Graph 管理員，在發生新事件時，將 Windows 訊息傳送至指定的視窗。 這可讓應用程式在視窗的訊息迴圈內部回應。 首先，定義將傳送至應用程式視窗的訊息。 應用程式可以使用來自 WM 應用程式透過0xBFFF 的範圍中的訊息編號 \_ 作為私用訊息：


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



接下來，查詢 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)介面的篩選 Graph 管理員，然後呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)方法：


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



這個方法會指定指定的視窗 (g \_ hwnd) 作為訊息的收件者。 在您建立篩選圖形之後，但在執行圖形之前，請呼叫方法。

WM \_ GRAPHNOTIFY 是一般的 Windows 訊息。 每當篩選 Graph 管理員將新事件放在事件佇列時，它就會將 WM \_ GRAPHNOTIFY 訊息張貼到指定的應用程式視窗。 訊息的 *lParam* 參數等於 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)中的第三個參數。 此參數可讓您使用訊息傳送實例資料。 視窗訊息的 *wParam* 參數一律為零。

在應用程式的 **WindowProc** 函式中，為 WM GRAPHNOTIFY 訊息新增 case 語句 \_ ：


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



在事件處理常式函式中，呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 方法，以從佇列中取出事件：


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



[**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)方法會捕獲事件程式碼和兩個事件參數。 第四個 **GetEvent** 參數會指定等待事件的時間長度（以毫秒為單位）。 因為應用程式會呼叫此方法來回應 WM \_ GRAPHNOTIFY 訊息，所以事件已排入佇列。 因此，我們將超時值設定為零。

事件通知和訊息迴圈都是非同步，因此在您的應用程式回應訊息時，佇列可能會保留一個以上的事件。 此外，篩選 Graph 管理員可以從佇列中移除特定事件（如果它們變成無效）。 因此，您應該呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) ，直到它傳回失敗碼，表示佇列是空的。

在此範例中，應用程式會藉由叫用應用程式定義的清除函式來回應 [**EC \_ COMPLETE**](ec-complete.md)、 [**ec \_ USERABORT**](ec-userabort.md)和 [**ec \_ ERRORABORT**](ec-errorabort.md) ，這會導致應用程式正常結束。 此範例會忽略兩個事件參數。 在您抓取事件之後，請呼叫 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) ，以取得與事件參數相關聯的任何可用資源。

請注意， [**EC \_ 完成**](ec-complete.md) 事件不會造成篩選圖形停止。 應用程式可以停止或暫停圖形。 如果您停止圖形，則篩選會釋出它們所持有的任何資源。 如果您暫停圖形，篩選準則會繼續保留資源。 此外，當影片轉譯器暫停時，它會顯示最新框架的靜態影像。

釋放 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)指標之前，請使用 **Null** 視窗控制碼來呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) ，以取消事件通知：


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



在 WM \_ GRAPHNOTIFY 訊息處理常式中，請先檢查 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 指標，再呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)：


```C++
if (g_pEvent == NULL) return;
```



這可防止應用程式在釋放指標之後收到事件通知時可能發生的錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本 DirectShow 工作](basic-directshow-tasks.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 



