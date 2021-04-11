---
description: 本主題說明如何在 Microsoft DirectShow 來源篩選器中執行搜尋。 它使用球形濾波器範例作為起點，並說明在此篩選準則中支援搜尋所需的其他程式碼。
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: 支援在來源篩選準則中搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852404"
---
# <a name="supporting-seeking-in-a-source-filter"></a>支援在來源篩選準則中搜尋

本主題說明如何在 Microsoft DirectShow 來源篩選器中執行搜尋。 它使用 [球形濾波器](ball-filter-sample.md) 範例作為起點，並說明在此篩選準則中支援搜尋所需的其他程式碼。

[球形濾波器](ball-filter-sample.md)範例是一種來源篩選器，可建立動畫彈跳球。 本文說明如何將搜尋功能新增到此篩選器。 加入這項功能之後，您就可以在 GraphEdit 中轉譯篩選，並藉由拖曳 GraphEdit 滑杆來控制球體。

本主題包含下列幾節：

-   [在 DirectShow 中搜尋的總覽](#overview-of-seeking-in-directshow)
-   [球形濾波器的快速概覽](#quick-overview-of-the-ball-filter)
-   [修改球篩選以進行搜尋](#modifying-the-ball-filter-for-seeking)
-   [CSourceSeeking 類別的限制](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>在 DirectShow 中搜尋的總覽

應用程式會藉由呼叫篩選圖形管理員上的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法來搜尋篩選圖形。 然後，篩選圖形管理員會將呼叫分散至圖形中的每個轉譯器。 每個轉譯器都會透過下一個上游篩選的輸出釘選，傳送呼叫上游。 呼叫會傳送上游，直到到達可執行 seek 命令的篩選準則（通常是來源篩選或剖析器篩選器）。 一般而言，產生時間戳記的篩選器也會處理搜尋。

篩選準則會回應搜尋命令，如下所示：

1.  篩選會排清圖形。 這會清除圖形中任何過時的資料，進而改善回應能力。 否則，在搜尋命令之前緩衝的範例可能會被傳遞。
2.  篩選準則會呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) ，以通知下游篩選新的停止時間、開始時間和播放速率。
3.  然後，篩選準則會在 seek 命令之後的第一個範例上設定不連續旗標。

時間戳記會在任何搜尋命令之後從零開始 (包括速率變更) 。

## <a name="quick-overview-of-the-ball-filter"></a>球形濾波器的快速概覽

球形濾波器是一個推播來源，這表示它會使用背景工作執行緒來傳遞下游範例，而不是提取來源，被動等候下游篩選要求範例。 球濾波器是從 [**CSource**](csource.md) 類別建立的，而其輸出圖釘是從 [**CSourceStream**](csourcestream.md) 類別建立的。 **CSourceStream** 類別會建立驅動資料流程程的背景工作執行緒。 這個執行緒會進入迴圈，從配置器取得範例、將資料填入資料，然後將它們傳遞給下游。

[**CSourceStream**](csourcestream.md)中的大部分動作都會發生在衍生類別所 [**執行的 CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md)方法中。 此方法的引數是要傳遞之範例的指標。 球濾波器的 **FillBuffer** 會抓取範例緩衝區的位址，並藉由設定個別圖元值，直接繪製到緩衝區。  (繪圖是由 helper 類別 CBall 完成，因此您可以忽略有關位深度、調色板等的詳細資料。 ) 

## <a name="modifying-the-ball-filter-for-seeking"></a>修改球篩選以進行搜尋

若要讓球篩選成為可搜尋，請使用 [**CSourceSeeking**](csourceseeking.md) 類別，其設計目的是要在篩選準則中使用一個輸出圖釘來執行搜尋。 將 **CSourceSeeking** 類別新增至 CBallStream 類別的繼承清單：


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



此外，您必須將 [**CSourceSeeking**](csourceseeking.md) 的初始化運算式加入至 CBallStream 的函式：


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



此語句會針對 [**CSourceSeeking**](csourceseeking.md)呼叫基底的函式。 這些參數是名稱、擁有釘選的指標、 **HRESULT** 值，以及重要區段物件的位址。 名稱只用于進行偵錯工具，而 [**name**](name.md) 宏會編譯為零售組建中的空字串。 Pin 會直接繼承 **CSourceSeeking**，因此第二個參數是指向其本身的指標，轉換成 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 指標。 在目前的基類版本中，會忽略 **HRESULT** 值;它會維持與舊版的相容性。 重要區段可保護共用資料，例如目前的開始時間、停止時間和播放速率。

在 [**CSourceSeeking**](csourceseeking.md) 的函式中新增下列語句：


```C++
m_rtStop = 60 * UNITS;
```



*M \_ rtStop* 變數會指定停止時間。 根據預設，此值為 \_ I64 \_ MAX/2，大約是14600年。 上一個語句會將它設定為更保守的60秒。

您必須將兩個額外的成員變數新增至 CBallStream：


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



在每個搜尋命令之後，篩選準則必須藉由呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)，在下一個範例上設定不中斷旗標。 *M \_ bDiscontinuity* 變數將會追蹤這個。 *M \_ rtBallPosition* 變數會指定球在影片框架中的位置。 原始球濾波器會計算來自資料流程時間的位置，但是資料流程時間會在每個搜尋命令之後重設為零。 在可搜尋的資料流程中，絕對位置與資料流程時間無關。

### <a name="queryinterface"></a>QueryInterface

[**CSourceSeeking**](csourceseeking.md)類別會實 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面。 若要將此介面公開給用戶端，請覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法：


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



方法稱為「NonDelegating」，因為 DirectShow 基類支援元件物件模型的方式 (COM) 匯總。 如需詳細資訊，請參閱 DirectShow SDK 中的「如何執行 IUnknown」主題。

### <a name="seeking-methods"></a>搜尋方法

[**CSourceSeeking**](csourceseeking.md)類別會維護數個與搜尋相關的成員變數。



| 變數          | 描述   | 預設值  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | 開始時間    | 零個           |
| *m \_ rtStop*       | 停止時間     | \_I64 \_ MAX/2 |
| *m \_ dRateSeeking* | 播放速率 | 1.0            |



 

[**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)的 [**CSourceSeeking**](csourceseeking.md)執行會更新開始和停止時間，然後在衍生的類別上呼叫兩個純虛擬方法 [**： CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)和 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)。 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)的實作為類似：它會更新播放速率，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)。 在這些虛擬方法中，pin 必須執行下列動作：

