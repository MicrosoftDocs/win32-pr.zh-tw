---
description: AsynchronousBlockOutputPin 方法會封鎖釘選。 在封鎖 pin 之前，方法可能會傳回。
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: 'CDynamicOutputPin. AsynchronousBlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996095"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="00cd7-104">CDynamicOutputPin. AsynchronousBlockOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="00cd7-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="00cd7-105">`AsynchronousBlockOutputPin`方法會封鎖釘選。</span><span class="sxs-lookup"><span data-stu-id="00cd7-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="00cd7-106">在封鎖 pin 之前，方法可能會傳回。</span><span class="sxs-lookup"><span data-stu-id="00cd7-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cd7-107">語法</span><span class="sxs-lookup"><span data-stu-id="00cd7-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="00cd7-108">參數</span><span class="sxs-lookup"><span data-stu-id="00cd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00cd7-109">*hNotifyCallerPinBlockedEvent*</span><span class="sxs-lookup"><span data-stu-id="00cd7-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="00cd7-110">事件的控制代碼。</span><span class="sxs-lookup"><span data-stu-id="00cd7-110">Handle to an event.</span></span> <span data-ttu-id="00cd7-111">封鎖輸出 pin 或呼叫端取消封鎖作業時，就會發出事件。</span><span class="sxs-lookup"><span data-stu-id="00cd7-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00cd7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="00cd7-112">Return value</span></span>

<span data-ttu-id="00cd7-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="00cd7-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="00cd7-114">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="00cd7-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="00cd7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="00cd7-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="00cd7-116">Description</span><span class="sxs-lookup"><span data-stu-id="00cd7-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="00cd7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="00cd7-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="00cd7-118">成功。</span><span class="sxs-lookup"><span data-stu-id="00cd7-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="00cd7-119"><dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt></span><span class="sxs-lookup"><span data-stu-id="00cd7-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="00cd7-120">Pin 已在另一個執行緒上遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="00cd7-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="00cd7-121"><dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt></span><span class="sxs-lookup"><span data-stu-id="00cd7-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="00cd7-122">呼叫執行緒上已封鎖 Pin。</span><span class="sxs-lookup"><span data-stu-id="00cd7-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00cd7-123">備註</span><span class="sxs-lookup"><span data-stu-id="00cd7-123">Remarks</span></span>

<span data-ttu-id="00cd7-124">請勿從串流執行緒呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="00cd7-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="00cd7-125">如果沒有任何串流執行緒使用 pin，這個方法會立即封鎖 pin。</span><span class="sxs-lookup"><span data-stu-id="00cd7-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="00cd7-126">否則，它會將 pin 狀態設定為「擱置」，並傳回。</span><span class="sxs-lookup"><span data-stu-id="00cd7-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="00cd7-127">當串流作業完成時，串流執行緒會呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法，它會封鎖釘選併發出 **hNotifyCallerPinBlockedEvent** 事件的信號。</span><span class="sxs-lookup"><span data-stu-id="00cd7-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="00cd7-128">若要取消暫止的區塊，請呼叫 [**CDynamicOutputPin：： UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="00cd7-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="00cd7-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="00cd7-129">Requirements</span></span>



| <span data-ttu-id="00cd7-130">需求</span><span class="sxs-lookup"><span data-stu-id="00cd7-130">Requirement</span></span> | <span data-ttu-id="00cd7-131">值</span><span class="sxs-lookup"><span data-stu-id="00cd7-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00cd7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="00cd7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="00cd7-133"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="00cd7-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="00cd7-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="00cd7-134">Library</span></span><br/> | <dl> <span data-ttu-id="00cd7-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="00cd7-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00cd7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00cd7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00cd7-137">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="00cd7-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




