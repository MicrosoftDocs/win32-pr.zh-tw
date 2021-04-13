---
description: 本主題說明如何撰寫適用于 DirectShow 的自訂來源篩選。
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: 如何撰寫 DirectShow 的來源篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510291"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a><span data-ttu-id="59c23-103">如何撰寫 DirectShow 的來源篩選</span><span class="sxs-lookup"><span data-stu-id="59c23-103">How to Write a Source Filter for DirectShow</span></span>

<span data-ttu-id="59c23-104">本主題說明如何撰寫適用于 DirectShow 的自訂來源篩選。</span><span class="sxs-lookup"><span data-stu-id="59c23-104">This topic describes how to write a custom source filter for DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="59c23-105">本主題僅描述推送來源;它不會描述提取來源（例如，非同步讀取器篩選器）或連接到提取來源的分隔器篩選。</span><span class="sxs-lookup"><span data-stu-id="59c23-105">This topic describes push sources only; it does not describe pull sources, such as the Async Reader Filter, or splitter filters that connect to pull sources.</span></span> <span data-ttu-id="59c23-106">如需 *推送* 和 *提取* 來源之間的差異，請參閱 [篩選開發人員的資料流程](data-flow-for-filter-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="59c23-106">For the distinction between *push* and *pull* sources, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 

## <a name="the-directshow-streaming-model"></a><span data-ttu-id="59c23-107">DirectShow 串流模型</span><span class="sxs-lookup"><span data-stu-id="59c23-107">The DirectShow Streaming Model</span></span>

<span data-ttu-id="59c23-108">當您撰寫來源篩選器時，請務必瞭解推播來源與即時來源的內容不同。</span><span class="sxs-lookup"><span data-stu-id="59c23-108">When you write a source filter, it is important to understand that a push source is not the same thing as a live source.</span></span> <span data-ttu-id="59c23-109">即時來源會從某個外部來源（例如相機或網路串流）取得資料。</span><span class="sxs-lookup"><span data-stu-id="59c23-109">A live source gets data from some external source, such as a camera or a network stream.</span></span> <span data-ttu-id="59c23-110">一般情況下，即時來源無法控制傳入資料的速率。</span><span class="sxs-lookup"><span data-stu-id="59c23-110">Generally, a live source cannot control the incoming rate of data.</span></span> <span data-ttu-id="59c23-111">如果下游篩選器的資料不夠快，則來源需要卸載範例。</span><span class="sxs-lookup"><span data-stu-id="59c23-111">If the downstream filters do not consume the data fast enough, the source will need to drop samples.</span></span>

<span data-ttu-id="59c23-112">但推送來源不必是即時來源。</span><span class="sxs-lookup"><span data-stu-id="59c23-112">But a push source does not have to be a live source.</span></span> <span data-ttu-id="59c23-113">例如，推送來源可以從本機檔案讀取資料。</span><span class="sxs-lookup"><span data-stu-id="59c23-113">For example, a push source can read data from a local file.</span></span> <span data-ttu-id="59c23-114">在這種情況下，下游轉譯器篩選器會根據參考時鐘和取樣時間戳記，判斷其從來源取用資料的速度。</span><span class="sxs-lookup"><span data-stu-id="59c23-114">In that case, the downstream renderer filters determine how fast they consume the data from the source, based on the reference clock and the sample time stamps.</span></span> <span data-ttu-id="59c23-115">來源篩選器會儘快傳遞範例，但實際的資料流程會受到轉譯器的限制。</span><span class="sxs-lookup"><span data-stu-id="59c23-115">The source filter delivers samples as quickly as possible, but the actual data flow is gated limited by the renderers.</span></span> <span data-ttu-id="59c23-116">[篩選器開發人員](data-flow-for-filter-developers.md)的資料流程中描述了控制資料流程的機制。</span><span class="sxs-lookup"><span data-stu-id="59c23-116">The mechanisms for gating the data flow are described in [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

<span data-ttu-id="59c23-117">來源篩選器上的每個輸出釘選都會建立一個稱為 *串流執行緒* 的執行緒。</span><span class="sxs-lookup"><span data-stu-id="59c23-117">Each output pin on the source filter creates a thread called a *streaming thread*.</span></span> <span data-ttu-id="59c23-118">Pin 會在串流處理執行緒上提供範例。</span><span class="sxs-lookup"><span data-stu-id="59c23-118">The pin delivers samples on the streaming thread.</span></span> <span data-ttu-id="59c23-119">一般而言，所有的解碼、處理和轉譯都會發生在此執行緒上，不過某些下游篩選器可能會建立額外的執行緒，以將其輸出範例排入佇列。</span><span class="sxs-lookup"><span data-stu-id="59c23-119">Typically, all of the decoding, processing, and rendering happens on this thread, although some downstream filters might create additional threads to queue their output samples.</span></span>

<span data-ttu-id="59c23-120">串流執行緒會使用下列結構執行迴圈：</span><span class="sxs-lookup"><span data-stu-id="59c23-120">The streaming thread runs a loop with the following structure:</span></span>

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

<span data-ttu-id="59c23-121">如果沒有可用的範例，步驟1會封鎖，直到範例可供使用為止。</span><span class="sxs-lookup"><span data-stu-id="59c23-121">If no samples are available, step 1 blocks until a sample becomes available.</span></span> <span data-ttu-id="59c23-122">步驟4也可以封鎖;例如，它可以在圖形暫停時封鎖。</span><span class="sxs-lookup"><span data-stu-id="59c23-122">Step 4 can also block; for example, it can block while the graph is paused.</span></span>

<span data-ttu-id="59c23-123">迴圈會儘快執行，但受限於轉譯器篩選器轉譯每個樣本的速度。</span><span class="sxs-lookup"><span data-stu-id="59c23-123">The loop runs as quickly as possible, but is limited by how quickly the renderer filter renders each sample.</span></span> <span data-ttu-id="59c23-124">假設篩選圖形具有參考時鐘，則速率取決於樣本上的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="59c23-124">Assuming the filter graph has a reference clock, the rate is determined by the presentation times on the samples.</span></span> <span data-ttu-id="59c23-125">如果沒有參考時鐘，轉譯器會儘快取用樣本。</span><span class="sxs-lookup"><span data-stu-id="59c23-125">If there is no reference clock, the renderer consumes samples as quickly as possible.</span></span>

## <a name="using-csource-and-csourcestream"></a><span data-ttu-id="59c23-126">使用 CSource 和 CSourceStream</span><span class="sxs-lookup"><span data-stu-id="59c23-126">Using CSource and CSourceStream</span></span>

<span data-ttu-id="59c23-127">DirectShow 基礎類別包含兩個支援推送來源的類別： [**CSource**](csource.md) 和 [**CSourceStream**](csourcestream.md)。</span><span class="sxs-lookup"><span data-stu-id="59c23-127">The DirectShow base classes include two classes that support push sources: [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

-   <span data-ttu-id="59c23-128">[**CSource**](csource.md) 是篩選的基類，並會執行 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面。</span><span class="sxs-lookup"><span data-stu-id="59c23-128">[**CSource**](csource.md) is the base class for the filter and implements the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>
-   <span data-ttu-id="59c23-129">[**CSourceStream**](csourcestream.md) 是輸出圖釘的基類，並會執行 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面。</span><span class="sxs-lookup"><span data-stu-id="59c23-129">[**CSourceStream**](csourcestream.md) is the base class for the output pins, and implements the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

### <a name="output-pins"></a><span data-ttu-id="59c23-130">輸出圖釘</span><span class="sxs-lookup"><span data-stu-id="59c23-130">Output Pins</span></span>

<span data-ttu-id="59c23-131">來源篩選器可以有一個以上的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="59c23-131">A source filter can have more than one output pin.</span></span> <span data-ttu-id="59c23-132">在篩選器的函式方法中，建立一或多個衍生自 [**CSourceStream**](csourcestream.md) 的 pin (每個輸出資料流程) 一個 pin。</span><span class="sxs-lookup"><span data-stu-id="59c23-132">In your filter's constructor method, create one or more pins derived from [**CSourceStream**](csourcestream.md) (one pin per output stream).</span></span> <span data-ttu-id="59c23-133">您不需要儲存釘選的指標;pin 會在建立時自動將自己新增至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="59c23-133">You don't need to store pointers to the pins; the pins automatically add themselves to the filter when they are created.</span></span>

### <a name="output-formats"></a><span data-ttu-id="59c23-134">輸出格式</span><span class="sxs-lookup"><span data-stu-id="59c23-134">Output Formats</span></span>

<span data-ttu-id="59c23-135">輸出圖釘會使用下列 [**CSourceStream**](csourcestream.md) 方法來處理格式的協商：</span><span class="sxs-lookup"><span data-stu-id="59c23-135">The output pin handles format negotiation with the following [**CSourceStream**](csourcestream.md) methods:</span></span>



| <span data-ttu-id="59c23-136">方法</span><span class="sxs-lookup"><span data-stu-id="59c23-136">Method</span></span>                                                 | <span data-ttu-id="59c23-137">描述</span><span class="sxs-lookup"><span data-stu-id="59c23-137">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59c23-138">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="59c23-138">**GetMediaType**</span></span>](csourcestream-getmediatype.md)     | <span data-ttu-id="59c23-139">從輸出圖釘取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="59c23-139">Gets a media type from the output pin.</span></span> <br/> <span data-ttu-id="59c23-140">Pin 必須至少提議一個媒體類型，因為下游篩選器可能不會建議任何類型。</span><span class="sxs-lookup"><span data-stu-id="59c23-140">The pin must propose at least one media type, because the downstream filter might not propose any types.</span></span> <span data-ttu-id="59c23-141">在大部分情況下，下游篩選器會是一個解碼器或轉譯器，視來源篩選器是否提供壓縮或未壓縮的資料而定。</span><span class="sxs-lookup"><span data-stu-id="59c23-141">In most cases, the downstream filter will be a decoder or a renderer, depending on whether the source filter delivers compressed or uncompressed data.</span></span> <span data-ttu-id="59c23-142">轉譯器篩選器通常需要完整的媒體類型，其中包含轉譯資料流程所需的所有格式資訊。</span><span class="sxs-lookup"><span data-stu-id="59c23-142">A renderer filter usually requires a complete media type, containing all of the format information needed to render the stream.</span></span> <span data-ttu-id="59c23-143">若為解碼器，媒體類型中所需的資訊數量，會非常依賴編碼格式。</span><span class="sxs-lookup"><span data-stu-id="59c23-143">For a decoder, the amount of information that is required in the media type depends very much on the encoding format.</span></span><br/> |
| [<span data-ttu-id="59c23-144">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="59c23-144">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md) | <span data-ttu-id="59c23-145">檢查輸出釘選是否接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="59c23-145">Checks if the output pin accepts a given media type.</span></span> <span data-ttu-id="59c23-146">覆寫這個方法是選擇性的，視您執行 [**GetMediaType**](csourcestream-getmediatype.md)的方式而定。</span><span class="sxs-lookup"><span data-stu-id="59c23-146">Overriding this method is optional, depending on how you implement [**GetMediaType**](csourcestream-getmediatype.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="59c23-147">[**GetMediaType**](csourcestream-getmediatype.md)方法超載：</span><span class="sxs-lookup"><span data-stu-id="59c23-147">The [**GetMediaType**](csourcestream-getmediatype.md) method is overloaded:</span></span>

-   <span data-ttu-id="59c23-148">[**GetMediaType**](csourcestream-getmediatype.md) (1) 接受單一參數，也就是 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="59c23-148">[**GetMediaType**](csourcestream-getmediatype.md) (1) takes a single parameter, a pointer to a [**CMediaType**](cmediatype.md) object.</span></span>
-   <span data-ttu-id="59c23-149">[**GetMediaType**](csourcestream-getmediatype2.md) (2) 接受索引變數和 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="59c23-149">[**GetMediaType**](csourcestream-getmediatype2.md) (2) takes an index variable and a pointer to a [**CMediaType**](cmediatype.md) object.</span></span>

<span data-ttu-id="59c23-150">如果來源篩選的輸出 pin 只支援一個媒體格式，您應該覆寫 (1) ，以使用該格式來初始化 [**CMediaType**](cmediatype.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="59c23-150">If the source filter's output pin supports exactly one media format, you should override (1) to initialize the [**CMediaType**](cmediatype.md) object with that format.</span></span> <span data-ttu-id="59c23-151">保留 (2) 的預設值，並保留 [**CheckMediaType**](csourcestream-checkmediatype.md)的預設執行。</span><span class="sxs-lookup"><span data-stu-id="59c23-151">Leave the default implementation of (2) and also leave the default implementation of [**CheckMediaType**](csourcestream-checkmediatype.md).</span></span>

<span data-ttu-id="59c23-152">如果 pin 支援一種以上的格式，請覆寫 (2) 。</span><span class="sxs-lookup"><span data-stu-id="59c23-152">If the pin supports more than one format, override (2).</span></span> <span data-ttu-id="59c23-153">根據索引變數的值，初始化 [**CMediaType**](cmediatype.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="59c23-153">Initialize the [**CMediaType**](cmediatype.md) object according to the value of the index variable.</span></span> <span data-ttu-id="59c23-154">Pin 應會以排序清單的形式傳回格式。</span><span class="sxs-lookup"><span data-stu-id="59c23-154">The pin should return the formats as an ordered list.</span></span> <span data-ttu-id="59c23-155">在此情況下，您也必須覆寫 [**CheckMediaType**](csourcestream-checkmediatype.md) ，以根據您的格式清單來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="59c23-155">In this case, you must also override the [**CheckMediaType**](csourcestream-checkmediatype.md) to check the media type against your list of formats.</span></span>

<span data-ttu-id="59c23-156">針對未壓縮的影片格式，請記住下游篩選器可以使用各種 stride 值來建議格式。</span><span class="sxs-lookup"><span data-stu-id="59c23-156">For uncompressed video formats, remember that the downstream filter can propose formats with various stride values.</span></span> <span data-ttu-id="59c23-157">您的篩選準則應該接受任何有效的 stride 值。</span><span class="sxs-lookup"><span data-stu-id="59c23-157">Your filter should accept any valid stride value.</span></span> <span data-ttu-id="59c23-158">如需詳細資訊，請參閱 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)。</span><span class="sxs-lookup"><span data-stu-id="59c23-158">For more information, see [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).</span></span>

<span data-ttu-id="59c23-159">您也必須覆寫純虛擬 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="59c23-159">You must also override the pure-virtual [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="59c23-160">您可以使用這個方法來設定範例緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="59c23-160">Use this method to set the size of the sample buffers.</span></span>

### <a name="streaming"></a><span data-ttu-id="59c23-161">串流</span><span class="sxs-lookup"><span data-stu-id="59c23-161">Streaming</span></span>

<span data-ttu-id="59c23-162">[**CSourceStream**](csourcestream.md)類別會建立 pin 的串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="59c23-162">The [**CSourceStream**](csourcestream.md) class creates the streaming thread for the pin.</span></span> <span data-ttu-id="59c23-163">執行緒程式是在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法中執行。</span><span class="sxs-lookup"><span data-stu-id="59c23-163">The thread procedure is implemented in the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="59c23-164">這個方法會呼叫衍生類別必須覆寫的純虛擬 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="59c23-164">This method calls the pure-virtual [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class must override.</span></span> <span data-ttu-id="59c23-165">此方法是 pin 將資料填入緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="59c23-165">This method is where the pin fills the buffer with data.</span></span> <span data-ttu-id="59c23-166">例如，如果您的篩選器提供未壓縮的影片，這就是您要在其中繪製影片畫面的位置。</span><span class="sxs-lookup"><span data-stu-id="59c23-166">For example, if your filter delivers uncompressed video, this is where you would draw the video frames.</span></span>

<span data-ttu-id="59c23-167">當篩選暫停或停止時，基類會自動啟動，並且在正確的時間停止執行緒迴圈。</span><span class="sxs-lookup"><span data-stu-id="59c23-167">The base class automatically starts and stops the thread loop at the right times, when the filter pauses or stops.</span></span> <span data-ttu-id="59c23-168">發生這種情況時， [**CSourceStream**](csourcestream.md) 類別會呼叫一些方法來通知您的衍生類別：</span><span class="sxs-lookup"><span data-stu-id="59c23-168">When this happens, the [**CSourceStream**](csourcestream.md) class calls some methods to notify your derived class:</span></span>

-   [<span data-ttu-id="59c23-169">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="59c23-169">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="59c23-170">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="59c23-170">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="59c23-171">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="59c23-171">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="59c23-172">如果您需要新增任何特殊處理，可以覆寫這些方法。</span><span class="sxs-lookup"><span data-stu-id="59c23-172">You can override these methods if you need to add any special handling.</span></span> <span data-ttu-id="59c23-173">否則，預設的實值只會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="59c23-173">Otherwise, the default implementations simply return **S\_OK**.</span></span>

## <a name="seeking"></a><span data-ttu-id="59c23-174">尋求</span><span class="sxs-lookup"><span data-stu-id="59c23-174">Seeking</span></span>

<span data-ttu-id="59c23-175">如果您的來源篩選具有一個輸出釘選，您可以使用 [**CSourceSeeking**](csourceseeking.md) 類別做為實作為搜尋起點的起點。</span><span class="sxs-lookup"><span data-stu-id="59c23-175">If you have a source filter with one output pin, you can use the [**CSourceSeeking**](csourceseeking.md) class as a starting point for implementing seeking.</span></span> <span data-ttu-id="59c23-176">從 [**CSourceStream**](csourcestream.md) 和 **CSourceSeeking** 繼承您的 pin 類別。</span><span class="sxs-lookup"><span data-stu-id="59c23-176">Inherit your pin class from both [**CSourceStream**](csourcestream.md) and **CSourceSeeking**.</span></span>

> [!Note]  
> <span data-ttu-id="59c23-177">如果篩選具有多個輸出釘選，則不建議使用 [**CSourceSeeking**](csourceseeking.md) 。</span><span class="sxs-lookup"><span data-stu-id="59c23-177">[**CSourceSeeking**](csourceseeking.md) is not recommended for a filter with more than one output pin.</span></span> <span data-ttu-id="59c23-178">主要的問題是只有一個 pin 應該回應搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="59c23-178">The main issue is that only one pin should respond to seeking requests.</span></span> <span data-ttu-id="59c23-179">這通常需要 pin 和篩選之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="59c23-179">Typically this requires communication among the pins and the filter.</span></span>

 

<span data-ttu-id="59c23-180">[**CSourceSeeking**](csourceseeking.md)類別會管理播放速率、開始時間、停止時間和持續時間。</span><span class="sxs-lookup"><span data-stu-id="59c23-180">The [**CSourceSeeking**](csourceseeking.md) class manages the playback rate, start time, stop time, and duration.</span></span> <span data-ttu-id="59c23-181">您的衍生類別應該設定初始停止時間和持續時間。</span><span class="sxs-lookup"><span data-stu-id="59c23-181">Your derived class should set the initial stop time and duration.</span></span> <span data-ttu-id="59c23-182">每當其中一個值變更時，就會適當地呼叫 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)、 [**CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)或 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="59c23-182">Whenever one of these values changes, the [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md), [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md), or [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md) method is called, as appropriate.</span></span> <span data-ttu-id="59c23-183">這些方法都是純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="59c23-183">The methods are all pure virtual methods.</span></span> <span data-ttu-id="59c23-184">衍生的 pin 類別會覆寫這些方法以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="59c23-184">The derived pin class overrides these methods to do the following:</span></span>

1.  <span data-ttu-id="59c23-185">在下游 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 。</span><span class="sxs-lookup"><span data-stu-id="59c23-185">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) on the downstream pin.</span></span> <span data-ttu-id="59c23-186">這會導致下游篩選器發行它們所持有的範例，並拒絕新的範例。</span><span class="sxs-lookup"><span data-stu-id="59c23-186">This causes downstream filters to release samples they are holding and reject new samples.</span></span>
2.  <span data-ttu-id="59c23-187">呼叫 [**CSourceStream：： stop**](csourcestream-stop.md) 以停止串流處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="59c23-187">Call [**CSourceStream::Stop**](csourcestream-stop.md) to stop the streaming thread.</span></span> <span data-ttu-id="59c23-188">來源篩選器會暫停產生新的資料。</span><span class="sxs-lookup"><span data-stu-id="59c23-188">The source filter suspends producing new data.</span></span>
3.  <span data-ttu-id="59c23-189">在下游 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。</span><span class="sxs-lookup"><span data-stu-id="59c23-189">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on the downstream pin.</span></span> <span data-ttu-id="59c23-190">這會通知下游篩選器接受新的資料。</span><span class="sxs-lookup"><span data-stu-id="59c23-190">This signals the downstream filters to accept new data.</span></span>
4.  <span data-ttu-id="59c23-191">以新的開始和停止時間和速率呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 。</span><span class="sxs-lookup"><span data-stu-id="59c23-191">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) with the new start and stop times and rate.</span></span>
5.  <span data-ttu-id="59c23-192">在下一個範例中，設定 [不中斷] 屬性。</span><span class="sxs-lookup"><span data-stu-id="59c23-192">Set the discontinuity property on the next sample.</span></span>

<span data-ttu-id="59c23-193">如需詳細資訊，請參閱 [在來源篩選中支援搜尋](supporting-seeking-in-a-source-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="59c23-193">For more information, see [Supporting Seeking in a Source Filter](supporting-seeking-in-a-source-filter.md).</span></span>

<span data-ttu-id="59c23-194">如果您的篩選準則支援搜尋，則資料流程位置現在與展示時間無關。</span><span class="sxs-lookup"><span data-stu-id="59c23-194">If your filter supports seeking, the stream position is now independent of the presentation time.</span></span> <span data-ttu-id="59c23-195">搜尋之後，時間戳記會重設為零。</span><span class="sxs-lookup"><span data-stu-id="59c23-195">After a seek, time stamps reset to zero.</span></span> <span data-ttu-id="59c23-196">時間戳記的一般公式為：</span><span class="sxs-lookup"><span data-stu-id="59c23-196">The general formula for time stamps is:</span></span>

-   <span data-ttu-id="59c23-197">範例開始時間 = 經過時間/播放速率</span><span class="sxs-lookup"><span data-stu-id="59c23-197">sample start time = time elapsed / playback rate</span></span>
-   <span data-ttu-id="59c23-198">範例結束時間 = 取樣開始時間 + 每個畫面格/播放速率 (時間) </span><span class="sxs-lookup"><span data-stu-id="59c23-198">sample end time = sample start time + (time per frame / playback rate)</span></span>

<span data-ttu-id="59c23-199">*經過的時間* 是從篩選開始執行或自上次搜尋命令以來經過的時間。</span><span class="sxs-lookup"><span data-stu-id="59c23-199">where *time elapsed* is the time that has elapsed since the filter started running or since the last seek command.</span></span>

### <a name="time-formats-for-seeking"></a><span data-ttu-id="59c23-200">搜尋的時間格式</span><span class="sxs-lookup"><span data-stu-id="59c23-200">Time Formats for Seeking</span></span>

<span data-ttu-id="59c23-201">依預設，搜尋命令的單位為 100-毫微秒。</span><span class="sxs-lookup"><span data-stu-id="59c23-201">By default, seek commands are in units of 100-nanoseconds.</span></span> <span data-ttu-id="59c23-202">來源篩選器可支援其他時間格式，例如依框架編號搜尋。</span><span class="sxs-lookup"><span data-stu-id="59c23-202">Your source filter can support additional time formats, such as seeking by frame number.</span></span> <span data-ttu-id="59c23-203">每一段時間的格式都是由 GUID 來識別;請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="59c23-203">Each time format is identified by a GUID; see [**Time Format GUIDs**](time-format-guids.md).</span></span>

<span data-ttu-id="59c23-204">若要支援其他時間格式，您必須在輸出釘選上執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="59c23-204">To support additional time formats, you must implement the following methods on your output pin:</span></span>

-   [<span data-ttu-id="59c23-205">**IMediaSeeking::ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="59c23-205">**IMediaSeeking::ConvertTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [<span data-ttu-id="59c23-206">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="59c23-206">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="59c23-207">**IMediaSeeking::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="59c23-207">**IMediaSeeking::IsFormatSupported**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [<span data-ttu-id="59c23-208">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="59c23-208">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="59c23-209">**IMediaSeeking::QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="59c23-209">**IMediaSeeking::QueryPreferredFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [<span data-ttu-id="59c23-210">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="59c23-210">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="59c23-211">如果應用程式設定新的時間格式，則會根據新的時間格式來解讀 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法中的所有位置參數。</span><span class="sxs-lookup"><span data-stu-id="59c23-211">If the application sets a new time format, all of the position parameters in the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods are interpreted in terms of the new time format.</span></span> <span data-ttu-id="59c23-212">例如，如果時間格式是畫面格， [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法必須傳回框架中的持續時間。</span><span class="sxs-lookup"><span data-stu-id="59c23-212">For example, if the time format is frames, the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the duration in frames.</span></span>

<span data-ttu-id="59c23-213">在實務上，少數的 DirectShow 篩選器支援額外的時間格式，因此，少數的 DirectShow 應用程式會使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="59c23-213">In practice, few DirectShow filters support additional time formats, and as a result, few DirectShow applications make use of this capability.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59c23-214">相關主題</span><span class="sxs-lookup"><span data-stu-id="59c23-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59c23-215">寫入來源篩選</span><span class="sxs-lookup"><span data-stu-id="59c23-215">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




