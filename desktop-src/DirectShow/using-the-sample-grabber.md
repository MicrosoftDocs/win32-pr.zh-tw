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
# <a name="using-the-sample-grabber"></a><span data-ttu-id="b3e6d-103">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="b3e6d-103">Using the Sample Grabber</span></span>

<span data-ttu-id="b3e6d-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b3e6d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b3e6d-105">[**範例捕獲**](sample-grabber-filter.md)篩選器是一種轉換篩選器，可用來從資料流程取得媒體範例，因為它們通過篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="b3e6d-106">如果您只是要從影片檔案抓取點陣圖， [ (MediaDet) ](media-detector--mediadet.md) 物件中使用媒體偵測器會比較容易。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="b3e6d-107">如需詳細資訊，請參閱 [抓取海報框架](grabbing-a-poster-frame.md) 。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="b3e6d-108">不過，範例抓取程式更有彈性，因為它幾乎適用于任何媒體類型 (請參閱 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md)) 的幾個例外狀況，並為應用程式提供更多控制權。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="b3e6d-109">建立篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="b3e6d-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="b3e6d-110">將範例捕獲新增至篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="b3e6d-111">設定媒體類型</span><span class="sxs-lookup"><span data-stu-id="b3e6d-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="b3e6d-112">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="b3e6d-113">執行圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="b3e6d-114">抓取範例</span><span class="sxs-lookup"><span data-stu-id="b3e6d-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="b3e6d-115">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b3e6d-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="b3e6d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3e6d-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="b3e6d-117">建立篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="b3e6d-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="b3e6d-118">若要開始，請建立 [篩選圖形管理員](filter-graph-manager.md) 並查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


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





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="b3e6d-119">將範例捕獲新增至篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="b3e6d-120">建立範例捕獲篩選器的實例，並 addit 至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="b3e6d-121">查詢 [**ISampleGrabber**](isamplegrabber.md) 介面的範例捕獲篩選器。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


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





## <a name="set-the-media-type"></a><span data-ttu-id="b3e6d-122">設定媒體類型</span><span class="sxs-lookup"><span data-stu-id="b3e6d-122">Set the Media Type</span></span>

<span data-ttu-id="b3e6d-123">當您第一次建立範例抓取器時，它沒有慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="b3e6d-124">這表示您可以連接到圖表中幾乎任何篩選器，但無法控制其所接收的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="b3e6d-125">因此，在建立圖形的其餘部分之前，您必須藉由呼叫 [**ISampleGrabber：： SetMediaType**](isamplegrabber-setmediatype.md) 方法，來設定範例抓取器的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="b3e6d-126">當範例抓取器連線時，它會比較此媒體類型與其他篩選器所提供的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="b3e6d-127">它檢查的唯一欄位是主要類型、子類型和格式類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="b3e6d-128">針對上述任何一種，值 GUID \_ Null 表示「接受任何值」。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="b3e6d-129">在大部分的情況下，您會想要設定主要類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="b3e6d-130">例如，下列程式碼指定未壓縮的24位 RGB 影片：</span><span class="sxs-lookup"><span data-stu-id="b3e6d-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


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



## <a name="build-the-filter-graph"></a><span data-ttu-id="b3e6d-131">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-131">Build the Filter Graph</span></span>

<span data-ttu-id="b3e6d-132">現在您可以建立篩選圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="b3e6d-133">因為範例抓取器只會使用您指定的媒體類型進行連線，這可讓您在建立圖表時利用篩選圖形管理員的 [智慧型連接](intelligent-connect.md) 機制。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="b3e6d-134">例如，如果您指定了未壓縮的影片，您可以將來源篩選連接到範例抓取器，而篩選圖形管理員會自動加入檔案剖析器和解碼器。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="b3e6d-135">下列範例會使用 ConnectFilters helper 函式，它會列在 [[連接兩個篩選器]](connect-two-filters.md)中：</span><span class="sxs-lookup"><span data-stu-id="b3e6d-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


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





