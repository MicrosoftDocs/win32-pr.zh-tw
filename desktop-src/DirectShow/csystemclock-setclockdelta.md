---
description: SetClockDelta 方法會調整時鐘時間。 這個方法會實 IAMClockAdjust：： SetClockDelta 方法。
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: 'CSystemClock. SetClockDelta 方法 (Sysclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975741"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="5a19b-104">CSystemClock. SetClockDelta 方法</span><span class="sxs-lookup"><span data-stu-id="5a19b-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="5a19b-105">`SetClockDelta`方法會調整時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="5a19b-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="5a19b-106">這個方法會實 [**IAMClockAdjust：： SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a19b-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a19b-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a19b-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="5a19b-108">參數</span><span class="sxs-lookup"><span data-stu-id="5a19b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a19b-109">*rtDelta*</span><span class="sxs-lookup"><span data-stu-id="5a19b-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="5a19b-110">指定用來調整時鐘的量，作為 [**參考 \_ 時間**](reference-time.md) 值。</span><span class="sxs-lookup"><span data-stu-id="5a19b-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="5a19b-111">正值會將時鐘往前移動，負值會將時鐘向後移動。</span><span class="sxs-lookup"><span data-stu-id="5a19b-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a19b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a19b-112">Return value</span></span>

<span data-ttu-id="5a19b-113">傳回 S \_ OK 或 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a19b-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a19b-114">備註</span><span class="sxs-lookup"><span data-stu-id="5a19b-114">Remarks</span></span>

<span data-ttu-id="5a19b-115">這個方法只會呼叫 [**CBaseReferenceClock：： SetTimeDelta**](cbasereferenceclock-settimedelta.md)。</span><span class="sxs-lookup"><span data-stu-id="5a19b-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="5a19b-116">[**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)所傳回的時間值會以單純方式遞增。</span><span class="sxs-lookup"><span data-stu-id="5a19b-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="5a19b-117">如果您將時鐘設定回來， **GetTime** 會繼續回報舊的時間，直到內部時鐘趕上為止。</span><span class="sxs-lookup"><span data-stu-id="5a19b-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a19b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a19b-118">Requirements</span></span>



| <span data-ttu-id="5a19b-119">需求</span><span class="sxs-lookup"><span data-stu-id="5a19b-119">Requirement</span></span> | <span data-ttu-id="5a19b-120">值</span><span class="sxs-lookup"><span data-stu-id="5a19b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a19b-121">版本</span><span class="sxs-lookup"><span data-stu-id="5a19b-121">Version</span></span><br/> | <span data-ttu-id="5a19b-122">CSystemClock 類別</span><span class="sxs-lookup"><span data-stu-id="5a19b-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="5a19b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5a19b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5a19b-124"><dt>Sysclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5a19b-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a19b-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a19b-125">Library</span></span><br/> | <dl> <span data-ttu-id="5a19b-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5a19b-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




