---
description: 要提供的緩衝區數目。
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'CBaseAllocator：： m_lCount 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989881"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="4abd5-103">CBaseAllocator：： m \_ lCount 成員</span><span class="sxs-lookup"><span data-stu-id="4abd5-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="4abd5-104">要提供的緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="4abd5-104">Number of buffers to provide.</span></span> <span data-ttu-id="4abd5-105">[**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md)方法會設定此值。</span><span class="sxs-lookup"><span data-stu-id="4abd5-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="4abd5-106">在呼叫 [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法之前，不會配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4abd5-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="4abd5-107">目前已配置的緩衝區數是由 [**CBaseAllocator：： m \_ lAllocated**](cbaseallocator-m-lallocated.md) 成員變數所指定。</span><span class="sxs-lookup"><span data-stu-id="4abd5-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abd5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4abd5-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="4abd5-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="4abd5-109">Requirements</span></span>



| <span data-ttu-id="4abd5-110">需求</span><span class="sxs-lookup"><span data-stu-id="4abd5-110">Requirement</span></span> | <span data-ttu-id="4abd5-111">值</span><span class="sxs-lookup"><span data-stu-id="4abd5-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abd5-112">標頭</span><span class="sxs-lookup"><span data-stu-id="4abd5-112">Header</span></span><br/>  | <dl> <span data-ttu-id="4abd5-113"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4abd5-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4abd5-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="4abd5-114">Library</span></span><br/> | <dl> <span data-ttu-id="4abd5-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4abd5-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4abd5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4abd5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abd5-117">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="4abd5-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




