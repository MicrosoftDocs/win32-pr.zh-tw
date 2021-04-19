---
description: GetMediaType 方法會依索引值抓取慣用的媒體類型。
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: 'CBasePin. GetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987981"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="ea498-103">CBasePin. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="ea498-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="ea498-104">`GetMediaType`方法會依索引值抓取慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ea498-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea498-105">語法</span><span class="sxs-lookup"><span data-stu-id="ea498-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ea498-106">參數</span><span class="sxs-lookup"><span data-stu-id="ea498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea498-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="ea498-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="ea498-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="ea498-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="ea498-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="ea498-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="ea498-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ea498-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea498-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea498-111">Return value</span></span>

<span data-ttu-id="ea498-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ea498-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ea498-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="ea498-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="ea498-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea498-114">Return code</span></span>                                                                                            | <span data-ttu-id="ea498-115">Description</span><span class="sxs-lookup"><span data-stu-id="ea498-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ea498-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea498-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ea498-117">成功。</span><span class="sxs-lookup"><span data-stu-id="ea498-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="ea498-118"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="ea498-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="ea498-119">索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="ea498-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="ea498-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea498-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="ea498-121">索引小於零。</span><span class="sxs-lookup"><span data-stu-id="ea498-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="ea498-122"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="ea498-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="ea498-123">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea498-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ea498-124">備註</span><span class="sxs-lookup"><span data-stu-id="ea498-124">Remarks</span></span>

<span data-ttu-id="ea498-125">從 pin 的慣用媒體類型清單中，此方法會傳回索引值為 *ipositionsummaryview* 的類型。</span><span class="sxs-lookup"><span data-stu-id="ea498-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="ea498-126">[**CEnumMediaTypes**](cenummediatypes.md)類別會呼叫這個方法來列舉慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ea498-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="ea498-127">基類傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="ea498-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="ea498-128">在您的衍生類別中覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ea498-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea498-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea498-129">Requirements</span></span>



| <span data-ttu-id="ea498-130">需求</span><span class="sxs-lookup"><span data-stu-id="ea498-130">Requirement</span></span> | <span data-ttu-id="ea498-131">值</span><span class="sxs-lookup"><span data-stu-id="ea498-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea498-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ea498-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ea498-133"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ea498-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea498-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea498-134">Library</span></span><br/> | <dl> <span data-ttu-id="ea498-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ea498-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea498-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea498-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea498-137">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="ea498-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




