---
description: AdvisePeriodic 方法會建立週期性建議要求。 這個方法會實 IReferenceClock：： AdvisePeriodic 方法。
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: 'CBaseReferenceClock. AdvisePeriodic 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993557"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="4a189-104">CBaseReferenceClock. AdvisePeriodic 方法</span><span class="sxs-lookup"><span data-stu-id="4a189-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="4a189-105">`AdvisePeriodic`方法會建立週期性建議要求。</span><span class="sxs-lookup"><span data-stu-id="4a189-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="4a189-106">這個方法會實 [**IReferenceClock：： AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) 方法。</span><span class="sxs-lookup"><span data-stu-id="4a189-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a189-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a189-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="4a189-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a189-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a189-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="4a189-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="4a189-110">第一個通知的時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="4a189-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="4a189-111">必須大於零且小於最大 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="4a189-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="4a189-112">*PeriodTime*</span><span class="sxs-lookup"><span data-stu-id="4a189-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="4a189-113">通知之間的時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="4a189-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="4a189-114">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="4a189-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a189-115">*hSemaphore*</span><span class="sxs-lookup"><span data-stu-id="4a189-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="4a189-116">呼叫端所建立之信號的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a189-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="4a189-117">*pdwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="4a189-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="4a189-118">變數的指標，此變數會接收通知要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a189-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a189-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a189-119">Return value</span></span>

<span data-ttu-id="4a189-120">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4a189-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4a189-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4a189-121">Return code</span></span>                                                                                   | <span data-ttu-id="4a189-122">Description</span><span class="sxs-lookup"><span data-stu-id="4a189-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="4a189-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4a189-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4a189-124">Success</span><span class="sxs-lookup"><span data-stu-id="4a189-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="4a189-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a189-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4a189-126">時間值無效</span><span class="sxs-lookup"><span data-stu-id="4a189-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="4a189-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4a189-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4a189-128">失敗</span><span class="sxs-lookup"><span data-stu-id="4a189-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="4a189-129"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4a189-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4a189-130">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="4a189-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a189-131">備註</span><span class="sxs-lookup"><span data-stu-id="4a189-131">Remarks</span></span>

<span data-ttu-id="4a189-132">在每個通知時間，時鐘會釋放 *hSemaphore* 參數中指定的信號。</span><span class="sxs-lookup"><span data-stu-id="4a189-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="4a189-133">如果不再需要任何通知，請呼叫 [**CBaseReferenceClock：： Unadvise**](cbasereferenceclock-unadvise.md) 方法，並傳遞從此呼叫傳回的 *pdwAdviseToken* 值。</span><span class="sxs-lookup"><span data-stu-id="4a189-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a189-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a189-134">Requirements</span></span>



| <span data-ttu-id="4a189-135">需求</span><span class="sxs-lookup"><span data-stu-id="4a189-135">Requirement</span></span> | <span data-ttu-id="4a189-136">值</span><span class="sxs-lookup"><span data-stu-id="4a189-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a189-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4a189-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4a189-138"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4a189-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a189-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a189-139">Library</span></span><br/> | <dl> <span data-ttu-id="4a189-140"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4a189-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a189-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a189-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a189-142">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="4a189-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




