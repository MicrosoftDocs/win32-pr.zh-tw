---
description: 保護篩選狀態的重要區段。 如需詳細資訊，請參閱篩選開發人員的資料流程。
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'CTransformFilter：： m_csFilter 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995411"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="86598-104">CTransformFilter：： m \_ csFilter 成員</span><span class="sxs-lookup"><span data-stu-id="86598-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="86598-105">保護篩選狀態的重要區段。</span><span class="sxs-lookup"><span data-stu-id="86598-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="86598-106">如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="86598-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86598-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86598-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="86598-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="86598-108">Requirements</span></span>



| <span data-ttu-id="86598-109">需求</span><span class="sxs-lookup"><span data-stu-id="86598-109">Requirement</span></span> | <span data-ttu-id="86598-110">值</span><span class="sxs-lookup"><span data-stu-id="86598-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86598-111">標頭</span><span class="sxs-lookup"><span data-stu-id="86598-111">Header</span></span><br/>  | <dl> <span data-ttu-id="86598-112"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="86598-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="86598-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="86598-113">Library</span></span><br/> | <dl> <span data-ttu-id="86598-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="86598-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86598-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86598-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86598-116">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="86598-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




