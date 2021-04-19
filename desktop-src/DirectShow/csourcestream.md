---
description: CSourceStream 類別提供 CSource 篩選類別的輸出圖釘。
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: 'CSourceStream 類別 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999417"
---
# <a name="csourcestream-class"></a><span data-ttu-id="40421-103">CSourceStream 類別</span><span class="sxs-lookup"><span data-stu-id="40421-103">CSourceStream class</span></span>

![csourcestream 類別階層](images/source02.png)

<span data-ttu-id="40421-105">**CSourceStream** 類別提供 [**CSource**](csource.md)篩選類別的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="40421-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="40421-106">如需使用這個類別的詳細資訊，請參閱 [**CSource**](csource.md)。</span><span class="sxs-lookup"><span data-stu-id="40421-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="40421-107">此類別會繼承 [**CAMThread**](camthread.md) 類別，此類別會提供背景工作執行緒來串流處理來自 pin 的資料。</span><span class="sxs-lookup"><span data-stu-id="40421-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="40421-108">**CSourceStream** 類別會執行下列 helper 方法，以將要求傳送至執行緒：</span><span class="sxs-lookup"><span data-stu-id="40421-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="40421-109">**CSourceStream：： Exit**</span><span class="sxs-lookup"><span data-stu-id="40421-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="40421-110">**CSourceStream：： Init**</span><span class="sxs-lookup"><span data-stu-id="40421-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="40421-111">**CSourceStream：:P ause**</span><span class="sxs-lookup"><span data-stu-id="40421-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="40421-112">**CSourceStream：： Run**</span><span class="sxs-lookup"><span data-stu-id="40421-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="40421-113">**CSourceStream：： Stop**</span><span class="sxs-lookup"><span data-stu-id="40421-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="40421-114">對執行緒的第一個要求必須是 [**Init**](csourcestream-init.md)。</span><span class="sxs-lookup"><span data-stu-id="40421-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="40421-115">[**Exit**](csourcestream-exit.md)要求會終止執行緒。</span><span class="sxs-lookup"><span data-stu-id="40421-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="40421-116">在實務上，不需要直接呼叫任何方法，因為釘選的 [**CSourceStream：： Active**](csourcestream-active.md) 和 [**CSourceStream：：非**](csourcestream-inactive.md) 使用中方法會視需要呼叫這些方法。</span><span class="sxs-lookup"><span data-stu-id="40421-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="40421-117">類別也提供數個「處理常式」方法：</span><span class="sxs-lookup"><span data-stu-id="40421-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="40421-118">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="40421-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="40421-119">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="40421-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="40421-120">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="40421-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="40421-121">這些都不會在基類中執行任何動作，但衍生類別可以覆寫它們。</span><span class="sxs-lookup"><span data-stu-id="40421-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="40421-122">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="40421-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="40421-123">Description</span><span class="sxs-lookup"><span data-stu-id="40421-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40421-124">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="40421-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="40421-125">包含此 pin 之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="40421-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="40421-126">保護方法</span><span class="sxs-lookup"><span data-stu-id="40421-126">Protected Methods</span></span>                                                      | <span data-ttu-id="40421-127">Description</span><span class="sxs-lookup"><span data-stu-id="40421-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="40421-128">**OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="40421-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="40421-129">在串流處理執行緒初始化時呼叫。</span><span class="sxs-lookup"><span data-stu-id="40421-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="40421-130">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="40421-131">**OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="40421-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="40421-132">當串流執行緒即將結束時呼叫。</span><span class="sxs-lookup"><span data-stu-id="40421-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="40421-133">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="40421-134">**OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="40421-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="40421-135">在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法開始時呼叫。</span><span class="sxs-lookup"><span data-stu-id="40421-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="40421-136">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-136">Virtual.</span></span> |
| [<span data-ttu-id="40421-137">**使用中**</span><span class="sxs-lookup"><span data-stu-id="40421-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="40421-138">通知釘選篩選現在已啟用。</span><span class="sxs-lookup"><span data-stu-id="40421-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="40421-139">**非使用中**</span><span class="sxs-lookup"><span data-stu-id="40421-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="40421-140">通知 pin 此篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="40421-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="40421-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="40421-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="40421-142">等候下一個執行緒要求。</span><span class="sxs-lookup"><span data-stu-id="40421-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="40421-143">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="40421-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="40421-144">檢查是否有線程要求，而不封鎖。</span><span class="sxs-lookup"><span data-stu-id="40421-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="40421-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="40421-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="40421-146">執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="40421-146">Thread procedure.</span></span> <span data-ttu-id="40421-147">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="40421-148">**DoBufferProcessingLoop**</span><span class="sxs-lookup"><span data-stu-id="40421-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="40421-149">產生媒體資料，並將其傳遞至下游輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="40421-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="40421-150">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="40421-151">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="40421-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="40421-152">判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="40421-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="40421-153">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="40421-154">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="40421-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="40421-155">捕獲慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="40421-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="40421-156">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="40421-157">公用方法</span><span class="sxs-lookup"><span data-stu-id="40421-157">Public Methods</span></span>                                                         | <span data-ttu-id="40421-158">Description</span><span class="sxs-lookup"><span data-stu-id="40421-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="40421-159">**CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="40421-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="40421-160">函式方法。</span><span class="sxs-lookup"><span data-stu-id="40421-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="40421-161">**~ CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="40421-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="40421-162">函式方法。</span><span class="sxs-lookup"><span data-stu-id="40421-162">Destructor method.</span></span> <span data-ttu-id="40421-163">虛擬。</span><span class="sxs-lookup"><span data-stu-id="40421-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="40421-164">**Init**</span><span class="sxs-lookup"><span data-stu-id="40421-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="40421-165">初始化串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="40421-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="40421-166">**結束**</span><span class="sxs-lookup"><span data-stu-id="40421-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="40421-167">通知串流執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="40421-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="40421-168">**執行**</span><span class="sxs-lookup"><span data-stu-id="40421-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="40421-169">指示要執行的串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="40421-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="40421-170">**暫停**</span><span class="sxs-lookup"><span data-stu-id="40421-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="40421-171">通知串流執行緒成為作用中。</span><span class="sxs-lookup"><span data-stu-id="40421-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="40421-172">**停止**</span><span class="sxs-lookup"><span data-stu-id="40421-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="40421-173">通知串流執行緒停止。</span><span class="sxs-lookup"><span data-stu-id="40421-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="40421-174">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="40421-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="40421-175">Description</span><span class="sxs-lookup"><span data-stu-id="40421-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="40421-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="40421-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="40421-177">使用資料填滿媒體範例。</span><span class="sxs-lookup"><span data-stu-id="40421-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="40421-178">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="40421-178">IPin Methods</span></span>                                                           | <span data-ttu-id="40421-179">Description</span><span class="sxs-lookup"><span data-stu-id="40421-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="40421-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="40421-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="40421-181">抓取 pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40421-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="40421-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="40421-182">Requirements</span></span>



| <span data-ttu-id="40421-183">需求</span><span class="sxs-lookup"><span data-stu-id="40421-183">Requirement</span></span> | <span data-ttu-id="40421-184">值</span><span class="sxs-lookup"><span data-stu-id="40421-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40421-185">標頭</span><span class="sxs-lookup"><span data-stu-id="40421-185">Header</span></span><br/>  | <dl> <span data-ttu-id="40421-186"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="40421-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40421-187">程式庫</span><span class="sxs-lookup"><span data-stu-id="40421-187">Library</span></span><br/> | <dl> <span data-ttu-id="40421-188"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="40421-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40421-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40421-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40421-190">寫入來源篩選</span><span class="sxs-lookup"><span data-stu-id="40421-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