<span data-ttu-id="b3e6d-136">範例抓取器是轉換篩選，因此輸出的 pin 必須連接到另一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="b3e6d-137">通常，您可能只想要在完成後捨棄範例。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="b3e6d-138">在這種情況下，請將範例抓取 [**器連接到 Null 轉譯器篩選器**](null-renderer-filter.md)，這會捨棄它所收到的資料。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="b3e6d-139">下列範例會將範例抓取器連接到 Null 轉譯器篩選準則：</span><span class="sxs-lookup"><span data-stu-id="b3e6d-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


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





<span data-ttu-id="b3e6d-140">請注意，在影片解碼和影片轉譯器之間放置範例，可能會大幅影響轉譯效能。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="b3e6d-141">範例抓取器是一種就地篩選，這表示輸出緩衝區與輸入緩衝區相同。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="b3e6d-142">針對影片轉譯，輸出緩衝區可能位於圖形配接器上，其中讀取作業的速度會比主儲存體中的讀取作業慢很多。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="b3e6d-143">執行圖形</span><span class="sxs-lookup"><span data-stu-id="b3e6d-143">Run the Graph</span></span>

<span data-ttu-id="b3e6d-144">範例抓取程式會以兩種模式的其中一種方式運作：</span><span class="sxs-lookup"><span data-stu-id="b3e6d-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="b3e6d-145">緩衝模式會在傳遞範例下游之前，先複製每個範例。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="b3e6d-146">回呼模式會在每個範例上叫用應用程式定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="b3e6d-147">本文說明緩衝模式。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-147">This article describes buffering mode.</span></span> <span data-ttu-id="b3e6d-148"> (在使用回呼模式之前，請注意回呼函數必須有相當大的限制。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="b3e6d-149">否則，它可能會大幅降低效能，甚至造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="b3e6d-150">如需詳細資訊，請參閱 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)。 ) 若要啟用緩衝處理模式，請使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="b3e6d-151">（選擇性）使用值 **TRUE** 來呼叫 [**ISampleGrabber：： SetOneShot**](isamplegrabber-setoneshot.md)方法。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="b3e6d-152">這會導致範例捕獲程式在收到第一個媒體範例之後停止，這在您想要從資料流程抓取單一畫面格時很有用。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="b3e6d-153">搜尋所需的時間、執行圖形，然後等候 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="b3e6d-154">請注意，畫面格精確度的層級取決於來源。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="b3e6d-155">例如，在尋找 MPEG 檔案時，通常不會有正確的框架。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="b3e6d-156">若要儘快執行圖形，請依照 [設定圖形時鐘](setting-the-graph-clock.md)中所述的方式來開啟圖形時鐘。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="b3e6d-157">下列範例會啟用一次模式和緩衝模式、執行篩選圖形，並等候完成。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


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



## <a name="grab-the-sample"></a><span data-ttu-id="b3e6d-158">抓取範例</span><span class="sxs-lookup"><span data-stu-id="b3e6d-158">Grab the Sample</span></span>

<span data-ttu-id="b3e6d-159">在緩衝模式中，範例捕獲會儲存每個範例的複本。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="b3e6d-160">[**ISampleGrabber：： GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)方法會將緩衝區複製到呼叫端配置的陣列中。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="b3e6d-161">若要判斷所需陣列的大小，請先使用陣列位址的 **Null** 指標來呼叫 **GetCurrentBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="b3e6d-162">然後配置陣列，並再次呼叫方法來複製緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="b3e6d-163">下列範例會示範這些步驟。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-163">The following example shows these steps.</span></span>


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



<span data-ttu-id="b3e6d-164">您將需要知道緩衝區中資料的確切格式。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="b3e6d-165">若要取得此資訊，請呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="b3e6d-166">這個方法會使用格式來填滿 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="b3e6d-167">若是未壓縮的影片資料流程，格式資訊會包含在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構中。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="b3e6d-168">下列範例顯示如何取得未壓縮影片串流的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


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
> <span data-ttu-id="b3e6d-169">範例捕獲不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="b3e6d-170">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b3e6d-170">Example Code</span></span>

<span data-ttu-id="b3e6d-171">以下是上述範例的完整程式碼。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="b3e6d-172">此範例會使用 [SafeRelease](../medfound/saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="b3e6d-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


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





## <a name="related-topics"></a><span data-ttu-id="b3e6d-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3e6d-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3e6d-174">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="b3e6d-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
