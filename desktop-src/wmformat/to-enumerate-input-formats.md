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
# <a name="to-enumerate-input-formats"></a>列舉輸入格式

每個 Windows Media 編解碼器都會接受一或多個類型的輸入媒體進行壓縮。 Windows Media Format SDK 可讓您輸入比編解碼器支援更多的格式。 SDK 會執行這項操作，方法是在必要時對輸入執行前置處理轉換，例如調整影片畫面的大小或重新取樣音訊。 在任何情況下，您都必須確定您所寫入之檔案的輸入格式符合您傳送給寫入器的資料。 每個編解碼器都有載入設定檔時，在寫入器中設定的預設輸入媒體格式。 您可以藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)來檢查預設輸入格式。

影片編解碼器支援下列格式： IYUV、I420、YV12、YUY2、UYVY、YVYU、YVU9、RGB 32、RGB 24、RGB 565、RGB 555 和 RGB 8。 音訊編解碼器支援 PCM 音訊。

若要列舉編解碼器所支援的輸入格式，請執行下列步驟：

1.  建立寫入器物件，並設定要使用的設定檔。 如需在寫入器中設定設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。
2.  識別您想要檢查其格式的輸入編號。 如需識別輸入數位的詳細資訊，請參閱 [以數位識別](to-identify-inputs-by-number.md)輸入。
3.  藉由呼叫 [**IWMWriter：： GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount)，取得所需輸入所支援的輸入格式總數。
4.  對所有支援的輸入格式執行迴圈，並為每個輸入格式執行下列步驟。
    -   藉由呼叫 [**IWMWriter：： GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat)，取出輸入格式的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面。
    -   取得輸入格式的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構。 呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)，傳遞 **Null** 做為 *pType* 參數，以取得結構的大小。 然後，配置記憶體來保存結構，並再次呼叫 **GetMediaType** 以取得結構。 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)繼承自 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)，因此您可以從上一個步驟中取出的 **IWMInputMediaProps** 實例進行 **GetMediaType** 的呼叫。
    -   [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構中所述的格式包含輸入格式的所有相關資訊。 媒體的基本格式是以 **WM 媒體類型來識別。 \_ \_ 子類型**。 若為影片串流， **pbFormat** 成員會指向動態配置的 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) 結構，其中包含有關資料流程的進一步詳細資料，包括矩形大小。 輸入框架的大小不需要完全符合編解碼器支援的大小。 如果兩者不相符，則在許多情況下，SDK 執行時間元件會自動將輸入影片畫面的大小調整為編解碼器可以接受的內容。

下列範例程式碼會尋找作為參數傳遞之子類型的輸入格式。 如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




