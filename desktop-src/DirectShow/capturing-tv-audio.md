---
description: 捕獲電視音訊
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: 捕獲電視音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991602"
---
# <a name="capturing-tv-audio"></a><span data-ttu-id="020fe-103">捕獲電視音訊</span><span class="sxs-lookup"><span data-stu-id="020fe-103">Capturing TV Audio</span></span>

<span data-ttu-id="020fe-104">若要從類比電視將音訊捕獲到檔案，請使用 [音訊捕獲篩選器](audio-capture-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="020fe-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="020fe-105">使用系統裝置列舉值建立音訊捕獲篩選器。</span><span class="sxs-lookup"><span data-stu-id="020fe-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="020fe-106">使用者的系統上可能有數個音訊捕獲裝置;使用者必須選取代表音效卡的裝置。</span><span class="sxs-lookup"><span data-stu-id="020fe-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="020fe-107">將音訊捕獲輸出釘選至 mux 篩選器：</span><span class="sxs-lookup"><span data-stu-id="020fe-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="020fe-108">輸入 pin 不需要連接到任何動作。</span><span class="sxs-lookup"><span data-stu-id="020fe-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="020fe-109">每個輸入的 pin 代表音訊捕獲裝置上的實體輸入。</span><span class="sxs-lookup"><span data-stu-id="020fe-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="020fe-110">您可以使用 [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) 介面來啟用從調諧器接收音訊串流的輸入。</span><span class="sxs-lookup"><span data-stu-id="020fe-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="020fe-111">輸入 pin 是依名稱識別，例如「線路輸入」或「CD 音訊」。</span><span class="sxs-lookup"><span data-stu-id="020fe-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="020fe-112">可惜的是，這些名稱可能會從一部裝置變更為下一個裝置。</span><span class="sxs-lookup"><span data-stu-id="020fe-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="020fe-113">此外，不同的電視調諧器介面卡會使用不同的聲音輸入。</span><span class="sxs-lookup"><span data-stu-id="020fe-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="020fe-114">因此，使用者可以識別要使用的輸入。</span><span class="sxs-lookup"><span data-stu-id="020fe-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="020fe-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="020fe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="020fe-116">類比電視音訊</span><span class="sxs-lookup"><span data-stu-id="020fe-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="020fe-117">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="020fe-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



