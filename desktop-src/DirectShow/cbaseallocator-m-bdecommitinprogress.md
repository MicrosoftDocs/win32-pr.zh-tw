---
description: 旗標，指出取消認可作業是否正在進行中。
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'CBaseAllocator：： m_bDecommitInProgress 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978642"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="2bb98-103">CBaseAllocator：： m \_ bDecommitInProgress 成員</span><span class="sxs-lookup"><span data-stu-id="2bb98-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="2bb98-104">旗標，指出取消認可作業是否正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2bb98-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="2bb98-105">在呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md)方法之後，但在釋放所有緩衝區之前，此值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="2bb98-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="2bb98-106">如果值為 **TRUE**， [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2bb98-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="2bb98-107">此外，在值為 **TRUE** 時，配置器不應該刪除本身。</span><span class="sxs-lookup"><span data-stu-id="2bb98-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb98-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="2bb98-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bb98-109">Requirements</span></span>



| <span data-ttu-id="2bb98-110">需求</span><span class="sxs-lookup"><span data-stu-id="2bb98-110">Requirement</span></span> | <span data-ttu-id="2bb98-111">值</span><span class="sxs-lookup"><span data-stu-id="2bb98-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb98-112">標頭</span><span class="sxs-lookup"><span data-stu-id="2bb98-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2bb98-113"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2bb98-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2bb98-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="2bb98-114">Library</span></span><br/> | <dl> <span data-ttu-id="2bb98-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2bb98-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb98-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bb98-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb98-117">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="2bb98-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




