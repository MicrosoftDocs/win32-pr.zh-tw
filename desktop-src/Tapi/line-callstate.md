---
description: '\_當指定之呼叫的狀態變更時，就會傳送 TAPI 線路 CALLSTATE 訊息。'
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: 'LINE_CALLSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982592"
---
# <a name="line_callstate-message"></a><span data-ttu-id="9f6f2-103">行 \_ CALLSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="9f6f2-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="9f6f2-104">當指定之呼叫的狀態變更時，就會傳送 TAPI **線路 \_ CALLSTATE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="9f6f2-105">一般來說，在呼叫的存留期間，會收到數個這類訊息。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="9f6f2-106">應用程式會收到此訊息的新來電通知;新的呼叫處於供應專案 *狀態。*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="9f6f2-107">應用程式可以使用 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) 來取得有關目前通話狀態的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9f6f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f6f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6f2-109">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6f2-110">呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="9f6f2-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6f2-112">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="9f6f2-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6f2-114">新的通話狀態。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-114">The new call state.</span></span> <span data-ttu-id="9f6f2-115">此參數必須是下列其中一個 [**LINECALLSTATE \_ 常數**](linecallstate--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="9f6f2-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="9f6f2-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="9f6f2-117">意義</span><span class="sxs-lookup"><span data-stu-id="9f6f2-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="9f6f2-118"><dt>**LINECALLSTATE \_ 忙碌**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="9f6f2-119">*dwParam2* 包含忙碌模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="9f6f2-120">此參數會使用其中一個 [**LINEBUSYMODE \_ 常數**](linebusymode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="9f6f2-121"><dt>**LINECALLSTATE \_ 已連線**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="9f6f2-122">*dwParam2* 包含連接模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="9f6f2-123">此參數會使用其中一個 [**LINECONNECTEDMODE \_ 常數**](lineconnectedmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="9f6f2-124"><dt>**LINECALLSTATE \_ 撥號**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="9f6f2-125">*dwParam2* 包含撥號音模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="9f6f2-126">此參數會使用其中一個 [**LINEDIALTONEMODE \_ 常數**](linedialtonemode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="9f6f2-127"><dt>**LINECALLSTATE \_ 供應專案**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="9f6f2-128">*dwParam2* 包含連接模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="9f6f2-129">此參數會使用其中一個 [**LINEOFFERINGMODE \_ 常數**](lineofferingmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="9f6f2-130"><dt>**LINECALLSTATE \_ SPECIALINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="9f6f2-131">*dwParam2* 包含有關特殊資訊模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="9f6f2-132">此參數會使用其中一個 [**LINESPECIALINFO \_ 常數**](linespecialinfo--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="9f6f2-133"><dt>**LINECALLSTATE 已 \_ 中斷連線**</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9f6f2-134">*dwParam2* 包含有關中斷連線模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="9f6f2-135">此參數會使用其中一個 [**LINEDISCONNECTMODE \_ 常數**](linedisconnectmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="9f6f2-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6f2-137">撥號狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-137">Call-state-dependent information.</span></span> <span data-ttu-id="9f6f2-138">請參閱 *dwParam1*。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="9f6f2-139">在 *延遲* 回應適當的情況下，請使用 LINEDISCONNECTMODE \_ TEMPFAILURE。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="9f6f2-140">*封鎖* 回應是適當的，請使用 \_ 封鎖 LINEDISCONNECT。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="9f6f2-141">如需詳細資訊，請參閱 [**LINEDISCONNECTMODE \_ 常數**](linedisconnectmode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="9f6f2-142">如果 *dwParam1* 是 LINECALLSTATE \_ CONFERENCED， *DwParam2* 會包含主旨 *hConfCall* 為其成員之會議父呼叫的 *hCall* 參數。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="9f6f2-143">如果在 *dwParam2* 中指定的呼叫之前，應用程式不會將它視為父會議呼叫 (*hConfCall*，則應用程式必須在此訊息的結果中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="9f6f2-144">如果應用程式沒有會議之父呼叫的控制碼 (因為它先前在該控制碼上呼叫 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ，) *dwParam2* 會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f6f2-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9f6f2-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6f2-146">如果為零，此參數表示應用程式的呼叫許可權不會變更。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="9f6f2-147">如果是非零值，它會指定應用程式的呼叫許可權。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="9f6f2-148">這會發生在下列情況中：當應用程式第一次提供此呼叫的控制碼時， (1) ; (2) 當應用程式是呼叫切換的目標時 (即使應用程式已經是呼叫) 的擁有者也一樣。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="9f6f2-149">此參數會使用下列其中一個 [**LINECALLPRIVILEGE \_ 常數**](linecallprivilege--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6f2-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f6f2-150">Return value</span></span>

