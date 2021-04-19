---
description: PeekAllocator 方法會傳回釘選配置器的指標。 方法不會遞增介面上的參考計數。
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: 'CTransInPlaceOutputPin. PeekAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992852"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="9815a-104">CTransInPlaceOutputPin. PeekAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="9815a-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="9815a-105">方法會傳回釘選配置器的 `PeekAllocator` 指標。</span><span class="sxs-lookup"><span data-stu-id="9815a-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="9815a-106">方法不會遞增介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="9815a-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9815a-107">語法</span><span class="sxs-lookup"><span data-stu-id="9815a-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="9815a-108">參數</span><span class="sxs-lookup"><span data-stu-id="9815a-108">Parameters</span></span>

<span data-ttu-id="9815a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9815a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9815a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9815a-110">Return value</span></span>

<span data-ttu-id="9815a-111">傳回 [**CBaseOutputPin：： m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="9815a-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9815a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9815a-112">Requirements</span></span>



| <span data-ttu-id="9815a-113">需求</span><span class="sxs-lookup"><span data-stu-id="9815a-113">Requirement</span></span> | <span data-ttu-id="9815a-114">值</span><span class="sxs-lookup"><span data-stu-id="9815a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9815a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9815a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9815a-116"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9815a-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9815a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="9815a-117">Library</span></span><br/> | <dl> <span data-ttu-id="9815a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9815a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9815a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9815a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9815a-120">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9815a-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




