---
description: Free 方法會釋放所有緩衝區記憶體。 當主控篩選器在最後一個媒體樣本釋出之後解除配置器時，就會呼叫這個方法。
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: 'CBaseAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995939"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="0e213-104">CBaseAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="0e213-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="0e213-105">`Free`方法會釋放所有緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="0e213-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="0e213-106">當主控篩選器在最後一個媒體樣本釋出之後解除配置器時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0e213-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e213-107">語法</span><span class="sxs-lookup"><span data-stu-id="0e213-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0e213-108">參數</span><span class="sxs-lookup"><span data-stu-id="0e213-108">Parameters</span></span>

<span data-ttu-id="0e213-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0e213-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e213-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e213-110">Return value</span></span>

<span data-ttu-id="0e213-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0e213-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e213-112">備註</span><span class="sxs-lookup"><span data-stu-id="0e213-112">Remarks</span></span>

<span data-ttu-id="0e213-113">呼叫 [**取消認可**](cbaseallocator-decommit.md) 方法之後，配置器會在釋放最後一個媒體範例時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0e213-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="0e213-114">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="0e213-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e213-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e213-115">Requirements</span></span>



| <span data-ttu-id="0e213-116">需求</span><span class="sxs-lookup"><span data-stu-id="0e213-116">Requirement</span></span> | <span data-ttu-id="0e213-117">值</span><span class="sxs-lookup"><span data-stu-id="0e213-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e213-118">標頭</span><span class="sxs-lookup"><span data-stu-id="0e213-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0e213-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0e213-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0e213-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e213-120">Library</span></span><br/> | <dl> <span data-ttu-id="0e213-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0e213-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e213-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e213-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e213-123">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="0e213-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




