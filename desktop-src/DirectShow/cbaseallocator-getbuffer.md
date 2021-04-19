---
description: GetBuffer 方法會抓取包含緩衝區的媒體範例。 這個方法會實 IMemAllocator：： GetBuffer 方法。
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: 'CBaseAllocator. GetBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997731"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="d55a7-104">CBaseAllocator. GetBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="d55a7-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="d55a7-105">`GetBuffer`方法會抓取包含緩衝區的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="d55a7-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="d55a7-106">這個方法會實 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法。</span><span class="sxs-lookup"><span data-stu-id="d55a7-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55a7-107">語法</span><span class="sxs-lookup"><span data-stu-id="d55a7-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d55a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="d55a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55a7-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="d55a7-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d55a7-110">接收緩衝區 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d55a7-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="d55a7-111">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="d55a7-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d55a7-112">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="d55a7-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d55a7-113">範例開始時間的指標。</span><span class="sxs-lookup"><span data-stu-id="d55a7-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="d55a7-114">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="d55a7-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d55a7-115">範例結束時間的指標。</span><span class="sxs-lookup"><span data-stu-id="d55a7-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="d55a7-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d55a7-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="d55a7-117">零或多個旗標的位元組合。</span><span class="sxs-lookup"><span data-stu-id="d55a7-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="d55a7-118">基類支援下列旗標。</span><span class="sxs-lookup"><span data-stu-id="d55a7-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="d55a7-119">值</span><span class="sxs-lookup"><span data-stu-id="d55a7-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="d55a7-120">意義</span><span class="sxs-lookup"><span data-stu-id="d55a7-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="d55a7-121"><dt>**AM \_ GBF \_ NOWAIT**</dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="d55a7-122">請勿等候緩衝區變成可用。</span><span class="sxs-lookup"><span data-stu-id="d55a7-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d55a7-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="d55a7-123">Return value</span></span>

<span data-ttu-id="d55a7-124">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d55a7-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d55a7-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d55a7-125">Return code</span></span>                                                                                           | <span data-ttu-id="d55a7-126">Description</span><span class="sxs-lookup"><span data-stu-id="d55a7-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d55a7-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d55a7-128">成功。</span><span class="sxs-lookup"><span data-stu-id="d55a7-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="d55a7-129"><dt>**VFW \_ E \_ 未 \_ 認可**</dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="d55a7-130">未認可配置器。</span><span class="sxs-lookup"><span data-stu-id="d55a7-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="d55a7-131"><dt>**VFW \_ E \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="d55a7-132">逾時。</span><span class="sxs-lookup"><span data-stu-id="d55a7-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="d55a7-133">備註</span><span class="sxs-lookup"><span data-stu-id="d55a7-133">Remarks</span></span>

<span data-ttu-id="d55a7-134">除非呼叫端在 *dwFlags* 中指定 **AM \_ GBF \_ NOWAIT** 旗標，否則這個方法會封鎖，直到下一個範例可供使用為止。</span><span class="sxs-lookup"><span data-stu-id="d55a7-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="d55a7-135">抓取的媒體範例具有已配置緩衝區的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d55a7-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="d55a7-136">呼叫端負責設定範例上的任何其他屬性，例如時間戳記、媒體時間或同步點屬性。</span><span class="sxs-lookup"><span data-stu-id="d55a7-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="d55a7-137">如需詳細資訊，請參閱 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)。</span><span class="sxs-lookup"><span data-stu-id="d55a7-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="d55a7-138">在基類中， *pStartTime* 和 *pEndTime* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d55a7-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="d55a7-139">衍生的類別可以使用這些值。</span><span class="sxs-lookup"><span data-stu-id="d55a7-139">Derived classes can use these values.</span></span> <span data-ttu-id="d55a7-140">例如， [影片](video-renderer-filter.md) 轉譯器篩選器的配置器會使用這些值，在 DirectDraw 表面之間進行同步切換。</span><span class="sxs-lookup"><span data-stu-id="d55a7-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="d55a7-141">如果此方法需要等候範例，則會將等待物件的計數遞增 ([**CBaseAllocator：： m \_ LCount**](cbaseallocator-m-lcount.md)) ，而信號 ([**CBaseAllocator：： m \_ HSem**](cbaseallocator-m-hsem.md)) 上的呼叫 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)函數。</span><span class="sxs-lookup"><span data-stu-id="d55a7-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="d55a7-142">當範例變成可用時，它會在配置器上呼叫 [**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md) 方法，這會增加 **m \_ lCount** (的信號計數，藉此釋出等候中的執行緒) 並將 **\_ lCount** 回零。</span><span class="sxs-lookup"><span data-stu-id="d55a7-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d55a7-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="d55a7-143">Requirements</span></span>



| <span data-ttu-id="d55a7-144">需求</span><span class="sxs-lookup"><span data-stu-id="d55a7-144">Requirement</span></span> | <span data-ttu-id="d55a7-145">值</span><span class="sxs-lookup"><span data-stu-id="d55a7-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d55a7-146">標頭</span><span class="sxs-lookup"><span data-stu-id="d55a7-146">Header</span></span><br/>  | <dl> <span data-ttu-id="d55a7-147"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d55a7-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="d55a7-148">Library</span></span><br/> | <dl> <span data-ttu-id="d55a7-149"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d55a7-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55a7-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d55a7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55a7-151">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="d55a7-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

