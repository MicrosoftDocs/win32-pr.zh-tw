---
description: 下一個方法會抓取指定的媒體類型數目。 這個方法會實 IEnumMediaTypes：： Next 方法。
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: 'CEnumMediaTypes 下一個方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998886"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="04df4-104">CEnumMediaTypes. Next 方法</span><span class="sxs-lookup"><span data-stu-id="04df4-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="04df4-105">方法會抓取 `Next` 指定的媒體類型數目。</span><span class="sxs-lookup"><span data-stu-id="04df4-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="04df4-106">這個方法會實 [**IEnumMediaTypes：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) 方法。</span><span class="sxs-lookup"><span data-stu-id="04df4-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04df4-107">語法</span><span class="sxs-lookup"><span data-stu-id="04df4-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="04df4-108">參數</span><span class="sxs-lookup"><span data-stu-id="04df4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04df4-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="04df4-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="04df4-110">要取出的媒體類型數目。</span><span class="sxs-lookup"><span data-stu-id="04df4-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="04df4-111">*ppMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="04df4-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="04df4-112">[**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構指標的陣列，大小為 *cPins*。</span><span class="sxs-lookup"><span data-stu-id="04df4-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="04df4-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="04df4-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="04df4-114">變數的指標，此變數會接收此方法所傳回的媒體類型數目。</span><span class="sxs-lookup"><span data-stu-id="04df4-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="04df4-115">如果 *cMediaTypes* 是1，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="04df4-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04df4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="04df4-116">Return value</span></span>

<span data-ttu-id="04df4-117">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="04df4-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="04df4-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="04df4-118">Return code</span></span>                                                                                                | <span data-ttu-id="04df4-119">Description</span><span class="sxs-lookup"><span data-stu-id="04df4-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04df4-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="04df4-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="04df4-121">未依要求抓取任何數量的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="04df4-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="04df4-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="04df4-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="04df4-123">成功。</span><span class="sxs-lookup"><span data-stu-id="04df4-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="04df4-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="04df4-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="04df4-125">無效引數。</span><span class="sxs-lookup"><span data-stu-id="04df4-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="04df4-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="04df4-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="04df4-127">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="04df4-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="04df4-128"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="04df4-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="04df4-129">Pin 的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="04df4-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04df4-130">備註</span><span class="sxs-lookup"><span data-stu-id="04df4-130">Remarks</span></span>

<span data-ttu-id="04df4-131">如果方法成功， *ppMediaTypes* 所指定的陣列就會包含 \_ 媒體 \_ 類型結構的指標。</span><span class="sxs-lookup"><span data-stu-id="04df4-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="04df4-132">結構的數目等於 *\* pcFetched*。</span><span class="sxs-lookup"><span data-stu-id="04df4-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="04df4-133">藉由呼叫 [**DeleteMediaType**](deletemediatype.md) 函式來釋放每個媒體類型。</span><span class="sxs-lookup"><span data-stu-id="04df4-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="04df4-134">這個方法會呼叫釘選的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法，以取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="04df4-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="04df4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="04df4-135">Requirements</span></span>



| <span data-ttu-id="04df4-136">需求</span><span class="sxs-lookup"><span data-stu-id="04df4-136">Requirement</span></span> | <span data-ttu-id="04df4-137">值</span><span class="sxs-lookup"><span data-stu-id="04df4-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04df4-138">標頭</span><span class="sxs-lookup"><span data-stu-id="04df4-138">Header</span></span><br/>  | <dl> <span data-ttu-id="04df4-139"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="04df4-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04df4-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="04df4-140">Library</span></span><br/> | <dl> <span data-ttu-id="04df4-141"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="04df4-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04df4-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04df4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04df4-143">**CEnumMediaTypes 類別**</span><span class="sxs-lookup"><span data-stu-id="04df4-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




