---
description: M \_ EndSample 成員變數會指定最新範例的停止時間。
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'CDrawImage：： m_EndSample 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977750"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="f4876-103">CDrawImage：： m \_ EndSample 成員</span><span class="sxs-lookup"><span data-stu-id="f4876-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="f4876-104">`m_EndSample`成員變數會指定最新範例的停止時間。</span><span class="sxs-lookup"><span data-stu-id="f4876-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4876-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4876-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="f4876-106">備註</span><span class="sxs-lookup"><span data-stu-id="f4876-106">Remarks</span></span>

<span data-ttu-id="f4876-107">此值只在 [**CDrawImage：:D isplaysampletimes**](cdrawimage-displaysampletimes.md) 方法內有效。</span><span class="sxs-lookup"><span data-stu-id="f4876-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4876-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4876-108">Requirements</span></span>



| <span data-ttu-id="f4876-109">需求</span><span class="sxs-lookup"><span data-stu-id="f4876-109">Requirement</span></span> | <span data-ttu-id="f4876-110">值</span><span class="sxs-lookup"><span data-stu-id="f4876-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4876-111">標頭</span><span class="sxs-lookup"><span data-stu-id="f4876-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f4876-112"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f4876-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4876-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="f4876-113">Library</span></span><br/> | <dl> <span data-ttu-id="f4876-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f4876-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4876-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4876-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4876-116">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="f4876-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




