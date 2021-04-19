---
description: ReceiveMultiple 方法會接收範例陣列。 這個方法會實 IMemInputPin：： ReceiveMultiple 方法。
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: 'CBaseInputPin. ReceiveMultiple 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984876"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="39213-104">CBaseInputPin. ReceiveMultiple 方法</span><span class="sxs-lookup"><span data-stu-id="39213-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="39213-105">`ReceiveMultiple`方法會接收範例的陣列。</span><span class="sxs-lookup"><span data-stu-id="39213-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="39213-106">這個方法會實 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。</span><span class="sxs-lookup"><span data-stu-id="39213-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39213-107">語法</span><span class="sxs-lookup"><span data-stu-id="39213-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="39213-108">參數</span><span class="sxs-lookup"><span data-stu-id="39213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39213-109">*pSamples*</span><span class="sxs-lookup"><span data-stu-id="39213-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="39213-110">[**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)指標陣列的位址，其大小為 *nSamples*。</span><span class="sxs-lookup"><span data-stu-id="39213-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="39213-111">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="39213-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="39213-112">要處理的樣本數。</span><span class="sxs-lookup"><span data-stu-id="39213-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="39213-113">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="39213-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="39213-114">變數的指標，此變數會接收已處理的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="39213-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39213-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="39213-115">Return value</span></span>

<span data-ttu-id="39213-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="39213-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="39213-117">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="39213-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="39213-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="39213-118">Return code</span></span>                                                                                             | <span data-ttu-id="39213-119">Description</span><span class="sxs-lookup"><span data-stu-id="39213-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="39213-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="39213-121">成功。</span><span class="sxs-lookup"><span data-stu-id="39213-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="39213-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="39213-123">Pin 目前正在排清;已拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="39213-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="39213-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="39213-125">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="39213-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="39213-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="39213-127">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="39213-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="39213-128"><dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="39213-129">發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="39213-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="39213-130"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="39213-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="39213-131">已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="39213-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="39213-132">備註</span><span class="sxs-lookup"><span data-stu-id="39213-132">Remarks</span></span>

<span data-ttu-id="39213-133">這個方法的行為就像是 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法，但是會收到範例陣列。</span><span class="sxs-lookup"><span data-stu-id="39213-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="39213-134">在基類中，方法會在陣列中執行迴圈，並呼叫每個範例的 **Receive** 。</span><span class="sxs-lookup"><span data-stu-id="39213-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="39213-135">如果您的篩選可以更有效率地處理樣本批次，而不是一次處理一個樣本，請覆寫此函數。</span><span class="sxs-lookup"><span data-stu-id="39213-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="39213-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="39213-136">Requirements</span></span>



| <span data-ttu-id="39213-137">需求</span><span class="sxs-lookup"><span data-stu-id="39213-137">Requirement</span></span> | <span data-ttu-id="39213-138">值</span><span class="sxs-lookup"><span data-stu-id="39213-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39213-139">標頭</span><span class="sxs-lookup"><span data-stu-id="39213-139">Header</span></span><br/>  | <dl> <span data-ttu-id="39213-140"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="39213-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39213-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="39213-141">Library</span></span><br/> | <dl> <span data-ttu-id="39213-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="39213-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39213-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39213-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39213-144">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="39213-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




