---
description: 如何設定媒體會話的播放率
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: 如何設定媒體會話的播放率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696202"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>如何設定媒體會話的播放率

若要執行向前快轉和倒轉等播放功能，應用程式可能需要變更媒體資料流程的播放速度。 媒體基礎提供應用程式必須用來動態設定播放速率的速率控制服務。

在設定播放速率之前，應用程式應該檢查媒體來源是否支援速率。 如需查詢支援費率的詳細資訊，請參閱 [如何判斷支援的費率](how-to-determine-supported-rates.md)。

如需播放速率的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。

## <a name="to-set-the-playback-rate"></a>設定播放速率

1.  呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 以取得媒體會話的速率控制物件。

    呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 的應用程式必須確保下列各項：

    -   *>punkobject* 參數包含已初始化的 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)介面指標。
    -   在 *ppvObject* 參數中收到的速率控制物件會釋放，以避免記憶體流失。

2.  呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法來設定播放速率。 以非同步方式完成 **SetRate** 之後，應用程式會收到 [MESessionRateChanged](mesessionratechanged.md) 事件。

## <a name="example"></a>範例

下列程式碼示範如何透過呼叫 [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法來設定播放速率。


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



應用程式必須先停止或暫停，然後才能將負數或零的比率轉換成正面的速率。 如需這些狀態的詳細資訊，請參閱 [如何控制呈現狀態](how-to-control-presentation-states.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[速率控制](rate-control.md)
</dt> <dt>

[搜尋、向前快轉及反向播放](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



