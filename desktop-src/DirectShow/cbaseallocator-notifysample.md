---
description: NotifySample 方法會釋放任何正在等候樣本的執行緒。
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: 'CBaseAllocator. NotifySample 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990084"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="665f4-103">CBaseAllocator. NotifySample 方法</span><span class="sxs-lookup"><span data-stu-id="665f4-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="665f4-104">`NotifySample`方法會釋放任何正在等候樣本的執行緒。</span><span class="sxs-lookup"><span data-stu-id="665f4-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="665f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="665f4-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="665f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="665f4-106">Parameters</span></span>

<span data-ttu-id="665f4-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="665f4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="665f4-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="665f4-108">Return value</span></span>

<span data-ttu-id="665f4-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="665f4-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="665f4-110">備註</span><span class="sxs-lookup"><span data-stu-id="665f4-110">Remarks</span></span>

<span data-ttu-id="665f4-111">當有線程等候樣本時， [**CBaseAllocator：： m \_ lWaiting**](cbaseallocator-m-lwaiting.md) 的值大於零。</span><span class="sxs-lookup"><span data-stu-id="665f4-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="665f4-112">如果 *m \_ lWaiting* 大於零，則這個方法會呼叫 [**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md)信號上的 **ReleaseSemaphore** 函式，以啟用任何等候中的執行緒。</span><span class="sxs-lookup"><span data-stu-id="665f4-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="665f4-113">它也會將 *m \_ lWaiting* 重設為零。</span><span class="sxs-lookup"><span data-stu-id="665f4-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="665f4-114">當範例傳回至可用清單時，會從 [**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md) 方法內呼叫這個方法;當配置器已取消認可時，從 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="665f4-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="665f4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="665f4-115">Requirements</span></span>



| <span data-ttu-id="665f4-116">需求</span><span class="sxs-lookup"><span data-stu-id="665f4-116">Requirement</span></span> | <span data-ttu-id="665f4-117">值</span><span class="sxs-lookup"><span data-stu-id="665f4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="665f4-118">標頭</span><span class="sxs-lookup"><span data-stu-id="665f4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="665f4-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="665f4-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="665f4-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="665f4-120">Library</span></span><br/> | <dl> <span data-ttu-id="665f4-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="665f4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="665f4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="665f4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665f4-123">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="665f4-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




