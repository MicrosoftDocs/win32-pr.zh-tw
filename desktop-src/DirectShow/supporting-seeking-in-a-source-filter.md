---
description: 本主題說明如何在 Microsoft DirectShow 來源篩選器中執行搜尋。 它使用球形濾波器範例作為起點，並說明在此篩選準則中支援搜尋所需的其他程式碼。
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: 支援在來源篩選準則中搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852404"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="8e98d-104">支援在來源篩選準則中搜尋</span><span class="sxs-lookup"><span data-stu-id="8e98d-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="8e98d-105">本主題說明如何在 Microsoft DirectShow 來源篩選器中執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="8e98d-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="8e98d-106">它使用 [球形濾波器](ball-filter-sample.md) 範例作為起點，並說明在此篩選準則中支援搜尋所需的其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="8e98d-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="8e98d-107">[球形濾波器](ball-filter-sample.md)範例是一種來源篩選器，可建立動畫彈跳球。</span><span class="sxs-lookup"><span data-stu-id="8e98d-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="8e98d-108">本文說明如何將搜尋功能新增到此篩選器。</span><span class="sxs-lookup"><span data-stu-id="8e98d-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="8e98d-109">加入這項功能之後，您就可以在 GraphEdit 中轉譯篩選，並藉由拖曳 GraphEdit 滑杆來控制球體。</span><span class="sxs-lookup"><span data-stu-id="8e98d-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="8e98d-110">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="8e98d-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="8e98d-111">在 DirectShow 中搜尋的總覽</span><span class="sxs-lookup"><span data-stu-id="8e98d-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="8e98d-112">球形濾波器的快速概覽</span><span class="sxs-lookup"><span data-stu-id="8e98d-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="8e98d-113">修改球篩選以進行搜尋</span><span class="sxs-lookup"><span data-stu-id="8e98d-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="8e98d-114">CSourceSeeking 類別的限制</span><span class="sxs-lookup"><span data-stu-id="8e98d-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="8e98d-115">在 DirectShow 中搜尋的總覽</span><span class="sxs-lookup"><span data-stu-id="8e98d-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="8e98d-116">應用程式會藉由呼叫篩選圖形管理員上的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法來搜尋篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="8e98d-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="8e98d-117">然後，篩選圖形管理員會將呼叫分散至圖形中的每個轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8e98d-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="8e98d-118">每個轉譯器都會透過下一個上游篩選的輸出釘選，傳送呼叫上游。</span><span class="sxs-lookup"><span data-stu-id="8e98d-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="8e98d-119">呼叫會傳送上游，直到到達可執行 seek 命令的篩選準則（通常是來源篩選或剖析器篩選器）。</span><span class="sxs-lookup"><span data-stu-id="8e98d-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="8e98d-120">一般而言，產生時間戳記的篩選器也會處理搜尋。</span><span class="sxs-lookup"><span data-stu-id="8e98d-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="8e98d-121">篩選準則會回應搜尋命令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8e98d-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="8e98d-122">篩選會排清圖形。</span><span class="sxs-lookup"><span data-stu-id="8e98d-122">The filter flushes the graph.</span></span> <span data-ttu-id="8e98d-123">這會清除圖形中任何過時的資料，進而改善回應能力。</span><span class="sxs-lookup"><span data-stu-id="8e98d-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="8e98d-124">否則，在搜尋命令之前緩衝的範例可能會被傳遞。</span><span class="sxs-lookup"><span data-stu-id="8e98d-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="8e98d-125">篩選準則會呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) ，以通知下游篩選新的停止時間、開始時間和播放速率。</span><span class="sxs-lookup"><span data-stu-id="8e98d-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="8e98d-126">然後，篩選準則會在 seek 命令之後的第一個範例上設定不連續旗標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="8e98d-127">時間戳記會在任何搜尋命令之後從零開始 (包括速率變更) 。</span><span class="sxs-lookup"><span data-stu-id="8e98d-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="8e98d-128">球形濾波器的快速概覽</span><span class="sxs-lookup"><span data-stu-id="8e98d-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="8e98d-129">球形濾波器是一個推播來源，這表示它會使用背景工作執行緒來傳遞下游範例，而不是提取來源，被動等候下游篩選要求範例。</span><span class="sxs-lookup"><span data-stu-id="8e98d-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="8e98d-130">球濾波器是從 [**CSource**](csource.md) 類別建立的，而其輸出圖釘是從 [**CSourceStream**](csourcestream.md) 類別建立的。</span><span class="sxs-lookup"><span data-stu-id="8e98d-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="8e98d-131">**CSourceStream** 類別會建立驅動資料流程程的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="8e98d-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="8e98d-132">這個執行緒會進入迴圈，從配置器取得範例、將資料填入資料，然後將它們傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="8e98d-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="8e98d-133">[**CSourceStream**](csourcestream.md)中的大部分動作都會發生在衍生類別所 [**執行的 CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md)方法中。</span><span class="sxs-lookup"><span data-stu-id="8e98d-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="8e98d-134">此方法的引數是要傳遞之範例的指標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="8e98d-135">球濾波器的 **FillBuffer** 會抓取範例緩衝區的位址，並藉由設定個別圖元值，直接繪製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e98d-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="8e98d-136"> (繪圖是由 helper 類別 CBall 完成，因此您可以忽略有關位深度、調色板等的詳細資料。 ) </span><span class="sxs-lookup"><span data-stu-id="8e98d-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="8e98d-137">修改球篩選以進行搜尋</span><span class="sxs-lookup"><span data-stu-id="8e98d-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="8e98d-138">若要讓球篩選成為可搜尋，請使用 [**CSourceSeeking**](csourceseeking.md) 類別，其設計目的是要在篩選準則中使用一個輸出圖釘來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="8e98d-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="8e98d-139">將 **CSourceSeeking** 類別新增至 CBallStream 類別的繼承清單：</span><span class="sxs-lookup"><span data-stu-id="8e98d-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="8e98d-140">此外，您必須將 [**CSourceSeeking**](csourceseeking.md) 的初始化運算式加入至 CBallStream 的函式：</span><span class="sxs-lookup"><span data-stu-id="8e98d-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="8e98d-141">此語句會針對 [**CSourceSeeking**](csourceseeking.md)呼叫基底的函式。</span><span class="sxs-lookup"><span data-stu-id="8e98d-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="8e98d-142">這些參數是名稱、擁有釘選的指標、 **HRESULT** 值，以及重要區段物件的位址。</span><span class="sxs-lookup"><span data-stu-id="8e98d-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="8e98d-143">名稱只用于進行偵錯工具，而 [**name**](name.md) 宏會編譯為零售組建中的空字串。</span><span class="sxs-lookup"><span data-stu-id="8e98d-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="8e98d-144">Pin 會直接繼承 **CSourceSeeking**，因此第二個參數是指向其本身的指標，轉換成 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 指標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="8e98d-145">在目前的基類版本中，會忽略 **HRESULT** 值;它會維持與舊版的相容性。</span><span class="sxs-lookup"><span data-stu-id="8e98d-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="8e98d-146">重要區段可保護共用資料，例如目前的開始時間、停止時間和播放速率。</span><span class="sxs-lookup"><span data-stu-id="8e98d-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="8e98d-147">在 [**CSourceSeeking**](csourceseeking.md) 的函式中新增下列語句：</span><span class="sxs-lookup"><span data-stu-id="8e98d-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="8e98d-148">*M \_ rtStop* 變數會指定停止時間。</span><span class="sxs-lookup"><span data-stu-id="8e98d-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="8e98d-149">根據預設，此值為 \_ I64 \_ MAX/2，大約是14600年。</span><span class="sxs-lookup"><span data-stu-id="8e98d-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="8e98d-150">上一個語句會將它設定為更保守的60秒。</span><span class="sxs-lookup"><span data-stu-id="8e98d-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="8e98d-151">您必須將兩個額外的成員變數新增至 CBallStream：</span><span class="sxs-lookup"><span data-stu-id="8e98d-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="8e98d-152">在每個搜尋命令之後，篩選準則必須藉由呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)，在下一個範例上設定不中斷旗標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="8e98d-153">*M \_ bDiscontinuity* 變數將會追蹤這個。</span><span class="sxs-lookup"><span data-stu-id="8e98d-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="8e98d-154">*M \_ rtBallPosition* 變數會指定球在影片框架中的位置。</span><span class="sxs-lookup"><span data-stu-id="8e98d-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="8e98d-155">原始球濾波器會計算來自資料流程時間的位置，但是資料流程時間會在每個搜尋命令之後重設為零。</span><span class="sxs-lookup"><span data-stu-id="8e98d-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="8e98d-156">在可搜尋的資料流程中，絕對位置與資料流程時間無關。</span><span class="sxs-lookup"><span data-stu-id="8e98d-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="8e98d-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="8e98d-157">QueryInterface</span></span>

