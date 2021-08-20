---
description: 如何尋找媒體檔案的持續時間。
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: 如何尋找媒體檔案的持續時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1885d356be54875079341eabc7433c9753792daf01c4848a00ee4ed4fbb343ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878842"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>如何尋找媒體檔案的持續時間

若要尋找媒體檔案的持續時間，請執行下列步驟：

1.  使用 [來源解析程式](source-resolver.md) 來建立可剖析媒體檔案的媒體來源。
2.  在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 。 這個方法會傳回描述媒體檔案內容的簡報描述項。
3.  藉由呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)方法，查詢適用于 [MF \_ PD \_ DURATION](mf-pd-duration-attribute.md)屬性的簡報描述項。 屬性的值（如果有的話）是檔案持續時間（以 100-毫微秒為單位）。


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



