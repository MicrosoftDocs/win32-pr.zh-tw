---
description: 控制捕捉圖形
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: 控制捕捉圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0089fa11adbc0ac861fb9e8e30e2cd0f56b23680
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909046"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="3fe9e-103">控制捕捉圖形</span><span class="sxs-lookup"><span data-stu-id="3fe9e-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="3fe9e-104">篩選圖形管理員的 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面具有執行、停止和暫停整個圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="3fe9e-105">但是，如果篩選圖形具有 capture 和 preview 資料流程，您可能會想要獨立控制兩個數據流。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="3fe9e-106">例如，您可能想要預覽影片而不加以捕捉。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="3fe9e-107">您可以透過 [**ICaptureGraphBuilder2：： ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) 方法來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="3fe9e-108">當捕捉到 Advanced 系統格式 (ASF) 檔案時，此方法無法運作。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="3fe9e-109">控制 Capture 資料流程</span><span class="sxs-lookup"><span data-stu-id="3fe9e-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="3fe9e-110">下列程式碼會將影片捕獲串流設定為執行四秒，並在圖形執行後一秒啟動：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="3fe9e-111">第一個參數會指定要控制的資料流程，做為釘選類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="3fe9e-112">第二個參數會提供媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-112">The second parameter gives the media type.</span></span> <span data-ttu-id="3fe9e-113">第三個參數是 capture 篩選器的指標。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="3fe9e-114">若要控制圖形中的所有 capture 資料流程，請將第二個和第三個參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="3fe9e-115">接下來的兩個參數會定義資料流程的開始和停止時間（相對於圖形開始執行的時間）。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="3fe9e-116">呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 以執行圖形。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="3fe9e-117">在您執行圖形之前， **ControlStream** 方法不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="3fe9e-118">如果圖形已在執行中，則設定會立即生效。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="3fe9e-119">最後兩個參數是用來在資料流程啟動和停止時取得事件通知。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="3fe9e-120">針對您使用這個方法所控制的每個資料流程，篩選圖形都會傳送一組事件：在資料流程啟動時 [**開始使用 ec \_ stream \_ \_ control**](ec-stream-control-started.md) ，而當資料流程停止時，則會 [**\_ \_ \_ 停止 ec 資料流程**](ec-stream-control-stopped.md) 控制。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="3fe9e-121">**WStartCookie** 和 **wStopCookie** 的值會當做第二個事件參數使用。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="3fe9e-122">因此，start 事件中的 *lParam2* 等於 **wStartCookie**，而 Stop 事件中的 *lParam2* 等於 **wStopCookie**。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="3fe9e-123">下列程式碼顯示如何取得這些事件：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="3fe9e-124">**ControlStream** 方法會定義一些開始和停止時間的特殊值。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="3fe9e-125">標籤</span><span class="sxs-lookup"><span data-stu-id="3fe9e-125">Label</span></span> | <span data-ttu-id="3fe9e-126">值</span><span class="sxs-lookup"><span data-stu-id="3fe9e-126">Value</span></span> |
|-------------|----------------------------------------|------------------------------------|
|             | <span data-ttu-id="3fe9e-127">開始</span><span class="sxs-lookup"><span data-stu-id="3fe9e-127">Start</span></span>                                  | <span data-ttu-id="3fe9e-128">Stop</span><span class="sxs-lookup"><span data-stu-id="3fe9e-128">Stop</span></span>                               |
| <span data-ttu-id="3fe9e-129">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="3fe9e-129">MAXLONGLONG</span></span> | <span data-ttu-id="3fe9e-130">永遠不會啟動此資料流程。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-130">Never start this stream.</span></span>               | <span data-ttu-id="3fe9e-131">除非圖形停止，否則請勿停止。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-131">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="3fe9e-132">**NULL**</span><span class="sxs-lookup"><span data-stu-id="3fe9e-132">**NULL**</span></span>    | <span data-ttu-id="3fe9e-133">在圖形執行時立即啟動。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-133">Start immediately when the graph runs.</span></span> | <span data-ttu-id="3fe9e-134">立即停止。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-134">Stop immediately.</span></span>                  |



 