1.  呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 以開始排清資料。
2.  停止串流執行緒。
3.  呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)。
4.  重新開機串流執行緒。
5.  呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)。
6.  設定下一個範例的不連續旗標。

這些步驟的順序很重要，因為串流執行緒可能會在等候傳遞範例或取得新範例時封鎖。 [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)方法可確保不會封鎖串流執行緒，因此不會在步驟2中產生鎖死。 [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)呼叫會通知下游篩選器預期新的範例，因此當執行緒在步驟4中再次啟動時，不會拒絕它們。

下列私用方法會執行步驟1到4：


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



當串流執行緒再次開始時，它會呼叫 [**CSourceStream：： OnThreadStartPlay**](csourcestream-onthreadstartplay.md) 方法。 覆寫此方法以執行步驟5和6：


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



在 [**ChangeStart**](csourceseeking-changestart.md) 方法中，將資料流程時間設定為零，並將球的位置設定為新的開始時間。 然後呼叫 CBallStream：： UpdateFromSeek：


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



在 [**ChangeStop**](csourceseeking-changestop.md) 方法中，如果新的停止時間小於目前的位置，請呼叫 CBallStream：： UpdateFromSeek。 否則，停止時間仍在未來，因此不需要排清圖形。


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



針對速率變更， [**CSourceSeeking：： SetRate**](csourceseeking-setrate.md) 方法會將 *m \_ dRateSeeking* 設定為新的速率， (在它呼叫 [**ChangeRate**](csourceseeking-changerate.md)之前捨棄舊值) 。 可惜的是，如果呼叫者給予的速率無效（例如，小於零），則會在呼叫 **ChangeRate** 時延遲太晚。 其中一個解決方案是覆寫 **SetRate** 並檢查有效的費率：


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a>在緩衝區中繪圖

以下是 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md)的修改版本，此常式會在每個畫面格上繪製球：


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



此版本和原始版本之間的主要差異如下：

-   如先前所述， *m \_ rtBallPosition* 變數用來設定球的位置，而不是資料流程時間。
-   在保存重要區段之後，方法會檢查目前的位置是否超過停止時間。 如果是，則會 **傳回 \_ FALSE**，表示基類停止傳送資料並傳遞資料流程結束通知。
-   時間戳記會除以目前的速率。
-   如果 *m \_ BDiscontinuity* 為 **TRUE**，則方法會在範例上設定不中斷旗標。

還有另一個小差異。 因為原始版本依賴只有一個緩衝區，所以它會在串流處理開始時，將零次填滿整個緩衝區。 之後，它只會從先前的位置清除球。 不過，這項優化會在球濾波器中顯示稍微錯誤的錯誤。 當 [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md) 方法呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)時，它會將唯讀旗標設為 **FALSE**。 因此，下游篩選器可自由寫入緩衝區。 其中一個解決方法是覆寫 **DecideAllocator** ，讓它將唯讀旗標設為 **TRUE**。 但為了簡單起見，新版本只會移除優化。 相反地，此版本每次都會以零填滿緩衝區。

### <a name="miscellaneous-changes"></a>其他變更

在新版本中，這兩行會從 CBall 的函式移除：


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



原始球形濾波器會使用這些值，將一些隨機性新增至初始球的位置。 基於我們的目的，我們希望球具有決定性。 此外，有些變數已經從 [**CRefTime**](creftime.md) 物件變更為 [**參考 \_ 時間**](reference-time.md) 變數。  (**CRefTime** 類別是 **參考 \_ 時間** 值的精簡型包裝函式。 ) 最後， [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 的實值已稍微修改; 您可以參考原始程式碼以取得詳細資料。

## <a name="limitations-of-the-csourceseeking-class"></a>CSourceSeeking 類別的限制

[**CSourceSeeking**](csourceseeking.md)類別不適用於具有多個輸出圖釘的篩選，因為有跨 pin 通訊的問題。 例如，假設剖析器篩選器會接收交錯式音訊影片串流、將資料流程分割成音訊和影片元件，並從另一個輸出圖釘和音訊傳遞影片。 這兩個輸出接點都會接收每個搜尋命令，但是篩選準則應該只搜尋每個 seek 命令一次。 解決方法是指定其中一個 pin 來控制搜尋，並忽略其他 pin 所接收的搜尋命令。

不過，在 seek 命令之後，這兩個圖釘都應該排清資料。 為了更複雜一點，seek 命令會在應用程式執行緒上發生，而不是在串流執行緒上進行。 因此，您必須確定未封鎖任何 pin，並等待 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 呼叫傳回，否則可能會造成鎖死。 如需有關 pin 中安全線程排清的詳細資訊，請參閱 [執行緒和重要區段](threads-and-critical-sections.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寫入來源篩選](writing-source-filters.md)
</dt> </dl>

 

 



