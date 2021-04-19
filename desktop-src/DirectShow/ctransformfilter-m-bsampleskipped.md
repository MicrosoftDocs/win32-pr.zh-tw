---
description: 指出最近樣本是否已卸載的旗標。 如果接收方法卸載範例，則會將值設定為 TRUE。
ms.assetid: 6143f948-75b0-47c6-9951-4c18c0773857
title: 'CTransformFilter：： m_bSampleSkipped 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSampleSkipped
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61d8ceda20fed4c8ec89538cbe9675ad1f3e4549
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001135"
---
# <a name="ctransformfilterm_bsampleskipped-member"></a><span data-ttu-id="a390b-104">CTransformFilter：： m \_ bSampleSkipped 成員</span><span class="sxs-lookup"><span data-stu-id="a390b-104">CTransformFilter::m\_bSampleSkipped member</span></span>

<span data-ttu-id="a390b-105">指出最近樣本是否已卸載的旗標。</span><span class="sxs-lookup"><span data-stu-id="a390b-105">Flag that indicates whether the most recent sample was dropped.</span></span> <span data-ttu-id="a390b-106">如果 [**接收**](ctransformfilter-receive.md) 方法卸載範例，則會將值設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a390b-106">If the [**Receive**](ctransformfilter-receive.md) method drops a sample, it sets the value to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a390b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a390b-107">Syntax</span></span>


```C++
BOOL m_bSampleSkipped;
```



## <a name="requirements"></a><span data-ttu-id="a390b-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="a390b-108">Requirements</span></span>



| <span data-ttu-id="a390b-109">需求</span><span class="sxs-lookup"><span data-stu-id="a390b-109">Requirement</span></span> | <span data-ttu-id="a390b-110">值</span><span class="sxs-lookup"><span data-stu-id="a390b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a390b-111">標頭</span><span class="sxs-lookup"><span data-stu-id="a390b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a390b-112"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a390b-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a390b-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="a390b-113">Library</span></span><br/> | <dl> <span data-ttu-id="a390b-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a390b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a390b-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a390b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a390b-116">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="a390b-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




