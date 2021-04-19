---
description: 每個緩衝區的對齊方式。 每個緩衝區的位址都必須是此值的偶數倍數。 前置詞必須計算為對齊;請參閱 CBaseAllocator：： m \_ lPrefix。
ms.assetid: 2b71b60a-feeb-4f09-bd56-e126eac8e150
title: 'CBaseAllocator：： m_lAlignment 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lAlignment
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bfdfe7a83a244d5c8cd40a0a4ec747f286c5099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984128"
---
# <a name="cbaseallocatorm_lalignment-member"></a><span data-ttu-id="a030c-105">CBaseAllocator：： m \_ lAlignment 成員</span><span class="sxs-lookup"><span data-stu-id="a030c-105">CBaseAllocator::m\_lAlignment member</span></span>

<span data-ttu-id="a030c-106">每個緩衝區的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="a030c-106">Alignment of each buffer.</span></span> <span data-ttu-id="a030c-107">每個緩衝區的位址都必須是此值的偶數倍數。</span><span class="sxs-lookup"><span data-stu-id="a030c-107">The address of each buffer must be an even multiple of this value.</span></span> <span data-ttu-id="a030c-108">前置詞必須計算為對齊;請參閱 [**CBaseAllocator：： m \_ lPrefix**](cbaseallocator-m-lprefix.md)。</span><span class="sxs-lookup"><span data-stu-id="a030c-108">The prefix must be calculated into the alignment; see [**CBaseAllocator::m\_lPrefix**](cbaseallocator-m-lprefix.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a030c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a030c-109">Syntax</span></span>


```C++
long m_lAlignment;
```



## <a name="requirements"></a><span data-ttu-id="a030c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a030c-110">Requirements</span></span>



| <span data-ttu-id="a030c-111">需求</span><span class="sxs-lookup"><span data-stu-id="a030c-111">Requirement</span></span> | <span data-ttu-id="a030c-112">值</span><span class="sxs-lookup"><span data-stu-id="a030c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a030c-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a030c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a030c-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a030c-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a030c-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="a030c-115">Library</span></span><br/> | <dl> <span data-ttu-id="a030c-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a030c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a030c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a030c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a030c-118">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="a030c-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




