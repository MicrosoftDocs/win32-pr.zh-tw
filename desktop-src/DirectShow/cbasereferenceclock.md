---
description: CBaseReferenceClock 類別會實行參考時鐘。
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: 'CBaseReferenceClock 類別 (Refclock) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977571"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="d1463-103">CBaseReferenceClock 類別</span><span class="sxs-lookup"><span data-stu-id="d1463-103">CBaseReferenceClock class</span></span>

![cbasereferenceclock 類別階層](images/rclock01.png)

<span data-ttu-id="d1463-105">類別會實 `CBaseReferenceClock` 作為參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="d1463-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="d1463-106">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="d1463-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="d1463-107">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1463-108">**m \_ pSchedule**</span><span class="sxs-lookup"><span data-stu-id="d1463-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="d1463-109">處理時鐘排程工作的 [**CAMSchedule**](camschedule.md)物件。</span><span class="sxs-lookup"><span data-stu-id="d1463-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="d1463-110">保護方法</span><span class="sxs-lookup"><span data-stu-id="d1463-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="d1463-111">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-111">Description</span></span>                                                                            |
| [<span data-ttu-id="d1463-112">**~ CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="d1463-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="d1463-113">函式方法。</span><span class="sxs-lookup"><span data-stu-id="d1463-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="d1463-114">公用方法</span><span class="sxs-lookup"><span data-stu-id="d1463-114">Public Methods</span></span>                                                                     | <span data-ttu-id="d1463-115">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-115">Description</span></span>                                                                            |
| [<span data-ttu-id="d1463-116">**CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="d1463-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="d1463-117">函式方法。</span><span class="sxs-lookup"><span data-stu-id="d1463-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="d1463-118">**GetPrivateTime**</span><span class="sxs-lookup"><span data-stu-id="d1463-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="d1463-119">從時鐘取出即時時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="d1463-120">**SetTimeDelta**</span><span class="sxs-lookup"><span data-stu-id="d1463-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="d1463-121">調整內部時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="d1463-122">**GetSchedule**</span><span class="sxs-lookup"><span data-stu-id="d1463-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="d1463-123">抓取時鐘排程物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d1463-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="d1463-124">**TriggerThread**</span><span class="sxs-lookup"><span data-stu-id="d1463-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="d1463-125">喚醒處理排程的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="d1463-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="d1463-126">IReferenceClock 方法</span><span class="sxs-lookup"><span data-stu-id="d1463-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="d1463-127">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-127">Description</span></span>                                                                            |
| [<span data-ttu-id="d1463-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="d1463-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="d1463-129">抓取目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="d1463-130">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="d1463-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="d1463-131">建立一次性的建議要求。</span><span class="sxs-lookup"><span data-stu-id="d1463-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="d1463-132">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="d1463-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="d1463-133">建立週期性建議要求。</span><span class="sxs-lookup"><span data-stu-id="d1463-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="d1463-134">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="d1463-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="d1463-135">移除暫止的建議要求。</span><span class="sxs-lookup"><span data-stu-id="d1463-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="d1463-136">IReferenceClockTimerControl 方法</span><span class="sxs-lookup"><span data-stu-id="d1463-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="d1463-137">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-137">Description</span></span>                                                                            |
| [<span data-ttu-id="d1463-138">**GetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="d1463-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="d1463-139">傳回目前的參考時鐘計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="d1463-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="d1463-140">**SetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="d1463-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="d1463-141">設定參考時鐘計時器的解析度。</span><span class="sxs-lookup"><span data-stu-id="d1463-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="d1463-142">輔助函式</span><span class="sxs-lookup"><span data-stu-id="d1463-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="d1463-143">Description</span><span class="sxs-lookup"><span data-stu-id="d1463-143">Description</span></span>                                                                            |
| [<span data-ttu-id="d1463-144">**ConvertToMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="d1463-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="d1463-145">將參考時間轉換為毫秒。</span><span class="sxs-lookup"><span data-stu-id="d1463-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="d1463-146">備註</span><span class="sxs-lookup"><span data-stu-id="d1463-146">Remarks</span></span>

<span data-ttu-id="d1463-147">這個類別會執行支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 和 [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) 介面的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="d1463-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="d1463-148">如果篩選器可以提供篩選圖形的參考時鐘，例如藉由存取硬體裝置，則可以使用這個類別來執行時鐘。</span><span class="sxs-lookup"><span data-stu-id="d1463-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="d1463-149">`CBaseReferenceClock`物件會維護兩個不同的時間值：</span><span class="sxs-lookup"><span data-stu-id="d1463-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="d1463-150">就內部而言， [**CBaseReferenceClock：： GetPrivateTime**](cbasereferenceclock-getprivatetime.md) 方法會傳回時鐘所保留的實際時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="d1463-151">在外部， [**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md) 方法會傳回篩選圖形的參考時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="d1463-152">它適用于內部時鐘在短暫期間後執行。</span><span class="sxs-lookup"><span data-stu-id="d1463-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="d1463-153">例如，如果時鐘向前偏離，篩選可以向後調整。</span><span class="sxs-lookup"><span data-stu-id="d1463-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="d1463-154"> (參閱 [**CBaseReferenceClock：： SetTimeDelta**](cbasereferenceclock-settimedelta.md)。 ) **GetTime** 方法會使用 **GetPrivateTime** 所報告的時間值。</span><span class="sxs-lookup"><span data-stu-id="d1463-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="d1463-155">不過，參考時間是單純增加的，換句話說，它永遠不會往後執行。</span><span class="sxs-lookup"><span data-stu-id="d1463-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="d1463-156">因此，如果內部時鐘回溯執行， **GetTime** 會繼續報告舊的時間，直到內部時鐘趕上為止。</span><span class="sxs-lookup"><span data-stu-id="d1463-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="d1463-157">例如，這兩個方法可能會傳回下列順序：</span><span class="sxs-lookup"><span data-stu-id="d1463-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="d1463-158">在第三個時鐘刻度上，內部時鐘會向前跳到103。</span><span class="sxs-lookup"><span data-stu-id="d1463-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="d1463-159">**GetTime** 方法會繼續報告106，直到內部時鐘趕上為止。</span><span class="sxs-lookup"><span data-stu-id="d1463-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="d1463-160">根據預設， **GetPrivateTime** 會透過呼叫 **timeGetTime** 函數來傳回系統時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="d1463-161">提供來自外部裝置之參考時鐘的篩選準則，可以執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d1463-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="d1463-162">覆寫 **GetPrivateTime** 以傳回裝置的時間。</span><span class="sxs-lookup"><span data-stu-id="d1463-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="d1463-163">監視裝置時間與系統時間之間的差異，然後呼叫 **SetTimeDelta** 來進行修正。</span><span class="sxs-lookup"><span data-stu-id="d1463-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="d1463-164">這個類別會使用 [**CAMSchedule**](camschedule.md) 物件來處理建議要求的排程。</span><span class="sxs-lookup"><span data-stu-id="d1463-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="d1463-165">如需詳細資訊，請參閱 **CAMSchedule** 類別的檔。</span><span class="sxs-lookup"><span data-stu-id="d1463-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1463-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1463-166">Requirements</span></span>



| <span data-ttu-id="d1463-167">需求</span><span class="sxs-lookup"><span data-stu-id="d1463-167">Requirement</span></span> | <span data-ttu-id="d1463-168">值</span><span class="sxs-lookup"><span data-stu-id="d1463-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1463-169">標頭</span><span class="sxs-lookup"><span data-stu-id="d1463-169">Header</span></span><br/>  | <dl> <span data-ttu-id="d1463-170"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d1463-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1463-171">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1463-171">Library</span></span><br/> | <dl> <span data-ttu-id="d1463-172"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d1463-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




