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
# <a name="learning-when-an-event-occurs"></a>學習何時發生事件

若要處理 DirectShow 事件，應用程式需要一種方法來找出佇列中的事件何時等候。 篩選圖形管理員提供兩種方式來執行此作業：

-   **視窗通知：** 每當有新的事件時，篩選圖形管理員就會將使用者定義的 Windows 訊息傳送至應用程式視窗。
-   **事件信號：** 如果佇列中有 DirectShow 事件，篩選圖形管理員會通知 Windows 事件，如果佇列是空的，則會重設事件。

應用程式可以使用這兩種技術。 視窗通知通常更簡單。

**視窗通知**

若要設定視窗通知，請呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) 方法，並指定私用訊息。 應用程式可以使用來自 WM 應用程式透過0xBFFF 的範圍中的訊息編號 \_ 作為私用訊息。 每當篩選圖形管理員在佇列中放置新的事件通知時，就會將此訊息張貼至指定的視窗。 應用程式會從視窗的訊息迴圈內回應訊息。

下列程式碼範例顯示如何設定通知視窗。


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



此訊息是一般的 Windows 訊息，而且會與 DirectShow 事件通知佇列分開張貼。 這種方法的優點是大部分的應用程式都已執行訊息迴圈。 因此，您可以納入 DirectShow 事件處理，而不需要執行其他工作。

下列程式碼範例顯示如何回應通知訊息的大綱。 如需完整的範例，請參閱 [回應事件](responding-to-events.md)。


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



由於事件通知和訊息迴圈都是非同步，因此在您的應用程式回應訊息時，佇列可能會包含一個以上的事件。 此外，如果事件變成無效，有時也可以從佇列中清除事件。 因此，在事件處理常式代碼中，呼叫 [**IAMMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 直到傳回失敗碼，表示佇列是空的。

釋放 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)指標之前，請使用 **Null** 指標呼叫 [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)來取消事件通知。 在您的事件處理常式代碼中，檢查 **IMediaEventEx** 指標是否有效，然後再呼叫 [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)。 這些步驟會防止可能發生的錯誤，在此情況下，應用程式會在發行 **IMediaEventEx** 指標之後接收事件通知。

**事件信號**

篩選圖形管理員會保留手動重設事件，以反映事件佇列的狀態。 如果佇列包含暫止的事件通知，則篩選圖形管理員會發出手動重設事件的信號。 如果佇列是空的，則呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 方法會重設事件。 應用程式可以使用此事件來判斷佇列的狀態。

> [!Note]  
> 術語在此可能會造成混淆。 手動重設事件是由 Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數所建立的事件種類;與 DirectShow 所定義的事件無關。

 

呼叫 [**IMediaEvent：： GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) 方法，以取得手動重設事件的控制碼。 藉由呼叫 [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)之類的函式，等候事件發出信號。 通知事件之後，請呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 來取得 DirectShow 事件。

下列程式碼範例說明此方法。 它會取得事件控制碼，然後以100毫秒的間隔等候事件收到信號。 如果事件收到信號，就會呼叫 **GetEvent** ，並將事件程式碼和事件參數列印至主控台視窗。 當執行 [**EC \_ 完成**](ec-complete.md) 事件（表示播放已完成）時，迴圈就會終止。


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



因為篩選圖形會在適當時自動設定或重設事件，所以您的應用程式不應該這麼做。 此外，當您放開篩選圖形時，篩選圖形會關閉事件控制碼，因此請勿在該點之後使用事件控制碼。

 

 
