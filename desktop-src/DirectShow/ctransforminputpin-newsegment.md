---
description: NewSegment 方法會在此呼叫群組為區段之後，通知 pin 所收到的媒體範例。 這個方法會實 IPin：： NewSegment 方法。
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: 'CTransformInputPin. NewSegment 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989683"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="20871-104">CTransformInputPin. NewSegment 方法</span><span class="sxs-lookup"><span data-stu-id="20871-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="20871-105">`NewSegment`方法會通知釘選在此呼叫群組為區段之後所收到的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="20871-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="20871-106">這個方法會實 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。</span><span class="sxs-lookup"><span data-stu-id="20871-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20871-107">語法</span><span class="sxs-lookup"><span data-stu-id="20871-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="20871-108">參數</span><span class="sxs-lookup"><span data-stu-id="20871-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20871-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="20871-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="20871-110">區段的開始時間。</span><span class="sxs-lookup"><span data-stu-id="20871-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="20871-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="20871-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="20871-112">區段的停止時間。</span><span class="sxs-lookup"><span data-stu-id="20871-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="20871-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="20871-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="20871-114">區段的速率。</span><span class="sxs-lookup"><span data-stu-id="20871-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20871-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="20871-115">Return value</span></span>

<span data-ttu-id="20871-116">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="20871-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20871-117">備註</span><span class="sxs-lookup"><span data-stu-id="20871-117">Remarks</span></span>

<span data-ttu-id="20871-118">這個方法會覆寫 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="20871-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="20871-119">它會呼叫篩選器的 [**CTransformFilter：： NewSegment**](ctransformfilter-newsegment.md) 方法，以傳遞下游的呼叫。</span><span class="sxs-lookup"><span data-stu-id="20871-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="20871-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="20871-120">Requirements</span></span>



| <span data-ttu-id="20871-121">需求</span><span class="sxs-lookup"><span data-stu-id="20871-121">Requirement</span></span> | <span data-ttu-id="20871-122">值</span><span class="sxs-lookup"><span data-stu-id="20871-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20871-123">標頭</span><span class="sxs-lookup"><span data-stu-id="20871-123">Header</span></span><br/>  | <dl> <span data-ttu-id="20871-124"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="20871-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20871-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="20871-125">Library</span></span><br/> | <dl> <span data-ttu-id="20871-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="20871-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




