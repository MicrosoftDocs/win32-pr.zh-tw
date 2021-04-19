---
description: LINECALLREASON \_ 位旗標常數描述呼叫的原因。
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: 'LINECALLREASON_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998704"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="904b2-103">LINECALLREASON \_ 常數</span><span class="sxs-lookup"><span data-stu-id="904b2-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="904b2-104">**LINECALLREASON \_** 位旗標常數描述呼叫的原因。</span><span class="sxs-lookup"><span data-stu-id="904b2-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="904b2-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**</span><span class="sxs-lookup"><span data-stu-id="904b2-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-106">呼叫完成要求的結果。</span><span class="sxs-lookup"><span data-stu-id="904b2-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**</span><span class="sxs-lookup"><span data-stu-id="904b2-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-108">已 camped 位址上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="904b2-108">The call was camped on the address.</span></span> <span data-ttu-id="904b2-109">通常，它一開始會處於舉 servicerequeststatusenum.onhold 狀態，而且可以切換為使用 [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)。</span><span class="sxs-lookup"><span data-stu-id="904b2-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="904b2-110">如果使用中的呼叫變成閒置，camped 呼叫可能會變更為供應狀態，且裝置會開始響鈴。</span><span class="sxs-lookup"><span data-stu-id="904b2-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ DIRECT**</span><span class="sxs-lookup"><span data-stu-id="904b2-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-112">這是直接傳入或傳出的呼叫。</span><span class="sxs-lookup"><span data-stu-id="904b2-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**</span><span class="sxs-lookup"><span data-stu-id="904b2-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-114">此呼叫已從另一個在呼叫時忙碌的延伸模組轉送。</span><span class="sxs-lookup"><span data-stu-id="904b2-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**</span><span class="sxs-lookup"><span data-stu-id="904b2-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-116">已從另一個延伸模組轉送呼叫，而該擴充未在數個環形之後接聽通話。</span><span class="sxs-lookup"><span data-stu-id="904b2-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**</span><span class="sxs-lookup"><span data-stu-id="904b2-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-118">呼叫已從另一個數位無條件轉送。</span><span class="sxs-lookup"><span data-stu-id="904b2-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ INTRUDE**</span><span class="sxs-lookup"><span data-stu-id="904b2-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-120">呼叫會 intruded 到行上，由另一個工作站或運算子動作叫用的呼叫完成動作。</span><span class="sxs-lookup"><span data-stu-id="904b2-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="904b2-121">視切換執行而定，呼叫可能會顯示在線上狀態中，或使用現有的使用中呼叫 conferenced。</span><span class="sxs-lookup"><span data-stu-id="904b2-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="904b2-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-123">通話已在位址上暫停。</span><span class="sxs-lookup"><span data-stu-id="904b2-123">The call was parked on the address.</span></span> <span data-ttu-id="904b2-124">通常，它一開始會處於舉 servicerequeststatusenum.onhold 狀態。</span><span class="sxs-lookup"><span data-stu-id="904b2-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON \_ 取貨**</span><span class="sxs-lookup"><span data-stu-id="904b2-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-126">已從另一個擴充功能挑選呼叫。</span><span class="sxs-lookup"><span data-stu-id="904b2-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON 重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="904b2-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-128">已將呼叫重新導向至此工作站。</span><span class="sxs-lookup"><span data-stu-id="904b2-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON \_ 提醒**</span><span class="sxs-lookup"><span data-stu-id="904b2-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-130">此呼叫是提醒 (或「回想」 ) 使用者已暫停或保持 (可能) 很長一段時間。</span><span class="sxs-lookup"><span data-stu-id="904b2-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="904b2-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-132">呼叫會顯示在位址上，因為交換器需要來自應用程式的路由指示。</span><span class="sxs-lookup"><span data-stu-id="904b2-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="904b2-133">應用程式應該檢查 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **CalledID** 成員，然後使用 [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)函式來提供新的可撥打位址給呼叫。</span><span class="sxs-lookup"><span data-stu-id="904b2-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="904b2-134">如果要改為封鎖呼叫，應用程式可能會呼叫 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)。</span><span class="sxs-lookup"><span data-stu-id="904b2-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="904b2-135">如果應用程式無法在參數定義的超時期間內採取動作，則會執行預設動作。</span><span class="sxs-lookup"><span data-stu-id="904b2-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="904b2-136">只有當該行的協商版本是2.0 或更高版本時，服務提供者才能使用此常數。</span><span class="sxs-lookup"><span data-stu-id="904b2-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="904b2-137">否則服務提供者應替代 LINECALLREASON \_ UNAVAIL。</span><span class="sxs-lookup"><span data-stu-id="904b2-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="904b2-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-139">呼叫已從另一個數位轉移。</span><span class="sxs-lookup"><span data-stu-id="904b2-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="904b2-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-141">呼叫的原因無法使用，稍後將不會變成已知。</span><span class="sxs-lookup"><span data-stu-id="904b2-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="904b2-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-143">呼叫的原因目前未知，但稍後可能會變成已知。</span><span class="sxs-lookup"><span data-stu-id="904b2-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="904b2-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON \_ UNPARK**</span><span class="sxs-lookup"><span data-stu-id="904b2-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="904b2-145">已將呼叫取出為暫停呼叫。</span><span class="sxs-lookup"><span data-stu-id="904b2-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="904b2-146">備註</span><span class="sxs-lookup"><span data-stu-id="904b2-146">Remarks</span></span>

<span data-ttu-id="904b2-147">無延伸。</span><span class="sxs-lookup"><span data-stu-id="904b2-147">No extensibility.</span></span> <span data-ttu-id="904b2-148">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="904b2-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="904b2-149">LINECALLREASON \_ 常數用於 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)資料結構的 **dwReason** 成員。</span><span class="sxs-lookup"><span data-stu-id="904b2-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="904b2-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="904b2-150">Requirements</span></span>



| <span data-ttu-id="904b2-151">需求</span><span class="sxs-lookup"><span data-stu-id="904b2-151">Requirement</span></span> | <span data-ttu-id="904b2-152">值</span><span class="sxs-lookup"><span data-stu-id="904b2-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="904b2-153">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="904b2-153">TAPI version</span></span><br/> | <span data-ttu-id="904b2-154">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="904b2-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="904b2-155">標頭</span><span class="sxs-lookup"><span data-stu-id="904b2-155">Header</span></span><br/>       | <dl> <span data-ttu-id="904b2-156"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="904b2-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904b2-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="904b2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904b2-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="904b2-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="904b2-159">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="904b2-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="904b2-160">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="904b2-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="904b2-161">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="904b2-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




