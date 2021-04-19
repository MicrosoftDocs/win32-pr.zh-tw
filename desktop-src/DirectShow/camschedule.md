---
description: CAMSchedule 類別會實作為參考時鐘的排程器。
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: 'CAMSchedule 類別 (Dsschedule) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983128"
---
# <a name="camschedule-class"></a><span data-ttu-id="1e201-103">CAMSchedule 類別</span><span class="sxs-lookup"><span data-stu-id="1e201-103">CAMSchedule class</span></span>

<span data-ttu-id="1e201-104">類別會實作為參考時鐘的排程器 `CAMSchedule` 。</span><span class="sxs-lookup"><span data-stu-id="1e201-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="1e201-105">公用方法</span><span class="sxs-lookup"><span data-stu-id="1e201-105">Public Methods</span></span>                                             | <span data-ttu-id="1e201-106">Description</span><span class="sxs-lookup"><span data-stu-id="1e201-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e201-107">**CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="1e201-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="1e201-108">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1e201-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="1e201-109">**~ CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="1e201-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="1e201-110">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1e201-110">Destructor method.</span></span> <span data-ttu-id="1e201-111">虛擬。</span><span class="sxs-lookup"><span data-stu-id="1e201-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="1e201-112">**GetAdviseCount**</span><span class="sxs-lookup"><span data-stu-id="1e201-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="1e201-113">抓取暫止的建議要求數目。</span><span class="sxs-lookup"><span data-stu-id="1e201-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="1e201-114">**GetNextAdviseTime**</span><span class="sxs-lookup"><span data-stu-id="1e201-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="1e201-115">抓取下一個建議要求的時間。</span><span class="sxs-lookup"><span data-stu-id="1e201-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="1e201-116">**AddAdvisePacket**</span><span class="sxs-lookup"><span data-stu-id="1e201-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="1e201-117">將建議要求新增至暫止的要求清單。</span><span class="sxs-lookup"><span data-stu-id="1e201-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="1e201-118">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="1e201-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="1e201-119">移除建議要求。</span><span class="sxs-lookup"><span data-stu-id="1e201-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="1e201-120">**建議**</span><span class="sxs-lookup"><span data-stu-id="1e201-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="1e201-121">分派排程于指定時間或更早時間的所有要求。</span><span class="sxs-lookup"><span data-stu-id="1e201-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="1e201-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="1e201-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="1e201-123">抓取事件控制碼，此控制碼可用來在下一個建議時間中通知變更。</span><span class="sxs-lookup"><span data-stu-id="1e201-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e201-124">備註</span><span class="sxs-lookup"><span data-stu-id="1e201-124">Remarks</span></span>

<span data-ttu-id="1e201-125">此 helper 物件會維護參考時鐘的建議要求清單。</span><span class="sxs-lookup"><span data-stu-id="1e201-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="1e201-126">[**CBaseReferenceClock**](cbasereferenceclock.md)類別會使用它來協助排程建議的要求。</span><span class="sxs-lookup"><span data-stu-id="1e201-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="1e201-127">時鐘會以下列方式使用此物件：</span><span class="sxs-lookup"><span data-stu-id="1e201-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="1e201-128">時鐘會建立背景工作執行緒來處理排程。</span><span class="sxs-lookup"><span data-stu-id="1e201-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="1e201-129">背景工作執行緒會呼叫 [**CAMSchedule：： GetEvent**](camschedule-getevent.md) 方法，以從排程器取出事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="1e201-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="1e201-130">它會等候這個事件，一開始會有無限的超時時間。</span><span class="sxs-lookup"><span data-stu-id="1e201-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="1e201-131">為了排程新的建議要求，時鐘會呼叫 [**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1e201-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="1e201-132">建議要求可以是一次或週期性要求。</span><span class="sxs-lookup"><span data-stu-id="1e201-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="1e201-133">排程器會以時間順序保留要求清單。</span><span class="sxs-lookup"><span data-stu-id="1e201-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="1e201-134">如果要求已加入清單的前面，則排程器會發出事件的信號。</span><span class="sxs-lookup"><span data-stu-id="1e201-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="1e201-135"> (清單一開始是空的，因此第一個要求會保證事件的信號。 ) </span><span class="sxs-lookup"><span data-stu-id="1e201-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="1e201-136">當事件收到信號時，背景工作執行緒會呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法，並指定目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="1e201-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="1e201-137">如果有任何擱置的要求過期，排程器就會分派它們。</span><span class="sxs-lookup"><span data-stu-id="1e201-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="1e201-138">「建議」方法會傳回下一個要求的時間。</span><span class="sxs-lookup"><span data-stu-id="1e201-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="1e201-139">背景工作執行緒會使用這個值來計算新的超時值。</span><span class="sxs-lookup"><span data-stu-id="1e201-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="1e201-140">步驟 2 6 會無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="1e201-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="1e201-141">若要終止背景工作執行緒，時鐘會設定內部旗標，並為事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="1e201-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="1e201-142">在步驟2中，可能是因為事件已發出信號，或等候超時。如果事件收到信號，表示新的要求已新增至清單前端。</span><span class="sxs-lookup"><span data-stu-id="1e201-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="1e201-143">工作者執行緒必須計算新的超時值。</span><span class="sxs-lookup"><span data-stu-id="1e201-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="1e201-144">另一方面，如果等候時間很大，則表示提出要求已到期且必須分派。</span><span class="sxs-lookup"><span data-stu-id="1e201-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="1e201-145">在步驟5中的建議呼叫會處理這兩種情況。</span><span class="sxs-lookup"><span data-stu-id="1e201-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e201-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e201-146">Requirements</span></span>



| <span data-ttu-id="1e201-147">需求</span><span class="sxs-lookup"><span data-stu-id="1e201-147">Requirement</span></span> | <span data-ttu-id="1e201-148">值</span><span class="sxs-lookup"><span data-stu-id="1e201-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e201-149">標頭</span><span class="sxs-lookup"><span data-stu-id="1e201-149">Header</span></span><br/>  | <dl> <span data-ttu-id="1e201-150"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1e201-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="1e201-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e201-151">Library</span></span><br/> | <dl> <span data-ttu-id="1e201-152"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1e201-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




