---
description: 當偵測到通話媒體類型的變更時，就會傳送 TAPI LINE_MONITORMEDIA 訊息。 此訊息的傳送是使用 lineMonitorMedia 函式來控制
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: 'LINE_MONITORMEDIA 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994280"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="6efa7-104">行 \_ MONITORMEDIA 訊息</span><span class="sxs-lookup"><span data-stu-id="6efa7-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="6efa7-105">當偵測到通話媒體類型的變更時，就會傳送 TAPI **線路 \_ MONITORMEDIA** 訊息。</span><span class="sxs-lookup"><span data-stu-id="6efa7-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="6efa7-106">此訊息的傳送是使用 [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) 函式來控制。</span><span class="sxs-lookup"><span data-stu-id="6efa7-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6efa7-107">參數</span><span class="sxs-lookup"><span data-stu-id="6efa7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6efa7-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6efa7-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6efa7-109">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6efa7-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="6efa7-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6efa7-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6efa7-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="6efa7-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6efa7-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6efa7-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6efa7-113">新的媒體類型 (或模式) 。</span><span class="sxs-lookup"><span data-stu-id="6efa7-113">The new media type (or mode).</span></span> <span data-ttu-id="6efa7-114">這個參數必須是一個 [**LINEMEDIAMODE \_ 常數**](linemediamode--constants.md)，而且只能是其中一個。</span><span class="sxs-lookup"><span data-stu-id="6efa7-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6efa7-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6efa7-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6efa7-116">未使用的。</span><span class="sxs-lookup"><span data-stu-id="6efa7-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="6efa7-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6efa7-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6efa7-118">「滴答計數」 (從 Windows 啟動) 偵測到指定媒體的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="6efa7-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="6efa7-119">若是早于2.0 的 TAPI 版本，則不會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="6efa7-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6efa7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6efa7-120">Return value</span></span>

<span data-ttu-id="6efa7-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6efa7-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6efa7-122">備註</span><span class="sxs-lookup"><span data-stu-id="6efa7-122">Remarks</span></span>

<span data-ttu-id="6efa7-123">**線路 \_ MONITORMEDIA** 訊息會傳送至已偵測到媒體類型的媒體監視功能的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6efa7-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="6efa7-124">因為這個時間戳記可能是在執行應用程式的電腦以外的電腦上產生，所以它只會與同一行裝置上產生的其他類似的時間戳記訊息進行比較， ( [**行 \_ GATHERDIGITS**](line-gatherdigits.md)、 [**行 \_ 產生**](line-generate.md)、 [**行 \_ MONITORDIGITS**](line-monitordigits.md)、 [**行 \_ MONITORTONE**](line-monitortone.md)) ），以判斷其相對計時 (事件) 之間的分隔。</span><span class="sxs-lookup"><span data-stu-id="6efa7-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="6efa7-125">在大約49.7 天后，滴答計數可以「換行」;在執行計算時，應用程式必須將這一點列入考慮。</span><span class="sxs-lookup"><span data-stu-id="6efa7-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="6efa7-126">如果服務提供者未產生時間戳記 (例如，如果它是使用舊版的 TAPI) 所建立，則 TAPI 會在最接近服務提供者產生事件的時間點提供時間戳記，讓合成的時間戳記盡可能準確。</span><span class="sxs-lookup"><span data-stu-id="6efa7-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="6efa7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6efa7-127">Requirements</span></span>



| <span data-ttu-id="6efa7-128">需求</span><span class="sxs-lookup"><span data-stu-id="6efa7-128">Requirement</span></span> | <span data-ttu-id="6efa7-129">值</span><span class="sxs-lookup"><span data-stu-id="6efa7-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6efa7-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6efa7-130">TAPI version</span></span><br/> | <span data-ttu-id="6efa7-131">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6efa7-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6efa7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6efa7-132">Header</span></span><br/>       | <dl> <span data-ttu-id="6efa7-133"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="6efa7-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6efa7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6efa7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efa7-135">**行 \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="6efa7-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="6efa7-136">**行 \_ 產生**</span><span class="sxs-lookup"><span data-stu-id="6efa7-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="6efa7-137">**行 \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="6efa7-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="6efa7-138">**行 \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="6efa7-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




