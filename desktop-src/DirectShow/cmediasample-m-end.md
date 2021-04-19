---
description: 範例結束時間。 只有當 CMediaSample：： m \_ dwFlags 成員變數包含 AM \_ 範例 STOPVALID 旗標時，此值才有效 \_ 。
ms.assetid: 01488984-579b-49e0-923e-bfbeba96b4d8
title: 'CMediaSample：： m_End 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_End
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e103622d69f6e472c368851ce18f2a026bd25e84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977414"
---
# <a name="cmediasamplem_end-member"></a><span data-ttu-id="625a8-104">CMediaSample：： m \_ End 成員</span><span class="sxs-lookup"><span data-stu-id="625a8-104">CMediaSample::m\_End member</span></span>

<span data-ttu-id="625a8-105">範例結束時間。</span><span class="sxs-lookup"><span data-stu-id="625a8-105">Sample end time.</span></span> <span data-ttu-id="625a8-106">只有當 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數包含 AM \_ 範例 STOPVALID 旗標時，此值才有效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="625a8-106">This value is valid only if the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable contains the AM\_SAMPLE\_STOPVALID flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="625a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="625a8-107">Syntax</span></span>


```C++
REFERENCE_TIME m_End;
```



## <a name="requirements"></a><span data-ttu-id="625a8-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="625a8-108">Requirements</span></span>



| <span data-ttu-id="625a8-109">需求</span><span class="sxs-lookup"><span data-stu-id="625a8-109">Requirement</span></span> | <span data-ttu-id="625a8-110">值</span><span class="sxs-lookup"><span data-stu-id="625a8-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="625a8-111">標頭</span><span class="sxs-lookup"><span data-stu-id="625a8-111">Header</span></span><br/>  | <dl> <span data-ttu-id="625a8-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="625a8-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="625a8-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="625a8-113">Library</span></span><br/> | <dl> <span data-ttu-id="625a8-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="625a8-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="625a8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="625a8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="625a8-116">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="625a8-116">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




