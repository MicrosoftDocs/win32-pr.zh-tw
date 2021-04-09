---
description: 從靜止影像 Pin 捕捉影像
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: 從靜止影像 Pin 捕捉影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687720"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="01f44-103">從靜止影像 Pin 捕捉影像</span><span class="sxs-lookup"><span data-stu-id="01f44-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="01f44-104">有些攝影機可以產生與 capture 串流不同的靜止影像，而且仍有影像的品質高於 capture 串流所產生的影像。</span><span class="sxs-lookup"><span data-stu-id="01f44-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="01f44-105">相機可能會有作為硬體觸發程式的按鈕，或可能支援觸發軟體。</span><span class="sxs-lookup"><span data-stu-id="01f44-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="01f44-106">支援仍影像的相機會公開靜止的影像釘選，也就是釘選類別目錄釘選 \_ 類別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01f44-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="01f44-107">從裝置取得靜止影像的建議方式是使用 Windows 映像取得 (WIA) Api。</span><span class="sxs-lookup"><span data-stu-id="01f44-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="01f44-108">如需詳細資訊，請參閱 Platform SDK 檔中的「Windows 映像取得」。</span><span class="sxs-lookup"><span data-stu-id="01f44-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="01f44-109">不過，您也可以使用 DirectShow 來捕捉映射。</span><span class="sxs-lookup"><span data-stu-id="01f44-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="01f44-110">若要觸發靜止的 pin，請在圖形執行時使用 [**IAMVideoControl：： SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) 方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="01f44-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


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



<span data-ttu-id="01f44-111">查詢 [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)的捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="01f44-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="01f44-112">如果支援介面，請呼叫 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)方法來取得仍釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標，如先前範例所示。</span><span class="sxs-lookup"><span data-stu-id="01f44-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="01f44-113">然後使用 **IPin** 指標和 VideoControlFlag 觸發程式旗標來呼叫 [**IAMVideoControl：： SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) \_ 。</span><span class="sxs-lookup"><span data-stu-id="01f44-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="01f44-114">根據相機的不同，您可能需要先轉譯捕捉釘 (釘選 \_ 類別 \_ 捕獲) ，才能連接到仍在連線的 pin。</span><span class="sxs-lookup"><span data-stu-id="01f44-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="01f44-115">範例：使用範例捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="01f44-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="01f44-116">捕捉映射的其中一種方式是使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="01f44-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="01f44-117">範例捕獲會使用應用程式定義的回呼函式來處理影像。</span><span class="sxs-lookup"><span data-stu-id="01f44-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="01f44-118">如需範例捕獲篩選器的詳細資訊，請參閱 [使用範例](using-the-sample-grabber.md)抓取器。</span><span class="sxs-lookup"><span data-stu-id="01f44-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="01f44-119">下列範例假設仍有 pin 可傳遞未壓縮的 RGB 映射。</span><span class="sxs-lookup"><span data-stu-id="01f44-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="01f44-120">首先，定義將會執行範例捕獲程式回呼介面（ [**ISampleGrabberCB**](isamplegrabbercb.md)）的類別：</span><span class="sxs-lookup"><span data-stu-id="01f44-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="01f44-121">類別的實作為很快的說明。</span><span class="sxs-lookup"><span data-stu-id="01f44-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="01f44-122">接下來，將仍釘選到範例抓取器，並將範例抓取器連接到 [**Null**](null-renderer-filter.md) 轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="01f44-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="01f44-123">Null 轉譯器只會捨棄所接收的媒體範例;實際的工作將在回呼中完成。</span><span class="sxs-lookup"><span data-stu-id="01f44-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="01f44-124"> (Null 轉譯器的唯一原因是要將範例抓取器的輸出圖釘連接到某個東西。 ) 呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立範例抓取器和 Null 轉譯器篩選器，並呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將這兩個篩選器新增至圖形：</span><span class="sxs-lookup"><span data-stu-id="01f44-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


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



<span data-ttu-id="01f44-125">您可以使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，在一個方法呼叫中連接所有三個篩選準則，從仍釘選到範例抓取器，再從範例抓取到 Null 轉譯器：</span><span class="sxs-lookup"><span data-stu-id="01f44-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="01f44-126">現在使用 [**ISampleGrabber**](isamplegrabber.md) 介面設定範例抓取程式，使其可緩衝範例：</span><span class="sxs-lookup"><span data-stu-id="01f44-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


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



<span data-ttu-id="01f44-127">使用回呼物件的指標設定回呼介面：</span><span class="sxs-lookup"><span data-stu-id="01f44-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="01f44-128">取得仍用來與範例抓取程式連接的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="01f44-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="01f44-129">此媒體類型將包含定義靜止影像格式的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="01f44-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="01f44-130">在應用程式結束之前釋放媒體類型：</span><span class="sxs-lookup"><span data-stu-id="01f44-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="01f44-131">接下來是回呼類別的範例。</span><span class="sxs-lookup"><span data-stu-id="01f44-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="01f44-132">請注意，類別會實 [**ISampleGrabber**](isamplegrabber.md)介面所繼承的 **IUnknown**，但不會保留參考計數。</span><span class="sxs-lookup"><span data-stu-id="01f44-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="01f44-133">這是安全的，因為應用程式會在堆疊上建立物件，而物件在篩選圖形的整個存留期內仍維持在範圍內。</span><span class="sxs-lookup"><span data-stu-id="01f44-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="01f44-134">所有的工作都是在 [**BufferCB**](isamplegrabbercb-buffercb.md) 方法中執行，而此方法會在每次取得新的範例時由範例抓取程式呼叫。</span><span class="sxs-lookup"><span data-stu-id="01f44-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="01f44-135">在下列範例中，方法會將點陣圖寫入至檔案：</span><span class="sxs-lookup"><span data-stu-id="01f44-135">In the following example, the method writes the bitmap to a file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="01f44-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="01f44-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f44-137">影片捕獲工作</span><span class="sxs-lookup"><span data-stu-id="01f44-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
