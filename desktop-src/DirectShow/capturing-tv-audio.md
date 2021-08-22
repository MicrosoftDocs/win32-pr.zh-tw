---
description: 捕獲電視音訊
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: 捕獲電視音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d699533480bdeaaa528e362c0773e9df8100fda3dc2195a65c055ae7f7d5bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641008"
---
# <a name="capturing-tv-audio"></a>捕獲電視音訊

若要從類比電視將音訊捕獲到檔案，請使用 [音訊捕獲篩選器](audio-capture-filter.md)。 使用系統裝置列舉值建立音訊捕獲篩選器。 使用者的系統上可能有數個音訊捕獲裝置;使用者必須選取代表音效卡的裝置。

連線音訊捕獲輸出釘選至 mux 篩選器：


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



輸入 pin 不需要連接到任何動作。 每個輸入的 pin 代表音訊捕獲裝置上的實體輸入。 您可以使用 [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) 介面來啟用從調諧器接收音訊串流的輸入。 輸入 pin 是依名稱識別，例如「線路輸入」或「CD 音訊」。 可惜的是，這些名稱可能會從一部裝置變更為下一個裝置。 此外，不同的電視調諧器介面卡會使用不同的聲音輸入。 因此，使用者可以識別要使用的輸入。


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[類比電視音訊](analog-television-audio.md)
</dt> <dt>

[音訊捕獲](audio-capture.md)
</dt> </dl>

 

 



