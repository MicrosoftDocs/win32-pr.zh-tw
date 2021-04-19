---
description: EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: 'CTransInPlaceOutputPin. EnumMediaTypes 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d214004412264272c64d0efaf20a5da7e1ca3cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990560"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="73ff2-104">CTransInPlaceOutputPin. EnumMediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="73ff2-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="73ff2-105">`EnumMediaTypes`方法會列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="73ff2-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="73ff2-106">這個方法會實 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法。</span><span class="sxs-lookup"><span data-stu-id="73ff2-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ff2-107">語法</span><span class="sxs-lookup"><span data-stu-id="73ff2-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="73ff2-108">參數</span><span class="sxs-lookup"><span data-stu-id="73ff2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ff2-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="73ff2-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="73ff2-110">接收 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="73ff2-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ff2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73ff2-111">Return value</span></span>

<span data-ttu-id="73ff2-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="73ff2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="73ff2-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="73ff2-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="73ff2-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="73ff2-114">Return code</span></span>                                                                                           | <span data-ttu-id="73ff2-115">Description</span><span class="sxs-lookup"><span data-stu-id="73ff2-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="73ff2-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="73ff2-117">成功。</span><span class="sxs-lookup"><span data-stu-id="73ff2-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="73ff2-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="73ff2-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="73ff2-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="73ff2-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="73ff2-121">**Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="73ff2-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="73ff2-122"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="73ff2-123">篩選的輸入 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="73ff2-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73ff2-124">備註</span><span class="sxs-lookup"><span data-stu-id="73ff2-124">Remarks</span></span>

<span data-ttu-id="73ff2-125">這個方法會從上游輸出釘選傳回 **IEnumMediaTypes** 介面。</span><span class="sxs-lookup"><span data-stu-id="73ff2-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ff2-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="73ff2-126">Requirements</span></span>



| <span data-ttu-id="73ff2-127">需求</span><span class="sxs-lookup"><span data-stu-id="73ff2-127">Requirement</span></span> | <span data-ttu-id="73ff2-128">值</span><span class="sxs-lookup"><span data-stu-id="73ff2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ff2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="73ff2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="73ff2-130"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73ff2-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="73ff2-131">Library</span></span><br/> | <dl> <span data-ttu-id="73ff2-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="73ff2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ff2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73ff2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ff2-134">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="73ff2-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




