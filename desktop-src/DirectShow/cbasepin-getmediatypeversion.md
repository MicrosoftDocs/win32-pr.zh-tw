---
description: GetMediaTypeVersion 方法會抓取慣用媒體類型集的版本號碼。
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: 'CBasePin. GetMediaTypeVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999539"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="8f2d3-103">CBasePin. GetMediaTypeVersion 方法</span><span class="sxs-lookup"><span data-stu-id="8f2d3-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="8f2d3-104">方法會抓取一 `GetMediaTypeVersion` 組慣用媒體類型的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f2d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f2d3-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="8f2d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f2d3-106">Parameters</span></span>

<span data-ttu-id="8f2d3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f2d3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f2d3-108">Return value</span></span>

<span data-ttu-id="8f2d3-109">傳回 [**CBasePin：： m \_ TypeVersion**](cbasepin-m-typeversion.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f2d3-110">備註</span><span class="sxs-lookup"><span data-stu-id="8f2d3-110">Remarks</span></span>

<span data-ttu-id="8f2d3-111">**CBasePin** 函式會將版本號碼初始化為1。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="8f2d3-112">在基類中，此數位永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-112">In the base class, this number never changes.</span></span> <span data-ttu-id="8f2d3-113">如果 pin 會動態變更其慣用媒體類型的清單，則每當清單變更時，就應該遞增版本號碼。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="8f2d3-114">若要遞增版本號碼，請呼叫 [**CBasePin：： IncrementTypeVersion**](cbasepin-incrementtypeversion.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="8f2d3-115">由 [**CEnumMediaTypes**](cenummediatypes.md) 類別所執行的媒體類型列舉值會使用版本號碼，使其本身與釘選同步。</span><span class="sxs-lookup"><span data-stu-id="8f2d3-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2d3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f2d3-116">Requirements</span></span>



| <span data-ttu-id="8f2d3-117">需求</span><span class="sxs-lookup"><span data-stu-id="8f2d3-117">Requirement</span></span> | <span data-ttu-id="8f2d3-118">值</span><span class="sxs-lookup"><span data-stu-id="8f2d3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2d3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8f2d3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8f2d3-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8f2d3-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f2d3-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f2d3-121">Library</span></span><br/> | <dl> <span data-ttu-id="8f2d3-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8f2d3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f2d3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f2d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2d3-124">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="8f2d3-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




