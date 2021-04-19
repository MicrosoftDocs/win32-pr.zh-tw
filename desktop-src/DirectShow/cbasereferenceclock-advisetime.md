---
description: AdviseTime 方法會建立一次建議的要求。 這個方法會實 IReferenceClock：： AdviseTime 方法。
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: 'CBaseReferenceClock. AdviseTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990703"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="66e9b-104">CBaseReferenceClock. AdviseTime 方法</span><span class="sxs-lookup"><span data-stu-id="66e9b-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="66e9b-105">`AdviseTime`方法會建立一次建議的要求。</span><span class="sxs-lookup"><span data-stu-id="66e9b-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="66e9b-106">這個方法會實 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法。</span><span class="sxs-lookup"><span data-stu-id="66e9b-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="66e9b-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="66e9b-108">參數</span><span class="sxs-lookup"><span data-stu-id="66e9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e9b-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="66e9b-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="66e9b-110">基底參考時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="66e9b-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="66e9b-111">*streamTime*</span><span class="sxs-lookup"><span data-stu-id="66e9b-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="66e9b-112">資料流程位移時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="66e9b-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="66e9b-113">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="66e9b-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="66e9b-114">事件的控制碼，由呼叫端建立。</span><span class="sxs-lookup"><span data-stu-id="66e9b-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="66e9b-115">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="66e9b-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="66e9b-116">變數的指標，此變數會接收通知要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="66e9b-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e9b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e9b-117">Return value</span></span>

<span data-ttu-id="66e9b-118">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="66e9b-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="66e9b-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="66e9b-119">Return code</span></span>                                                                                   | <span data-ttu-id="66e9b-120">Description</span><span class="sxs-lookup"><span data-stu-id="66e9b-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="66e9b-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="66e9b-122">Success</span><span class="sxs-lookup"><span data-stu-id="66e9b-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="66e9b-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="66e9b-124">時間值無效</span><span class="sxs-lookup"><span data-stu-id="66e9b-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="66e9b-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="66e9b-126">失敗</span><span class="sxs-lookup"><span data-stu-id="66e9b-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="66e9b-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="66e9b-128">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="66e9b-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66e9b-129">備註</span><span class="sxs-lookup"><span data-stu-id="66e9b-129">Remarks</span></span>

<span data-ttu-id="66e9b-130">這個方法會建立參考時間 *baseTime* streamTime 的一次建議要求  +  \*\*。</span><span class="sxs-lookup"><span data-stu-id="66e9b-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="66e9b-131">總和必須大於零且小於最大 \_ 時間，否則方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="66e9b-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="66e9b-132">在要求的時間內，時鐘表示 *hEvent* 參數中指定的事件。</span><span class="sxs-lookup"><span data-stu-id="66e9b-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="66e9b-133">若要在到達時間之前取消通知，請呼叫 [**CBaseReferenceClock：： Unadvise**](cbasereferenceclock-unadvise.md) 方法，並傳遞從此呼叫傳回的 *pdwAdviseToken* 值。</span><span class="sxs-lookup"><span data-stu-id="66e9b-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="66e9b-134">在通知發生之後，時鐘會自動將其清除，因此不需要呼叫 **Unadvise**。</span><span class="sxs-lookup"><span data-stu-id="66e9b-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="66e9b-135">不過，這樣做並不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="66e9b-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e9b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e9b-136">Requirements</span></span>



| <span data-ttu-id="66e9b-137">需求</span><span class="sxs-lookup"><span data-stu-id="66e9b-137">Requirement</span></span> | <span data-ttu-id="66e9b-138">值</span><span class="sxs-lookup"><span data-stu-id="66e9b-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e9b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="66e9b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="66e9b-140"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66e9b-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="66e9b-141">Library</span></span><br/> | <dl> <span data-ttu-id="66e9b-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="66e9b-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e9b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e9b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e9b-144">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="66e9b-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




