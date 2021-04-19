---
description: 要卸載之 delta 框架的目前最大數目。
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'CVideoTransformFilter：： m_nWaitForKey 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985952"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="575cc-103">CVideoTransformFilter：： m \_ nWaitForKey 成員</span><span class="sxs-lookup"><span data-stu-id="575cc-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="575cc-104">要卸載之 delta 框架的目前最大數目。</span><span class="sxs-lookup"><span data-stu-id="575cc-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="575cc-105">雖然此變數大於零，但是篩選會捨棄框架，直到到達主要畫面格為止。</span><span class="sxs-lookup"><span data-stu-id="575cc-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="575cc-106">針對每個已卸載的框架，篩選器會將此變數遞減一，以防止篩選器卸載過多的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="575cc-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="575cc-107">在沒有主要畫面格的資料列中有30個差異框架之後，篩選器會再次開始傳遞框架。</span><span class="sxs-lookup"><span data-stu-id="575cc-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="575cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="575cc-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="575cc-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="575cc-109">Requirements</span></span>



| <span data-ttu-id="575cc-110">需求</span><span class="sxs-lookup"><span data-stu-id="575cc-110">Requirement</span></span> | <span data-ttu-id="575cc-111">值</span><span class="sxs-lookup"><span data-stu-id="575cc-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="575cc-112">標頭</span><span class="sxs-lookup"><span data-stu-id="575cc-112">Header</span></span><br/>  | <dl> <span data-ttu-id="575cc-113"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="575cc-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="575cc-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="575cc-114">Library</span></span><br/> | <dl> <span data-ttu-id="575cc-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="575cc-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575cc-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="575cc-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575cc-117">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="575cc-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




