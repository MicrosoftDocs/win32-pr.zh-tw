---
description: QueryAccept 方法會判斷 pin 是否接受指定的媒體類型。 這個方法會實 IPin：： QueryAccept 方法。
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: 'CBasePin. QueryAccept 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995522"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="d10f6-104">CBasePin. QueryAccept 方法</span><span class="sxs-lookup"><span data-stu-id="d10f6-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="d10f6-105">`QueryAccept`方法會判斷 pin 是否接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d10f6-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="d10f6-106">這個方法會實 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。</span><span class="sxs-lookup"><span data-stu-id="d10f6-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="d10f6-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d10f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d10f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10f6-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="d10f6-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d10f6-110">指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d10f6-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10f6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d10f6-111">Return value</span></span>

<span data-ttu-id="d10f6-112">\_如果媒體類型是可接受的，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="d10f6-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="d10f6-113">否則，會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="d10f6-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d10f6-114">備註</span><span class="sxs-lookup"><span data-stu-id="d10f6-114">Remarks</span></span>

<span data-ttu-id="d10f6-115">在基類中，這個方法會委派給 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d10f6-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="d10f6-116">如果 **CheckMediaType** 失敗，會傳回 `QueryAccept` \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="d10f6-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="d10f6-117">這個方法不會保存釘選的重要區段 ([**CBasePin：： m \_ pLock**](cbasepin-m-plock.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d10f6-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="d10f6-118">如果您的衍生類別動態修改了可接受的媒體類型集，您應該覆寫此方法以保存重要區段。</span><span class="sxs-lookup"><span data-stu-id="d10f6-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10f6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d10f6-119">Requirements</span></span>



| <span data-ttu-id="d10f6-120">需求</span><span class="sxs-lookup"><span data-stu-id="d10f6-120">Requirement</span></span> | <span data-ttu-id="d10f6-121">值</span><span class="sxs-lookup"><span data-stu-id="d10f6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10f6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d10f6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d10f6-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d10f6-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d10f6-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d10f6-124">Library</span></span><br/> | <dl> <span data-ttu-id="d10f6-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d10f6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10f6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d10f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10f6-127">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d10f6-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




