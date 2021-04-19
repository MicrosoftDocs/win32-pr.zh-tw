---
description: ChangeMediaType 方法會動態變更連接的媒體類型。
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: 'CDynamicOutputPin. ChangeMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001002"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a><span data-ttu-id="afb5d-103">CDynamicOutputPin. ChangeMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="afb5d-103">CDynamicOutputPin.ChangeMediaType method</span></span>

<span data-ttu-id="afb5d-104">`ChangeMediaType`方法會動態變更連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="afb5d-104">The `ChangeMediaType` method dynamically changes the media type for the connection.</span></span> <span data-ttu-id="afb5d-105">當篩選圖形正在執行時，就會發生變更。</span><span class="sxs-lookup"><span data-stu-id="afb5d-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="afb5d-106">呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。</span><span class="sxs-lookup"><span data-stu-id="afb5d-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="afb5d-107">呼叫端必須確定沒有任何舊的樣本暫止。</span><span class="sxs-lookup"><span data-stu-id="afb5d-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb5d-108">語法</span><span class="sxs-lookup"><span data-stu-id="afb5d-108">Syntax</span></span>


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="afb5d-109">參數</span><span class="sxs-lookup"><span data-stu-id="afb5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb5d-110">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="afb5d-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="afb5d-111">指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="afb5d-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb5d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="afb5d-112">Return value</span></span>

<span data-ttu-id="afb5d-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="afb5d-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="afb5d-114">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="afb5d-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="afb5d-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="afb5d-115">Return code</span></span>                                                                                           | <span data-ttu-id="afb5d-116">Description</span><span class="sxs-lookup"><span data-stu-id="afb5d-116">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afb5d-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="afb5d-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="afb5d-118">成功。</span><span class="sxs-lookup"><span data-stu-id="afb5d-118">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="afb5d-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="afb5d-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="afb5d-120">失敗。</span><span class="sxs-lookup"><span data-stu-id="afb5d-120">Failure.</span></span> <span data-ttu-id="afb5d-121">可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)。</span><span class="sxs-lookup"><span data-stu-id="afb5d-121">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="afb5d-122"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="afb5d-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="afb5d-123">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="afb5d-123">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="afb5d-124">備註</span><span class="sxs-lookup"><span data-stu-id="afb5d-124">Remarks</span></span>

<span data-ttu-id="afb5d-125">呼叫這個方法之前，請先呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="afb5d-125">Call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

<span data-ttu-id="afb5d-126">這個方法會先檢查下游輸入 pin 是否可以接受新的格式，而不需要重新連接。</span><span class="sxs-lookup"><span data-stu-id="afb5d-126">This method first checks whether the downstream input pin can accept the new format without reconnecting.</span></span> <span data-ttu-id="afb5d-127">它會查詢 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="afb5d-127">It queries the input pin for the [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) interface.</span></span> <span data-ttu-id="afb5d-128">如果輸入 pin 支援 **IPinConnection**，此方法會以建議的媒體類型呼叫 [**IPinConnection：:D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) 方法。</span><span class="sxs-lookup"><span data-stu-id="afb5d-128">If the input pin supports **IPinConnection**, the method calls the [**IPinConnection::DynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) method with the proposed media type.</span></span> <span data-ttu-id="afb5d-129">如果輸入 pin 接受新的媒體類型，方法會呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法，並重新協商配置器需求。</span><span class="sxs-lookup"><span data-stu-id="afb5d-129">If the input pin accepts the new media type, the method calls the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method and renegotiates the allocator requirements.</span></span>

<span data-ttu-id="afb5d-130">另一方面，如果下游 pin 不支援 **IPinConnection**，或者它拒絕新的媒體類型，則方法會呼叫 [**CDynamicOutputPin：:D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) 方法來執行動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="afb5d-130">On the other hand, if the downstream pin does not support **IPinConnection**, or if it rejects the new media type, the method calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to perform a dynamic reconnection.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb5d-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="afb5d-131">Requirements</span></span>



| <span data-ttu-id="afb5d-132">需求</span><span class="sxs-lookup"><span data-stu-id="afb5d-132">Requirement</span></span> | <span data-ttu-id="afb5d-133">值</span><span class="sxs-lookup"><span data-stu-id="afb5d-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb5d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="afb5d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="afb5d-135"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="afb5d-135"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="afb5d-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="afb5d-136">Library</span></span><br/> | <dl> <span data-ttu-id="afb5d-137"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="afb5d-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb5d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afb5d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb5d-139">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="afb5d-139">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




