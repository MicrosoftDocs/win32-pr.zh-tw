---
description: 寫入檔案
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: 寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995826"
---
# <a name="writing-the-file"></a><span data-ttu-id="e27b6-103">寫入檔案</span><span class="sxs-lookup"><span data-stu-id="e27b6-103">Writing the File</span></span>

<span data-ttu-id="e27b6-104">若要寫入檔案，只要呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法，即可執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e27b6-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="e27b6-105">等候播放完成，並呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)，以明確地停止圖形。否則，不會正確寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="e27b6-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="e27b6-106">若要顯示檔案寫入作業的進度，請查詢 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的 Mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="e27b6-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="e27b6-107">呼叫 [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法，以取得檔案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e27b6-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="e27b6-108">當圖形正在執行時，會定期呼叫 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法，以抓取圖形在資料流程中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="e27b6-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="e27b6-109">依持續時間劃分的目前位置會讓百分比完成。</span><span class="sxs-lookup"><span data-stu-id="e27b6-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="e27b6-110">應用程式通常會查詢篩選圖形管理員以進行 **IMediaSeeking**，但是檔案寫入是此規則的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e27b6-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="e27b6-111">篩選圖形管理員會從開始位置和圖形執行的時間計算出目前的位置，這對檔案播放而言是正確的，但無法寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="e27b6-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="e27b6-112">因此，若要取得精確的結果，您應該從 MUX 篩選器取出位置。</span><span class="sxs-lookup"><span data-stu-id="e27b6-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="e27b6-113">下列程式碼會取得檔案的持續時間、啟動計時器以更新應用程式 UI，以及執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e27b6-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="e27b6-114">為了清楚起見，會忽略 (錯誤檢查。 ) </span><span class="sxs-lookup"><span data-stu-id="e27b6-114">(Error checking is omitted for clarity.)</span></span>


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



<span data-ttu-id="e27b6-115">當應用程式收到計時器事件時，它可以使用目前的位置來更新 UI：</span><span class="sxs-lookup"><span data-stu-id="e27b6-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


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



<span data-ttu-id="e27b6-116">當應用程式收到 DirectShow 完成事件時，它應該會停止圖形，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="e27b6-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


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



 

 



