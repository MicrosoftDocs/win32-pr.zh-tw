---
description: 保護串流狀態的重要區段。 如需詳細資訊，請參閱篩選開發人員的資料流程。
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'CTransformFilter：： m_csReceive 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995410"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="e05c5-104">CTransformFilter：： m \_ csReceive 成員</span><span class="sxs-lookup"><span data-stu-id="e05c5-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="e05c5-105">保護串流狀態的重要區段。</span><span class="sxs-lookup"><span data-stu-id="e05c5-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="e05c5-106">如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="e05c5-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e05c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e05c5-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="e05c5-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="e05c5-108">Requirements</span></span>



| <span data-ttu-id="e05c5-109">需求</span><span class="sxs-lookup"><span data-stu-id="e05c5-109">Requirement</span></span> | <span data-ttu-id="e05c5-110">值</span><span class="sxs-lookup"><span data-stu-id="e05c5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05c5-111">標頭</span><span class="sxs-lookup"><span data-stu-id="e05c5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e05c5-112"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e05c5-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e05c5-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="e05c5-113">Library</span></span><br/> | <dl> <span data-ttu-id="e05c5-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e05c5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e05c5-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e05c5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05c5-116">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e05c5-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




