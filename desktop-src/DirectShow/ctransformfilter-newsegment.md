---
description: NewSegment 方法會通知篩選此呼叫之後所收到的媒體範例會分組為區段。
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: 'CTransformFilter. NewSegment 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995409"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="dd2a3-103">CTransformFilter. NewSegment 方法</span><span class="sxs-lookup"><span data-stu-id="dd2a3-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="dd2a3-104">`NewSegment`方法會在此呼叫群組為區段之後，通知篩選出所收到的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd2a3-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="dd2a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2a3-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="dd2a3-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="dd2a3-108">相對於原始來源之區段的開始時間。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="dd2a3-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="dd2a3-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="dd2a3-110">相對於原始來源之區段的停止時間。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="dd2a3-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="dd2a3-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="dd2a3-112">應處理區段的速率。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2a3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd2a3-113">Return value</span></span>

<span data-ttu-id="dd2a3-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2a3-115">備註</span><span class="sxs-lookup"><span data-stu-id="dd2a3-115">Remarks</span></span>

<span data-ttu-id="dd2a3-116">輸入釘選的 [**CTransformInputPin：： NewSegment**](ctransforminputpin-newsegment.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="dd2a3-117">這個方法會傳遞對 `NewSegment` 下游輸入 pin 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="dd2a3-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2a3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd2a3-118">Requirements</span></span>



| <span data-ttu-id="dd2a3-119">需求</span><span class="sxs-lookup"><span data-stu-id="dd2a3-119">Requirement</span></span> | <span data-ttu-id="dd2a3-120">值</span><span class="sxs-lookup"><span data-stu-id="dd2a3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2a3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="dd2a3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dd2a3-122"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dd2a3-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dd2a3-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd2a3-123">Library</span></span><br/> | <dl> <span data-ttu-id="dd2a3-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dd2a3-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2a3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd2a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2a3-126">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="dd2a3-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




