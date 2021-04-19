---
description: IncrementTypeVersion 方法會遞增一組慣用媒體類型的版本號碼。
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: 'CBasePin. IncrementTypeVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978494"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="b3a4d-103">CBasePin. IncrementTypeVersion 方法</span><span class="sxs-lookup"><span data-stu-id="b3a4d-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="b3a4d-104">`IncrementTypeVersion`方法會遞增一組慣用媒體類型的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a4d-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3a4d-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="b3a4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3a4d-106">Parameters</span></span>

<span data-ttu-id="b3a4d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3a4d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3a4d-108">Return value</span></span>

<span data-ttu-id="b3a4d-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3a4d-110">備註</span><span class="sxs-lookup"><span data-stu-id="b3a4d-110">Remarks</span></span>

<span data-ttu-id="b3a4d-111">這個方法會遞增 [**CBasePin：： m \_ TypeVersion**](cbasepin-m-typeversion.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="b3a4d-112">如果 pin 會動態變更慣用媒體類型的清單，則每當清單變更時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="b3a4d-113">如需詳細資訊，請參閱 [**CBasePin：： GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)。</span><span class="sxs-lookup"><span data-stu-id="b3a4d-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a4d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3a4d-114">Requirements</span></span>



| <span data-ttu-id="b3a4d-115">需求</span><span class="sxs-lookup"><span data-stu-id="b3a4d-115">Requirement</span></span> | <span data-ttu-id="b3a4d-116">值</span><span class="sxs-lookup"><span data-stu-id="b3a4d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a4d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b3a4d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b3a4d-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b3a4d-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3a4d-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3a4d-119">Library</span></span><br/> | <dl> <span data-ttu-id="b3a4d-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b3a4d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a4d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3a4d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a4d-122">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="b3a4d-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




