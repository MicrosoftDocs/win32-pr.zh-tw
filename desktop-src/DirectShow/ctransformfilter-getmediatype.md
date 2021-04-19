---
description: GetMediaType 方法會抓取輸出圖釘的慣用媒體類型。
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: 'CTransformFilter. GetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991155"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="cd94f-103">CTransformFilter. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="cd94f-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="cd94f-104">方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cd94f-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd94f-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd94f-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="cd94f-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd94f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd94f-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="cd94f-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="cd94f-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="cd94f-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="cd94f-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="cd94f-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="cd94f-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="cd94f-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd94f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd94f-111">Return value</span></span>

<span data-ttu-id="cd94f-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cd94f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cd94f-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="cd94f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cd94f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cd94f-114">Return code</span></span>                                                                                            | <span data-ttu-id="cd94f-115">Description</span><span class="sxs-lookup"><span data-stu-id="cd94f-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cd94f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cd94f-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="cd94f-117">成功。</span><span class="sxs-lookup"><span data-stu-id="cd94f-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="cd94f-118"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="cd94f-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="cd94f-119">索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="cd94f-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="cd94f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cd94f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="cd94f-121">索引小於零。</span><span class="sxs-lookup"><span data-stu-id="cd94f-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd94f-122">備註</span><span class="sxs-lookup"><span data-stu-id="cd94f-122">Remarks</span></span>

<span data-ttu-id="cd94f-123">輸出釘選的 [**CTransformOutputPin：： GetMediaType**](ctransformoutputpin-getmediatype.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="cd94f-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="cd94f-124">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="cd94f-124">The derived class must implement this method.</span></span> <span data-ttu-id="cd94f-125">如需詳細資訊，請參閱 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="cd94f-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd94f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd94f-126">Requirements</span></span>



| <span data-ttu-id="cd94f-127">需求</span><span class="sxs-lookup"><span data-stu-id="cd94f-127">Requirement</span></span> | <span data-ttu-id="cd94f-128">值</span><span class="sxs-lookup"><span data-stu-id="cd94f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd94f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="cd94f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cd94f-130"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cd94f-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd94f-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd94f-131">Library</span></span><br/> | <dl> <span data-ttu-id="cd94f-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cd94f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd94f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd94f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd94f-134">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="cd94f-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




