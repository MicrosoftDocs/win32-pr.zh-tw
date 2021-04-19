---
description: InputPin 方法會抓取篩選的輸入圖釘指標。
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: 'CTransInPlaceFilter. InputPin 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000729"
---
# <a name="ctransinplacefilterinputpin-method"></a><span data-ttu-id="dd5d3-103">CTransInPlaceFilter. InputPin 方法</span><span class="sxs-lookup"><span data-stu-id="dd5d3-103">CTransInPlaceFilter.InputPin method</span></span>

<span data-ttu-id="dd5d3-104">方法會抓取 `InputPin` 篩選的輸入圖釘指標。</span><span class="sxs-lookup"><span data-stu-id="dd5d3-104">The `InputPin` method retrieves a pointer to the filter's input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd5d3-105">Syntax</span></span>


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a><span data-ttu-id="dd5d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd5d3-106">Parameters</span></span>

<span data-ttu-id="dd5d3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dd5d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd5d3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd5d3-108">Return value</span></span>

<span data-ttu-id="dd5d3-109">傳回 [**CTransformFilter：： m \_ pInput**](ctransformfilter-m-pinput.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="dd5d3-109">Returns the [**CTransformFilter::m\_pInput**](ctransformfilter-m-pinput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5d3-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd5d3-110">Requirements</span></span>



| <span data-ttu-id="dd5d3-111">需求</span><span class="sxs-lookup"><span data-stu-id="dd5d3-111">Requirement</span></span> | <span data-ttu-id="dd5d3-112">值</span><span class="sxs-lookup"><span data-stu-id="dd5d3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5d3-113">標頭</span><span class="sxs-lookup"><span data-stu-id="dd5d3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="dd5d3-114"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dd5d3-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd5d3-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd5d3-115">Library</span></span><br/> | <dl> <span data-ttu-id="dd5d3-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dd5d3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5d3-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd5d3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5d3-118">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="dd5d3-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




