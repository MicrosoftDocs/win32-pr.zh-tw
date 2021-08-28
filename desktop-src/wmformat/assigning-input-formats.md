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
ms.openlocfilehash: f6f87ec74bc5d3750d65ecc91e2df4640a6ed02c9e9a9425b27897e70f825983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840328"
---
# <a name="assigning-input-formats"></a>指派輸入格式

當您識別出符合資料的輸入格式時，您可以藉由呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)來設定它以供寫入器使用。

針對影片串流，您必須在輸入範例中設定框架的大小。 下列範例程式碼示範如何設定和設定影片輸入。 它會使用中所定義的 **FindInputFormat** 函數 [來列舉輸入格式](to-enumerate-input-formats.md) 區段，以取得24位 RGB 影片的輸入格式。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


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





## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> </dl>

 

 




