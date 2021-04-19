---
description: SetWaiting 方法會遞增等候執行緒的計數。
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: 'CBaseAllocator. SetWaiting 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991175"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="d9e3e-103">CBaseAllocator. SetWaiting 方法</span><span class="sxs-lookup"><span data-stu-id="d9e3e-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="d9e3e-104">`SetWaiting`方法會遞增等候中線程的計數。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e3e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d9e3e-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="d9e3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9e3e-106">Parameters</span></span>

<span data-ttu-id="d9e3e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9e3e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9e3e-108">Return value</span></span>

<span data-ttu-id="d9e3e-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e3e-110">備註</span><span class="sxs-lookup"><span data-stu-id="d9e3e-110">Remarks</span></span>

<span data-ttu-id="d9e3e-111">這個方法會遞增 [**CBaseAllocator：： m \_ lWaiting**](cbaseallocator-m-lwaiting.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="d9e3e-112">如果執行緒在 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法中遭到封鎖，配置器 `SetWaiting` 就會呼叫，然後等候 [**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md) 信號發出信號。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="d9e3e-113">[**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md)方法會表示信號，並將 *m \_ lWaiting* 設回零。</span><span class="sxs-lookup"><span data-stu-id="d9e3e-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e3e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9e3e-114">Requirements</span></span>



| <span data-ttu-id="d9e3e-115">需求</span><span class="sxs-lookup"><span data-stu-id="d9e3e-115">Requirement</span></span> | <span data-ttu-id="d9e3e-116">值</span><span class="sxs-lookup"><span data-stu-id="d9e3e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e3e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d9e3e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d9e3e-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d9e3e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d9e3e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d9e3e-119">Library</span></span><br/> | <dl> <span data-ttu-id="d9e3e-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d9e3e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9e3e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9e3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e3e-122">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="d9e3e-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




