---
description: 偵測 \_ 到音調時，會傳送 TAPI 線路 MONITORTONE 訊息。 此訊息的傳送是使用 lineMonitorTones 函式來控制。
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: 'LINE_MONITORTONE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996070"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="13533-104">行 \_ MONITORTONE 訊息</span><span class="sxs-lookup"><span data-stu-id="13533-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="13533-105">偵測到音調時，會傳送 TAPI **線路 \_ MONITORTONE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="13533-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="13533-106">此訊息的傳送是使用 [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) 函式來控制。</span><span class="sxs-lookup"><span data-stu-id="13533-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="13533-107">參數</span><span class="sxs-lookup"><span data-stu-id="13533-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13533-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="13533-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="13533-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13533-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="13533-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="13533-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="13533-111">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="13533-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="13533-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="13533-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="13533-113">偵測到的色調之 [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)結構的應用程式特定 **dwAppSpecific** 成員。</span><span class="sxs-lookup"><span data-stu-id="13533-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="13533-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="13533-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="13533-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="13533-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="13533-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="13533-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="13533-117">「滴答計數」 (從 Windows 開始) 偵測到色調的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="13533-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="13533-118">如果是早于2.0 的 API 版本，則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="13533-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13533-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="13533-119">Return value</span></span>

<span data-ttu-id="13533-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="13533-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13533-121">備註</span><span class="sxs-lookup"><span data-stu-id="13533-121">Remarks</span></span>

<span data-ttu-id="13533-122">這 **行 \_ MONITORTONE** 訊息只會傳送至已要求監視其色調的應用程式。</span><span class="sxs-lookup"><span data-stu-id="13533-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="13533-123">因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 **行 \_ MONITORTONE**) ），以判斷其相對計時 (事件) 之間的分隔。</span><span class="sxs-lookup"><span data-stu-id="13533-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="13533-124">在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。</span><span class="sxs-lookup"><span data-stu-id="13533-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="13533-125">如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。</span><span class="sxs-lookup"><span data-stu-id="13533-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="13533-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="13533-126">Requirements</span></span>



| <span data-ttu-id="13533-127">需求</span><span class="sxs-lookup"><span data-stu-id="13533-127">Requirement</span></span> | <span data-ttu-id="13533-128">值</span><span class="sxs-lookup"><span data-stu-id="13533-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="13533-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="13533-129">TAPI version</span></span><br/> | <span data-ttu-id="13533-130">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="13533-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="13533-131">標頭</span><span class="sxs-lookup"><span data-stu-id="13533-131">Header</span></span><br/>       | <dl> <span data-ttu-id="13533-132"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="13533-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13533-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13533-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13533-134">**行 \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="13533-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="13533-135">**行 \_ 產生**</span><span class="sxs-lookup"><span data-stu-id="13533-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="13533-136">**行 \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="13533-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="13533-137">**LINEMONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="13533-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="13533-138">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="13533-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




