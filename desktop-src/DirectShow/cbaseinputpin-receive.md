---
description: Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會實 IMemInputPin：： Receive 方法。
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: 'CBaseInputPin 的 Receive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000678"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="d024c-104">CBaseInputPin 接收方法</span><span class="sxs-lookup"><span data-stu-id="d024c-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="d024c-105">`Receive`方法會接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="d024c-106">這個方法會實 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。</span><span class="sxs-lookup"><span data-stu-id="d024c-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d024c-107">語法</span><span class="sxs-lookup"><span data-stu-id="d024c-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="d024c-108">參數</span><span class="sxs-lookup"><span data-stu-id="d024c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d024c-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="d024c-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d024c-110">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d024c-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d024c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d024c-111">Return value</span></span>

<span data-ttu-id="d024c-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d024c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d024c-113">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="d024c-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="d024c-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d024c-114">Return code</span></span>                                                                                             | <span data-ttu-id="d024c-115">Description</span><span class="sxs-lookup"><span data-stu-id="d024c-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="d024c-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d024c-117">成功。</span><span class="sxs-lookup"><span data-stu-id="d024c-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="d024c-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="d024c-119">Pin 目前正在排清;已拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="d024c-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="d024c-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d024c-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="d024c-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="d024c-123">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="d024c-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="d024c-124"><dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="d024c-125">發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="d024c-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="d024c-126"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="d024c-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="d024c-127">已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="d024c-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="d024c-128">備註</span><span class="sxs-lookup"><span data-stu-id="d024c-128">Remarks</span></span>

<span data-ttu-id="d024c-129">上游輸出圖釘會呼叫這個方法，以將範例傳遞給輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="d024c-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="d024c-130">輸入 pin 必須執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d024c-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="d024c-131">在傳回之前處理範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="d024c-132">傳回並處理工作者執行緒中的範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="d024c-133">拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-133">Reject the sample.</span></span>

<span data-ttu-id="d024c-134">如果 pin 使用背景工作執行緒來處理範例，請在此方法內的範例中新增參考計數。</span><span class="sxs-lookup"><span data-stu-id="d024c-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="d024c-135">在方法傳回之後，上游 pin 會釋放範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="d024c-136">當範例的參考計數到達零時，此範例會回到配置器以供重複使用。</span><span class="sxs-lookup"><span data-stu-id="d024c-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="d024c-137">這個方法是同步的，而且可以封鎖。</span><span class="sxs-lookup"><span data-stu-id="d024c-137">This method is synchronous and can block.</span></span> <span data-ttu-id="d024c-138">如果此方法可能會封鎖，pin 的 [**CBaseInputPin：： ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) 方法應該會傳回 s \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d024c-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="d024c-139">在基類中，這個方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d024c-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="d024c-140">呼叫 [**CBaseInputPin：： CheckStreaming**](cbaseinputpin-checkstreaming.md) 方法，以確認釘選可以立即處理範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="d024c-141">如果無法這樣做，例如，如果已停止 pin，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="d024c-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="d024c-142">抓取範例屬性，並檢查格式是否已變更 (請參閱下面的) 。</span><span class="sxs-lookup"><span data-stu-id="d024c-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="d024c-143">如果格式已變更，則方法會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以判斷是否可接受新的格式。</span><span class="sxs-lookup"><span data-stu-id="d024c-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="d024c-144">如果無法接受新的格式，方法會呼叫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法、張貼 EC \_ ERRORABORT 事件，並傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d024c-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="d024c-145">假設沒有任何錯誤，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d024c-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="d024c-146">測試格式變更，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d024c-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="d024c-147">如果範例支援 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)介面，請檢查 [**AM \_ Sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="d024c-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="d024c-148">如果有 AM \_ 範例 \_ TYPECHANGED 旗標，則格式已變更。</span><span class="sxs-lookup"><span data-stu-id="d024c-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="d024c-149">否則，如果範例不支援 **IMediaSample2**，請呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="d024c-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="d024c-150">如果此方法傳回非 **Null** 值，則格式已變更。</span><span class="sxs-lookup"><span data-stu-id="d024c-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="d024c-151">在基類中，此方法不會處理範例。</span><span class="sxs-lookup"><span data-stu-id="d024c-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="d024c-152">衍生的類別必須覆寫這個方法以執行處理。</span><span class="sxs-lookup"><span data-stu-id="d024c-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="d024c-153"> (這牽涉到的內容完全取決於篩選器。 ) 衍生類別應該呼叫基類方法，以檢查先前所述的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d024c-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="d024c-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="d024c-154">Requirements</span></span>



| <span data-ttu-id="d024c-155">需求</span><span class="sxs-lookup"><span data-stu-id="d024c-155">Requirement</span></span> | <span data-ttu-id="d024c-156">值</span><span class="sxs-lookup"><span data-stu-id="d024c-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d024c-157">標頭</span><span class="sxs-lookup"><span data-stu-id="d024c-157">Header</span></span><br/>  | <dl> <span data-ttu-id="d024c-158"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d024c-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d024c-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="d024c-159">Library</span></span><br/> | <dl> <span data-ttu-id="d024c-160"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d024c-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d024c-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d024c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d024c-162">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="d024c-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




