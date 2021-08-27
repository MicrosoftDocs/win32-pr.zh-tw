---
description: 本主題說明如何搭配 MFPlay 使用音訊/影片效果。
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: 如何新增音訊或影片效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af2bb310ab4818cac5dd2804d2bb696c284fdd868d916e4e543a205328e909e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061548"
---
# <a name="how-to-add-audio-or-video-effects"></a>如何新增音訊或影片效果

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本主題說明如何搭配 MFPlay 使用音訊/影片效果。

若要搭配 MFPlay 使用效果，必須將效果實作為媒體基礎轉換 (MFT) 。 如需詳細資訊，請參閱 [媒體基礎轉換](media-foundation-transforms.md)。

**新增音訊或影片效果**

1.  建立可執行效果的 MFT 實例。
2.  呼叫 [**IMFPMediaPlayer：： InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)。

開啟媒體檔案來播放之前，請先呼叫 [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) 。 MFPlay 會自動判斷效果是影片效果或音訊效果。

[**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)方法也會採用布林值參數，指定效果是選擇性或必要的。 如果 MFPlay 無法新增必要的效果 (例如，因為資料流程格式與) 不相容，所以會發生播放錯誤。 在大部分的情況下，最好將效果設定為選擇性。

MFPlay 會繼續使用所有後續播放的效果。 若要移除效果，請呼叫 [**IMFPMediaPlayer：： RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) 或 [**IMFPMediaPlayer：： RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects)。


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



