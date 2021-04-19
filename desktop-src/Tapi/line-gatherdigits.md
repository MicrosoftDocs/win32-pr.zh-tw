---
description: '\_當目前經緩衝處理的數位收集要求終止或取消時，會傳送 TAPI 線路 GATHERDIGITS 訊息。 當應用程式收到此訊息之後，就可以檢查數位緩衝區。'
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: 'LINE_GATHERDIGITS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990190"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="b8435-104">行 \_ GATHERDIGITS 訊息</span><span class="sxs-lookup"><span data-stu-id="b8435-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="b8435-105">當目前經緩衝處理的數位收集要求終止或取消時，會傳送 TAPI **線路 \_ GATHERDIGITS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="b8435-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="b8435-106">當應用程式收到此訊息之後，就可以檢查數位緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8435-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b8435-107">參數</span><span class="sxs-lookup"><span data-stu-id="b8435-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8435-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b8435-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b8435-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8435-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="b8435-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b8435-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b8435-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="b8435-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b8435-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b8435-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b8435-113">數位收集終止的原因。</span><span class="sxs-lookup"><span data-stu-id="b8435-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="b8435-114">這個參數必須是一個 [**LINEGATHERTERM \_ 常數**](linegatherterm--constants.md)，而且只能是其中一個。</span><span class="sxs-lookup"><span data-stu-id="b8435-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8435-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b8435-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b8435-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b8435-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b8435-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b8435-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b8435-118">「滴答計數」 (從 Windows 開始) 完成數位收集的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="b8435-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="b8435-119">若是早于2.0 的 TAPI 版本，則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="b8435-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8435-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8435-120">Return value</span></span>

<span data-ttu-id="b8435-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8435-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8435-122">備註</span><span class="sxs-lookup"><span data-stu-id="b8435-122">Remarks</span></span>

<span data-ttu-id="b8435-123">這 **行 \_ GATHERDIGITS** 訊息只會傳送至應用程式，該應用程式會使用 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)在呼叫上起始數位收集。</span><span class="sxs-lookup"><span data-stu-id="b8435-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="b8435-124">如果使用 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) 函式來取消前一個要求以收集數位，則 TAPI 會傳送 **一行 \_ GATHERDIGITS** 訊息，其中 *dwParam1* 設定為 LINEGATHERTERM \_ cancel 至應用程式，指出原始指定的緩衝區包含收集到取消的數位。</span><span class="sxs-lookup"><span data-stu-id="b8435-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="b8435-125">由於 *dwParam3* 所指定的時間戳記可能是在執行應用程式的電腦以外的電腦上產生，因此只適用于與在同一行裝置上產生的其他類似時間戳記的訊息比較， ( [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ，以判斷其相對計時 (事件) 之間的分隔。</span><span class="sxs-lookup"><span data-stu-id="b8435-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="b8435-126">在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。</span><span class="sxs-lookup"><span data-stu-id="b8435-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="b8435-127">如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。</span><span class="sxs-lookup"><span data-stu-id="b8435-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="b8435-128">當應用程式叫用將資料寫入至應用程式記憶體的任何非同步作業時，應用程式必須保留該記憶體以供寫入，直到收到 [**一行 \_ 回復**](line-reply.md) 或 **行 \_ GATHERDIGITS** 訊息為止。</span><span class="sxs-lookup"><span data-stu-id="b8435-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8435-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8435-129">Requirements</span></span>



| <span data-ttu-id="b8435-130">需求</span><span class="sxs-lookup"><span data-stu-id="b8435-130">Requirement</span></span> | <span data-ttu-id="b8435-131">值</span><span class="sxs-lookup"><span data-stu-id="b8435-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b8435-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b8435-132">TAPI version</span></span><br/> | <span data-ttu-id="b8435-133">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b8435-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b8435-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b8435-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b8435-135"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="b8435-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8435-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8435-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8435-137">**行 \_ 產生**</span><span class="sxs-lookup"><span data-stu-id="b8435-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="b8435-138">**行 \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="b8435-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="b8435-139">**行 \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="b8435-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="b8435-140">**行 \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="b8435-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="b8435-141">**行 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="b8435-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="b8435-142">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="b8435-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




