---
description: 如何執行清理
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: 如何執行清理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512452"
---
# <a name="how-to-perform-scrubbing"></a>如何執行清理

您可以藉由與時間的視覺標記法（例如捲軸）進行互動，藉以立即搜尋檔案內的特定點。 在媒體基礎中，清除表示搜尋檔案並取得一個更新的畫面格。

如需有關清除的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。

## <a name="to-perform-scrubbing"></a>執行清理

1.  呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)以從 [媒體會話](media-session.md)取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)介面。
    > [!Note]  
    > 請勿從媒體來源取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。 一律從媒體會話取得介面。

     

2.  呼叫 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) ，將播放速率設定為零。 如需呼叫這個方法的詳細資訊，請參閱 [如何設定媒體會話的播放速度](how-to-set-the-playback-rate-on-the-media-session.md)。
3.  藉由指定要在 **MFTIME** 類型中搜尋的呈現時間，在 **PROPVARIANT** 中建立搜尋位置。
4.  呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以搜尋位置開始播放。
5.  當清除操作完成時，媒體會話會傳送 [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) 事件。 請先等候這個事件，再呼叫另一個清除操作的 [ [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) ]。

## <a name="example"></a>範例

下列程式碼範例顯示如何執行清除。


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



成功的清除作業會在所有資料流程接收更新為新的框架，而且清除作業順利完成之後，產生 [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) 事件。 清除影片檔案會顯示已 seeked 至，但不會產生音訊輸出的畫面格。

應用程式可以藉由將播放速率設定為零，然後在 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)的呼叫中將設定為 **VT \_ 空白** 的 **PROPVARIANT** ，來執行框架逐步執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[速率控制](rate-control.md)
</dt> </dl>

 

 



