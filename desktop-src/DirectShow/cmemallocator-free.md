---
description: 在取消認可操作期間會呼叫 Free 方法。
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: 'CMemAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998644"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="839ad-103">CMemAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="839ad-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="839ad-104">在 `Free` 取消認可作業期間會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="839ad-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="839ad-105">這個方法會執行純虛擬 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法，但不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="839ad-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="839ad-106">在 **CMemAllocator** 物件終結之前，不會實際釋放緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="839ad-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="839ad-107">「函式」方法會呼叫 [**CMemAllocator：： ReallyFree**](cmemallocator-reallyfree.md) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="839ad-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="839ad-108">語法</span><span class="sxs-lookup"><span data-stu-id="839ad-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="839ad-109">參數</span><span class="sxs-lookup"><span data-stu-id="839ad-109">Parameters</span></span>

<span data-ttu-id="839ad-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="839ad-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="839ad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="839ad-111">Return value</span></span>

<span data-ttu-id="839ad-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="839ad-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="839ad-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="839ad-113">Requirements</span></span>



| <span data-ttu-id="839ad-114">需求</span><span class="sxs-lookup"><span data-stu-id="839ad-114">Requirement</span></span> | <span data-ttu-id="839ad-115">值</span><span class="sxs-lookup"><span data-stu-id="839ad-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839ad-116">標頭</span><span class="sxs-lookup"><span data-stu-id="839ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="839ad-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="839ad-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="839ad-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="839ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="839ad-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="839ad-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="839ad-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="839ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839ad-121">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="839ad-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




