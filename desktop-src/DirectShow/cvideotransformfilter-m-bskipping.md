---
description: 指出篩選目前是否正在卸載框架的布林值。 如果這個值為 TRUE，則篩選會繼續卸載框架，直到到達下一個主要畫面格，或直到它在沒有主要畫面格的資料列中收到30個差異框架為止。
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'CVideoTransformFilter：： m_bSkipping 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995949"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="d8c95-104">CVideoTransformFilter：： m \_ bSkipping 成員</span><span class="sxs-lookup"><span data-stu-id="d8c95-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="d8c95-105">指出篩選目前是否正在卸載框架的布林值。</span><span class="sxs-lookup"><span data-stu-id="d8c95-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="d8c95-106">如果這個值為 **TRUE**，則篩選會繼續卸載框架，直到到達下一個主要畫面格，或直到它在沒有主要畫面格的資料列中收到30個差異框架為止。</span><span class="sxs-lookup"><span data-stu-id="d8c95-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c95-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8c95-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="d8c95-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8c95-108">Requirements</span></span>



| <span data-ttu-id="d8c95-109">需求</span><span class="sxs-lookup"><span data-stu-id="d8c95-109">Requirement</span></span> | <span data-ttu-id="d8c95-110">值</span><span class="sxs-lookup"><span data-stu-id="d8c95-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c95-111">標頭</span><span class="sxs-lookup"><span data-stu-id="d8c95-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c95-112"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d8c95-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d8c95-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8c95-113">Library</span></span><br/> | <dl> <span data-ttu-id="d8c95-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8c95-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c95-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8c95-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c95-116">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="d8c95-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




