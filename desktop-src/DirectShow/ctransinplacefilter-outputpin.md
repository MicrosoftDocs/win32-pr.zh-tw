---
description: OutputPin 方法會抓取篩選的輸出圖釘指標。
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: 'CTransInPlaceFilter. OutputPin 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001573"
---
# <a name="ctransinplacefilteroutputpin-method"></a><span data-ttu-id="fe282-103">CTransInPlaceFilter. OutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="fe282-103">CTransInPlaceFilter.OutputPin method</span></span>

<span data-ttu-id="fe282-104">方法會抓取 `OutputPin` 篩選的輸出圖釘指標。</span><span class="sxs-lookup"><span data-stu-id="fe282-104">The `OutputPin` method retrieves a pointer to the filter's output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe282-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe282-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a><span data-ttu-id="fe282-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe282-106">Parameters</span></span>

<span data-ttu-id="fe282-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fe282-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe282-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe282-108">Return value</span></span>

<span data-ttu-id="fe282-109">傳回 [**CTransformFilter：： m \_ pOutput**](ctransformfilter-m-poutput.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="fe282-109">Returns the [**CTransformFilter::m\_pOutput**](ctransformfilter-m-poutput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe282-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe282-110">Requirements</span></span>



| <span data-ttu-id="fe282-111">需求</span><span class="sxs-lookup"><span data-stu-id="fe282-111">Requirement</span></span> | <span data-ttu-id="fe282-112">值</span><span class="sxs-lookup"><span data-stu-id="fe282-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe282-113">標頭</span><span class="sxs-lookup"><span data-stu-id="fe282-113">Header</span></span><br/>  | <dl> <span data-ttu-id="fe282-114"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fe282-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe282-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe282-115">Library</span></span><br/> | <dl> <span data-ttu-id="fe282-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fe282-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe282-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe282-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe282-118">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="fe282-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