<span data-ttu-id="9f6f2-151">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6f2-152">備註</span><span class="sxs-lookup"><span data-stu-id="9f6f2-152">Remarks</span></span>

<span data-ttu-id="9f6f2-153">此訊息會傳送至任何具有呼叫控制碼的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="9f6f2-154">程式 **行 \_ CALLSTATE** 訊息也會通知應用程式，以監視其他應用程式所建立之輸出呼叫的存在和狀態，或 (使用者手動（例如，在連結的手機裝置) 上）。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="9f6f2-155">這類呼叫的撥號狀態會反映未 *提供* 之呼叫的實際狀態。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="9f6f2-156">藉由檢查撥號狀態，應用程式可以判斷呼叫是否為需要回答的輸入呼叫。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="9f6f2-157">具有未知撥號狀態的 **行 \_ CALLSTATE** 訊息可以傳送至監視應用程式，因為成功 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)、 [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)、 [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark)、 [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)、 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)、 [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)或 [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) 已由另一個應用程式所要求的結果。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="9f6f2-158">在提出要求的應用程式的同時，若要求 [**的 \_ 作業 (成功) ，該行上**](line-reply.md) 的任何監視應用程式都會傳送 **該行 \_ CALLSTATE** (未知的) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="9f6f2-159">**\_ CALLSTATE** 訊息，指出新產生之呼叫的「實際」撥號狀態，會使用服務提供者所提供的資訊，在之後不久的要求和監視應用程式) 傳送 (。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="9f6f2-160">**一行 \_ CALLSTATE** (未知的) 訊息只會在 [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)讓呼叫被解析成三向會議時，才會傳送到監視應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="9f6f2-161">為了回溯相容性，較舊的應用程式在 *DWPARAM2* LINECALLSTATE CONFERENCED 訊息時，不需要任何特定的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="9f6f2-162">因此，TAPI 會在 *dwParam2* 中傳遞父呼叫 *hConfCall* ，不論接收訊息的應用程式 API 版本為何。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="9f6f2-163">在服務提供者所起始的會議通話案例中，繼承應用程式並不知道父呼叫已成為電話會議，除非它會以自發的方式檢查其他資訊 (例如，呼叫 [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)) 。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="9f6f2-164">無法停用此訊息。</span><span class="sxs-lookup"><span data-stu-id="9f6f2-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6f2-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f6f2-165">Requirements</span></span>



| <span data-ttu-id="9f6f2-166">需求</span><span class="sxs-lookup"><span data-stu-id="9f6f2-166">Requirement</span></span> | <span data-ttu-id="9f6f2-167">值</span><span class="sxs-lookup"><span data-stu-id="9f6f2-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9f6f2-168">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9f6f2-168">TAPI version</span></span><br/> | <span data-ttu-id="9f6f2-169">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9f6f2-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9f6f2-170">標頭</span><span class="sxs-lookup"><span data-stu-id="9f6f2-170">Header</span></span><br/>       | <dl> <span data-ttu-id="9f6f2-171"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="9f6f2-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6f2-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f6f2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6f2-173">**行 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="9f6f2-174">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="9f6f2-175">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="9f6f2-176">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="9f6f2-177">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="9f6f2-178">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="9f6f2-179">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="9f6f2-180">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="9f6f2-181">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="9f6f2-182">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="9f6f2-183">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="9f6f2-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="9f6f2-185">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="9f6f2-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




