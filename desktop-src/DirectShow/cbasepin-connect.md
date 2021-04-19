---
description: Connect 方法會將 pin 連接到另一個 pin。 這個方法會實 IPin：： Connect 方法。
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: 'CBasePin 連接方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995499"
---
# <a name="cbasepinconnect-method"></a><span data-ttu-id="23a11-104">CBasePin 方法</span><span class="sxs-lookup"><span data-stu-id="23a11-104">CBasePin.Connect method</span></span>

<span data-ttu-id="23a11-105">方法會將 `Connect` 釘選連接到另一個 pin。</span><span class="sxs-lookup"><span data-stu-id="23a11-105">The `Connect` method connects the pin to another pin.</span></span> <span data-ttu-id="23a11-106">這個方法會實 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法。</span><span class="sxs-lookup"><span data-stu-id="23a11-106">This method implements the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a11-107">語法</span><span class="sxs-lookup"><span data-stu-id="23a11-107">Syntax</span></span>


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="23a11-108">參數</span><span class="sxs-lookup"><span data-stu-id="23a11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a11-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="23a11-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="23a11-110">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="23a11-110">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="23a11-111">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="23a11-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="23a11-112">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標，指定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="23a11-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type for the connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a11-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="23a11-113">Return value</span></span>

<span data-ttu-id="23a11-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="23a11-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="23a11-115">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="23a11-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="23a11-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="23a11-116">Return code</span></span>                                                                                                  | <span data-ttu-id="23a11-117">Description</span><span class="sxs-lookup"><span data-stu-id="23a11-117">Description</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23a11-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="23a11-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="23a11-119">成功。</span><span class="sxs-lookup"><span data-stu-id="23a11-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="23a11-120"><dt>**VFW \_ E \_ 已 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="23a11-120"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>    | <span data-ttu-id="23a11-121">Pin 已連線。</span><span class="sxs-lookup"><span data-stu-id="23a11-121">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="23a11-122"><dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="23a11-122"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="23a11-123">找不到可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="23a11-123">Could not find an acceptable media type.</span></span><br/>                                |
| <dl> <span data-ttu-id="23a11-124"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="23a11-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>          | <span data-ttu-id="23a11-125">篩選準則為使用中，且 pin 不支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="23a11-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="23a11-126"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="23a11-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl>   | <span data-ttu-id="23a11-127">無法接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="23a11-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="23a11-128">備註</span><span class="sxs-lookup"><span data-stu-id="23a11-128">Remarks</span></span>

<span data-ttu-id="23a11-129">*Pmt* 參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="23a11-129">The *pmt* parameter can be **NULL**.</span></span> <span data-ttu-id="23a11-130">它也可以指定部分媒體類型，且 \_ 主要類型、子類型或格式的值為 GUID Null。</span><span class="sxs-lookup"><span data-stu-id="23a11-130">It can also specify a partial media type, with a value of GUID\_NULL for the major type, subtype, or format.</span></span>

<span data-ttu-id="23a11-131">在基類中，這個方法會測試是否已連接釘選，以及是否停止篩選。</span><span class="sxs-lookup"><span data-stu-id="23a11-131">In the base class, this method tests whether the pin is already connected and whether the filter is stopped.</span></span> <span data-ttu-id="23a11-132">它會將連接進程的其餘部分委派給 [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="23a11-132">It delegates the rest of the connection process to the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a11-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="23a11-133">Requirements</span></span>



| <span data-ttu-id="23a11-134">需求</span><span class="sxs-lookup"><span data-stu-id="23a11-134">Requirement</span></span> | <span data-ttu-id="23a11-135">值</span><span class="sxs-lookup"><span data-stu-id="23a11-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a11-136">標頭</span><span class="sxs-lookup"><span data-stu-id="23a11-136">Header</span></span><br/>  | <dl> <span data-ttu-id="23a11-137"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="23a11-137"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="23a11-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="23a11-138">Library</span></span><br/> | <dl> <span data-ttu-id="23a11-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="23a11-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a11-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23a11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a11-141">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="23a11-141">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




