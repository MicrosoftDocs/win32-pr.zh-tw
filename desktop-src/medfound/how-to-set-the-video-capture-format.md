---
description: 影片捕獲裝置可能支援數個捕捉格式。 格式通常會依壓縮類型、色彩空間 (YUV 或 RGB) 、框架大小或畫面播放速率而有所不同。
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: 如何設定影片捕捉格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0968560772345bea91f5acfb79e7157a6376f388a5c0065634a273196b7552cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974397"
---
# <a name="how-to-set-the-video-capture-format"></a>如何設定影片捕捉格式

影片捕獲裝置可能支援數個捕捉格式。 格式通常會依壓縮類型、色彩空間 (YUV 或 RGB) 、框架大小或畫面播放速率而有所不同。

支援的格式清單包含在 *展示描述* 項中。 如需詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。

列舉支援的格式：

1.  建立 capture 裝置的媒體來源。 請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。
2.  在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以取得簡報描述項。
3.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 來取得影片資料流程的資料流程描述項。
4.  對資料流程描述元呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。
5.  呼叫 [**IMFMediaTypeHandler：： GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) 以取得支援的格式數目。
6.  在迴圈中，呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) 來取得每個格式。 格式是以 *媒體類型* 表示。 如需詳細資訊，請參閱 [影片媒體類型](video-media-types.md)。

下列範例會列舉裝置的捕獲格式：


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



`LogMediaType`此範例中使用的函式會列在「[媒體類型」偵錯工具代碼](media-type-debugging-code.md)中。

若要設定捕捉格式：

1.  取得 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面的指標，如先前範例所示。
2.  呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) ，以取得索引所指定的所需格式。
3.  呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 來設定格式。

如果您未設定捕捉格式，裝置將會使用其預設格式。

下列範例會設定捕捉格式：


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



傳回格式的順序取決於裝置。 通常會先依壓縮類型或色彩空間來分組：然後從最小的框架大小到每個群組內的最大框架大小。

畫面播放速率的處理方式與其他格式屬性稍有不同。 如需詳細資訊，請參閱 [如何設定影片捕獲畫面播放速率](how-to-set-the-video-capture-frame-rate.md)。

> [!Note]  
> 在某些裝置中，格式清單會包含每個格式的重複專案。 例如，如果裝置支援15種不同的捕捉格式，此清單將包含30個專案。 在每個配對中，其中一種媒體類型會有一個與 **format \_ VideoInfo** 相同的 VideoInfo2 [**\_ \_ \_ \_ 類別**](mf-mt-am-format-type-attribute.md)，而另一個則是具有等於 format **\_** 格式的 **mf \_ mt \_ am \_ 格式 \_** 類型。  (這兩個值會定義在標頭檔的 uuid. h. ) 第二種類型也可能包含額外的色彩資訊 ([擴充色彩資訊](extended-color-information.md)) 或顯示不同的值，以交錯 ([**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md)) 。 這些重複的類型存在，可支援舊版 DirectShow 應用程式。 在媒體基礎應用程式中，每當列出重複的 **格式 \_ VideoInfo2** 類型時，應該忽略 **format \_ VideoInfo** type。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



