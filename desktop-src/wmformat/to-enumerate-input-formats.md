---
title: 列舉輸入格式
description: 列舉輸入格式
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF) ，列舉輸入格式
- ASF (Advanced 系統格式) ，列舉輸入格式
- 設定檔，列舉輸入格式
- 編解碼器，列舉輸入格式
- Advanced Systems Format (ASF) 、輸入格式列舉
- ASF (Advanced 系統格式) 、輸入格式列舉
- 設定檔，輸入格式列舉
- 編解碼器，輸入格式列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023171"
---
# <a name="to-enumerate-input-formats"></a><span data-ttu-id="48a4e-111">列舉輸入格式</span><span class="sxs-lookup"><span data-stu-id="48a4e-111">To Enumerate Input Formats</span></span>

<span data-ttu-id="48a4e-112">每個 Windows Media 編解碼器都會接受一或多個類型的輸入媒體進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="48a4e-112">Each of the Windows Media codecs accepts one or more types of input media for compression.</span></span> <span data-ttu-id="48a4e-113">Windows Media Format SDK 可讓您輸入比編解碼器支援更多的格式。</span><span class="sxs-lookup"><span data-stu-id="48a4e-113">The Windows Media Format SDK enables you to input a wider variety of formats than those supported by the codecs.</span></span> <span data-ttu-id="48a4e-114">SDK 會執行這項操作，方法是在必要時對輸入執行前置處理轉換，例如調整影片畫面的大小或重新取樣音訊。</span><span class="sxs-lookup"><span data-stu-id="48a4e-114">The SDK does this by performing pre-processing transformations on the inputs when necessary, such as resizing video frames or resampling audio.</span></span> <span data-ttu-id="48a4e-115">在任何情況下，您都必須確定您所寫入之檔案的輸入格式符合您傳送給寫入器的資料。</span><span class="sxs-lookup"><span data-stu-id="48a4e-115">In any case, you must ensure that the input formats for the files you write match the data you send to the writer.</span></span> <span data-ttu-id="48a4e-116">每個編解碼器都有載入設定檔時，在寫入器中設定的預設輸入媒體格式。</span><span class="sxs-lookup"><span data-stu-id="48a4e-116">Each codec has a default input media format that is set in the writer when the profile is loaded.</span></span> <span data-ttu-id="48a4e-117">您可以藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)來檢查預設輸入格式。</span><span class="sxs-lookup"><span data-stu-id="48a4e-117">You can examine the default input format by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>

<span data-ttu-id="48a4e-118">影片編解碼器支援下列格式： IYUV、I420、YV12、YUY2、UYVY、YVYU、YVU9、RGB 32、RGB 24、RGB 565、RGB 555 和 RGB 8。</span><span class="sxs-lookup"><span data-stu-id="48a4e-118">The video codecs support the following formats: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555, and RGB 8.</span></span> <span data-ttu-id="48a4e-119">音訊編解碼器支援 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="48a4e-119">The audio codecs support PCM audio.</span></span>

<span data-ttu-id="48a4e-120">若要列舉編解碼器所支援的輸入格式，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="48a4e-120">To enumerate the input formats supported by a codec, perform the following steps:</span></span>

1.  <span data-ttu-id="48a4e-121">建立寫入器物件，並設定要使用的設定檔。</span><span class="sxs-lookup"><span data-stu-id="48a4e-121">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="48a4e-122">如需在寫入器中設定設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="48a4e-122">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
2.  <span data-ttu-id="48a4e-123">識別您想要檢查其格式的輸入編號。</span><span class="sxs-lookup"><span data-stu-id="48a4e-123">Identify the input number for which you want to check the formats.</span></span> <span data-ttu-id="48a4e-124">如需識別輸入數位的詳細資訊，請參閱 [以數位識別](to-identify-inputs-by-number.md)輸入。</span><span class="sxs-lookup"><span data-stu-id="48a4e-124">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="48a4e-125">藉由呼叫 [**IWMWriter：： GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount)，取得所需輸入所支援的輸入格式總數。</span><span class="sxs-lookup"><span data-stu-id="48a4e-125">Retrieve the total number of input formats supported by the desired input by calling [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).</span></span>
4.  <span data-ttu-id="48a4e-126">對所有支援的輸入格式執行迴圈，並為每個輸入格式執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="48a4e-126">Loop through all of the supported input formats, performing the following steps for each.</span></span>
    -   <span data-ttu-id="48a4e-127">藉由呼叫 [**IWMWriter：： GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat)，取出輸入格式的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="48a4e-127">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input format by calling [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).</span></span>
    -   <span data-ttu-id="48a4e-128">取得輸入格式的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="48a4e-128">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the input format.</span></span> <span data-ttu-id="48a4e-129">呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)，傳遞 **Null** 做為 *pType* 參數，以取得結構的大小。</span><span class="sxs-lookup"><span data-stu-id="48a4e-129">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passing **NULL** for the *pType* parameter to get the size of the structure.</span></span> <span data-ttu-id="48a4e-130">然後，配置記憶體來保存結構，並再次呼叫 **GetMediaType** 以取得結構。</span><span class="sxs-lookup"><span data-stu-id="48a4e-130">Then allocate memory to hold the structure and call **GetMediaType** again to get the structure.</span></span> <span data-ttu-id="48a4e-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)繼承自 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)，因此您可以從上一個步驟中取出的 **IWMInputMediaProps** 實例進行 **GetMediaType** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="48a4e-131">[**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) inherits from [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), so you can make the calls to **GetMediaType** from the instance of **IWMInputMediaProps** retrieved in the previous step.</span></span>
    -   <span data-ttu-id="48a4e-132">[**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構中所述的格式包含輸入格式的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="48a4e-132">The format described in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains all of the pertinent information about the input format.</span></span> <span data-ttu-id="48a4e-133">媒體的基本格式是以 **WM 媒體類型來識別。 \_ \_ 子類型**。</span><span class="sxs-lookup"><span data-stu-id="48a4e-133">The basic format of the media is identified by **WM\_MEDIA\_TYPE.subtype**.</span></span> <span data-ttu-id="48a4e-134">若為影片串流， **pbFormat** 成員會指向動態配置的 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) 結構，其中包含有關資料流程的進一步詳細資料，包括矩形大小。</span><span class="sxs-lookup"><span data-stu-id="48a4e-134">For video streams, the **pbFormat** member points to a dynamically allocated [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure which contains further details about the stream, including rectangle size.</span></span> <span data-ttu-id="48a4e-135">輸入框架的大小不需要完全符合編解碼器支援的大小。</span><span class="sxs-lookup"><span data-stu-id="48a4e-135">The size of the input frames is not required to match exactly a size supported by the codec.</span></span> <span data-ttu-id="48a4e-136">如果兩者不相符，則在許多情況下，SDK 執行時間元件會自動將輸入影片畫面的大小調整為編解碼器可以接受的內容。</span><span class="sxs-lookup"><span data-stu-id="48a4e-136">If they do not match, the SDK run-time components, in many cases, will automatically resize the input video frames to something the codec can accept.</span></span>

<span data-ttu-id="48a4e-137">下列範例程式碼會尋找作為參數傳遞之子類型的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="48a4e-137">The following example code finds the input format of the subtype passed as a parameter.</span></span> <span data-ttu-id="48a4e-138">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="48a4e-138">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="48a4e-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="48a4e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48a4e-140">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="48a4e-140">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="48a4e-141">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="48a4e-141">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




