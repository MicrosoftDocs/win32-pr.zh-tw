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
# <a name="implementing-a-seek-bar"></a>執行搜尋列

本節說明如何針對媒體播放機應用程式執行搜尋列。 搜尋列會實作為提要欄位控制項。 如需在 DirectShow 中搜尋的總覽，請參閱 [搜尋篩選圖形](seeking-the-filter-graph.md)。

當應用程式啟動時，請將下列程式初始化：


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



除非使用者開啟媒體檔案，否則會停用這些跟蹤。 從0到100的 [程式集] 範圍設定。 在檔案播放期間，應用程式會將播放位置計算為檔案持續時間的百分比，並據以更新這些程式。 例如，程式點位置 "50" 一律對應至檔案的中間。

當使用者開啟檔案時，請使用 **RenderFile** 建立檔案播放圖形。 此程式碼會顯示在 [如何播放](how-to-play-a-file.md)檔案中。 然後查詢 **IMediaSeeking** 介面的 [篩選圖形管理員]，並儲存介面指標：


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



若要判斷檔案是否可搜尋，請呼叫 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法或 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。 這些方法幾乎是相同的，但它們的語法稍有不同。 下列範例會使用 **CheckCapabilites**：


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



AM \_ 搜尋 \_ CanSeekAbsolute 旗標會檢查原始程式檔是否可搜尋，而 am \_ 搜尋 \_ CanGetDuration 旗標會檢查檔案的持續時間是否可以事先決定。 如果同時支援這兩項功能，應用程式會啟用此類程式並抓取檔案持續時間。

如果圖表是可搜尋的，應用程式將會使用計時器來更新播放期間的程式段位置。 當您執行篩選圖形來播放檔案時，請呼叫其中一個 Windows 計時器函式（例如 **SetTimer**）來啟動計時器事件。 如需計時器的詳細資訊，請參閱 Platform SDK 中的「計時器」主題。


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



使用計時器事件來更新執行程式的位置。 呼叫 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 來取出 currant 播放位置，然後以檔案持續時間的百分比來計算位置：


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



使用者也可以移動 []，以搜尋檔案。 當使用者拖曳或按一下 [點擊] 控制項時，應用程式會收到 WM \_ HSCROLL 事件。 *WParam* 參數的低字組是「顯示」通知訊息。 例如，在 \_ [ENDTRACK] 動作結束時，會傳送 tb 的，而 \_ 在使用者拖曳這些狀態列時，會持續傳送 tb 的 THUMBTRACK。 下列程式碼顯示處理 WM HSCROLL 訊息的一種方式 \_ ：


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



如果使用者拖曳資料提示，應用程式會發出一系列的搜尋命令，每個 \_ 接收到的 THUMBTRACK 訊息都有一個。 為了讓搜尋作業盡可能順暢，應用程式會暫停圖形。 暫停圖形會中止播放，但會確保影片視窗已更新。 當應用程式收到 TB 的 \_ ENDTRACK 訊息時，它會將圖形還原為其原始狀態。

 

 