<span data-ttu-id="8e98d-158">[**CSourceSeeking**](csourceseeking.md)類別會實 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面。</span><span class="sxs-lookup"><span data-stu-id="8e98d-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="8e98d-159">若要將此介面公開給用戶端，請覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="8e98d-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="8e98d-160">方法稱為「NonDelegating」，因為 DirectShow 基類支援元件物件模型的方式 (COM) 匯總。</span><span class="sxs-lookup"><span data-stu-id="8e98d-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="8e98d-161">如需詳細資訊，請參閱 DirectShow SDK 中的「如何執行 IUnknown」主題。</span><span class="sxs-lookup"><span data-stu-id="8e98d-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="8e98d-162">搜尋方法</span><span class="sxs-lookup"><span data-stu-id="8e98d-162">Seeking Methods</span></span>

<span data-ttu-id="8e98d-163">[**CSourceSeeking**](csourceseeking.md)類別會維護數個與搜尋相關的成員變數。</span><span class="sxs-lookup"><span data-stu-id="8e98d-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="8e98d-164">變數</span><span class="sxs-lookup"><span data-stu-id="8e98d-164">Variable</span></span>          | <span data-ttu-id="8e98d-165">描述</span><span class="sxs-lookup"><span data-stu-id="8e98d-165">Description</span></span>   | <span data-ttu-id="8e98d-166">預設值</span><span class="sxs-lookup"><span data-stu-id="8e98d-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="8e98d-167">*m \_ rtStart*</span><span class="sxs-lookup"><span data-stu-id="8e98d-167">*m\_rtStart*</span></span>      | <span data-ttu-id="8e98d-168">開始時間</span><span class="sxs-lookup"><span data-stu-id="8e98d-168">Start time</span></span>    | <span data-ttu-id="8e98d-169">零個</span><span class="sxs-lookup"><span data-stu-id="8e98d-169">Zero</span></span>           |
| <span data-ttu-id="8e98d-170">*m \_ rtStop*</span><span class="sxs-lookup"><span data-stu-id="8e98d-170">*m\_rtStop*</span></span>       | <span data-ttu-id="8e98d-171">停止時間</span><span class="sxs-lookup"><span data-stu-id="8e98d-171">Stop time</span></span>     | <span data-ttu-id="8e98d-172">\_I64 \_ MAX/2</span><span class="sxs-lookup"><span data-stu-id="8e98d-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="8e98d-173">*m \_ dRateSeeking*</span><span class="sxs-lookup"><span data-stu-id="8e98d-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="8e98d-174">播放速率</span><span class="sxs-lookup"><span data-stu-id="8e98d-174">Playback rate</span></span> | <span data-ttu-id="8e98d-175">1.0</span><span class="sxs-lookup"><span data-stu-id="8e98d-175">1.0</span></span>            |



 

