---
description: 偵測 \_ 到數位時，會傳送 TAPI 線路 MONITORDIGITS 訊息。 此訊息的傳送是使用 lineMonitorDigits 函式來控制。
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: 'LINE_MONITORDIGITS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994716"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="1f304-104">行 \_ MONITORDIGITS 訊息</span><span class="sxs-lookup"><span data-stu-id="1f304-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="1f304-105">偵測到數位時，會傳送 TAPI **線路 \_ MONITORDIGITS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1f304-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="1f304-106">此訊息的傳送是使用 [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) 函式來控制。</span><span class="sxs-lookup"><span data-stu-id="1f304-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1f304-107">參數</span><span class="sxs-lookup"><span data-stu-id="1f304-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f304-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="1f304-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="1f304-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1f304-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="1f304-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="1f304-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1f304-111">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="1f304-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="1f304-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1f304-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f304-113">低序位位元組包含在文字表示中收到的最後一個數位。</span><span class="sxs-lookup"><span data-stu-id="1f304-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="1f304-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1f304-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f304-115">偵測到的數位模式。</span><span class="sxs-lookup"><span data-stu-id="1f304-115">The digit mode that was detected.</span></span> <span data-ttu-id="1f304-116">這個參數必須是一個 [**LINEDIGITMODE \_ 常數**](linedigitmode--constants.md)，而且只能是其中一個。</span><span class="sxs-lookup"><span data-stu-id="1f304-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f304-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1f304-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1f304-118">「滴答計數」 (毫秒數，自 Windows 啟動後偵測到指定數位的) 。</span><span class="sxs-lookup"><span data-stu-id="1f304-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="1f304-119">若是早于2.0 的 TAPI 版本，則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="1f304-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f304-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f304-120">Return value</span></span>

<span data-ttu-id="1f304-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f304-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f304-122">備註</span><span class="sxs-lookup"><span data-stu-id="1f304-122">Remarks</span></span>

<span data-ttu-id="1f304-123">**該行 \_ MONITORDIGITS** 訊息會傳送至已啟用數位監視的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1f304-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="1f304-124">因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ），以判斷其相對計時 (事件) 之間的分隔。</span><span class="sxs-lookup"><span data-stu-id="1f304-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="1f304-125">在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。</span><span class="sxs-lookup"><span data-stu-id="1f304-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="1f304-126">如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。</span><span class="sxs-lookup"><span data-stu-id="1f304-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f304-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f304-127">Requirements</span></span>



| <span data-ttu-id="1f304-128">需求</span><span class="sxs-lookup"><span data-stu-id="1f304-128">Requirement</span></span> | <span data-ttu-id="1f304-129">值</span><span class="sxs-lookup"><span data-stu-id="1f304-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1f304-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1f304-130">TAPI version</span></span><br/> | <span data-ttu-id="1f304-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f304-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1f304-132">標頭</span><span class="sxs-lookup"><span data-stu-id="1f304-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1f304-133"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="1f304-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f304-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f304-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f304-135">**行 \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="1f304-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="1f304-136">**行 \_ 產生**</span><span class="sxs-lookup"><span data-stu-id="1f304-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="1f304-137">**行 \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="1f304-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="1f304-138">**行 \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="1f304-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="1f304-139">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="1f304-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




