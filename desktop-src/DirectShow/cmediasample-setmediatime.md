---
description: SetMediaTime 方法會設定此範例的媒體時間。 這個方法會實 IMediaSample：： SetMediaTime 方法。
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: 'CMediaSample. SetMediaTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994191"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="67ff6-104">CMediaSample. SetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="67ff6-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="67ff6-105">`SetMediaTime`方法會設定此範例的媒體時間。</span><span class="sxs-lookup"><span data-stu-id="67ff6-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="67ff6-106">這個方法會實 [**IMediaSample：： SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) 方法。</span><span class="sxs-lookup"><span data-stu-id="67ff6-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ff6-107">語法</span><span class="sxs-lookup"><span data-stu-id="67ff6-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="67ff6-108">參數</span><span class="sxs-lookup"><span data-stu-id="67ff6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ff6-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="67ff6-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="67ff6-110">媒體開始時間的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="67ff6-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67ff6-111">*暫止*</span><span class="sxs-lookup"><span data-stu-id="67ff6-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="67ff6-112">媒體停止時間的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="67ff6-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ff6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67ff6-113">Return value</span></span>

<span data-ttu-id="67ff6-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="67ff6-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ff6-115">備註</span><span class="sxs-lookup"><span data-stu-id="67ff6-115">Remarks</span></span>

<span data-ttu-id="67ff6-116">媒體停止時間必須大於媒體開始時間。</span><span class="sxs-lookup"><span data-stu-id="67ff6-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="67ff6-117">使用 **Null** 來使媒體時間失效。</span><span class="sxs-lookup"><span data-stu-id="67ff6-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="67ff6-118">*暫* 止的參數會指定絕對媒體時間，但 [**CMediaSample：： m \_ MediaEnd**](cmediasample-m-mediaend.md)成員變數會計算為 *pStart* 的位移。</span><span class="sxs-lookup"><span data-stu-id="67ff6-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="67ff6-119">換句話說， **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*。  </span><span class="sxs-lookup"><span data-stu-id="67ff6-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="67ff6-120">如需媒體時間的相關資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="67ff6-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ff6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ff6-121">Requirements</span></span>



| <span data-ttu-id="67ff6-122">需求</span><span class="sxs-lookup"><span data-stu-id="67ff6-122">Requirement</span></span> | <span data-ttu-id="67ff6-123">值</span><span class="sxs-lookup"><span data-stu-id="67ff6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ff6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="67ff6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67ff6-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="67ff6-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67ff6-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="67ff6-126">Library</span></span><br/> | <dl> <span data-ttu-id="67ff6-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="67ff6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ff6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67ff6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ff6-129">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="67ff6-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




