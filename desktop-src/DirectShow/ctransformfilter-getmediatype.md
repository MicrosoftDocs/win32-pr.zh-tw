---
description: CTransformFilter. GetMediaType 方法-GetMediaType 方法會針對輸出釘選慣用的媒體類型。
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
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095116"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="6fa81-103">CTransformFilter. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="6fa81-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="6fa81-104">方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6fa81-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa81-105">語法</span><span class="sxs-lookup"><span data-stu-id="6fa81-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6fa81-106">參數</span><span class="sxs-lookup"><span data-stu-id="6fa81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa81-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="6fa81-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa81-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="6fa81-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="6fa81-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="6fa81-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa81-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6fa81-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa81-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fa81-111">Return value</span></span>

<span data-ttu-id="6fa81-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6fa81-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6fa81-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="6fa81-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6fa81-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6fa81-114">Return code</span></span>                                                                                            | <span data-ttu-id="6fa81-115">Description</span><span class="sxs-lookup"><span data-stu-id="6fa81-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6fa81-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa81-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6fa81-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6fa81-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="6fa81-118"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa81-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="6fa81-119">索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="6fa81-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="6fa81-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa81-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="6fa81-121">索引小於零。</span><span class="sxs-lookup"><span data-stu-id="6fa81-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6fa81-122">備註</span><span class="sxs-lookup"><span data-stu-id="6fa81-122">Remarks</span></span>

<span data-ttu-id="6fa81-123">輸出釘選的 [**CTransformOutputPin：： GetMediaType**](ctransformoutputpin-getmediatype.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6fa81-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="6fa81-124">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="6fa81-124">The derived class must implement this method.</span></span> <span data-ttu-id="6fa81-125">如需詳細資訊，請參閱 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="6fa81-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa81-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fa81-126">Requirements</span></span>



| <span data-ttu-id="6fa81-127">需求</span><span class="sxs-lookup"><span data-stu-id="6fa81-127">Requirement</span></span> | <span data-ttu-id="6fa81-128">值</span><span class="sxs-lookup"><span data-stu-id="6fa81-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa81-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6fa81-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6fa81-130"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6fa81-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6fa81-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="6fa81-131">Library</span></span><br/> | <dl> <span data-ttu-id="6fa81-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6fa81-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa81-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fa81-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa81-134">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="6fa81-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




