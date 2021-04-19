---
description: SetTime 方法會設定這個範例開始和完成時的資料流程時間。 這個方法會實 IMediaSample：： SetTime 方法。
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: 'CMediaSample. SetTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975723"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="3c6a6-104">CMediaSample. SetTime 方法</span><span class="sxs-lookup"><span data-stu-id="3c6a6-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="3c6a6-105">`SetTime`方法會設定這個範例開始和完成時的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="3c6a6-106">這個方法會實 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c6a6-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c6a6-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="3c6a6-108">參數</span><span class="sxs-lookup"><span data-stu-id="3c6a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6a6-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="3c6a6-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6a6-110">範例開始的資料流程時間指標，以 100-毫微秒單位表示，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3c6a6-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="3c6a6-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6a6-112">樣本結束的資料流程時間指標，以 100-毫微秒單位表示，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6a6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c6a6-113">Return value</span></span>

<span data-ttu-id="3c6a6-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c6a6-115">備註</span><span class="sxs-lookup"><span data-stu-id="3c6a6-115">Remarks</span></span>

<span data-ttu-id="3c6a6-116">這個方法會設定 [**CMediaSample：： m \_ Start**](cmediasample-m-start.md) 和 [**CMediaSample：： m \_ End**](cmediasample-m-end.md) 成員變數，以指定時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="3c6a6-117">它也會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定時間戳記是否有效。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="3c6a6-118">如需時間戳記的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="3c6a6-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6a6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c6a6-119">Requirements</span></span>



| <span data-ttu-id="3c6a6-120">需求</span><span class="sxs-lookup"><span data-stu-id="3c6a6-120">Requirement</span></span> | <span data-ttu-id="3c6a6-121">值</span><span class="sxs-lookup"><span data-stu-id="3c6a6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6a6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3c6a6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3c6a6-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3c6a6-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3c6a6-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c6a6-124">Library</span></span><br/> | <dl> <span data-ttu-id="3c6a6-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3c6a6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6a6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c6a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c6a6-127">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="3c6a6-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




