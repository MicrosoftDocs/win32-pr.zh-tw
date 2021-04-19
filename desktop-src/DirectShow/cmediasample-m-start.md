---
description: 範例開始時間。 只有當 CMediaSample：： m \_ dwFlags 成員變數包含 AM \_ 範例 TIMEVALID 旗標時，此值才有效 \_ 。
ms.assetid: 31af979b-4c10-4f15-aa8a-90807b5cc156
title: 'CMediaSample：： m_Start 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_Start
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c8be533c28a2b8a166d87d1751682cf6b09329b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990522"
---
# <a name="cmediasamplem_start-member"></a><span data-ttu-id="39dd1-104">CMediaSample：： m \_ Start 成員</span><span class="sxs-lookup"><span data-stu-id="39dd1-104">CMediaSample::m\_Start member</span></span>

<span data-ttu-id="39dd1-105">範例開始時間。</span><span class="sxs-lookup"><span data-stu-id="39dd1-105">Sample start time.</span></span> <span data-ttu-id="39dd1-106">只有當 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數包含 AM \_ 範例 TIMEVALID 旗標時，此值才有效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="39dd1-106">This value is valid only if the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable contains the AM\_SAMPLE\_TIMEVALID flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dd1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39dd1-107">Syntax</span></span>


```C++
REFERENCE_TIME m_Start;
```



## <a name="requirements"></a><span data-ttu-id="39dd1-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="39dd1-108">Requirements</span></span>



| <span data-ttu-id="39dd1-109">需求</span><span class="sxs-lookup"><span data-stu-id="39dd1-109">Requirement</span></span> | <span data-ttu-id="39dd1-110">值</span><span class="sxs-lookup"><span data-stu-id="39dd1-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39dd1-111">標頭</span><span class="sxs-lookup"><span data-stu-id="39dd1-111">Header</span></span><br/>  | <dl> <span data-ttu-id="39dd1-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="39dd1-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39dd1-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="39dd1-113">Library</span></span><br/> | <dl> <span data-ttu-id="39dd1-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="39dd1-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39dd1-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39dd1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39dd1-116">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="39dd1-116">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




