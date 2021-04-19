---
description: 範例捕獲篩選器是一種轉換篩選器，可用來從資料流程取得媒體範例，因為它們通過篩選圖形。
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: 使用範例捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992481"
---
# <a name="using-the-sample-grabber"></a>使用範例捕獲

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

[**範例捕獲**](sample-grabber-filter.md)篩選器是一種轉換篩選器，可用來從資料流程取得媒體範例，因為它們通過篩選圖形。

如果您只是要從影片檔案抓取點陣圖， [ (MediaDet) ](media-detector--mediadet.md) 物件中使用媒體偵測器會比較容易。 如需詳細資訊，請參閱 [抓取海報框架](grabbing-a-poster-frame.md) 。 不過，範例抓取程式更有彈性，因為它幾乎適用于任何媒體類型 (請參閱 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md)) 的幾個例外狀況，並為應用程式提供更多控制權。

-   [建立篩選圖形管理員](#create-the-filter-graph-manager)
-   [將範例捕獲新增至篩選圖形](#add-the-sample-grabber-to-the-filter-graph)
-   [設定媒體類型](#set-the-media-type)
-   [建立篩選圖形](#build-the-filter-graph)
-   [執行圖形](#run-the-graph)
-   [抓取範例](#grab-the-sample)
-   [範例程式碼](#example-code)
-   [相關主題](#related-topics)

## <a name="create-the-filter-graph-manager"></a>建立篩選圖形管理員

若要開始，請建立 [篩選圖形管理員](filter-graph-manager.md) 並查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面。


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>將範例捕獲新增至篩選圖形

建立範例捕獲篩選器的實例，並 addit 至篩選圖形。 查詢 [**ISampleGrabber**](isamplegrabber.md) 介面的範例捕獲篩選器。


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>設定媒體類型

當您第一次建立範例抓取器時，它沒有慣用的媒體類型。 這表示您可以連接到圖表中幾乎任何篩選器，但無法控制其所接收的資料類型。 因此，在建立圖形的其餘部分之前，您必須藉由呼叫 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md) 方法，來設定範例抓取器的媒體類型。

當範例抓取器連線時，它會比較此媒體類型與其他篩選器所提供的媒體類型。 它檢查的唯一欄位是主要類型、子類型和格式類型。 針對上述任何一種，值 GUID \_ Null 表示「接受任何值」。 在大部分的情況下，您會想要設定主要類型和子類型。 例如，下列程式碼指定未壓縮的24位 RGB 影片：


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>建立篩選圖形

現在您可以建立篩選圖形的其餘部分。 因為範例抓取器只會使用您指定的媒體類型進行連線，這可讓您在建立圖表時利用篩選圖形管理員的 [智慧型連接](intelligent-connect.md) 機制。

例如，如果您指定了未壓縮的影片，您可以將來源篩選連接到範例抓取器，而篩選圖形管理員會自動加入檔案剖析器和解碼器。 下列範例會使用 ConnectFilters helper 函式，它會列在 [[連接兩個篩選器]](connect-two-filters.md)中：


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





範例抓取器是轉換篩選，因此輸出的 pin 必須連接到另一個篩選準則。 通常，您可能只想要在完成後捨棄範例。 在這種情況下，請將範例抓取 [**器連接到 Null 轉譯器篩選器**](null-renderer-filter.md)，這會捨棄它所收到的資料。

下列範例會將範例抓取器連接到 Null 轉譯器篩選準則：


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





請注意，在影片解碼和影片轉譯器之間放置範例，可能會大幅影響轉譯效能。 範例抓取器是一種就地篩選，這表示輸出緩衝區與輸入緩衝區相同。 針對影片轉譯，輸出緩衝區可能位於圖形配接器上，其中讀取作業的速度會比主儲存體中的讀取作業慢很多。

## <a name="run-the-graph"></a>執行圖形

範例抓取程式會以兩種模式的其中一種方式運作：

-   緩衝模式會在傳遞範例下游之前，先複製每個範例。
-   回呼模式會在每個範例上叫用應用程式定義的回呼函數。

本文說明緩衝模式。  (在使用回呼模式之前，請注意回呼函數必須有相當大的限制。 否則，它可能會大幅降低效能，甚至造成鎖死。 如需詳細資訊，請參閱 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)。 ) 若要啟用緩衝處理模式，請使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md)方法。

（選擇性）使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetOneShot**](isamplegrabber-setoneshot.md)方法。 這會導致範例捕獲程式在收到第一個媒體範例之後停止，這在您想要從資料流程抓取單一畫面格時很有用。 搜尋所需的時間、執行圖形，然後等候 [**EC \_ 完成**](ec-complete.md) 事件。 請注意，畫面格精確度的層級取決於來源。 例如，在尋找 MPEG 檔案時，通常不會有正確的框架。

若要儘快執行圖形，請依照 [設定圖形時鐘](setting-the-graph-clock.md)中所述的方式來開啟圖形時鐘。

下列範例會啟用一次模式和緩衝模式、執行篩選圖形，並等候完成。


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>抓取範例

在緩衝模式中，範例捕獲會儲存每個範例的複本。 [**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)方法會將緩衝區複製到呼叫端配置的陣列中。 若要判斷所需陣列的大小，請先使用陣列位址的 **Null** 指標來呼叫 **GetCurrentBuffer** 。 然後配置陣列，並再次呼叫方法來複製緩衝區。 下列範例會示範這些步驟。


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



您將需要知道緩衝區中資料的確切格式。 若要取得此資訊，請呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) 方法。 這個方法會使用格式來填滿 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。

若是未壓縮的影片資料流程，格式資訊會包含在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構中。 下列範例顯示如何取得未壓縮影片串流的格式資訊。


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> 範例捕獲不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)。

 

## <a name="example-code"></a>範例程式碼

以下是上述範例的完整程式碼。

> [!Note]  
> 此範例會使用 [SafeRelease](../medfound/saferelease.md) 函式來釋放介面指標。

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 
