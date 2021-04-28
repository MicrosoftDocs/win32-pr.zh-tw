---
description: CTransInPlaceInputPin. EnumMediaTypes 方法-EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: 'CTransInPlaceInputPin. EnumMediaTypes 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094756"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="9a387-104">CTransInPlaceInputPin. EnumMediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="9a387-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="9a387-105">`EnumMediaTypes`方法會列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9a387-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="9a387-106">這個方法會實 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法。</span><span class="sxs-lookup"><span data-stu-id="9a387-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a387-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a387-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9a387-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a387-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="9a387-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="9a387-110">接收 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9a387-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a387-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a387-111">Return value</span></span>

<span data-ttu-id="9a387-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="9a387-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9a387-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="9a387-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9a387-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a387-114">Return code</span></span>                                                                                           | <span data-ttu-id="9a387-115">Description</span><span class="sxs-lookup"><span data-stu-id="9a387-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="9a387-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a387-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9a387-117">成功。</span><span class="sxs-lookup"><span data-stu-id="9a387-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="9a387-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a387-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="9a387-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="9a387-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="9a387-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="9a387-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="9a387-121">**Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="9a387-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="9a387-122"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="9a387-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9a387-123">輸出針腳未連接。</span><span class="sxs-lookup"><span data-stu-id="9a387-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a387-124">備註</span><span class="sxs-lookup"><span data-stu-id="9a387-124">Remarks</span></span>

<span data-ttu-id="9a387-125">這個方法會從下游輸入 pin 傳回 **IEnumMediaTypes** 介面。</span><span class="sxs-lookup"><span data-stu-id="9a387-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a387-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a387-126">Requirements</span></span>



| <span data-ttu-id="9a387-127">需求</span><span class="sxs-lookup"><span data-stu-id="9a387-127">Requirement</span></span> | <span data-ttu-id="9a387-128">值</span><span class="sxs-lookup"><span data-stu-id="9a387-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a387-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9a387-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9a387-130"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9a387-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a387-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a387-131">Library</span></span><br/> | <dl> <span data-ttu-id="9a387-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9a387-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a387-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a387-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a387-134">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9a387-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




