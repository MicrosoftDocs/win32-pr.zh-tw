---
description: 本主題說明如何使用 MFPlay 播放一連串音訊/影片檔案。
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: 如何播放一連串的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf9cfc6fe48caf5eb185a19ec98ac119fcfbbb78d5e2363bd2db9607a4875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828158"
---
# <a name="how-to-play-a-sequence-of-files"></a>如何播放一連串的檔案

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何使用 MFPlay 播放一連串音訊/影片檔案。


[MFPlay 開始使用](getting-started-with-mfplay.md)的主題顯示如何播放單一媒體檔案。 您也可以使用 MFPlay 來播放一連串的檔案。

### <a name="synchronous-blocking-method"></a>同步 (封鎖) 方法

1.  呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 方法。 方法會建立一個媒體專案。
2.  呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) ，將媒體專案排入佇列以供播放。
3.  呼叫 [**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始播放。

下列程式碼顯示這些步驟。


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



[**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)方法會採用下列參數：

-   第一個參數是檔案的 URL。
-   第二個參數會指定方法是否封鎖。 如果指定值 **TRUE**（如下所示），則會導致方法封鎖，直到建立媒體專案為止。
-   第三個參數會將任意 **DWORD \_ 指標** 值與媒體專案產生關聯。 您稍後可以藉由呼叫 [**IMFPMediaItem：： GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata)來取得此值。
-   第四個參數會接收媒體專案之 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標。

### <a name="asynchronous-non-blocking-method"></a>非同步 (非封鎖) 方法

如果您從 UI 執行緒呼叫 [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ，請避免封鎖選項，因為它可能需要花費相當長的時間才能完成。 方法通常會開啟檔案或網路連線，並讀取足夠的資料來剖析檔案標頭，這一切都需要一些時間。 因此，通常最好是將第二個參數設定為 **FALSE**。 此選項會使方法以非同步方式執行。 使用非同步選項時，最後一個參數必須是 **Null**：


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



建立媒體專案時，您的應用程式會收到 **\_ \_ \_ MEDIAITEM \_ 建立事件的 MFP 事件種類** 。 此事件的資料結構包含媒體專案的指標。 將此指標傳遞至 [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 方法，以將專案排入佇列以供播放。


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



