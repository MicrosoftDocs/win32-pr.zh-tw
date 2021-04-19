---
description: 取消認可方法將解除配置器。 這個方法會實 IMemAllocator：:D ecommit 方法。
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: 'CBaseAllocator. 取消認可方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998617"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="1078e-104">CBaseAllocator. 取消認可方法</span><span class="sxs-lookup"><span data-stu-id="1078e-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="1078e-105">`Decommit`方法會解除配置配置器。</span><span class="sxs-lookup"><span data-stu-id="1078e-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="1078e-106">這個方法會實 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) 方法。</span><span class="sxs-lookup"><span data-stu-id="1078e-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1078e-107">語法</span><span class="sxs-lookup"><span data-stu-id="1078e-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="1078e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1078e-108">Parameters</span></span>

<span data-ttu-id="1078e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1078e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1078e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1078e-110">Return value</span></span>

<span data-ttu-id="1078e-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1078e-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1078e-112">備註</span><span class="sxs-lookup"><span data-stu-id="1078e-112">Remarks</span></span>

<span data-ttu-id="1078e-113">呼叫這個方法之後，對 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法的呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="1078e-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="1078e-114">當範例釋出時，它們就會回到可用清單。</span><span class="sxs-lookup"><span data-stu-id="1078e-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="1078e-115">傳回最後一個範例時，配置器會呼叫 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法，它會釋放已配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1078e-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="1078e-116"> (在基類中， **Free** 是純虛擬方法。 ) </span><span class="sxs-lookup"><span data-stu-id="1078e-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="1078e-117">此外，這個方法會釋放 **GetBuffer** 呼叫封鎖的任何執行緒。</span><span class="sxs-lookup"><span data-stu-id="1078e-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="1078e-118">對 **GetBuffer** 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="1078e-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="1078e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1078e-119">Requirements</span></span>



| <span data-ttu-id="1078e-120">需求</span><span class="sxs-lookup"><span data-stu-id="1078e-120">Requirement</span></span> | <span data-ttu-id="1078e-121">值</span><span class="sxs-lookup"><span data-stu-id="1078e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1078e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1078e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1078e-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1078e-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1078e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="1078e-124">Library</span></span><br/> | <dl> <span data-ttu-id="1078e-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1078e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1078e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1078e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1078e-127">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="1078e-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