<span data-ttu-id="8e98d-176">[**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)的 [**CSourceSeeking**](csourceseeking.md)執行會更新開始和停止時間，然後在衍生的類別上呼叫兩個純虛擬方法 [**： CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)和 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)。</span><span class="sxs-lookup"><span data-stu-id="8e98d-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="8e98d-177">[**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)的實作為類似：它會更新播放速率，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)。</span><span class="sxs-lookup"><span data-stu-id="8e98d-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="8e98d-178">在這些虛擬方法中，pin 必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="8e98d-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="8e98d-179">呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 以開始排清資料。</span><span class="sxs-lookup"><span data-stu-id="8e98d-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="8e98d-180">停止串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="8e98d-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="8e98d-181">呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)。</span><span class="sxs-lookup"><span data-stu-id="8e98d-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="8e98d-182">重新開機串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="8e98d-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="8e98d-183">呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)。</span><span class="sxs-lookup"><span data-stu-id="8e98d-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="8e98d-184">設定下一個範例的不連續旗標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="8e98d-185">這些步驟的順序很重要，因為串流執行緒可能會在等候傳遞範例或取得新範例時封鎖。</span><span class="sxs-lookup"><span data-stu-id="8e98d-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="8e98d-186">[**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)方法可確保不會封鎖串流執行緒，因此不會在步驟2中產生鎖死。</span><span class="sxs-lookup"><span data-stu-id="8e98d-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="8e98d-187">[**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)呼叫會通知下游篩選器預期新的範例，因此當執行緒在步驟4中再次啟動時，不會拒絕它們。</span><span class="sxs-lookup"><span data-stu-id="8e98d-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="8e98d-188">下列私用方法會執行步驟1到4：</span><span class="sxs-lookup"><span data-stu-id="8e98d-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="8e98d-189">當串流執行緒再次開始時，它會呼叫 [**CSourceStream：： OnThreadStartPlay**](csourcestream-onthreadstartplay.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8e98d-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="8e98d-190">覆寫此方法以執行步驟5和6：</span><span class="sxs-lookup"><span data-stu-id="8e98d-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="8e98d-191">在 [**ChangeStart**](csourceseeking-changestart.md) 方法中，將資料流程時間設定為零，並將球的位置設定為新的開始時間。</span><span class="sxs-lookup"><span data-stu-id="8e98d-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="8e98d-192">然後呼叫 CBallStream：： UpdateFromSeek：</span><span class="sxs-lookup"><span data-stu-id="8e98d-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="8e98d-193">在 [**ChangeStop**](csourceseeking-changestop.md) 方法中，如果新的停止時間小於目前的位置，請呼叫 CBallStream：： UpdateFromSeek。</span><span class="sxs-lookup"><span data-stu-id="8e98d-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="8e98d-194">否則，停止時間仍在未來，因此不需要排清圖形。</span><span class="sxs-lookup"><span data-stu-id="8e98d-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="8e98d-195">針對速率變更， [**CSourceSeeking：： SetRate**](csourceseeking-setrate.md) 方法會將 *m \_ dRateSeeking* 設定為新的速率， (在它呼叫 [**ChangeRate**](csourceseeking-changerate.md)之前捨棄舊值) 。</span><span class="sxs-lookup"><span data-stu-id="8e98d-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="8e98d-196">可惜的是，如果呼叫者給予的速率無效（例如，小於零），則會在呼叫 **ChangeRate** 時延遲太晚。</span><span class="sxs-lookup"><span data-stu-id="8e98d-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="8e98d-197">其中一個解決方案是覆寫 **SetRate** 並檢查有效的費率：</span><span class="sxs-lookup"><span data-stu-id="8e98d-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="8e98d-198">在緩衝區中繪圖</span><span class="sxs-lookup"><span data-stu-id="8e98d-198">Drawing in the Buffer</span></span>

<span data-ttu-id="8e98d-199">以下是 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md)的修改版本，此常式會在每個畫面格上繪製球：</span><span class="sxs-lookup"><span data-stu-id="8e98d-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="8e98d-200">此版本和原始版本之間的主要差異如下：</span><span class="sxs-lookup"><span data-stu-id="8e98d-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="8e98d-201">如先前所述， *m \_ rtBallPosition* 變數用來設定球的位置，而不是資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="8e98d-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="8e98d-202">在保存重要區段之後，方法會檢查目前的位置是否超過停止時間。</span><span class="sxs-lookup"><span data-stu-id="8e98d-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="8e98d-203">如果是，則會 **傳回 \_ FALSE**，表示基類停止傳送資料並傳遞資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="8e98d-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="8e98d-204">時間戳記會除以目前的速率。</span><span class="sxs-lookup"><span data-stu-id="8e98d-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="8e98d-205">如果 *m \_ BDiscontinuity* 為 **TRUE**，則方法會在範例上設定不中斷旗標。</span><span class="sxs-lookup"><span data-stu-id="8e98d-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="8e98d-206">還有另一個小差異。</span><span class="sxs-lookup"><span data-stu-id="8e98d-206">There is another minor difference.</span></span> <span data-ttu-id="8e98d-207">因為原始版本依賴只有一個緩衝區，所以它會在串流處理開始時，將零次填滿整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e98d-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="8e98d-208">之後，它只會從先前的位置清除球。</span><span class="sxs-lookup"><span data-stu-id="8e98d-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="8e98d-209">不過，這項優化會在球濾波器中顯示稍微錯誤的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e98d-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="8e98d-210">當 [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md) 方法呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)時，它會將唯讀旗標設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8e98d-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="8e98d-211">因此，下游篩選器可自由寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e98d-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="8e98d-212">其中一個解決方法是覆寫 **DecideAllocator** ，讓它將唯讀旗標設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8e98d-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="8e98d-213">但為了簡單起見，新版本只會移除優化。</span><span class="sxs-lookup"><span data-stu-id="8e98d-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="8e98d-214">相反地，此版本每次都會以零填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8e98d-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="8e98d-215">其他變更</span><span class="sxs-lookup"><span data-stu-id="8e98d-215">Miscellaneous Changes</span></span>

