---
description: 「建議」方法會分派排程于指定時間或更早時間的所有要求。
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: 'CAMSchedule，建議方法 (Dsschedule) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982669"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="473af-103">CAMSchedule，建議方法</span><span class="sxs-lookup"><span data-stu-id="473af-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="473af-104">`Advise`方法會分派排程于指定時間或更早時間的所有要求。</span><span class="sxs-lookup"><span data-stu-id="473af-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="473af-105">語法</span><span class="sxs-lookup"><span data-stu-id="473af-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="473af-106">參數</span><span class="sxs-lookup"><span data-stu-id="473af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473af-107">*rtTime* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="473af-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="473af-108">指定目前參考時間的值。</span><span class="sxs-lookup"><span data-stu-id="473af-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473af-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="473af-109">Return value</span></span>

<span data-ttu-id="473af-110">傳回下一個排定的建議要求的參考時間，或如果沒有任何剩餘的時間，則為最大 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="473af-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="473af-111">備註</span><span class="sxs-lookup"><span data-stu-id="473af-111">Remarks</span></span>

<span data-ttu-id="473af-112">當時鐘呼叫這個方法時，它會指定目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="473af-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="473af-113">排程器會判斷哪些告知要求已過期（如果有的話），並分派這些要求。</span><span class="sxs-lookup"><span data-stu-id="473af-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="473af-114">如果單次要求過期，排程器就會將它刪除。</span><span class="sxs-lookup"><span data-stu-id="473af-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="473af-115">如果定期要求過期，排程器會在下一個建議時間重新排程它。</span><span class="sxs-lookup"><span data-stu-id="473af-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="473af-116">方法會傳回下一個暫止要求的時間。</span><span class="sxs-lookup"><span data-stu-id="473af-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="473af-117">為了分派提出建議的要求，排程器會向 [**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md)方法的 *hNotify* 參數中指定的事件或信號發出信號。</span><span class="sxs-lookup"><span data-stu-id="473af-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="473af-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="473af-118">Requirements</span></span>



| <span data-ttu-id="473af-119">需求</span><span class="sxs-lookup"><span data-stu-id="473af-119">Requirement</span></span> | <span data-ttu-id="473af-120">值</span><span class="sxs-lookup"><span data-stu-id="473af-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="473af-121">標頭</span><span class="sxs-lookup"><span data-stu-id="473af-121">Header</span></span><br/>  | <dl> <span data-ttu-id="473af-122"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="473af-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="473af-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="473af-123">Library</span></span><br/> | <dl> <span data-ttu-id="473af-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="473af-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473af-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="473af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473af-126">**CAMSchedule 類別**</span><span class="sxs-lookup"><span data-stu-id="473af-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




