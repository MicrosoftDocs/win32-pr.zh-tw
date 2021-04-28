---
description: CTransInPlaceOutputPin. PeekAllocator 方法-PeekAllocator 方法會傳回釘選配置器的指標。 方法不會遞增介面上的參考計數。
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
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084596"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="101f1-104">CTransInPlaceOutputPin. PeekAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="101f1-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="101f1-105">方法會傳回釘選配置器的 `PeekAllocator` 指標。</span><span class="sxs-lookup"><span data-stu-id="101f1-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="101f1-106">方法不會遞增介面上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="101f1-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="101f1-107">語法</span><span class="sxs-lookup"><span data-stu-id="101f1-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="101f1-108">參數</span><span class="sxs-lookup"><span data-stu-id="101f1-108">Parameters</span></span>

<span data-ttu-id="101f1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="101f1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="101f1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="101f1-110">Return value</span></span>

<span data-ttu-id="101f1-111">傳回 [**CBaseOutputPin：： m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="101f1-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="101f1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="101f1-112">Requirements</span></span>



| <span data-ttu-id="101f1-113">需求</span><span class="sxs-lookup"><span data-stu-id="101f1-113">Requirement</span></span> | <span data-ttu-id="101f1-114">值</span><span class="sxs-lookup"><span data-stu-id="101f1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101f1-115">標頭</span><span class="sxs-lookup"><span data-stu-id="101f1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="101f1-116"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="101f1-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="101f1-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="101f1-117">Library</span></span><br/> | <dl> <span data-ttu-id="101f1-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="101f1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="101f1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="101f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101f1-120">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="101f1-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




