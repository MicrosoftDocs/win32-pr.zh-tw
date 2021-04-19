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
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="0596b-103">如何設定影片捕獲畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="0596b-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="0596b-104">影片捕獲裝置可能會支援一系列的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="0596b-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="0596b-105">如果有此資訊，最小和最大畫面播放速率會儲存為媒體類型屬性：</span><span class="sxs-lookup"><span data-stu-id="0596b-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="0596b-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0596b-106">Attribute</span></span>                                                         | <span data-ttu-id="0596b-107">描述</span><span class="sxs-lookup"><span data-stu-id="0596b-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="0596b-108">MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最大值</span><span class="sxs-lookup"><span data-stu-id="0596b-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="0596b-109">最大畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="0596b-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="0596b-110">MF \_ MT \_ 幀 \_ 速率 \_ 範圍 \_ 最小值</span><span class="sxs-lookup"><span data-stu-id="0596b-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="0596b-111">最小畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="0596b-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="0596b-112">範圍可能會依捕捉格式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="0596b-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="0596b-113">例如，在較大的框架大小時，最大畫面播放速率可能會降低。</span><span class="sxs-lookup"><span data-stu-id="0596b-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="0596b-114">若要設定畫面播放速率：</span><span class="sxs-lookup"><span data-stu-id="0596b-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="0596b-115">建立 capture 裝置的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="0596b-115">Create the media source for the capture device.</span></span> <span data-ttu-id="0596b-116">請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="0596b-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="0596b-117">在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以取得簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="0596b-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="0596b-118">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 來取得影片資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="0596b-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="0596b-119">對資料流程描述元呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。</span><span class="sxs-lookup"><span data-stu-id="0596b-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="0596b-120">列舉捕捉格式，如 [如何設定影片捕捉格式](how-to-set-the-video-capture-format.md)所述。</span><span class="sxs-lookup"><span data-stu-id="0596b-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="0596b-121">從清單中選取想要的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="0596b-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="0596b-122">查詢適用于 [MF \_ mt \_ 幀 \_ 速率 \_ 範圍 \_ 最大值](mf-mt-frame-rate-range-max.md) 和 [MF \_ mt \_ 幀 \_ 速率 \_ 範圍 \_ 最小值](mf-mt-frame-rate-range-min.md) 屬性的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0596b-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="0596b-123">此值提供支援的畫面播放速率範圍。</span><span class="sxs-lookup"><span data-stu-id="0596b-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="0596b-124">裝置可能會支援此範圍內的其他畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="0596b-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="0596b-125">在媒體類型上設定 [ [**MF \_ MT \_ 框架**](mf-mt-frame-rate-attribute.md) ] 屬性，以指定所需的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="0596b-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="0596b-126">使用修改過的媒體類型呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 。</span><span class="sxs-lookup"><span data-stu-id="0596b-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="0596b-127">下列範例會將畫面播放速率設定為等於裝置所支援的最大畫面播放速率：</span><span class="sxs-lookup"><span data-stu-id="0596b-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0596b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="0596b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0596b-129">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="0596b-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



