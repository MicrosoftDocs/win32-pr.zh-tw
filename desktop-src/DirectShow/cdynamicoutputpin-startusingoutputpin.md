---
description: StartUsingOutputPin 方法會取得串流作業的釘選存取權。
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: 'CDynamicOutputPin. StartUsingOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001178"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="feb2f-103">CDynamicOutputPin. StartUsingOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="feb2f-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="feb2f-104">`StartUsingOutputPin`方法會取得串流作業的釘選存取權。</span><span class="sxs-lookup"><span data-stu-id="feb2f-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="feb2f-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="feb2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="feb2f-106">Parameters</span></span>

<span data-ttu-id="feb2f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="feb2f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="feb2f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="feb2f-108">Return value</span></span>

<span data-ttu-id="feb2f-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="feb2f-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="feb2f-110">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="feb2f-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="feb2f-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="feb2f-111">Return code</span></span>                                                                                           | <span data-ttu-id="feb2f-112">Description</span><span class="sxs-lookup"><span data-stu-id="feb2f-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="feb2f-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="feb2f-114">成功。</span><span class="sxs-lookup"><span data-stu-id="feb2f-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="feb2f-115"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="feb2f-116">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="feb2f-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="feb2f-117"><dt>**VFW \_ E \_ 狀態 \_ 已變更**</dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="feb2f-118">篩選已停止，或 pin 已開始排清。</span><span class="sxs-lookup"><span data-stu-id="feb2f-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="feb2f-119">備註</span><span class="sxs-lookup"><span data-stu-id="feb2f-119">Remarks</span></span>

<span data-ttu-id="feb2f-120">呼叫這個方法之前，請先呼叫這個方法，然後再呼叫任何方法，將資料傳遞到連接的輸入 pin 或變更連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feb2f-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="feb2f-121">例如，此規則適用于下列方法：</span><span class="sxs-lookup"><span data-stu-id="feb2f-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="feb2f-122">**CDynamicOutputPin::ChangeOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="feb2f-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="feb2f-123">**CDynamicOutputPin::ChangeMediaType**</span><span class="sxs-lookup"><span data-stu-id="feb2f-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="feb2f-124">**CDynamicOutputPin：:D ynamicReconnect**</span><span class="sxs-lookup"><span data-stu-id="feb2f-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="feb2f-125">**CBaseOutputPin：:D eliver**</span><span class="sxs-lookup"><span data-stu-id="feb2f-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="feb2f-126">**CBaseOutputPin：:D eliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="feb2f-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="feb2f-127">**CBaseOutputPin：:D eliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="feb2f-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="feb2f-128">**IMemInputPin：： Receive**</span><span class="sxs-lookup"><span data-stu-id="feb2f-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="feb2f-129">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="feb2f-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="feb2f-130">**IPin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="feb2f-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="feb2f-131">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="feb2f-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="feb2f-132">之後，請呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法來釋放對 pin 的存取。</span><span class="sxs-lookup"><span data-stu-id="feb2f-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="feb2f-133">如果釘選了 pin，會 `StartUsingOutputPin` 等候 pin 變成解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="feb2f-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="feb2f-134">如果在方法等候時，篩選準則停止，方法會立即傳回 VFW \_ E \_ 狀態 \_ 變更。</span><span class="sxs-lookup"><span data-stu-id="feb2f-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="feb2f-135">Pin 會維護已呼叫的次數， `StartUsingOutputPin` 而不需要對應的 **StopUsingOutputPin** 呼叫數目。</span><span class="sxs-lookup"><span data-stu-id="feb2f-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="feb2f-136">如果另一個執行緒嘗試在此計數為非零時封鎖 pin，則會將其封鎖狀態設為「擱置」。</span><span class="sxs-lookup"><span data-stu-id="feb2f-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="feb2f-137">一旦所有串流作業都已完成，最後呼叫 **StopUsingOutputPin** 時，就會封鎖該 pin。</span><span class="sxs-lookup"><span data-stu-id="feb2f-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="feb2f-138">當您呼叫這個方法時，請勿保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical 區段。</span><span class="sxs-lookup"><span data-stu-id="feb2f-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="feb2f-139">否則，如果 pin 遭到封鎖，則永遠不會解除封鎖，造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="feb2f-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb2f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="feb2f-140">Requirements</span></span>



| <span data-ttu-id="feb2f-141">需求</span><span class="sxs-lookup"><span data-stu-id="feb2f-141">Requirement</span></span> | <span data-ttu-id="feb2f-142">值</span><span class="sxs-lookup"><span data-stu-id="feb2f-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb2f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="feb2f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="feb2f-144"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="feb2f-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="feb2f-145">Library</span></span><br/> | <dl> <span data-ttu-id="feb2f-146"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb2f-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feb2f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb2f-148">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="feb2f-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




