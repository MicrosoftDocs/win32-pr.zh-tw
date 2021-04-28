---
description: CMemAllocator. ~ CMemAllocator 的函式-函式方法。
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: 'CMemAllocator. ~ CMemAllocator (Amfilter 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095406"
---
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="fe936-103">CMemAllocator. ~ CMemAllocator 的函式</span><span class="sxs-lookup"><span data-stu-id="fe936-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="fe936-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="fe936-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe936-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe936-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="fe936-106">備註</span><span class="sxs-lookup"><span data-stu-id="fe936-106">Remarks</span></span>

<span data-ttu-id="fe936-107">這個方法會覆寫基類的函式，以呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 和 [**CMemAllocator：： ReallyFree**](cmemallocator-reallyfree.md)。</span><span class="sxs-lookup"><span data-stu-id="fe936-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe936-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe936-108">Requirements</span></span>



| <span data-ttu-id="fe936-109">需求</span><span class="sxs-lookup"><span data-stu-id="fe936-109">Requirement</span></span> | <span data-ttu-id="fe936-110">值</span><span class="sxs-lookup"><span data-stu-id="fe936-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe936-111">標頭</span><span class="sxs-lookup"><span data-stu-id="fe936-111">Header</span></span><br/>  | <dl> <span data-ttu-id="fe936-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fe936-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe936-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe936-113">Library</span></span><br/> | <dl> <span data-ttu-id="fe936-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fe936-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe936-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe936-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe936-116">**CMemAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="fe936-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




