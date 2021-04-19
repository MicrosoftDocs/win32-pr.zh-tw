---
description: 影片捕獲裝置可能會支援一系列的畫面播放速率。
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: 如何設定影片捕獲畫面播放速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998469"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>如何設定影片捕獲畫面播放速率

影片捕獲裝置可能會支援一系列的畫面播放速率。 如果有此資訊，最小和最大畫面播放速率會儲存為媒體類型屬性：



| 屬性                                                         | 描述         |
|-------------------------------------------------------------------|---------------------|
| [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md) | 最大畫面播放速率。 |
| [MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最小值](mf-mt-frame-rate-range-min.md) | 最小畫面播放速率。 |



 

範圍可能會依捕捉格式而有所不同。 例如，在較大的框架大小時，最大畫面播放速率可能會降低。

若要設定畫面播放速率：

1.  建立 capture 裝置的媒體來源。 請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。
2.  在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以取得簡報描述項。
3.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 來取得影片資料流程的資料流程描述項。
4.  對資料流程描述元呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。
5.  列舉捕捉格式，如 [如何設定影片捕捉格式](how-to-set-the-video-capture-format.md)所述。
6.  從清單中選取想要的輸出格式。
7.  查詢適用于 [MF \_ mt \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md) 和 [MF \_ mt \_ 幀 \_ 速率 \_ 範圍 \_ 最小值](mf-mt-frame-rate-range-min.md) 屬性的媒體類型。 此值提供支援的畫面播放速率範圍。 裝置可能會支援此範圍內的其他畫面播放速率。
8.  在媒體類型上設定 [ [**MF \_ MT \_ 框架**](mf-mt-frame-rate-attribute.md) ] 屬性，以指定所需的畫面播放速率。
9.  使用修改過的媒體類型呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 。

下列範例會將畫面播放速率設定為等於裝置所支援的最大畫面播放速率：


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



