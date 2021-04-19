---
description: LINECALLSTATE \_ 位旗標常數描述呼叫可以位於的撥號狀態。
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: 'LINECALLSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994736"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="0cd4a-103">LINECALLSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="0cd4a-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="0cd4a-104">**LINECALLSTATE \_** 位旗標常數描述呼叫可以位於的撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="0cd4a-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE 已 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-106">通話處於供應狀態且已被接受。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="0cd4a-107">這會向其他 (監視，指出目前的擁有者應用程式已宣稱接聽通話的責任，) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="0cd4a-108">在 ISDN 中，當呼叫方設備傳送訊息給交換器時，即會輸入接受的狀態，指出它願意向呼叫的人員提出呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="0cd4a-109">這會產生警示 (在來電的兩端) 使用者的副作用。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="0cd4a-110">傳入的呼叫一律可以立即獲得解答，而不需要先個別接受。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-112">呼叫收到忙碌的聲音。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="0cd4a-113">忙碌的色調表示呼叫無法完成， (主幹) 或遠端合作物件的站在使用中。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="0cd4a-114">請參閱 [**LINEBUSYMODE \_ 常數**](linebusymode--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ CONFERENCED**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-116">呼叫是會議通話的成員，並在邏輯上處於已線上狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ 已連線**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-118">已建立通話，並進行連接。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="0cd4a-119">資訊可以在來源位址和目的地位址之間的呼叫之間流動。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-121">建立者是通話的撥號位數。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="0cd4a-122">交換器會收集撥號位數。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="0cd4a-123">請注意， [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) 和 [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) 都不會將這一行放入撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-125">呼叫會從交換器接收撥號音，這表示交換器已準備好接收撥接的號碼。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="0cd4a-126">請參閱特殊撥號音的識別碼 [**LINEDIALTONEMODE \_ 常數**](linedialtonemode--constants.md) ，例如一般語音信箱的斷斷續續聲。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE 已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-128">遠端方已與呼叫中斷連線。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ 閒置**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-130">呼叫存在但尚未連接。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-130">The call exists but has not been connected.</span></span> <span data-ttu-id="0cd4a-131">呼叫上沒有任何活動存在，這表示目前沒有作用中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="0cd4a-132">呼叫永遠不會從閒置狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE \_ 供應專案**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-134">呼叫會提供給站，以通知新通話的抵達。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="0cd4a-135">供應專案狀態與造成電話或電腦響鈴的情況不同。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="0cd4a-136">在某些環境中，供應專案狀態中的呼叫不會環形使用者，直到切換器指示線路響鈴為止。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="0cd4a-137">使用範例可能是撥入電話出現在數個工作站組上，但只有主要位址環形的位置。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="0cd4a-138">環形的指示不會影響任何撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ 舉 SERVICEREQUESTSTATUSENUM.ONHOLD**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-140">開關正在保留呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-140">The call is on hold by the switch.</span></span> <span data-ttu-id="0cd4a-141">這會釋出實體行，讓另一個呼叫使用該行。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-143">呼叫目前正在進行中，正在新增至會議中。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-145">呼叫目前正在等待轉移至另一個數位。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-147">撥號已完成，並透過交換器或電話網絡進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="0cd4a-148">這會發生在撥號完成之後，以及呼叫抵達撥打的合作物件之前，如回電、忙碌或解答。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE \_ 回電**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-150">已到達要呼叫的工作站，而目的地的交換器正在將環形聲提示傳回給建立者。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="0cd4a-151">*回電* 表示目的地位址會收到呼叫的警示。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-153">呼叫收到特殊的資訊信號，此信號位於預先錄製的宣告之前，指出無法完成呼叫的原因。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="0cd4a-154">請參閱 [**LINESPECIALINFO \_ 常數**](linespecialinfo--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0cd4a-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0cd4a-156">呼叫存在，但其狀態目前未知。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="0cd4a-157">這可能是因為服務提供者的呼叫進度偵測不佳所造成。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="0cd4a-158">可能也會產生撥號狀態設為 unknown 的撥號狀態消息，以在呼叫的實際撥號狀態不是已知時，一次通知 TAPI DLL 有新的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cd4a-159">備註</span><span class="sxs-lookup"><span data-stu-id="0cd4a-159">Remarks</span></span>

<span data-ttu-id="0cd4a-160">高序位8位可以定義任何預先定義狀態的裝置特定子狀態，前提 \_ 是您也會設定上述定義的其中一個 LINECALLSTATE 位。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="0cd4a-161">低序位24位是保留給預先定義的狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="0cd4a-162">傳送至應用程式的 [**行 \_ CALLSTATE**](line-callstate.md)訊息會使用 **LINECALLSTATE \_ 常數** 作為參數。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="0cd4a-163">訊息會攜帶呼叫轉換的新撥號狀態。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="0cd4a-164">這些常數也會當做 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)函數所傳回之 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)結構中的成員使用。</span><span class="sxs-lookup"><span data-stu-id="0cd4a-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd4a-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cd4a-165">Requirements</span></span>



| <span data-ttu-id="0cd4a-166">需求</span><span class="sxs-lookup"><span data-stu-id="0cd4a-166">Requirement</span></span> | <span data-ttu-id="0cd4a-167">值</span><span class="sxs-lookup"><span data-stu-id="0cd4a-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0cd4a-168">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0cd4a-168">TAPI version</span></span><br/> | <span data-ttu-id="0cd4a-169">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0cd4a-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0cd4a-170">標頭</span><span class="sxs-lookup"><span data-stu-id="0cd4a-170">Header</span></span><br/>       | <dl> <span data-ttu-id="0cd4a-171"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="0cd4a-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cd4a-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cd4a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd4a-173">**行 \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="0cd4a-174">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="0cd4a-175">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="0cd4a-176">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="0cd4a-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

