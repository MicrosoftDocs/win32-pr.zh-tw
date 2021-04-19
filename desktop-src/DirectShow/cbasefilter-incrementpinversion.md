---
description: IncremementPinVersion 方法會在一組 pin 上遞增版本號碼。
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: 'CBaseFilter. IncrementPinVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993608"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="123e9-103">CBaseFilter. IncrementPinVersion 方法</span><span class="sxs-lookup"><span data-stu-id="123e9-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="123e9-104">`IncremementPinVersion`方法會在一組 pin 上遞增版本號碼。</span><span class="sxs-lookup"><span data-stu-id="123e9-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="123e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="123e9-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="123e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="123e9-106">Parameters</span></span>

<span data-ttu-id="123e9-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="123e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="123e9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="123e9-108">Return value</span></span>

<span data-ttu-id="123e9-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="123e9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="123e9-110">備註</span><span class="sxs-lookup"><span data-stu-id="123e9-110">Remarks</span></span>

<span data-ttu-id="123e9-111">這個方法會遞增 [**CBaseFilter：： m \_ PinVersion**](cbasefilter-m-pinversion.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="123e9-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="123e9-112">如果篩選動態建立或終結 pin，請在 pin 變更時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="123e9-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="123e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="123e9-113">Requirements</span></span>



| <span data-ttu-id="123e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="123e9-114">Requirement</span></span> | <span data-ttu-id="123e9-115">值</span><span class="sxs-lookup"><span data-stu-id="123e9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123e9-116">標頭</span><span class="sxs-lookup"><span data-stu-id="123e9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="123e9-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="123e9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="123e9-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="123e9-118">Library</span></span><br/> | <dl> <span data-ttu-id="123e9-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="123e9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123e9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="123e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123e9-121">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="123e9-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="123e9-122">**CBaseFilter::GetPinVersion**</span><span class="sxs-lookup"><span data-stu-id="123e9-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




