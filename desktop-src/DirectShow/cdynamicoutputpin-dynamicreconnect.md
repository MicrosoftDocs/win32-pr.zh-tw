---
description: DynamicReconnect 方法會以新的媒體類型執行動態重新連接。 當篩選圖形正在執行時，就會發生重新連接。
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: 'CDynamicOutputPin. DynamicReconnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986783"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a><span data-ttu-id="ef2ef-104">CDynamicOutputPin. DynamicReconnect 方法</span><span class="sxs-lookup"><span data-stu-id="ef2ef-104">CDynamicOutputPin.DynamicReconnect method</span></span>

<span data-ttu-id="ef2ef-105">`DynamicReconnect`方法會以新的媒體類型執行動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-105">The `DynamicReconnect` method performs a dynamic reconnection with a new media type.</span></span> <span data-ttu-id="ef2ef-106">當篩選圖形正在執行時，就會發生重新連接。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-106">The reconnection can occur while the filter graph is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef2ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="ef2ef-107">Syntax</span></span>


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ef2ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef2ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef2ef-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="ef2ef-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2ef-110">指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef2ef-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef2ef-111">Return value</span></span>

<span data-ttu-id="ef2ef-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ef2ef-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ef2ef-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ef2ef-114">Return code</span></span>                                                                            | <span data-ttu-id="ef2ef-115">Description</span><span class="sxs-lookup"><span data-stu-id="ef2ef-115">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef2ef-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2ef-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ef2ef-117">成功。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-117">Success.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="ef2ef-118"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2ef-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ef2ef-119">失敗。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-119">Failure.</span></span> <span data-ttu-id="ef2ef-120">可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-120">Possibly the owning filter did not call the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef2ef-121">備註</span><span class="sxs-lookup"><span data-stu-id="ef2ef-121">Remarks</span></span>

<span data-ttu-id="ef2ef-122">您必須從將資料傳遞至 pin 的相同執行緒呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-122">This method must be called from the same thread that delivers data to the pin.</span></span> <span data-ttu-id="ef2ef-123">呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-123">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="ef2ef-124">呼叫端必須確定沒有任何舊的樣本暫止。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-124">The caller must ensure that no old samples are pending.</span></span>

<span data-ttu-id="ef2ef-125">呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) ，然後再呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ef2ef-125">Call [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2ef-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef2ef-126">Requirements</span></span>



| <span data-ttu-id="ef2ef-127">需求</span><span class="sxs-lookup"><span data-stu-id="ef2ef-127">Requirement</span></span> | <span data-ttu-id="ef2ef-128">值</span><span class="sxs-lookup"><span data-stu-id="ef2ef-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2ef-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ef2ef-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ef2ef-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ef2ef-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef2ef-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef2ef-131">Library</span></span><br/> | <dl> <span data-ttu-id="ef2ef-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ef2ef-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef2ef-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef2ef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2ef-134">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="ef2ef-134">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




