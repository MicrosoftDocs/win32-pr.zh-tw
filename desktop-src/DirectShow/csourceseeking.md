---
description: CSourceSeeking 類別是一個抽象類別，可在來源篩選準則中使用一個輸出圖釘來執行搜尋。
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: 'CSourceSeeking 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993377"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="9ddbd-103">CSourceSeeking 類別</span><span class="sxs-lookup"><span data-stu-id="9ddbd-103">CSourceSeeking class</span></span>

![csourceseeking 類別階層](images/cutil15.png)

<span data-ttu-id="9ddbd-105">**CSourceSeeking** 類別是一個抽象類別，可在來源篩選準則中使用一個輸出圖釘來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="9ddbd-106">這個類別支援 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="9ddbd-107">它會提供所有 **IMediaSeeking** 方法的預設執行。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="9ddbd-108">受保護的成員變數會儲存開始時間、停止時間和目前的速率。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="9ddbd-109">依預設，類別所支援的唯一時間格式是 **時間 \_ 格式 \_ 媒體 \_ 時間** (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="9ddbd-110">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-110">See Remarks for more information.</span></span>



| <span data-ttu-id="9ddbd-111">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="9ddbd-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="9ddbd-112">Description</span><span class="sxs-lookup"><span data-stu-id="9ddbd-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ddbd-113">**m \_ rtDuration**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="9ddbd-114">資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="9ddbd-115">**m \_ rtStart**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="9ddbd-116">開始時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="9ddbd-117">**m \_ rtStop**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="9ddbd-118">停止時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="9ddbd-119">**m \_ dRateSeeking**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="9ddbd-120">播放速率。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="9ddbd-121">**m \_ dwSeekingCaps**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="9ddbd-122">搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="9ddbd-123">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="9ddbd-124">要鎖定之重要區段物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="9ddbd-125">保護方法</span><span class="sxs-lookup"><span data-stu-id="9ddbd-125">Protected Methods</span></span>                                                   | <span data-ttu-id="9ddbd-126">Description</span><span class="sxs-lookup"><span data-stu-id="9ddbd-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="9ddbd-127">**CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="9ddbd-128">函式方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="9ddbd-129">純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="9ddbd-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="9ddbd-130">Description</span><span class="sxs-lookup"><span data-stu-id="9ddbd-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="9ddbd-131">**ChangeRate**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="9ddbd-132">當播放速率變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="9ddbd-133">**ChangeStart**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="9ddbd-134">開始位置變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="9ddbd-135">**ChangeStop**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="9ddbd-136">在停止位置變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="9ddbd-137">IMediaSeeking 方法</span><span class="sxs-lookup"><span data-stu-id="9ddbd-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="9ddbd-138">Description</span><span class="sxs-lookup"><span data-stu-id="9ddbd-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="9ddbd-139">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="9ddbd-140">判斷是否支援指定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="9ddbd-141">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="9ddbd-142">抓取物件的慣用時間格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="9ddbd-143">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="9ddbd-144">設定時間格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="9ddbd-145">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="9ddbd-146">判斷指定的時間格式是否為目前使用中的格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="9ddbd-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="9ddbd-148">抓取目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="9ddbd-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="9ddbd-150">捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="9ddbd-151">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="9ddbd-152">抓取將停止播放的時間（相對於資料流程的持續時間）。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="9ddbd-153">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="9ddbd-154">抓取目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="9ddbd-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="9ddbd-156">抓取資料流程的所有搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="9ddbd-157">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="9ddbd-158">查詢資料流程是否已指定搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="9ddbd-159">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="9ddbd-160">從一種時間格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="9ddbd-161">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="9ddbd-162">設定目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="9ddbd-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="9ddbd-164">抓取目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="9ddbd-165">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="9ddbd-166">抓取搜尋有效的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="9ddbd-167">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="9ddbd-168">設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="9ddbd-169">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="9ddbd-170">捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="9ddbd-171">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="9ddbd-172">捕獲預先進行的時間。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9ddbd-173">備註</span><span class="sxs-lookup"><span data-stu-id="9ddbd-173">Remarks</span></span>

<span data-ttu-id="9ddbd-174">只要開始位置、停止位置或播放速率變更， **CSourceSeeking** 物件就會呼叫對應的純虛擬方法：</span><span class="sxs-lookup"><span data-stu-id="9ddbd-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="9ddbd-175">開始位置： [ **CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbd-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="9ddbd-176">停止位置： [ **CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbd-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="9ddbd-177">播放速率： [ **CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="9ddbd-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="9ddbd-178">衍生的類別必須執行這些方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-178">The derived class must implement these methods.</span></span> <span data-ttu-id="9ddbd-179">進行任何搜尋作業之後，篩選準則必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9ddbd-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="9ddbd-180">在下游輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="9ddbd-181">中止傳遞資料的工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="9ddbd-182">在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="9ddbd-183">重新開機背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="9ddbd-184">在輸入 pin 上呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="9ddbd-185">設定第一個範例的不連續屬性。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="9ddbd-186">呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="9ddbd-187">如果執行緒已封鎖等候傳遞範例，則呼叫 [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 會釋出工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="9ddbd-188">在步驟2中，請確定執行緒已停止傳送資料。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="9ddbd-189">根據執行的不同，您可能需要等候執行緒結束，或讓執行緒發出某種類型的回應。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="9ddbd-190">如果您的篩選使用 [**CSourceStream**](csourcestream.md) 類別， [**CSourceStream：： Stop**](csourcestream-stop.md) 方法會封鎖，直到背景工作執行緒回復為止。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="9ddbd-191">在理想情況下，應該從背景工作執行緒傳遞新的區段 (步驟 5) 。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="9ddbd-192">它也可以透過 **CSourceSeeking** 物件來完成，只要篩選會以範例序列化它即可。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="9ddbd-193">下列範例顯示可能的執行。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="9ddbd-194">它會假設來源篩選器的輸出圖釘衍生自 **CSourceSeeking** 和 [**CSourceStream**](csourcestream.md)。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="9ddbd-195">這個範例會定義可執行步驟 1 4 的 helper 方法 UpdateFromSeek。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="9ddbd-196">覆寫 [**CSourceStream：： OnThreadStartPlay**](csourcestream-onthreadstartplay.md) 方法以傳送新的區段，並設定指出不中斷的旗標。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="9ddbd-197">背景工作執行緒會挑選此旗標，並呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法：</span><span class="sxs-lookup"><span data-stu-id="9ddbd-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="9ddbd-198">支援其他時間格式</span><span class="sxs-lookup"><span data-stu-id="9ddbd-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="9ddbd-199">根據預設，這個類別僅支援以參考時間的單位來搜尋 (時間 \_ 格式的 \_ 媒體 \_ 時間) 。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="9ddbd-200">若要支援其他時間格式，請覆寫處理時間格式的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法：</span><span class="sxs-lookup"><span data-stu-id="9ddbd-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="9ddbd-201">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="9ddbd-202">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="9ddbd-203">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="9ddbd-204">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="9ddbd-205">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="9ddbd-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="9ddbd-206">此外，請覆寫其餘的 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 方法，以在時間格式之間執行必要的轉換。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="9ddbd-207">在呼叫 [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法之後，所有的 **IMediaSeeking** 方法都必須將傳入和傳出的時間參數視為新的時間格式。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="9ddbd-208">例如，如果 *m \_ rtDuration* 變數以參考時間的單位來代表持續時間，但目前的時間格式為框架，則 [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法必須傳回轉換成框架的值 *m \_ rtDuration* 。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="9ddbd-209">例如：</span><span class="sxs-lookup"><span data-stu-id="9ddbd-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="9ddbd-210">此外，請務必 \_ \_ 在 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法中檢查 AM 搜尋 ReturnTime 旗標。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="9ddbd-211">如果出現此旗標，請將位置值轉換為參考時間，然後將它們傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="9ddbd-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ddbd-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ddbd-212">Requirements</span></span>



| <span data-ttu-id="9ddbd-213">需求</span><span class="sxs-lookup"><span data-stu-id="9ddbd-213">Requirement</span></span> | <span data-ttu-id="9ddbd-214">值</span><span class="sxs-lookup"><span data-stu-id="9ddbd-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddbd-215">標頭</span><span class="sxs-lookup"><span data-stu-id="9ddbd-215">Header</span></span><br/>  | <dl> <span data-ttu-id="9ddbd-216"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9ddbd-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ddbd-217">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ddbd-217">Library</span></span><br/> | <dl> <span data-ttu-id="9ddbd-218"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9ddbd-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ddbd-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ddbd-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ddbd-220">支援在來源篩選準則中搜尋</span><span class="sxs-lookup"><span data-stu-id="9ddbd-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




