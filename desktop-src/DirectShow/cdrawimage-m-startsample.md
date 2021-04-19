---
description: M \_ StartSample 成員變數會指定最新範例的開始時間。
ms.assetid: 2e6d6893-d57b-4009-a6ec-40dc0878d9c4
title: 'CDrawImage：： m_StartSample 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_StartSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fd8039b1d37d0e61a150ed6c6944f0052089b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987906"
---
# <a name="cdrawimagem_startsample-member"></a><span data-ttu-id="02dc4-103">CDrawImage：： m \_ StartSample 成員</span><span class="sxs-lookup"><span data-stu-id="02dc4-103">CDrawImage::m\_StartSample member</span></span>

<span data-ttu-id="02dc4-104">**M \_ StartSample** 成員變數會指定最新範例的開始時間。</span><span class="sxs-lookup"><span data-stu-id="02dc4-104">The **m\_StartSample** member variable specifies the start time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dc4-105">語法</span><span class="sxs-lookup"><span data-stu-id="02dc4-105">Syntax</span></span>


```C++
CRefTime m_StartSample;
```



## <a name="remarks"></a><span data-ttu-id="02dc4-106">備註</span><span class="sxs-lookup"><span data-stu-id="02dc4-106">Remarks</span></span>

<span data-ttu-id="02dc4-107">此值只在 [**CDrawImage：:D isplaysampletimes**](cdrawimage-displaysampletimes.md) 方法內有效。</span><span class="sxs-lookup"><span data-stu-id="02dc4-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02dc4-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="02dc4-108">Requirements</span></span>



| <span data-ttu-id="02dc4-109">需求</span><span class="sxs-lookup"><span data-stu-id="02dc4-109">Requirement</span></span> | <span data-ttu-id="02dc4-110">值</span><span class="sxs-lookup"><span data-stu-id="02dc4-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dc4-111">標頭</span><span class="sxs-lookup"><span data-stu-id="02dc4-111">Header</span></span><br/>  | <dl> <span data-ttu-id="02dc4-112"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="02dc4-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02dc4-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="02dc4-113">Library</span></span><br/> | <dl> <span data-ttu-id="02dc4-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="02dc4-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02dc4-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02dc4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dc4-116">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="02dc4-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




