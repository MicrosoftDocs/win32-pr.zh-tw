---
description: ReceiveConnection 方法會接受來自另一個 pin 的連接。 這個方法會實 IPin：： ReceiveConnection 方法。
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: 'CBasePin. ReceiveConnection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995375"
---
# <a name="cbasepinreceiveconnection-method"></a><span data-ttu-id="7d97c-104">CBasePin. ReceiveConnection 方法</span><span class="sxs-lookup"><span data-stu-id="7d97c-104">CBasePin.ReceiveConnection method</span></span>

<span data-ttu-id="7d97c-105">`ReceiveConnection`方法會接受來自另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="7d97c-105">The `ReceiveConnection` method accepts a connection from another pin.</span></span> <span data-ttu-id="7d97c-106">這個方法會實 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-106">This method implements the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d97c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d97c-107">Syntax</span></span>


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7d97c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7d97c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d97c-109">*pConnector*</span><span class="sxs-lookup"><span data-stu-id="7d97c-109">*pConnector*</span></span> 
</dt> <dd>

<span data-ttu-id="7d97c-110">連接釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7d97c-110">Pointer to the connecting pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7d97c-111">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="7d97c-111">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7d97c-112">指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d97c-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d97c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d97c-113">Return value</span></span>

<span data-ttu-id="7d97c-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7d97c-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7d97c-115">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="7d97c-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7d97c-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7d97c-116">Return code</span></span>                                                                                                | <span data-ttu-id="7d97c-117">Description</span><span class="sxs-lookup"><span data-stu-id="7d97c-117">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d97c-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-118"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7d97c-119">成功。</span><span class="sxs-lookup"><span data-stu-id="7d97c-119">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7d97c-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-120"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="7d97c-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="7d97c-121">**NULL** pointer argument.</span></span><br/>                                              |
| <dl> <span data-ttu-id="7d97c-122"><dt>**VFW \_ E \_ 已 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="7d97c-123">Pin 已連線。</span><span class="sxs-lookup"><span data-stu-id="7d97c-123">The pin is already connected.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7d97c-124"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-124"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl>        | <span data-ttu-id="7d97c-125">篩選準則為使用中，且 pin 不支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="7d97c-125">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |
| <dl> <span data-ttu-id="7d97c-126"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-126"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="7d97c-127">無法接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7d97c-127">The specified media type is not acceptable.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="7d97c-128">備註</span><span class="sxs-lookup"><span data-stu-id="7d97c-128">Remarks</span></span>

<span data-ttu-id="7d97c-129">輸出圖釘會在輸入 pin 上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-129">The output pin calls this method on the input pin.</span></span> <span data-ttu-id="7d97c-130">如果輸入 pin 傳回錯誤碼，連接將會失敗。</span><span class="sxs-lookup"><span data-stu-id="7d97c-130">If the input pin returns an error code, the connection fails.</span></span>

<span data-ttu-id="7d97c-131">在基類中，這個方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7d97c-131">In the base class, this method performs the following steps:</span></span>

-   <span data-ttu-id="7d97c-132">檢查 pin 是否已連接。</span><span class="sxs-lookup"><span data-stu-id="7d97c-132">Checks whether the pin is already connected.</span></span>
-   <span data-ttu-id="7d97c-133">檢查篩選是否已停止。</span><span class="sxs-lookup"><span data-stu-id="7d97c-133">Checks whether the filter is stopped.</span></span>
-   <span data-ttu-id="7d97c-134">呼叫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法以測試連接的 pin 是否適合。</span><span class="sxs-lookup"><span data-stu-id="7d97c-134">Calls the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method to test whether the connecting pin is suitable.</span></span>
-   <span data-ttu-id="7d97c-135">呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，測試是否可接受媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7d97c-135">Calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to test whether the media type is acceptable.</span></span>

<span data-ttu-id="7d97c-136">如果上述所有步驟都成功，則此方法會呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 和 [**SetMediaType**](cbasepin-setmediatype.md) 方法來完成連接。</span><span class="sxs-lookup"><span data-stu-id="7d97c-136">If all of these steps succeed, the method calls the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) and [**SetMediaType**](cbasepin-setmediatype.md) methods to complete the connection.</span></span> <span data-ttu-id="7d97c-137">這些方法會將媒體類型和指標儲存在輸出圖釘的上方。</span><span class="sxs-lookup"><span data-stu-id="7d97c-137">These methods store the media type and a pointer to the output pin.</span></span>

<span data-ttu-id="7d97c-138">如果 **CheckConnect** 或 **CheckMediaType** 失敗，基類會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法來中斷連接，然後從傳回錯誤碼 `ReceiveConnection` 。</span><span class="sxs-lookup"><span data-stu-id="7d97c-138">If **CheckConnect** or **CheckMediaType** fail, the base class calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method to break the connection and then returns an error code from `ReceiveConnection`.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d97c-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d97c-139">Requirements</span></span>



| <span data-ttu-id="7d97c-140">需求</span><span class="sxs-lookup"><span data-stu-id="7d97c-140">Requirement</span></span> | <span data-ttu-id="7d97c-141">值</span><span class="sxs-lookup"><span data-stu-id="7d97c-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d97c-142">標頭</span><span class="sxs-lookup"><span data-stu-id="7d97c-142">Header</span></span><br/>  | <dl> <span data-ttu-id="7d97c-143"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-143"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7d97c-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d97c-144">Library</span></span><br/> | <dl> <span data-ttu-id="7d97c-145"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-145"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d97c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d97c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d97c-147">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="7d97c-147">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




