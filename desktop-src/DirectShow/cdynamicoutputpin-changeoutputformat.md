---
description: ChangeOutputFormat 方法會動態變更連接的媒體類型，並提供新的區段資訊。
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: 'CDynamicOutputPin. ChangeOutputFormat 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993545"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="fc210-103">CDynamicOutputPin. ChangeOutputFormat 方法</span><span class="sxs-lookup"><span data-stu-id="fc210-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="fc210-104">`ChangeOutputFormat`方法會動態變更連接的媒體類型，並提供新的區段資訊。</span><span class="sxs-lookup"><span data-stu-id="fc210-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="fc210-105">當篩選圖形正在執行時，就會發生變更。</span><span class="sxs-lookup"><span data-stu-id="fc210-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="fc210-106">呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。</span><span class="sxs-lookup"><span data-stu-id="fc210-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="fc210-107">呼叫端必須確定沒有任何舊的樣本暫止。</span><span class="sxs-lookup"><span data-stu-id="fc210-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc210-108">語法</span><span class="sxs-lookup"><span data-stu-id="fc210-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="fc210-109">參數</span><span class="sxs-lookup"><span data-stu-id="fc210-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc210-110">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="fc210-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fc210-111">指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fc210-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="fc210-112">*tSegmentStart*</span><span class="sxs-lookup"><span data-stu-id="fc210-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fc210-113">區段的開始時間。</span><span class="sxs-lookup"><span data-stu-id="fc210-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="fc210-114">*tSegmentStop*</span><span class="sxs-lookup"><span data-stu-id="fc210-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fc210-115">區段的停止時間。</span><span class="sxs-lookup"><span data-stu-id="fc210-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="fc210-116">*dSegmentRate*</span><span class="sxs-lookup"><span data-stu-id="fc210-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="fc210-117">區段速率。</span><span class="sxs-lookup"><span data-stu-id="fc210-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc210-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc210-118">Return value</span></span>

<span data-ttu-id="fc210-119">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fc210-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fc210-120">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="fc210-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fc210-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fc210-121">Return code</span></span>                                                                                           | <span data-ttu-id="fc210-122">Description</span><span class="sxs-lookup"><span data-stu-id="fc210-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc210-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fc210-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="fc210-124">成功。</span><span class="sxs-lookup"><span data-stu-id="fc210-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="fc210-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="fc210-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="fc210-126">失敗。</span><span class="sxs-lookup"><span data-stu-id="fc210-126">Failure.</span></span> <span data-ttu-id="fc210-127">可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)。</span><span class="sxs-lookup"><span data-stu-id="fc210-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="fc210-128"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="fc210-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fc210-129">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="fc210-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fc210-130">備註</span><span class="sxs-lookup"><span data-stu-id="fc210-130">Remarks</span></span>

<span data-ttu-id="fc210-131">當篩選執行時，這個方法會變更格式類型。</span><span class="sxs-lookup"><span data-stu-id="fc210-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="fc210-132">如果下游 pin 接受新的格式，就不需要重新連接。</span><span class="sxs-lookup"><span data-stu-id="fc210-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="fc210-133">否則，方法會嘗試重新連接 pin。</span><span class="sxs-lookup"><span data-stu-id="fc210-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="fc210-134">如果方法成功變更格式，則會傳遞新的區段資訊。</span><span class="sxs-lookup"><span data-stu-id="fc210-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="fc210-135">這個方法會呼叫 [**CDynamicOutputPin：： ChangeMediaType**](cdynamicoutputpin-changemediatype.md) 方法來執行格式變更。</span><span class="sxs-lookup"><span data-stu-id="fc210-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="fc210-136">呼叫這個方法之前，您必須先呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fc210-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc210-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc210-137">Requirements</span></span>



| <span data-ttu-id="fc210-138">需求</span><span class="sxs-lookup"><span data-stu-id="fc210-138">Requirement</span></span> | <span data-ttu-id="fc210-139">值</span><span class="sxs-lookup"><span data-stu-id="fc210-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc210-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fc210-140">Header</span></span><br/>  | <dl> <span data-ttu-id="fc210-141"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc210-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fc210-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc210-142">Library</span></span><br/> | <dl> <span data-ttu-id="fc210-143"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc210-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc210-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc210-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc210-145">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="fc210-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




