---
description: 指出緩衝區需求是否已變更的旗標。
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'CBaseAllocator：： m_bChanged 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999668"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="d15c1-103">CBaseAllocator：： m \_ bChanged 成員</span><span class="sxs-lookup"><span data-stu-id="d15c1-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="d15c1-104">指出緩衝區需求是否已變更的旗標。</span><span class="sxs-lookup"><span data-stu-id="d15c1-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="d15c1-105">[**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md)方法會將值設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d15c1-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="d15c1-106">在衍生類別中，純虛擬方法 [**CBaseAllocator：：**](cbaseallocator-alloc.md) 配置應將值設回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d15c1-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="d15c1-107">一旦配置了緩衝區，就不需要重新配置它們，而 *m \_ BChanged* 為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d15c1-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d15c1-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="d15c1-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="d15c1-109">Requirements</span></span>



| <span data-ttu-id="d15c1-110">需求</span><span class="sxs-lookup"><span data-stu-id="d15c1-110">Requirement</span></span> | <span data-ttu-id="d15c1-111">值</span><span class="sxs-lookup"><span data-stu-id="d15c1-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d15c1-112">標頭</span><span class="sxs-lookup"><span data-stu-id="d15c1-112">Header</span></span><br/>  | <dl> <span data-ttu-id="d15c1-113"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d15c1-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d15c1-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="d15c1-114">Library</span></span><br/> | <dl> <span data-ttu-id="d15c1-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d15c1-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d15c1-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d15c1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15c1-117">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="d15c1-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




