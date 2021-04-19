---
description: GetTime 方法會抓取目前的參考時間。 這個方法會實 IReferenceClock：： GetTime 方法。
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: 'CBaseReferenceClock. GetTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999489"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="d8c61-104">CBaseReferenceClock. GetTime 方法</span><span class="sxs-lookup"><span data-stu-id="d8c61-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="d8c61-105">`GetTime`方法會捕獲目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="d8c61-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="d8c61-106">這個方法會實 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法。</span><span class="sxs-lookup"><span data-stu-id="d8c61-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c61-107">語法</span><span class="sxs-lookup"><span data-stu-id="d8c61-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="d8c61-108">參數</span><span class="sxs-lookup"><span data-stu-id="d8c61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c61-109">*pTime*</span><span class="sxs-lookup"><span data-stu-id="d8c61-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c61-110">接收目前時間的變數指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="d8c61-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c61-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8c61-111">Return value</span></span>

<span data-ttu-id="d8c61-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d8c61-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d8c61-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d8c61-113">Return code</span></span>                                                                               | <span data-ttu-id="d8c61-114">Description</span><span class="sxs-lookup"><span data-stu-id="d8c61-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d8c61-115"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d8c61-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d8c61-116">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d8c61-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="d8c61-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d8c61-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d8c61-118">傳回的時間與前一個值相同。</span><span class="sxs-lookup"><span data-stu-id="d8c61-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="d8c61-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d8c61-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d8c61-120">成功。</span><span class="sxs-lookup"><span data-stu-id="d8c61-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="d8c61-121">備註</span><span class="sxs-lookup"><span data-stu-id="d8c61-121">Remarks</span></span>

<span data-ttu-id="d8c61-122">這個方法會呼叫 [**CBaseReferenceClock：： GetPrivateTime**](cbasereferenceclock-getprivatetime.md) 方法來判斷實際的時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="d8c61-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="d8c61-123">如果時鐘時間嚴格大於先前的值，則會 `GetTime` 使用時鐘時間，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d8c61-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="d8c61-124">否則，會 `GetTime` 使用先前的值並傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="d8c61-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="d8c61-125">因此，內部時鐘可能會在短時間內執行，而不會導致參考時間回溯執行。</span><span class="sxs-lookup"><span data-stu-id="d8c61-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="d8c61-126">相反地，參考時間會「停止」相同的值，直到內部時鐘趕上為止。</span><span class="sxs-lookup"><span data-stu-id="d8c61-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c61-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8c61-127">Requirements</span></span>



| <span data-ttu-id="d8c61-128">需求</span><span class="sxs-lookup"><span data-stu-id="d8c61-128">Requirement</span></span> | <span data-ttu-id="d8c61-129">值</span><span class="sxs-lookup"><span data-stu-id="d8c61-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c61-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d8c61-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c61-131"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d8c61-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d8c61-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8c61-132">Library</span></span><br/> | <dl> <span data-ttu-id="d8c61-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8c61-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c61-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8c61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c61-135">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="d8c61-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




