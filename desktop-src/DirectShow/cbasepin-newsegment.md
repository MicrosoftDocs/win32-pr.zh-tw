---
description: NewSegment 方法會在此呼叫群組為區段之後，通知 pin 所收到的媒體範例。 實行 IPin：： NewSegment 方法。
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: 'CBasePin. NewSegment 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994309"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="3860c-104">CBasePin. NewSegment 方法</span><span class="sxs-lookup"><span data-stu-id="3860c-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="3860c-105">`NewSegment`方法會通知釘選在此呼叫群組為區段之後所收到的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3860c-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="3860c-106">實行 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。</span><span class="sxs-lookup"><span data-stu-id="3860c-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3860c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3860c-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="3860c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3860c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3860c-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="3860c-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3860c-110">區段的開始媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="3860c-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3860c-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="3860c-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="3860c-112">區段的結束媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="3860c-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3860c-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="3860c-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="3860c-114">此區段的處理速率（以原始費率的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="3860c-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3860c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3860c-115">Return value</span></span>

<span data-ttu-id="3860c-116">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3860c-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3860c-117">備註</span><span class="sxs-lookup"><span data-stu-id="3860c-117">Remarks</span></span>

<span data-ttu-id="3860c-118">這個方法會設定 [**CBasePin：： m \_ tStart**](cbasepin-m-tstart.md)、 [**CBasePin：： m \_ tStop**](cbasepin-m-tstop.md)和 [**CBasePin：： m \_ dRate**](cbasepin-m-drate.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="3860c-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="3860c-119">在您的衍生類別中，覆寫這個方法以傳遞通知下游。</span><span class="sxs-lookup"><span data-stu-id="3860c-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="3860c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3860c-120">Requirements</span></span>



| <span data-ttu-id="3860c-121">需求</span><span class="sxs-lookup"><span data-stu-id="3860c-121">Requirement</span></span> | <span data-ttu-id="3860c-122">值</span><span class="sxs-lookup"><span data-stu-id="3860c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3860c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3860c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3860c-124"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3860c-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3860c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="3860c-125">Library</span></span><br/> | <dl> <span data-ttu-id="3860c-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3860c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3860c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3860c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3860c-128">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="3860c-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