<span data-ttu-id="8e98d-216">在新版本中，這兩行會從 CBall 的函式移除：</span><span class="sxs-lookup"><span data-stu-id="8e98d-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="8e98d-217">原始球形濾波器會使用這些值，將一些隨機性新增至初始球的位置。</span><span class="sxs-lookup"><span data-stu-id="8e98d-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="8e98d-218">基於我們的目的，我們希望球具有決定性。</span><span class="sxs-lookup"><span data-stu-id="8e98d-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="8e98d-219">此外，有些變數已經從 [**CRefTime**](creftime.md) 物件變更為 [**參考 \_ 時間**](reference-time.md) 變數。</span><span class="sxs-lookup"><span data-stu-id="8e98d-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="8e98d-220"> (**CRefTime** 類別是 **參考 \_ 時間** 值的精簡型包裝函式。 ) 最後， [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 的實值已稍微修改; 您可以參考原始程式碼以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e98d-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="8e98d-221">CSourceSeeking 類別的限制</span><span class="sxs-lookup"><span data-stu-id="8e98d-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="8e98d-222">[**CSourceSeeking**](csourceseeking.md)類別不適用於具有多個輸出圖釘的篩選，因為有跨 pin 通訊的問題。</span><span class="sxs-lookup"><span data-stu-id="8e98d-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="8e98d-223">例如，假設剖析器篩選器會接收交錯式音訊影片串流、將資料流程分割成音訊和影片元件，並從另一個輸出圖釘和音訊傳遞影片。</span><span class="sxs-lookup"><span data-stu-id="8e98d-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="8e98d-224">這兩個輸出接點都會接收每個搜尋命令，但是篩選準則應該只搜尋每個 seek 命令一次。</span><span class="sxs-lookup"><span data-stu-id="8e98d-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="8e98d-225">解決方法是指定其中一個 pin 來控制搜尋，並忽略其他 pin 所接收的搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="8e98d-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="8e98d-226">不過，在 seek 命令之後，這兩個圖釘都應該排清資料。</span><span class="sxs-lookup"><span data-stu-id="8e98d-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="8e98d-227">為了更複雜一點，seek 命令會在應用程式執行緒上發生，而不是在串流執行緒上進行。</span><span class="sxs-lookup"><span data-stu-id="8e98d-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="8e98d-228">因此，您必須確定未封鎖任何 pin，並等待 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 呼叫傳回，否則可能會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="8e98d-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="8e98d-229">如需有關 pin 中安全線程排清的詳細資訊，請參閱 [執行緒和重要區段](threads-and-critical-sections.md)。</span><span class="sxs-lookup"><span data-stu-id="8e98d-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e98d-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e98d-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e98d-231">寫入來源篩選</span><span class="sxs-lookup"><span data-stu-id="8e98d-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



