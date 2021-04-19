---
description: Receive 方法會接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。 這個方法會覆寫 CTransformFilter：： Receive 方法。
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: 'CVideoTransformFilter 的 Receive 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977542"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="401fc-104">CVideoTransformFilter 接收方法</span><span class="sxs-lookup"><span data-stu-id="401fc-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="401fc-105">`Receive`方法會接收媒體範例、進行處理，並將輸出範例傳遞給下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="401fc-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="401fc-106">這個方法會覆寫 [**CTransformFilter：： Receive**](ctransformfilter-receive.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="401fc-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="401fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="401fc-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="401fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="401fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401fc-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="401fc-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="401fc-110">輸入範例上 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="401fc-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401fc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="401fc-111">Return value</span></span>

<span data-ttu-id="401fc-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="401fc-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="401fc-113">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="401fc-113">Possible values include the following:</span></span>



| <span data-ttu-id="401fc-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="401fc-114">Return code</span></span>                                                                             | <span data-ttu-id="401fc-115">Description</span><span class="sxs-lookup"><span data-stu-id="401fc-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="401fc-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="401fc-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="401fc-117">上游篩選應停止傳送範例。</span><span class="sxs-lookup"><span data-stu-id="401fc-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="401fc-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="401fc-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="401fc-119">成功。</span><span class="sxs-lookup"><span data-stu-id="401fc-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="401fc-120">備註</span><span class="sxs-lookup"><span data-stu-id="401fc-120">Remarks</span></span>

<span data-ttu-id="401fc-121">這個方法會呼叫 [**CVideoTransformFilter：： ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) 來判斷它是否應該傳遞此範例，或只是捨棄它。</span><span class="sxs-lookup"><span data-stu-id="401fc-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="401fc-122">如果 **ShouldSkipFrame** 傳回 **FALSE** (表示應將範例傳遞) ，方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="401fc-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="401fc-123">呼叫 [**CTransformFilter：： InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) 來準備輸出範例</span><span class="sxs-lookup"><span data-stu-id="401fc-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="401fc-124">呼叫 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 來處理輸入範例。</span><span class="sxs-lookup"><span data-stu-id="401fc-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="401fc-125">這個方法是純虛擬的，而且必須在衍生類別中執行。</span><span class="sxs-lookup"><span data-stu-id="401fc-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="401fc-126">呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md) 以傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="401fc-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="401fc-127">此外，這個方法會藉由呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)，檢查輸入或輸出範例上的格式變更。</span><span class="sxs-lookup"><span data-stu-id="401fc-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="401fc-128">如果有格式變更，方法會在對應的 pin 上設定連線類型。</span><span class="sxs-lookup"><span data-stu-id="401fc-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="401fc-129">在設定新型別之前，它會呼叫 **StopStreaming**。</span><span class="sxs-lookup"><span data-stu-id="401fc-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="401fc-130">在設定新的型別之後，它會呼叫 **StartStreaming**。</span><span class="sxs-lookup"><span data-stu-id="401fc-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="401fc-131">衍生的類別可以使用這些方法來更新其內部狀態。</span><span class="sxs-lookup"><span data-stu-id="401fc-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="401fc-132">衍生類別可能也需要在其 **轉換** 方法中檢查新的格式。</span><span class="sxs-lookup"><span data-stu-id="401fc-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="401fc-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="401fc-133">Requirements</span></span>



| <span data-ttu-id="401fc-134">需求</span><span class="sxs-lookup"><span data-stu-id="401fc-134">Requirement</span></span> | <span data-ttu-id="401fc-135">值</span><span class="sxs-lookup"><span data-stu-id="401fc-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401fc-136">標頭</span><span class="sxs-lookup"><span data-stu-id="401fc-136">Header</span></span><br/>  | <dl> <span data-ttu-id="401fc-137"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="401fc-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="401fc-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="401fc-138">Library</span></span><br/> | <dl> <span data-ttu-id="401fc-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="401fc-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="401fc-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="401fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401fc-141">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="401fc-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




