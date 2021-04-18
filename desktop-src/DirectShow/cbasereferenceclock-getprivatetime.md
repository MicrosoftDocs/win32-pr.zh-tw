---
description: GetPrivateTime 方法會從時鐘中取出即時時間。
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: 'CBaseReferenceClock. GetPrivateTime 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976223"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="c5c67-103">CBaseReferenceClock. GetPrivateTime 方法</span><span class="sxs-lookup"><span data-stu-id="c5c67-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="c5c67-104">`GetPrivateTime`方法會從時鐘中取出即時時間。</span><span class="sxs-lookup"><span data-stu-id="c5c67-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c67-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5c67-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="c5c67-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5c67-106">Parameters</span></span>

<span data-ttu-id="c5c67-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c5c67-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5c67-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5c67-108">Return value</span></span>

<span data-ttu-id="c5c67-109">傳回目前的時鐘時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="c5c67-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c67-110">備註</span><span class="sxs-lookup"><span data-stu-id="c5c67-110">Remarks</span></span>

<span data-ttu-id="c5c67-111">這個方法會傳回由時鐘回報的即時時間。</span><span class="sxs-lookup"><span data-stu-id="c5c67-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="c5c67-112">外部呼叫端會使用 [**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md) 方法，它會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5c67-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="c5c67-113">與 **GetTime** 方法不同的是，可以使用內部時鐘來向前移動。</span><span class="sxs-lookup"><span data-stu-id="c5c67-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="c5c67-114">如果發生這種情況， **GetTime** 方法會繼續傳回上次回報的時間，直到 `GetPrivateTime` 方法趕上為止。</span><span class="sxs-lookup"><span data-stu-id="c5c67-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="c5c67-115">這個方法會傳回系統時間。</span><span class="sxs-lookup"><span data-stu-id="c5c67-115">This method returns the system time.</span></span> <span data-ttu-id="c5c67-116">如果您的時鐘從另一個來源取得時間，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5c67-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c67-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5c67-117">Requirements</span></span>



| <span data-ttu-id="c5c67-118">需求</span><span class="sxs-lookup"><span data-stu-id="c5c67-118">Requirement</span></span> | <span data-ttu-id="c5c67-119">值</span><span class="sxs-lookup"><span data-stu-id="c5c67-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c67-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c5c67-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c5c67-121"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c5c67-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c5c67-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5c67-122">Library</span></span><br/> | <dl> <span data-ttu-id="c5c67-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c5c67-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c67-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5c67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c67-125">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="c5c67-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




