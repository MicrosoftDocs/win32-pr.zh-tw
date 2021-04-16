---
title: 指派輸入格式
description: 指派輸入格式
ms.assetid: 44c4ed7e-b35e-4ab5-9975-021f343dab6a
keywords:
- Advanced Systems Format (ASF) ，指派輸入格式
- ASF (Advanced 系統格式) ，指派輸入格式
- 設定檔，指派輸入格式
- 編解碼器，指派輸入格式
- Advanced Systems Format (ASF) 、輸入格式指派
- ASF (Advanced 系統格式) 、輸入格式指派
- 設定檔，輸入格式指派
- 編解碼器、輸入格式指派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c6ad1bcdf161b335d9367d7de4df84b7eb2e6ea
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507772"
---
# <a name="assigning-input-formats"></a><span data-ttu-id="97dfa-111">指派輸入格式</span><span class="sxs-lookup"><span data-stu-id="97dfa-111">Assigning Input Formats</span></span>

<span data-ttu-id="97dfa-112">當您識別出符合資料的輸入格式時，您可以藉由呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)來設定它以供寫入器使用。</span><span class="sxs-lookup"><span data-stu-id="97dfa-112">When you have identified the input format that matches your data, you can set it for use by the writer by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops).</span></span>

<span data-ttu-id="97dfa-113">針對影片串流，您必須在輸入範例中設定框架的大小。</span><span class="sxs-lookup"><span data-stu-id="97dfa-113">For video streams, you must set the size of the frames in the input samples.</span></span> <span data-ttu-id="97dfa-114">下列範例程式碼示範如何設定和設定影片輸入。</span><span class="sxs-lookup"><span data-stu-id="97dfa-114">The following example code demonstrates how to configure and set a video input.</span></span> <span data-ttu-id="97dfa-115">它會使用中所定義的 **FindInputFormat** 函數 [來列舉輸入格式](to-enumerate-input-formats.md) 區段，以取得24位 RGB 影片的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="97dfa-115">It uses the **FindInputFormat** function defined in the [To Enumerate Input Formats](to-enumerate-input-formats.md) section to get the input format for 24-bit RGB video.</span></span> <span data-ttu-id="97dfa-116">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="97dfa-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT ConfigureVideoInput(IWMWriter* pWriter,
                            DWORD dwInput,
                            GUID guidSubType,
                            LONG lFrameWidth,
                            LONG lFrameHeight)
{
    DWORD   cbSize = 0;
    LONG    lStride = 0;

    IWMInputMediaProps* pProps  = NULL;
    WM_MEDIA_TYPE*      pType   = NULL;
    WMVIDEOINFOHEADER*  pVidHdr = NULL;
    BITMAPINFOHEADER*   pbmi    = NULL;

    // Get the base input format for the required subtype.
    HRESULT hr = FindInputFormat(pWriter, dwInput, guidSubType, &pProps);
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

    // Adjust the format to match your source images.

    // First set pointers to the video structures.
    pVidHdr = (WMVIDEOINFOHEADER*) pType->pbFormat;
    pbmi  = &(pVidHdr->bmiHeader);
        
    pbmi->biWidth  = lFrameWidth;  
    pbmi->biHeight = lFrameHeight;
    
    // Stride = (width * bytes/pixel), rounded to the next DWORD boundary.
    lStride = (lFrameWidth * (pbmi->biBitCount / 8) + 3) & ~3;


    // Image size = stride * height. 
    pbmi->biSizeImage = lFrameHeight * lStride;

    // Apply the adjusted type to the video input. 
    hr = pProps->SetMediaType(pType);
    if (FAILED(hr))
    {
        goto Exit;
    }

    hr = pWriter->SetInputProps(dwInput, pProps);

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="97dfa-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="97dfa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97dfa-118">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="97dfa-118">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




