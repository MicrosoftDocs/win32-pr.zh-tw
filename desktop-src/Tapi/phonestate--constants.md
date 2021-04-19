---
description: PHONESTATE \_ 位旗標常數描述電話裝置的各種狀態專案。
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: 'PHONESTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990147"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="56374-103">PHONESTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="56374-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="56374-104">**PHONESTATE \_** 位旗標常數描述電話裝置的各種狀態專案。</span><span class="sxs-lookup"><span data-stu-id="56374-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="56374-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="56374-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-106">指出，由於使用者或其他情況所做的設定變更， [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 結構中的一或多個成員已經變更。</span><span class="sxs-lookup"><span data-stu-id="56374-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="56374-107">應用程式應該使用 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 來讀取更新的結構。</span><span class="sxs-lookup"><span data-stu-id="56374-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="56374-108">如果服務提供者將包含此值的 [**電話 \_ 狀態**](phone-state.md) 消息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式將會收到 \_ 指定 PHONESTATE 重新初始化的電話狀態訊息 \_ ，要求他們關閉並重新初始化連線到 TAPI 以取得更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="56374-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ 已連線**</span><span class="sxs-lookup"><span data-stu-id="56374-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-110">手機裝置與 TAPI 之間的連線剛剛進行。</span><span class="sxs-lookup"><span data-stu-id="56374-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="56374-111">這會發生在第一次叫用 TAPI 時，或連接電話與電腦的連線已插入 TAPI 作用中時。</span><span class="sxs-lookup"><span data-stu-id="56374-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="56374-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-113">手機的裝置特定資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE 已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="56374-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-115">電話裝置與 TAPI 之間的連線已中斷。</span><span class="sxs-lookup"><span data-stu-id="56374-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="56374-116">當 TAPI 正在使用中時，將電話設定連接到電腦的連線將會發生。</span><span class="sxs-lookup"><span data-stu-id="56374-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="56374-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-118">手機的顯示已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="56374-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-120">話筒的麥克風增益設定已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="56374-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-122">話筒 hookswitch 狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="56374-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-124">話筒的喇叭音量設定已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="56374-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-126">耳機的 hookswitch 狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="56374-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-128">耳機的麥克風增益設定已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="56374-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-130">耳機的喇叭音量設定已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE \_ 燈**</span><span class="sxs-lookup"><span data-stu-id="56374-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-132">電話指示燈已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE \_ 監視器**</span><span class="sxs-lookup"><span data-stu-id="56374-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-134">電話裝置的監視器數目。</span><span class="sxs-lookup"><span data-stu-id="56374-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="56374-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-136">以下列出的電話狀態專案已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="56374-137">應用程式應該檢查目前的電話狀態，以判斷哪些專案已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="56374-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-139">電話裝置的擁有者數目。</span><span class="sxs-lookup"><span data-stu-id="56374-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE \_ 重新初始化**</span><span class="sxs-lookup"><span data-stu-id="56374-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-141">手機裝置設定中的專案已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="56374-142">為了留意這些變更 (當) 的新電話裝置外觀時，應用程式應該重新初始化其使用的 TAPI。</span><span class="sxs-lookup"><span data-stu-id="56374-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ 已移除**</span><span class="sxs-lookup"><span data-stu-id="56374-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-144">指出服務提供者已將裝置從系統中移除 (很可能透過 [控制台] 或類似的公用程式) ，透過使用者動作。</span><span class="sxs-lookup"><span data-stu-id="56374-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="56374-145">具有此值的 [**電話 \_ 狀態**](phone-state.md) 消息通常會緊接在裝置上的 [**電話 \_ 關閉**](phone-close.md) 訊息後面。</span><span class="sxs-lookup"><span data-stu-id="56374-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="56374-146">後續在 TAPI 重新初始化之前存取裝置的嘗試，將會導致 PHONEERR \_ NODEVICE 傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="56374-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="56374-147">如果服務提供者將 \_ 包含此值的電話狀態訊息傳送給 tapi，tapi 會將它傳遞到已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。</span><span class="sxs-lookup"><span data-stu-id="56374-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE \_ RESUME**</span><span class="sxs-lookup"><span data-stu-id="56374-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-149">在暫停一段時間之後，應用程式會繼續使用手機裝置。</span><span class="sxs-lookup"><span data-stu-id="56374-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**</span><span class="sxs-lookup"><span data-stu-id="56374-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-151">手機的響鈴模式已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**</span><span class="sxs-lookup"><span data-stu-id="56374-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-153">手機的響鈴音量已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="56374-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-155">話筒的 hookswitch 狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**</span><span class="sxs-lookup"><span data-stu-id="56374-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-157">話筒的麥克風增益設定狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**</span><span class="sxs-lookup"><span data-stu-id="56374-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-159">話筒的喇叭音量設定已變更。</span><span class="sxs-lookup"><span data-stu-id="56374-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="56374-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="56374-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="56374-161">應用程式的電話使用已暫時暫止。</span><span class="sxs-lookup"><span data-stu-id="56374-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56374-162">備註</span><span class="sxs-lookup"><span data-stu-id="56374-162">Remarks</span></span>

<span data-ttu-id="56374-163">無延伸。</span><span class="sxs-lookup"><span data-stu-id="56374-163">No extensibility.</span></span> <span data-ttu-id="56374-164">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="56374-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="56374-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="56374-165">Requirements</span></span>



| <span data-ttu-id="56374-166">需求</span><span class="sxs-lookup"><span data-stu-id="56374-166">Requirement</span></span> | <span data-ttu-id="56374-167">值</span><span class="sxs-lookup"><span data-stu-id="56374-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="56374-168">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="56374-168">TAPI version</span></span><br/> | <span data-ttu-id="56374-169">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="56374-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="56374-170">標頭</span><span class="sxs-lookup"><span data-stu-id="56374-170">Header</span></span><br/>       | <dl> <span data-ttu-id="56374-171"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="56374-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56374-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56374-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56374-173">**電話 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="56374-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="56374-174">**電話 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="56374-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="56374-175">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="56374-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="56374-176">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="56374-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




