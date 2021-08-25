---
description: 寫入檔案
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: 寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cabb5575f371c6525e58cc8ede7d05c2701acc31be325af46e3b00e6e2d8d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051397"
---
# <a name="writing-the-file"></a>寫入檔案

若要寫入檔案，只要呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法，即可執行篩選圖形。 等候播放完成，並呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)，以明確地停止圖形。否則，不會正確寫入檔案。

若要顯示檔案寫入作業的進度，請查詢 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的 Mux 篩選器。 呼叫 [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法，以取得檔案的持續時間。 當圖形正在執行時，會定期呼叫 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法，以抓取圖形在資料流程中的目前位置。 依持續時間劃分的目前位置會讓百分比完成。

> [!Note]  
> 應用程式通常會查詢篩選 Graph 管理員以進行 **IMediaSeeking**，但是檔案寫入是此規則的例外狀況。 篩選 Graph 管理員會從開始位置和圖形執行的時間計算出目前的位置，這對檔案播放而言是正確的，但無法寫入檔案。 因此，若要取得精確的結果，您應該從 MUX 篩選器取出位置。

 

下列程式碼會取得檔案的持續時間、啟動計時器以更新應用程式 UI，以及執行篩選圖形。 為了清楚起見，會忽略 (錯誤檢查。 ) 


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



當應用程式收到計時器事件時，它可以使用目前的位置來更新 UI：


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



當應用程式收到 DirectShow 完成事件時，它應該會停止圖形，如下列程式碼所示：


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



