---
description: LINEDEVSTATE \_ 位旗標常數描述各種行狀態事件。
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: 'LINEDEVSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999405"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="2c762-103">LINEDEVSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="2c762-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="2c762-104">**LINEDEVSTATE \_** 位旗標常數描述各種行狀態事件。</span><span class="sxs-lookup"><span data-stu-id="2c762-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="2c762-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="2c762-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-106">電池計量已大幅改變 (行動電話) 。</span><span class="sxs-lookup"><span data-stu-id="2c762-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="2c762-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-108">指出，由於使用者或其他情況所做的設定變更，位址的 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) 結構中有一或多個成員已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="2c762-109">應用程式應該使用 [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) 來讀取更新的結構。</span><span class="sxs-lookup"><span data-stu-id="2c762-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="2c762-110">如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 TAPI 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 **行 \_ LINEDEVSTATE** 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="2c762-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="2c762-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-112">另一個應用程式已關閉該行。</span><span class="sxs-lookup"><span data-stu-id="2c762-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="2c762-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-114">表示已對一或多個與線路裝置相關聯的媒體裝置進行設定變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="2c762-115">如有需要，應用程式可以使用 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) 來讀取更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="2c762-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="2c762-116">如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。</span><span class="sxs-lookup"><span data-stu-id="2c762-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**</span><span class="sxs-lookup"><span data-stu-id="2c762-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-118">指出以 [**行 \_ LINEDEVSTATE**](line-linedevstate.md)訊息的 *dwParam2* 參數所包含的完成識別碼所識別的完成呼叫已從外部取消，不再被視為有效 (如果該值是在後續的 [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)呼叫中傳遞，此函式會失敗並出現 LINEERR \_ INVALCOMPLETIONID) 。</span><span class="sxs-lookup"><span data-stu-id="2c762-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="2c762-119">如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。</span><span class="sxs-lookup"><span data-stu-id="2c762-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ 已連線**</span><span class="sxs-lookup"><span data-stu-id="2c762-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-121">該行先前已中斷連線，而且現在已連線到 TAPI。</span><span class="sxs-lookup"><span data-stu-id="2c762-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="2c762-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-123">該行的裝置特定資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE 已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="2c762-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-125">這行先前已連線，且現在已與 TAPI 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="2c762-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**</span><span class="sxs-lookup"><span data-stu-id="2c762-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-127">線路連接到 TAPI。</span><span class="sxs-lookup"><span data-stu-id="2c762-127">The line is connected to TAPI.</span></span> <span data-ttu-id="2c762-128">這種情況發生于第一次啟動 TAPI 時，或是當 TAPI 處於作用中狀態時，會在開關上實際插入和服務。</span><span class="sxs-lookup"><span data-stu-id="2c762-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="2c762-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-130">線路裝置的鎖定狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="2c762-131"> (如需詳細資訊，請參閱 \_ 在 [**LINEDEVSTATUSFLAGS \_ 常數**](linedevstatusflags--constants.md)中鎖定 LINEDEVSTATUSFLAGS。 ) </span><span class="sxs-lookup"><span data-stu-id="2c762-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE \_ 維護**</span><span class="sxs-lookup"><span data-stu-id="2c762-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-133">正在切換的程式列上執行維護。</span><span class="sxs-lookup"><span data-stu-id="2c762-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="2c762-134">無法使用 TAPI 線上路裝置上運作。</span><span class="sxs-lookup"><span data-stu-id="2c762-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**</span><span class="sxs-lookup"><span data-stu-id="2c762-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-136">訊息等候指示器已關閉。</span><span class="sxs-lookup"><span data-stu-id="2c762-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**</span><span class="sxs-lookup"><span data-stu-id="2c762-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-138">訊息等候指示器已開啟。</span><span class="sxs-lookup"><span data-stu-id="2c762-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="2c762-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-140">線路裝置上的呼叫次數已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**</span><span class="sxs-lookup"><span data-stu-id="2c762-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-142">線路裝置上的未完成通話完成次數已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="2c762-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-144">另一個應用程式已開啟該行。</span><span class="sxs-lookup"><span data-stu-id="2c762-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="2c762-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-146">以下列出的裝置狀態專案已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="2c762-147">應用程式應該檢查目前的裝置狀態，以判斷哪些專案已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**</span><span class="sxs-lookup"><span data-stu-id="2c762-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-149">線路在切換時不在服務中，或已實際中斷連接。</span><span class="sxs-lookup"><span data-stu-id="2c762-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="2c762-150">無法使用 TAPI 線上路裝置上運作。</span><span class="sxs-lookup"><span data-stu-id="2c762-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ 重新初始化**</span><span class="sxs-lookup"><span data-stu-id="2c762-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-152">行裝置設定中的專案已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="2c762-153">若要瞭解這些變更 (，因為新線路裝置的外觀) 應用程式應該重新初始化其使用的 TAPI。</span><span class="sxs-lookup"><span data-stu-id="2c762-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ 已移除**</span><span class="sxs-lookup"><span data-stu-id="2c762-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-155">指出服務提供者已將裝置從系統中移除 (很可能透過 [控制台] 或類似的公用程式) ，透過使用者動作。</span><span class="sxs-lookup"><span data-stu-id="2c762-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="2c762-156">具有此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息通常會緊接在裝置上的 [**行 \_ 關閉**](line-close.md) 訊息後面。</span><span class="sxs-lookup"><span data-stu-id="2c762-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="2c762-157">後續在 TAPI 重新初始化之前存取裝置的嘗試，將會導致 LINEERR \_ NODEVICE 傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c762-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="2c762-158">如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。</span><span class="sxs-lookup"><span data-stu-id="2c762-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE \_ 響鈴**</span><span class="sxs-lookup"><span data-stu-id="2c762-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-160">此參數會告知這一行通知使用者。</span><span class="sxs-lookup"><span data-stu-id="2c762-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="2c762-161">**TAPI：** 服務提供者會重複傳送包含此常數的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息，以在每個通道週期通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c762-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="2c762-162">例如，在美國，服務提供者每隔六秒就會傳送一則包含這個常數的訊息。</span><span class="sxs-lookup"><span data-stu-id="2c762-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="2c762-163">**TSPI：** 在 POTS 裝置上，服務提供者可以在中央辦公室傳送環形電壓時傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="2c762-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="2c762-164">在數位裝置（例如 ISDN）上，如果交換器只產生一個環形要求，服務提供者可能需要合成重複的訊息。</span><span class="sxs-lookup"><span data-stu-id="2c762-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="2c762-165">每次重複訊息時，都應該會顯示增加的信號計數，讓「付費儲存」功能正常運作。</span><span class="sxs-lookup"><span data-stu-id="2c762-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="2c762-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-167">線路裝置的漫遊模式已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE \_ 信號**</span><span class="sxs-lookup"><span data-stu-id="2c762-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-169">信號等級已大幅改變 (行動電話) 。</span><span class="sxs-lookup"><span data-stu-id="2c762-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="2c762-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-171">終端機設定已變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-171">The terminal settings have changed.</span></span> <span data-ttu-id="2c762-172">例如，如果有多個線路裝置共用終端機，就會發生這種情況 (例如，兩行共用電話終端機) 。</span><span class="sxs-lookup"><span data-stu-id="2c762-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2c762-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="2c762-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2c762-174">指出，由於使用者或其他情況所做的設定變更， [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) 結構中的一或多個成員已經變更。</span><span class="sxs-lookup"><span data-stu-id="2c762-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="2c762-175">應用程式應該使用 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) 來讀取更新的結構。</span><span class="sxs-lookup"><span data-stu-id="2c762-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="2c762-176">如果服務提供者將包含此值的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 TAPI 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 **行 \_ LINEDEVSTATE** 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="2c762-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c762-177">備註</span><span class="sxs-lookup"><span data-stu-id="2c762-177">Remarks</span></span>

<span data-ttu-id="2c762-178">無延伸。</span><span class="sxs-lookup"><span data-stu-id="2c762-178">No extensibility.</span></span> <span data-ttu-id="2c762-179">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="2c762-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c762-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c762-180">Requirements</span></span>



| <span data-ttu-id="2c762-181">需求</span><span class="sxs-lookup"><span data-stu-id="2c762-181">Requirement</span></span> | <span data-ttu-id="2c762-182">值</span><span class="sxs-lookup"><span data-stu-id="2c762-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2c762-183">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2c762-183">TAPI version</span></span><br/> | <span data-ttu-id="2c762-184">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2c762-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2c762-185">標頭</span><span class="sxs-lookup"><span data-stu-id="2c762-185">Header</span></span><br/>       | <dl> <span data-ttu-id="2c762-186"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="2c762-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c762-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c762-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c762-188">**行 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="2c762-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="2c762-189">**行 \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="2c762-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="2c762-190">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="2c762-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="2c762-191">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="2c762-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="2c762-192">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="2c762-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="2c762-193">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="2c762-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="2c762-194">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="2c762-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="2c762-195">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="2c762-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




