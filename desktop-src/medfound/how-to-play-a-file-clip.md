---
description: 本主題說明如何藉由設定播放的開始和停止時間，在 MFPlay 中播放媒體檔案的區段。
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: 如何播放檔案剪輯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848377"
---
# <a name="how-to-play-a-file-clip"></a>如何播放檔案剪輯

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何藉由設定播放的開始和停止時間，在 MFPlay 中播放媒體檔案的區段。

**播放檔案剪輯**

1.  呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 或 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 來建立檔案的媒體專案。
2.  （選擇性）取得檔案的總持續時間，如 [如何取得播放持續時間](how-to-get-the-playback-duration.md)中所述。
3.  呼叫 [**IMFPMediaItem：： SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) 來設定開始和停止時間。 停止時間不得超過檔案持續時間。
4.  呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 以開始播放。

下列範例會使用 [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)的封鎖版本。 如果使用非封鎖版本，則在 **CreateMediaItemFromURL** 之後出現的程式碼應該放在 **\_ \_ \_ MEDIAITEM \_ 建立** 事件的處理常式中。 如需有關 MFPlay 中事件的詳細資訊，請參閱 [從播放程式接收事件](getting-started-with-mfplay.md)。

為了取得檔案持續時間，此範例會呼叫 `GetPlaybackDuration` 主題中顯示 [如何取得播放持續時間](how-to-get-the-playback-duration.md)的函式。


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



