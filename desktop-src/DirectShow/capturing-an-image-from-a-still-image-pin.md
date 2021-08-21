---
description: 從靜止影像 Pin 捕捉影像
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: 從靜止影像 Pin 捕捉影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab750fb6b847bc39d28c8906df8dcb982278f7a4447bfc3d79631ee58eb574e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158660"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>從靜止影像 Pin 捕捉影像

有些攝影機可以產生與 capture 串流不同的靜止影像，而且仍有影像的品質高於 capture 串流所產生的影像。 相機可能會有作為硬體觸發程式的按鈕，或可能支援觸發軟體。 支援仍影像的相機會公開靜止的影像釘選，也就是釘選類別目錄釘選 \_ 類別 \_ 。

從裝置取得靜止影像的建議方式，是使用 Windows 映像取得 (WIA) api。 如需詳細資訊，請參閱 Platform SDK 檔中的「Windows 映像取得」。 不過，您也可以使用 DirectShow 來捕捉映射。

若要觸發靜止的 pin，請在圖形執行時使用 [**IAMVideoControl：： SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) 方法，如下所示：


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



查詢 [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)的捕獲篩選。 如果支援介面，請呼叫 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)方法來取得仍釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標，如先前範例所示。 然後使用 **IPin** 指標和 VideoControlFlag 觸發程式旗標來呼叫 [**IAMVideoControl：： SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) \_ 。

> [!Note]  
> 根據相機的不同，您可能需要先轉譯捕捉釘 (釘選 \_ 類別 \_ 捕獲) ，才能連接到仍在連線的 pin。

 

### <a name="example-using-the-sample-grabber-filter"></a>範例：使用範例捕獲篩選器

捕捉映射的其中一種方式是使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器。 範例捕獲會使用應用程式定義的回呼函式來處理影像。 如需範例捕獲篩選器的詳細資訊，請參閱 [使用範例](using-the-sample-grabber.md)抓取器。

下列範例假設仍有 pin 可傳遞未壓縮的 RGB 映射。 首先，定義將會執行範例捕獲程式回呼介面（ [**ISampleGrabberCB**](isamplegrabbercb.md)）的類別：


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



類別的實作為很快的說明。

接下來，將仍釘選到範例抓取器，並將範例抓取器連接到 [**Null**](null-renderer-filter.md) 轉譯器篩選器。 Null 轉譯器只會捨棄所接收的媒體範例;實際的工作將在回呼中完成。  (Null 轉譯器的唯一原因是要將範例抓取器的輸出圖釘連接到某個東西。 ) 呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立範例抓取器和 Null 轉譯器篩選器，並呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將這兩個篩選器新增至圖形：


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



您可以使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，在一個方法呼叫中連接所有三個篩選準則，從仍釘選到範例抓取器，再從範例抓取到 Null 轉譯器：


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



現在使用 [**ISampleGrabber**](isamplegrabber.md) 介面設定範例抓取程式，使其可緩衝範例：


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



使用回呼物件的指標設定回呼介面：


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



取得仍用來與範例抓取程式連接的媒體類型：


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



此媒體類型將包含定義靜止影像格式的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。 在應用程式結束之前釋放媒體類型：


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



接下來是回呼類別的範例。 請注意，類別會實 [**ISampleGrabber**](isamplegrabber.md)介面所繼承的 **IUnknown**，但不會保留參考計數。 這是安全的，因為應用程式會在堆疊上建立物件，而物件在篩選圖形的整個存留期內仍維持在範圍內。

所有的工作都是在 [**BufferCB**](isamplegrabbercb-buffercb.md) 方法中執行，而此方法會在每次取得新的範例時由範例抓取程式呼叫。 在下列範例中，方法會將點陣圖寫入至檔案：


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲工作](video-capture-tasks.md)
</dt> </dl>

 

 
