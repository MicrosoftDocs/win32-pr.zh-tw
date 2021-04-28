---
description: CBasePin. EnumMediaTypes 方法-EnumMediaTypes 方法會列舉釘選的慣用媒體類型。 這個方法會實 IPin：： EnumMediaTypes 方法。
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: 'CBasePin. EnumMediaTypes 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099386"
---
# <a name="cbasepinenummediatypes-method"></a><span data-ttu-id="f0b07-104">CBasePin. EnumMediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="f0b07-104">CBasePin.EnumMediaTypes method</span></span>

<span data-ttu-id="f0b07-105">`EnumMediaTypes`方法會列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f0b07-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="f0b07-106">這個方法會實 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法。</span><span class="sxs-lookup"><span data-stu-id="f0b07-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b07-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0b07-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="f0b07-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0b07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b07-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="f0b07-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b07-110">接收 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="f0b07-110">Address of a variable that receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0b07-111">Return value</span></span>

<span data-ttu-id="f0b07-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f0b07-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f0b07-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="f0b07-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="f0b07-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f0b07-114">Return code</span></span>                                                                                   | <span data-ttu-id="f0b07-115">Description</span><span class="sxs-lookup"><span data-stu-id="f0b07-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f0b07-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f0b07-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0b07-117">成功。</span><span class="sxs-lookup"><span data-stu-id="f0b07-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f0b07-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f0b07-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0b07-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f0b07-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="f0b07-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f0b07-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0b07-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="f0b07-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0b07-122">備註</span><span class="sxs-lookup"><span data-stu-id="f0b07-122">Remarks</span></span>

<span data-ttu-id="f0b07-123">輸入 pin 不需要列舉任何慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="f0b07-123">Input pins are not required to enumerate any preferred types.</span></span> <span data-ttu-id="f0b07-124">輸出 pin 必須列舉至少一個慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="f0b07-124">Output pins must enumerate at least one preferred type.</span></span> <span data-ttu-id="f0b07-125">否則，這兩個 pin 可能缺乏慣用的類型，因此無法進行連線。</span><span class="sxs-lookup"><span data-stu-id="f0b07-125">Otherwise, both pins could lack a preferred type, making a connection impossible.</span></span>

<span data-ttu-id="f0b07-126">**IEnumMediaTypes** 介面的運作方式就像標準 COM 列舉值一樣。</span><span class="sxs-lookup"><span data-stu-id="f0b07-126">The **IEnumMediaTypes** interface works like a standard COM enumerator.</span></span> <span data-ttu-id="f0b07-127">如需詳細資訊，請參閱 [列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="f0b07-127">For more information, see [Enumerating Objects in a Filter Graph](enumerating-objects-in-a-filter-graph.md).</span></span> <span data-ttu-id="f0b07-128">如果方法成功，則 **IEnumMediaTypes** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="f0b07-128">If the method succeeds, the **IEnumMediaTypes** interface has an outstanding reference count.</span></span> <span data-ttu-id="f0b07-129">當您完成時，請務必放開。</span><span class="sxs-lookup"><span data-stu-id="f0b07-129">Be sure to release it when you are done.</span></span>

<span data-ttu-id="f0b07-130">[**CEnumMediaTypes**](cenummediatypes.md)基底類別會執行 **IEnumMediaTypes**。</span><span class="sxs-lookup"><span data-stu-id="f0b07-130">The [**CEnumMediaTypes**](cenummediatypes.md) base class implements **IEnumMediaTypes**.</span></span> <span data-ttu-id="f0b07-131">它會呼叫釘選的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法來列舉媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f0b07-131">It calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to enumerate the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b07-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0b07-132">Requirements</span></span>



| <span data-ttu-id="f0b07-133">需求</span><span class="sxs-lookup"><span data-stu-id="f0b07-133">Requirement</span></span> | <span data-ttu-id="f0b07-134">值</span><span class="sxs-lookup"><span data-stu-id="f0b07-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b07-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f0b07-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f0b07-136"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f0b07-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0b07-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0b07-137">Library</span></span><br/> | <dl> <span data-ttu-id="f0b07-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f0b07-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b07-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0b07-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b07-140">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="f0b07-140">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




