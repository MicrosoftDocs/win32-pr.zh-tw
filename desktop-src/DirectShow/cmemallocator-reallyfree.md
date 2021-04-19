---
description: ReallyFree 方法會釋放緩衝區的記憶體。
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: 'CMemAllocator. ReallyFree 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 187807658c8e15ddf530ca6687d860fe826f4208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989634"
---
# <a name="cmemallocatorreallyfree-method"></a><span data-ttu-id="1d70f-103">CMemAllocator. ReallyFree 方法</span><span class="sxs-lookup"><span data-stu-id="1d70f-103">CMemAllocator.ReallyFree method</span></span>

<span data-ttu-id="1d70f-104">`ReallyFree`方法會釋放緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1d70f-104">The `ReallyFree` method releases the memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d70f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d70f-105">Syntax</span></span>


```C++
void ReallyFree();
```



## <a name="parameters"></a><span data-ttu-id="1d70f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d70f-106">Parameters</span></span>

<span data-ttu-id="1d70f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1d70f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d70f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d70f-108">Return value</span></span>

<span data-ttu-id="1d70f-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1d70f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d70f-110">備註</span><span class="sxs-lookup"><span data-stu-id="1d70f-110">Remarks</span></span>

<span data-ttu-id="1d70f-111">[**CMemAllocator**](cmemallocator.md)類別會保留記憶體，直到刪除物件為止。</span><span class="sxs-lookup"><span data-stu-id="1d70f-111">The [**CMemAllocator**](cmemallocator.md) class holds memory until the object is deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d70f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d70f-112">Requirements</span></span>



| <span data-ttu-id="1d70f-113">需求</span><span class="sxs-lookup"><span data-stu-id="1d70f-113">Requirement</span></span> | <span data-ttu-id="1d70f-114">值</span><span class="sxs-lookup"><span data-stu-id="1d70f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d70f-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1d70f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1d70f-116"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1d70f-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1d70f-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d70f-117">Library</span></span><br/> | <dl> <span data-ttu-id="1d70f-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1d70f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d70f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d70f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d70f-120">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="1d70f-120">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




