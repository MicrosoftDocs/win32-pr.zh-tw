---
description: 保護篩選狀態的重要區段物件的指標。
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'CBasePin：： m_pLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000926"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="e1ec1-103">CBasePin：： m \_ pLock 成員</span><span class="sxs-lookup"><span data-stu-id="e1ec1-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="e1ec1-104">保護篩選狀態的重要區段物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e1ec1-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ec1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ec1-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="e1ec1-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1ec1-106">Requirements</span></span>



| <span data-ttu-id="e1ec1-107">需求</span><span class="sxs-lookup"><span data-stu-id="e1ec1-107">Requirement</span></span> | <span data-ttu-id="e1ec1-108">值</span><span class="sxs-lookup"><span data-stu-id="e1ec1-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ec1-109">標頭</span><span class="sxs-lookup"><span data-stu-id="e1ec1-109">Header</span></span><br/>  | <dl> <span data-ttu-id="e1ec1-110"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e1ec1-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1ec1-111">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1ec1-111">Library</span></span><br/> | <dl> <span data-ttu-id="e1ec1-112"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e1ec1-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ec1-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1ec1-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ec1-114">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="e1ec1-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="e1ec1-115">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="e1ec1-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




