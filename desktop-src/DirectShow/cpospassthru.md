---
description: CPosPassThru 類別會處理轉換篩選的搜尋命令，方法是將它們傳遞給下一個篩選準則。
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: 'CPosPassThru 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984075"
---
# <a name="cpospassthru-class"></a>CPosPassThru 類別

![cpospassthru 基類階層](images/cutil14.png)

`CPosPassThru`類別會處理轉換篩選的搜尋命令，方法是將它們傳遞給下一個篩選準則。

當應用程式搜尋篩選圖形時，篩選圖形管理員會向轉譯器篩選提供搜尋命令。 此命令會透過每個篩選器的輸出釘選上游傳遞，直到達到可執行命令 (的篩選準則（如果有任何) ）。 如需詳細資訊，請參閱 [搜尋](seeking.md)。 類別會將 `CPosPassThru` 所有搜尋命令傳遞至上游篩選器上的輸出圖釘，如下圖所示。

![cpospassthru 類別會傳送上游的搜尋命令。](images/cpospassthru.png)

雖然此類別是在基類庫中提供的，但 DirectShow 也會在 Quartz.dll 中提供相同的類別。 使用 Quartz.dll 版本可以稍微減少篩選中的程式碼大小，因為類別是在執行時間從 DLL 載入的。 若要使用該版本，請呼叫 [**CreatePosPassThru**](createpospassthru.md) 函數。

在輸出釘選的 **NonDelegatingQueryInterface** 方法中，每當要求的介面是 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)或 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)時，委派給 **CPosPassThru** 物件，如下列程式碼所示：


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



除非有注明，否則這個類別中的所有 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法都會呼叫連接的釘選上的對應方法，並傳回結果。



| 公用方法                                                    | Description                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | 函式方法。                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | 已過時。                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | 抓取目前樣本上的時間戳記。 虛擬。                                           |
| IMediaPosition 方法                                            | Description                                                                                         |
| [**取得 \_ 持續時間**](cpospassthru-get-duration.md)                | 捕獲資料流程的持續時間。                                                               |
| [**put \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | 設定目前的位置，相對於資料流程的總持續時間。                            |
| [**取得 \_ StopTime**](cpospassthru-get-stoptime.md)                | 抓取將停止播放的時間（相對於資料流程的持續時間）。         |
| [**put \_ StopTime**](cpospassthru-put-stoptime.md)                | 設定播放將停止的時間，相對於資料流程的持續時間。              |
| [**取得 \_ PrerollTime**](cpospassthru-get-prerolltime.md)          | 抓取在開始位置之前將排入佇列的資料量。                         |
| [**put \_ PrerollTime**](cpospassthru-put-prerolltime.md)          | 設定要在開始位置之前排入佇列的資料量。                              |
| [**取得 \_ 率**](cpospassthru-get-rate.md)                        | 捕獲播放速率。                                                                        |
| [**put \_ 率**](cpospassthru-put-rate.md)                        | 設定播放速率。                                                                             |
| [**取得 \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | 抓取目前的位置，相對於資料流程的總持續時間。                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | 判斷資料流程是否可以向後 seeked。                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | 判斷資料流程是否可以向前 seeked。                                                |
| IMediaSeeking 方法                                             | Description                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | 查詢資料流程是否已指定搜尋功能。                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | 從一種時間格式轉換成另一種格式。                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | 抓取搜尋有效的時間範圍。                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | 抓取資料流程的所有搜尋功能。                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | 抓取目前的位置，相對於資料流程的總持續時間。                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | 捕獲資料流程的持續時間。                                                               |
| [**GetPositions**](cpospassthru-getpositions.md)                 | 抓取目前的位置和停止位置，相對於資料流程的總持續時間。 |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | 抓取在開始位置之前將排入佇列的資料量。                         |
| [**GetRate**](cpospassthru-getrate.md)                           | 捕獲播放速率。                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | 抓取將停止播放的時間（相對於資料流程的持續時間）。         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | 抓取目前的時間格式。                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | 判斷是否支援指定的時間格式。                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | 判斷指定的時間格式是否為目前使用中的格式。                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | 抓取資料流程的慣用時間格式。                                                 |
| [**SetPositions**](cpospassthru-setpositions.md)                 | 設定目前的位置和停止位置。                                                    |
| [**SetRate**](cpospassthru-setrate.md)                           | 設定播放速率。                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | 設定時間格式。                                                                               |
| 輔助函式                                                  | Description                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | 建立 `CPosPassThru` 或 [**CRendererPosPassThru**](crendererpospassthru.md) 物件。            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




