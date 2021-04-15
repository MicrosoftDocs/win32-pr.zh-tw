---
description: 執行搜尋列
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: 執行搜尋列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510214"
---
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="df7ce-103">執行搜尋列</span><span class="sxs-lookup"><span data-stu-id="df7ce-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="df7ce-104">本節說明如何針對媒體播放機應用程式執行搜尋列。</span><span class="sxs-lookup"><span data-stu-id="df7ce-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="df7ce-105">搜尋列會實作為提要欄位控制項。</span><span class="sxs-lookup"><span data-stu-id="df7ce-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="df7ce-106">如需在 DirectShow 中搜尋的總覽，請參閱 [搜尋篩選圖形](seeking-the-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="df7ce-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="df7ce-107">當應用程式啟動時，請將下列程式初始化：</span><span class="sxs-lookup"><span data-stu-id="df7ce-107">When the application starts, initialize the trackbar:</span></span>


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



<span data-ttu-id="df7ce-108">除非使用者開啟媒體檔案，否則會停用這些跟蹤。</span><span class="sxs-lookup"><span data-stu-id="df7ce-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="df7ce-109">從0到100的 [程式集] 範圍設定。</span><span class="sxs-lookup"><span data-stu-id="df7ce-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="df7ce-110">在檔案播放期間，應用程式會將播放位置計算為檔案持續時間的百分比，並據以更新這些程式。</span><span class="sxs-lookup"><span data-stu-id="df7ce-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="df7ce-111">例如，程式點位置 "50" 一律對應至檔案的中間。</span><span class="sxs-lookup"><span data-stu-id="df7ce-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="df7ce-112">當使用者開啟檔案時，請使用 **RenderFile** 建立檔案播放圖形。</span><span class="sxs-lookup"><span data-stu-id="df7ce-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="df7ce-113">此程式碼會顯示在 [如何播放](how-to-play-a-file.md)檔案中。</span><span class="sxs-lookup"><span data-stu-id="df7ce-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="df7ce-114">然後查詢 **IMediaSeeking** 介面的 [篩選圖形管理員]，並儲存介面指標：</span><span class="sxs-lookup"><span data-stu-id="df7ce-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="df7ce-115">若要判斷檔案是否可搜尋，請呼叫 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法或 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="df7ce-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="df7ce-116">這些方法幾乎是相同的，但它們的語法稍有不同。</span><span class="sxs-lookup"><span data-stu-id="df7ce-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="df7ce-117">下列範例會使用 **CheckCapabilites**：</span><span class="sxs-lookup"><span data-stu-id="df7ce-117">The following example uses **CheckCapabilites**:</span></span>


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



<span data-ttu-id="df7ce-118">AM \_ 搜尋 \_ CanSeekAbsolute 旗標會檢查原始程式檔是否可搜尋，而 am \_ 搜尋 \_ CanGetDuration 旗標會檢查檔案的持續時間是否可以事先決定。</span><span class="sxs-lookup"><span data-stu-id="df7ce-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="df7ce-119">如果同時支援這兩項功能，應用程式會啟用此類程式並抓取檔案持續時間。</span><span class="sxs-lookup"><span data-stu-id="df7ce-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="df7ce-120">如果圖表是可搜尋的，應用程式將會使用計時器來更新播放期間的程式段位置。</span><span class="sxs-lookup"><span data-stu-id="df7ce-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="df7ce-121">當您執行篩選圖形來播放檔案時，請呼叫其中一個 Windows 計時器函式（例如 **SetTimer**）來啟動計時器事件。</span><span class="sxs-lookup"><span data-stu-id="df7ce-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="df7ce-122">如需計時器的詳細資訊，請參閱 Platform SDK 中的「計時器」主題。</span><span class="sxs-lookup"><span data-stu-id="df7ce-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



<span data-ttu-id="df7ce-123">使用計時器事件來更新執行程式的位置。</span><span class="sxs-lookup"><span data-stu-id="df7ce-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="df7ce-124">呼叫 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 來取出 currant 播放位置，然後以檔案持續時間的百分比來計算位置：</span><span class="sxs-lookup"><span data-stu-id="df7ce-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



<span data-ttu-id="df7ce-125">使用者也可以移動 []，以搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="df7ce-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="df7ce-126">當使用者拖曳或按一下 [點擊] 控制項時，應用程式會收到 WM \_ HSCROLL 事件。</span><span class="sxs-lookup"><span data-stu-id="df7ce-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="df7ce-127">*WParam* 參數的低字組是「顯示」通知訊息。</span><span class="sxs-lookup"><span data-stu-id="df7ce-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="df7ce-128">例如，在 \_ [ENDTRACK] 動作結束時，會傳送 tb 的，而 \_ 在使用者拖曳這些狀態列時，會持續傳送 tb 的 THUMBTRACK。</span><span class="sxs-lookup"><span data-stu-id="df7ce-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="df7ce-129">下列程式碼顯示處理 WM HSCROLL 訊息的一種方式 \_ ：</span><span class="sxs-lookup"><span data-stu-id="df7ce-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



<span data-ttu-id="df7ce-130">如果使用者拖曳資料提示，應用程式會發出一系列的搜尋命令，每個 \_ 接收到的 THUMBTRACK 訊息都有一個。</span><span class="sxs-lookup"><span data-stu-id="df7ce-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="df7ce-131">為了讓搜尋作業盡可能順暢，應用程式會暫停圖形。</span><span class="sxs-lookup"><span data-stu-id="df7ce-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="df7ce-132">暫停圖形會中止播放，但會確保影片視窗已更新。</span><span class="sxs-lookup"><span data-stu-id="df7ce-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="df7ce-133">當應用程式收到 TB 的 \_ ENDTRACK 訊息時，它會將圖形還原為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="df7ce-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



