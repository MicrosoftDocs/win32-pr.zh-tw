---
description: ReleaseBuffer 方法會將媒體範例傳回給可用媒體範例的清單。 這個方法會實 IMemAllocator：： ReleaseBuffer 方法。
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: 'CBaseAllocator. ReleaseBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993614"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="0c6c3-104">CBaseAllocator. ReleaseBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="0c6c3-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="0c6c3-105">方法會將 `ReleaseBuffer` 媒體範例傳回給可用媒體範例的清單。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="0c6c3-106">這個方法會實 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6c3-107">語法</span><span class="sxs-lookup"><span data-stu-id="0c6c3-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="0c6c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="0c6c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c6c3-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="0c6c3-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0c6c3-110">媒體範例物件之 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c6c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c6c3-111">Return value</span></span>

<span data-ttu-id="0c6c3-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c6c3-113">備註</span><span class="sxs-lookup"><span data-stu-id="0c6c3-113">Remarks</span></span>

<span data-ttu-id="0c6c3-114">當媒體範例的參考計數到達零時，此範例會以其本身做為參數來呼叫 **ReleaseBuffer** 。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="0c6c3-115">這個方法會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="0c6c3-116">將媒體範例傳回 ([**CBaseAllocator：： m \_ lFree**](cbaseallocator-m-lfree.md)) 的可用清單。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="0c6c3-117">呼叫 [**CBaseAllocator：： NotifySample**](cbaseallocator-notifysample.md) 方法，這個方法會釋放對 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法的呼叫所封鎖的任何執行緒。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="0c6c3-118">如果先前呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md) 方法，則會呼叫 **IMemAllocatorNotifyCallbackTemp：： NotifyRelease** 方法。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="0c6c3-119">當最後一個樣本釋出時，如果有擱置中的 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 呼叫，就會呼叫 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法來釋放緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="0c6c3-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="0c6c3-120"> (在基類中， **Free** 是純虛擬方法。 ) </span><span class="sxs-lookup"><span data-stu-id="0c6c3-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="0c6c3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c6c3-121">Requirements</span></span>



| <span data-ttu-id="0c6c3-122">需求</span><span class="sxs-lookup"><span data-stu-id="0c6c3-122">Requirement</span></span> | <span data-ttu-id="0c6c3-123">值</span><span class="sxs-lookup"><span data-stu-id="0c6c3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6c3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0c6c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0c6c3-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0c6c3-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0c6c3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c6c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="0c6c3-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0c6c3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c6c3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c6c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6c3-129">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="0c6c3-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




