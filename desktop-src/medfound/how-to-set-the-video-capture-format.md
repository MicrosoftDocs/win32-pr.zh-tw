---
description: 影片捕獲裝置可能支援數個捕捉格式。 格式通常會依壓縮類型、色彩空間 (YUV 或 RGB) 、框架大小或畫面播放速率而有所不同。
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: 如何設定影片捕捉格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984196"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="a242d-104">如何設定影片捕捉格式</span><span class="sxs-lookup"><span data-stu-id="a242d-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="a242d-105">影片捕獲裝置可能支援數個捕捉格式。</span><span class="sxs-lookup"><span data-stu-id="a242d-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="a242d-106">格式通常會依壓縮類型、色彩空間 (YUV 或 RGB) 、框架大小或畫面播放速率而有所不同。</span><span class="sxs-lookup"><span data-stu-id="a242d-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="a242d-107">支援的格式清單包含在 *展示描述* 項中。</span><span class="sxs-lookup"><span data-stu-id="a242d-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="a242d-108">如需詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="a242d-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="a242d-109">列舉支援的格式：</span><span class="sxs-lookup"><span data-stu-id="a242d-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="a242d-110">建立 capture 裝置的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="a242d-110">Create the media source for the capture device.</span></span> <span data-ttu-id="a242d-111">請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="a242d-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="a242d-112">在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以取得簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="a242d-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="a242d-113">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) 來取得影片資料流程的資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="a242d-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="a242d-114">對資料流程描述元呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。</span><span class="sxs-lookup"><span data-stu-id="a242d-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="a242d-115">呼叫 [**IMFMediaTypeHandler：： GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) 以取得支援的格式數目。</span><span class="sxs-lookup"><span data-stu-id="a242d-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="a242d-116">在迴圈中，呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) 來取得每個格式。</span><span class="sxs-lookup"><span data-stu-id="a242d-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="a242d-117">格式是以 *媒體類型* 表示。</span><span class="sxs-lookup"><span data-stu-id="a242d-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="a242d-118">如需詳細資訊，請參閱 [影片媒體類型](video-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a242d-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="a242d-119">下列範例會列舉裝置的捕獲格式：</span><span class="sxs-lookup"><span data-stu-id="a242d-119">The following example enumerates the capture formats for a device:</span></span>


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



<span data-ttu-id="a242d-120">`LogMediaType`此範例中使用的函式會列在「[媒體類型」偵錯工具代碼](media-type-debugging-code.md)中。</span><span class="sxs-lookup"><span data-stu-id="a242d-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="a242d-121">若要設定捕捉格式：</span><span class="sxs-lookup"><span data-stu-id="a242d-121">To set the capture format:</span></span>

1.  <span data-ttu-id="a242d-122">取得 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面的指標，如先前範例所示。</span><span class="sxs-lookup"><span data-stu-id="a242d-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="a242d-123">呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) ，以取得索引所指定的所需格式。</span><span class="sxs-lookup"><span data-stu-id="a242d-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="a242d-124">呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 來設定格式。</span><span class="sxs-lookup"><span data-stu-id="a242d-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="a242d-125">如果您未設定捕捉格式，裝置將會使用其預設格式。</span><span class="sxs-lookup"><span data-stu-id="a242d-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="a242d-126">下列範例會設定捕捉格式：</span><span class="sxs-lookup"><span data-stu-id="a242d-126">The following example sets the capture format:</span></span>


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



<span data-ttu-id="a242d-127">傳回格式的順序取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="a242d-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="a242d-128">通常會先依壓縮類型或色彩空間來分組：然後從最小的框架大小到每個群組內的最大框架大小。</span><span class="sxs-lookup"><span data-stu-id="a242d-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="a242d-129">畫面播放速率的處理方式與其他格式屬性稍有不同。</span><span class="sxs-lookup"><span data-stu-id="a242d-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="a242d-130">如需詳細資訊，請參閱 [如何設定影片捕獲畫面播放速率](how-to-set-the-video-capture-frame-rate.md)。</span><span class="sxs-lookup"><span data-stu-id="a242d-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="a242d-131">在某些裝置中，格式清單會包含每個格式的重複專案。</span><span class="sxs-lookup"><span data-stu-id="a242d-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="a242d-132">例如，如果裝置支援15種不同的捕捉格式，此清單將包含30個專案。</span><span class="sxs-lookup"><span data-stu-id="a242d-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="a242d-133">在每個配對中，其中一種媒體類型會有一個與 **format \_ VideoInfo** 相同的 VideoInfo2 [**\_ \_ \_ \_ 類別**](mf-mt-am-format-type-attribute.md)，而另一個則是具有等於 format **\_** 格式的 **mf \_ mt \_ am \_ 格式 \_** 類型。</span><span class="sxs-lookup"><span data-stu-id="a242d-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="a242d-134"> (這兩個值會定義在標頭檔的 uuid. h. ) 第二種類型也可能包含額外的色彩資訊 ([擴充色彩資訊](extended-color-information.md)) 或顯示不同的值，以交錯 ([**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a242d-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="a242d-135">這些重複的類型存在，可支援較舊的 DirectShow 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a242d-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="a242d-136">在媒體基礎應用程式中，每當列出重複的 **格式 \_ VideoInfo2** 類型時，應該忽略 **format \_ VideoInfo** type。</span><span class="sxs-lookup"><span data-stu-id="a242d-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a242d-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="a242d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a242d-138">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="a242d-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



