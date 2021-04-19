---
description: 傳遞方法會將媒體範例傳遞至連線的輸入 pin。
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: 'CBaseOutputPin 傳遞方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994847"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="357e8-103">CBaseOutputPin 傳遞方法</span><span class="sxs-lookup"><span data-stu-id="357e8-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="357e8-104">方法會將 `Deliver` 媒體範例傳遞到連接的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="357e8-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="357e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="357e8-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="357e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="357e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="357e8-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="357e8-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="357e8-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="357e8-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="357e8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="357e8-109">Return value</span></span>

<span data-ttu-id="357e8-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="357e8-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="357e8-111">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="357e8-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="357e8-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="357e8-112">Return code</span></span>                                                                                           | <span data-ttu-id="357e8-113">Description</span><span class="sxs-lookup"><span data-stu-id="357e8-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="357e8-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="357e8-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="357e8-115">成功。</span><span class="sxs-lookup"><span data-stu-id="357e8-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="357e8-116"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="357e8-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="357e8-117">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="357e8-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="357e8-118">備註</span><span class="sxs-lookup"><span data-stu-id="357e8-118">Remarks</span></span>

<span data-ttu-id="357e8-119">這個方法會呼叫輸入釘選上的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。</span><span class="sxs-lookup"><span data-stu-id="357e8-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="357e8-120">如果 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock)方法傳回 S OK，則 **Receive** 會封鎖 \_ 。</span><span class="sxs-lookup"><span data-stu-id="357e8-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="357e8-121">呼叫這個方法之後，請釋放範例。</span><span class="sxs-lookup"><span data-stu-id="357e8-121">Release the sample after calling this method.</span></span> <span data-ttu-id="357e8-122">輸入 pin 可能會保存範例上的參考計數，因此請勿重複使用範例。</span><span class="sxs-lookup"><span data-stu-id="357e8-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="357e8-123">一律呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) 方法，以取得新的範例。</span><span class="sxs-lookup"><span data-stu-id="357e8-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="357e8-124">在呼叫這個方法之前，請先保存篩選的重要區段。</span><span class="sxs-lookup"><span data-stu-id="357e8-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="357e8-125">否則，pin 可能會在方法呼叫期間中斷連線。</span><span class="sxs-lookup"><span data-stu-id="357e8-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="357e8-126">如果篩選使用背景工作執行緒來傳遞範例，請在篩選準則準備好傳遞範例時，按住重要區段。</span><span class="sxs-lookup"><span data-stu-id="357e8-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="357e8-127">否則，您可以在篩選器的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法中保存重要區段，篩選器會在其中處理範例。</span><span class="sxs-lookup"><span data-stu-id="357e8-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="357e8-128">工作者執行緒可能會產生潛在的鎖死。</span><span class="sxs-lookup"><span data-stu-id="357e8-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="357e8-129">當執行緒保留重要區段時，可能會等候篩選中的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="357e8-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="357e8-130">同時，狀態變更可能會等候執行緒完成。</span><span class="sxs-lookup"><span data-stu-id="357e8-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="357e8-131">為了避免這種情況，狀態變更程式碼應該發出終止執行緒的事件，然後等候執行緒完成信號。</span><span class="sxs-lookup"><span data-stu-id="357e8-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="357e8-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="357e8-132">Requirements</span></span>



| <span data-ttu-id="357e8-133">需求</span><span class="sxs-lookup"><span data-stu-id="357e8-133">Requirement</span></span> | <span data-ttu-id="357e8-134">值</span><span class="sxs-lookup"><span data-stu-id="357e8-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="357e8-135">標頭</span><span class="sxs-lookup"><span data-stu-id="357e8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="357e8-136"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="357e8-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="357e8-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="357e8-137">Library</span></span><br/> | <dl> <span data-ttu-id="357e8-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="357e8-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="357e8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="357e8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357e8-140">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="357e8-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




