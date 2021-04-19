---
description: '\_會傳送 TAPI 線路產生訊息，以通知應用程式目前的數位或語氣產生已終止。'
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: 'LINE_GENERATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990733"
---
# <a name="line_generate-message"></a><span data-ttu-id="ecf93-103">行 \_ 產生訊息</span><span class="sxs-lookup"><span data-stu-id="ecf93-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="ecf93-104">會傳送 TAPI **線路 \_ 產生** 訊息，以通知應用程式目前的數位或語氣產生已終止。</span><span class="sxs-lookup"><span data-stu-id="ecf93-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="ecf93-105">每次只有一個這類世代要求可以進行指定的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecf93-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="ecf93-106">當數位或語氣產生取消時，也會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ecf93-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ecf93-107">參數</span><span class="sxs-lookup"><span data-stu-id="ecf93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf93-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="ecf93-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf93-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ecf93-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="ecf93-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="ecf93-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf93-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="ecf93-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="ecf93-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ecf93-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf93-113">數位或語氣產生終止的原因。</span><span class="sxs-lookup"><span data-stu-id="ecf93-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="ecf93-114">這個參數必須是一個 [**LINEGENERATETERM \_ 常數**](linegenerateterm--constants.md)，而且只能是其中一個。</span><span class="sxs-lookup"><span data-stu-id="ecf93-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecf93-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ecf93-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf93-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="ecf93-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ecf93-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ecf93-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf93-118">「滴答計數」 (從 Windows 開始) 數位或語氣產生完成的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="ecf93-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="ecf93-119">如果是早于2.0 的 API 版本，則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ecf93-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf93-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecf93-120">Return value</span></span>

<span data-ttu-id="ecf93-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ecf93-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf93-122">備註</span><span class="sxs-lookup"><span data-stu-id="ecf93-122">Remarks</span></span>

<span data-ttu-id="ecf93-123">**該行 \_ 產生** 訊息只會傳送至要求數位或語氣產生的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ecf93-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="ecf93-124">由於 *dwParam3* 所指定的時間戳記可能是在執行應用程式的電腦以外的電腦上產生，因此只適用于與在同一行裝置上產生的其他類似時間戳記的訊息比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORMEDIA**](line-monitormedia.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ，以判斷其相對計時 (事件) 之間的分隔。</span><span class="sxs-lookup"><span data-stu-id="ecf93-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="ecf93-125">在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。</span><span class="sxs-lookup"><span data-stu-id="ecf93-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="ecf93-126">如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。</span><span class="sxs-lookup"><span data-stu-id="ecf93-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf93-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecf93-127">Requirements</span></span>



| <span data-ttu-id="ecf93-128">需求</span><span class="sxs-lookup"><span data-stu-id="ecf93-128">Requirement</span></span> | <span data-ttu-id="ecf93-129">值</span><span class="sxs-lookup"><span data-stu-id="ecf93-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ecf93-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ecf93-130">TAPI version</span></span><br/> | <span data-ttu-id="ecf93-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ecf93-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ecf93-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ecf93-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ecf93-133"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="ecf93-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf93-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecf93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf93-135">**行 \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="ecf93-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="ecf93-136">**行 \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="ecf93-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="ecf93-137">**行 \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="ecf93-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="ecf93-138">**行 \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="ecf93-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




