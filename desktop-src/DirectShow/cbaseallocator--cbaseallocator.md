---
description: 函式方法。
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: 'CBaseAllocator. ~ CBaseAllocator (Amfilter 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976761"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="9cb0b-103">CBaseAllocator. ~ CBaseAllocator 的函式</span><span class="sxs-lookup"><span data-stu-id="9cb0b-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="9cb0b-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="9cb0b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9cb0b-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="9cb0b-106">備註</span><span class="sxs-lookup"><span data-stu-id="9cb0b-106">Remarks</span></span>

<span data-ttu-id="9cb0b-107">在終結物件之前，請一律呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9cb0b-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="9cb0b-108">基類的函式無法呼叫 **取消認可**，因為該方法會呼叫純虛擬方法 [**CBaseAllocator：： Free**](cbaseallocator-free.md)。</span><span class="sxs-lookup"><span data-stu-id="9cb0b-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="9cb0b-109">衍生類別應該覆寫這個函式並呼叫 **取消認可**。</span><span class="sxs-lookup"><span data-stu-id="9cb0b-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cb0b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cb0b-110">Requirements</span></span>



| <span data-ttu-id="9cb0b-111">需求</span><span class="sxs-lookup"><span data-stu-id="9cb0b-111">Requirement</span></span> | <span data-ttu-id="9cb0b-112">值</span><span class="sxs-lookup"><span data-stu-id="9cb0b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb0b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9cb0b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9cb0b-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9cb0b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9cb0b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9cb0b-115">Library</span></span><br/> | <dl> <span data-ttu-id="9cb0b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9cb0b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cb0b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cb0b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb0b-118">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="9cb0b-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




