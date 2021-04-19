---
description: SetTimeDelta 方法會調整內部時鐘時間。
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: 'CBaseReferenceClock. SetTimeDelta 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990799"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="9428b-103">CBaseReferenceClock. SetTimeDelta 方法</span><span class="sxs-lookup"><span data-stu-id="9428b-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="9428b-104">`SetTimeDelta`方法會調整內部時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="9428b-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9428b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9428b-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="9428b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9428b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9428b-107">*TimeDelta* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="9428b-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9428b-108">要調整時鐘時間的數量，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="9428b-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="9428b-109">正值會將時鐘往前移動，負值會將時鐘向後移動。</span><span class="sxs-lookup"><span data-stu-id="9428b-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9428b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9428b-110">Return value</span></span>

<span data-ttu-id="9428b-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9428b-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9428b-112">備註</span><span class="sxs-lookup"><span data-stu-id="9428b-112">Remarks</span></span>

<span data-ttu-id="9428b-113">如果從提供時間資訊的裝置偏離，衍生類別可以使用這個方法來調整內部時鐘。</span><span class="sxs-lookup"><span data-stu-id="9428b-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="9428b-114">[**CBaseReferenceClock：： GetTime**](cbasereferenceclock-gettime.md)方法永遠不會傳回遞減的值。</span><span class="sxs-lookup"><span data-stu-id="9428b-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="9428b-115">如果您將時鐘向後調整， **GetTime** 會傳回先前的值，直到時鐘再次到達該值為止。</span><span class="sxs-lookup"><span data-stu-id="9428b-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="9428b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9428b-116">Requirements</span></span>



| <span data-ttu-id="9428b-117">需求</span><span class="sxs-lookup"><span data-stu-id="9428b-117">Requirement</span></span> | <span data-ttu-id="9428b-118">值</span><span class="sxs-lookup"><span data-stu-id="9428b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9428b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9428b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9428b-120"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9428b-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9428b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="9428b-121">Library</span></span><br/> | <dl> <span data-ttu-id="9428b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9428b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9428b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9428b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9428b-124">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="9428b-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




