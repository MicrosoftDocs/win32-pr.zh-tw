---
description: M \_ bUsingImageAllocator 成員變數會指出釘選連接的配置器是否為 CImageAllocator 物件。 如果該值為 TRUE，則配置器是 CImageAllocator 物件 (或衍生自該類別) 。
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'CDrawImage：： m_bUsingImageAllocator 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994795"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="2831b-104">CDrawImage：： m \_ bUsingImageAllocator 成員</span><span class="sxs-lookup"><span data-stu-id="2831b-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="2831b-105">`m_bUsingImageAllocator`成員變數會指出釘選連接的配置器是否為 **CImageAllocator** 物件。</span><span class="sxs-lookup"><span data-stu-id="2831b-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="2831b-106">如果該值為 **TRUE**，則配置器是 **CImageAllocator** 物件 (或衍生自該類別) 。</span><span class="sxs-lookup"><span data-stu-id="2831b-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="2831b-107">語法</span><span class="sxs-lookup"><span data-stu-id="2831b-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="2831b-108">備註</span><span class="sxs-lookup"><span data-stu-id="2831b-108">Remarks</span></span>

<span data-ttu-id="2831b-109">當此值為 **TRUE** 時， **CDrawImage** 物件可以使用 GDI **BitBlt** 和 **StretchBlt** 函式來轉譯影像，而不是使用較慢的 **SetDIBitsToDevice** 和 **StretchDIBits** 函數。</span><span class="sxs-lookup"><span data-stu-id="2831b-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2831b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2831b-110">Requirements</span></span>



| <span data-ttu-id="2831b-111">需求</span><span class="sxs-lookup"><span data-stu-id="2831b-111">Requirement</span></span> | <span data-ttu-id="2831b-112">值</span><span class="sxs-lookup"><span data-stu-id="2831b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2831b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="2831b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2831b-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2831b-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2831b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="2831b-115">Library</span></span><br/> | <dl> <span data-ttu-id="2831b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2831b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2831b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2831b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2831b-118">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="2831b-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="2831b-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="2831b-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="2831b-120">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="2831b-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




