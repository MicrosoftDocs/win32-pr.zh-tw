---
description: CBaseAllocator. ~ CBaseAllocator 的函式-函式方法。
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096416"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="ecc3f-103">CBaseAllocator. ~ CBaseAllocator 的函式</span><span class="sxs-lookup"><span data-stu-id="ecc3f-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="ecc3f-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ecc3f-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc3f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ecc3f-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="ecc3f-106">備註</span><span class="sxs-lookup"><span data-stu-id="ecc3f-106">Remarks</span></span>

<span data-ttu-id="ecc3f-107">在終結物件之前，請一律呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ecc3f-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="ecc3f-108">基類的函式無法呼叫 **取消認可**，因為該方法會呼叫純虛擬方法 [**CBaseAllocator：： Free**](cbaseallocator-free.md)。</span><span class="sxs-lookup"><span data-stu-id="ecc3f-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="ecc3f-109">衍生類別應該覆寫這個函式並呼叫 **取消認可**。</span><span class="sxs-lookup"><span data-stu-id="ecc3f-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc3f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecc3f-110">Requirements</span></span>



| <span data-ttu-id="ecc3f-111">需求</span><span class="sxs-lookup"><span data-stu-id="ecc3f-111">Requirement</span></span> | <span data-ttu-id="ecc3f-112">值</span><span class="sxs-lookup"><span data-stu-id="ecc3f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc3f-113">標頭</span><span class="sxs-lookup"><span data-stu-id="ecc3f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ecc3f-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ecc3f-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ecc3f-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="ecc3f-115">Library</span></span><br/> | <dl> <span data-ttu-id="ecc3f-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ecc3f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc3f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecc3f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc3f-118">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="ecc3f-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