<span data-ttu-id="3fe9e-135">例如，下列程式碼會立即停止 capture 資料流程：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-135">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="3fe9e-136">雖然您可以停止 capture 資料流程並于稍後重新開機，但這會在時間戳記中產生間距。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-136">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="3fe9e-137">在播放時，根據檔案格式) ，影片會顯示在間距 (期間會停止。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-137">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="3fe9e-138">控制預覽資料流程</span><span class="sxs-lookup"><span data-stu-id="3fe9e-138">Controlling the Preview Stream</span></span>

<span data-ttu-id="3fe9e-139">若要控制預覽 pin，請呼叫 **ControlStream** ，但設定第一個參數來釘選 \_ 類別目錄 \_ 預覽。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-139">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="3fe9e-140">其運作方式就像是釘選 \_ 類別 \_ 捕捉一樣，不同的是，您無法使用參考時間來指定開始和停止，因為預覽畫面沒有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-140">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="3fe9e-141">因此，您必須使用 **Null** 或 MAXLONGLONG。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-141">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="3fe9e-142">使用 **Null** 來啟動預覽資料流程：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-142">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="3fe9e-143">使用 MAXLONGLONG 來停止預覽資料流程：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-143">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="3fe9e-144">預覽資料流程是否來自 capture 篩選器上的預覽 pin，或來自智慧型指標篩選器，並不重要。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-144">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="3fe9e-145">**ControlStream** 方法的運作方式有兩種。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-145">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="3fe9e-146">不過，若為影片埠 pin，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-146">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="3fe9e-147">在這種情況下，另一種方法是隱藏影片視窗。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-147">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="3fe9e-148">查詢圖表以取得 **IVideoWindow**，並使用 [ [**IVideoWindow：:p] \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) 顯示或隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-148">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="3fe9e-149">此外，如果您在執行圖形之前呼叫 [**IVideoWindow：:p \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) ] OAFALSE 會顯示值，則影片轉譯器篩選會隱藏視窗，直到您另外指定為止。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-149">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="3fe9e-150">根據預設，影片轉譯器會在您執行圖形時顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-150">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="3fe9e-151">關於資料流程控制的備註</span><span class="sxs-lookup"><span data-stu-id="3fe9e-151">Remarks about Stream Control</span></span>

<span data-ttu-id="3fe9e-152">Pin 的預設行為是在圖形執行時傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-152">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="3fe9e-153">例如，假設您使用 PIN 類別捕獲來呼叫 **ControlStream** ， \_ \_ 而不是使用 pin \_ 類別 \_ 預覽。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-153">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="3fe9e-154">當您執行圖形時，預覽資料流程會立即執行，而 capture 資料流程則會在您于 **ControlStream** 中指定的任何時間執行。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-154">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="3fe9e-155">如果您要捕捉一個以上的資料流程，並將它們傳送至 mux 篩選器（例如，如果您要將音訊和影片捕獲到 AVI 檔案），您應該一次控制兩個數據流。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-155">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="3fe9e-156">否則，mux 篩選器可能會封鎖等候一個資料流程，因為它會嘗試交錯兩個數據流。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-156">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="3fe9e-157">在執行圖形之前，請在所有的捕獲資料流程上設定相同的開始和停止時間：</span><span class="sxs-lookup"><span data-stu-id="3fe9e-157">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="3fe9e-158">就內部而言， **ControlStream** 方法會使用 [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) 介面，此介面會在捕捉篩選器的釘選上、Smart t 濾波器 (（如果有的話) ，也可能是 mux 篩選器）。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-158">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="3fe9e-159">您可以直接使用此介面，而不是呼叫 **ControlStream**，不過這樣做並沒有任何特定的優點。</span><span class="sxs-lookup"><span data-stu-id="3fe9e-159">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe9e-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fe9e-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe9e-161">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="3fe9e-161">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



