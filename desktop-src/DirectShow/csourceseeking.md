---
description: CSourceSeeking 類別是一個抽象類別，可在來源篩選準則中使用一個輸出圖釘來執行搜尋。
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: 'CSourceSeeking 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993377"
---
# <a name="csourceseeking-class"></a>CSourceSeeking 類別

![csourceseeking 類別階層](images/cutil15.png)

**CSourceSeeking** 類別是一個抽象類別，可在來源篩選準則中使用一個輸出圖釘來執行搜尋。

這個類別支援 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。 它會提供所有 **IMediaSeeking** 方法的預設執行。 受保護的成員變數會儲存開始時間、停止時間和目前的速率。 依預設，類別所支援的唯一時間格式是 **時間 \_ 格式 \_ 媒體 \_ 時間** (100-毫微秒單位) 。 如需詳細資訊，請參閱「備註」。



| 受保護的成員變數                                          | Description                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**m \_ rtDuration**](csourceseeking-m-rtduration.md)                | 資料流程的持續時間。                                                                     |
| [**m \_ rtStart**](csourceseeking-m-rtstart.md)                      | 開始時間。                                                                                 |
| [**m \_ rtStop**](csourceseeking-m-rtstop.md)                        | 停止時間。                                                                                  |
| [**m \_ dRateSeeking**](csourceseeking-m-drateseeking.md)            | 播放速率。                                                                              |
| [**m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md)          | 搜尋功能。                                                                       |
| [**m \_ pLock**](csourceseeking-m-plock.md)                          | 要鎖定之重要區段物件的指標。                                           |
| 保護方法                                                   | Description                                                                                 |
| [**CSourceSeeking**](csourceseeking-csourceseeking.md)             | 函式方法。                                                                         |
| 純虛擬方法                                                | Description                                                                                 |
| [**ChangeRate**](csourceseeking-changerate.md)                     | 當播放速率變更時呼叫。                                                      |
| [**ChangeStart**](csourceseeking-changestart.md)                   | 開始位置變更時呼叫。                                                     |
| [**ChangeStop**](csourceseeking-changestop.md)                     | 在停止位置變更時呼叫。                                                      |
| IMediaSeeking 方法                                               | Description                                                                                 |
| [**IsFormatSupported**](csourceseeking-isformatsupported.md)       | 判斷是否支援指定的時間格式。                                    |
| [**QueryPreferredFormat**](csourceseeking-querypreferredformat.md) | 抓取物件的慣用時間格式。                                               |
| [**SetTimeFormat**](csourceseeking-settimeformat.md)               | 設定時間格式。                                                                       |
| [**IsUsingTimeFormat**](csourceseeking-isusingtimeformat.md)       | 判斷指定的時間格式是否為目前使用中的格式。                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | 抓取目前的時間格式。                                                          |
| [**GetDuration**](csourceseeking-getduration.md)                   | 捕獲資料流程的持續時間。                                                       |
| [**GetStopPosition**](csourceseeking-getstopposition.md)           | 抓取將停止播放的時間（相對於資料流程的持續時間）。 |
| [**GetCurrentPosition**](csourceseeking-getcurrentposition.md)     | 抓取目前的位置，相對於資料流程的總持續時間。               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | 抓取資料流程的所有搜尋功能。                                       |
| [**CheckCapabilities**](csourceseeking-checkcapabilities.md)       | 查詢資料流程是否已指定搜尋功能。                              |
| [**ConvertTimeFormat**](csourceseeking-converttimeformat.md)       | 從一種時間格式轉換成另一種格式。                                                   |
| [**SetPositions**](csourceseeking-setpositions.md)                 | 設定目前的位置和停止位置。                                            |
| [**GetPositions**](csourceseeking-getpositions.md)                 | 抓取目前的位置和停止位置。                                       |
| [**GetAvailable**](csourceseeking-getavailable.md)                 | 抓取搜尋有效的時間範圍。                                 |
| [**SetRate**](csourceseeking-setrate.md)                           | 設定播放速率。                                                                     |
| [**GetRate**](csourceseeking-getrate.md)                           | 捕獲播放速率。                                                                |
| [**GetPreroll**](csourceseeking-getpreroll.md)                     | 捕獲預先進行的時間。                                                                 |



 

## <a name="remarks"></a>備註

只要開始位置、停止位置或播放速率變更， **CSourceSeeking** 物件就會呼叫對應的純虛擬方法：

-   開始位置： [ **CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)
-   停止位置： [ **CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)
-   播放速率： [ **CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)

衍生的類別必須執行這些方法。 進行任何搜尋作業之後，篩選準則必須執行下列動作：

1.  在下游輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。
2.  中止傳遞資料的工作者執行緒。
3.  在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。
4.  重新開機背景工作執行緒。
5.  在輸入 pin 上呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。
6.  設定第一個範例的不連續屬性。 呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法。

如果執行緒已封鎖等候傳遞範例，則呼叫 [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 會釋出工作者執行緒。

在步驟2中，請確定執行緒已停止傳送資料。 根據執行的不同，您可能需要等候執行緒結束，或讓執行緒發出某種類型的回應。 如果您的篩選使用 [**CSourceStream**](csourcestream.md) 類別， [**CSourceStream：： Stop**](csourcestream-stop.md) 方法會封鎖，直到背景工作執行緒回復為止。

在理想情況下，應該從背景工作執行緒傳遞新的區段 (步驟 5) 。 它也可以透過 **CSourceSeeking** 物件來完成，只要篩選會以範例序列化它即可。

下列範例顯示可能的執行。 它會假設來源篩選器的輸出圖釘衍生自 **CSourceSeeking** 和 [**CSourceStream**](csourcestream.md)。 這個範例會定義可執行步驟 1 4 的 helper 方法 UpdateFromSeek。 覆寫 [**CSourceStream：： OnThreadStartPlay**](csourcestream-onthreadstartplay.md) 方法以傳送新的區段，並設定指出不中斷的旗標。 背景工作執行緒會挑選此旗標，並呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法：


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a>支援其他時間格式

根據預設，這個類別僅支援以參考時間的單位來搜尋 (時間 \_ 格式的 \_ 媒體 \_ 時間) 。 若要支援其他時間格式，請覆寫處理時間格式的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法：

-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

此外，請覆寫其餘的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法，以在時間格式之間執行必要的轉換。 在呼叫 [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法之後，所有的 **IMediaSeeking** 方法都必須將傳入和傳出的時間參數視為新的時間格式。 例如，如果 *m \_ rtDuration* 變數以參考時間的單位來代表持續時間，但目前的時間格式為框架，則 [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法必須傳回轉換成框架的值 *m \_ rtDuration* 。 例如：


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



此外，請務必 \_ \_ 在 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法中檢查 AM 搜尋 ReturnTime 旗標。 如果出現此旗標，請將位置值轉換為參考時間，然後將它們傳回給呼叫端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[支援在來源篩選準則中搜尋](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




