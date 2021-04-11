---
description: 裝置 \_ 狀態 \_ XXX 常數指出音訊端點裝置的目前狀態。
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: 'DEVICE_STATE_XXX 常數 (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688556"
---
# <a name="device_state_xxx-constants"></a><span data-ttu-id="7c108-103">裝置 \_ 狀態 \_ XXX 常數</span><span class="sxs-lookup"><span data-stu-id="7c108-103">DEVICE\_STATE\_XXX Constants</span></span>

<span data-ttu-id="7c108-104">裝置 \_ 狀態 \_ XXX 常數指出音訊端點裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7c108-104">The DEVICE\_STATE\_XXX constants indicate the current state of an audio endpoint device.</span></span>



| <span data-ttu-id="7c108-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="7c108-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="7c108-106">Description</span><span class="sxs-lookup"><span data-stu-id="7c108-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <span data-ttu-id="7c108-107"><dt>**裝置 \_狀態為 \_ ACTIVE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-107"><dt>**DEVICE\_STATE\_ACTIVE**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="7c108-108">音訊端點裝置處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="7c108-108">The audio endpoint device is active.</span></span> <span data-ttu-id="7c108-109">亦即，連接至端點裝置的音訊介面卡已存在並已啟用。</span><span class="sxs-lookup"><span data-stu-id="7c108-109">That is, the audio adapter that connects to the endpoint device is present and enabled.</span></span> <span data-ttu-id="7c108-110">此外，如果端點裝置插到介面卡上的插座，則會插入端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-110">In addition, if the endpoint device plugs into a jack on the adapter, then the endpoint device is plugged in.</span></span><br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <span data-ttu-id="7c108-111"><dt>**裝置 \_狀態 \_ 停用**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-111"><dt>**DEVICE\_STATE\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="7c108-112">音訊端點裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="7c108-112">The audio endpoint device is disabled.</span></span> <span data-ttu-id="7c108-113">使用者已在 [Windows 多媒體] 控制台中停用裝置，Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="7c108-113">The user has disabled the device in the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="7c108-114">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7c108-114">For more information, see Remarks.</span></span><br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <span data-ttu-id="7c108-115"><dt>**裝置 \_狀態 \_ NOTPRESENT**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-115"><dt>**DEVICE\_STATE\_NOTPRESENT**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="7c108-116">音訊端點裝置不存在，因為連接至端點裝置的音訊介面卡已從系統中移除，或使用者已在裝置管理員中停用介面卡裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-116">The audio endpoint device is not present because the audio adapter that connects to the endpoint device has been removed from the system, or the user has disabled the adapter device in Device Manager.</span></span><br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <span data-ttu-id="7c108-117"><dt>**裝置 \_狀態未 \_ 插**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-117"><dt>**DEVICE\_STATE\_UNPLUGGED**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="7c108-118">音訊端點裝置已插上。</span><span class="sxs-lookup"><span data-stu-id="7c108-118">The audio endpoint device is unplugged.</span></span> <span data-ttu-id="7c108-119">包含端點裝置之插孔的音訊介面卡已存在並已啟用，但端點裝置未插入至該插座。</span><span class="sxs-lookup"><span data-stu-id="7c108-119">The audio adapter that contains the jack for the endpoint device is present and enabled, but the endpoint device is not plugged into the jack.</span></span> <span data-ttu-id="7c108-120">只有具有插座狀態偵測的裝置才會處於此狀態。</span><span class="sxs-lookup"><span data-stu-id="7c108-120">Only a device with jack-presence detection can be in this state.</span></span> <span data-ttu-id="7c108-121">如需有關插座是否存在偵測的詳細資訊，請參閱 [音訊端點裝置](audio-endpoint-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="7c108-121">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span><br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <span data-ttu-id="7c108-122"><dt>**裝置 \_STATEMASK \_ 所有**</dt> <dt>0x0000000F</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-122"><dt>**DEVICE\_STATEMASK\_ALL**</dt> <dt>0x0000000F</dt></span></span> </dl>          | <span data-ttu-id="7c108-123">包含處於作用中、已停用、不存在和已插即用狀態的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-123">Includes audio endpoint devices in all states active, disabled, not present, and unplugged.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="7c108-124">備註</span><span class="sxs-lookup"><span data-stu-id="7c108-124">Remarks</span></span>

<span data-ttu-id="7c108-125">[**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)、 [**IMMDevice：： >getstate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)和 [**IMMNotificationClient：： OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)方法會使用裝置 \_ 狀態 \_ XXX 常數。</span><span class="sxs-lookup"><span data-stu-id="7c108-125">The [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate), and [**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) methods use the DEVICE\_STATE\_XXX constants.</span></span> <span data-ttu-id="7c108-126">這些方法可讓用戶端取得裝置 \_ 狀態 XXX 常數所代表之任何狀態的端點裝置相關資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7c108-126">These methods enable clients to obtain information about endpoint devices that are in any of the states represented by the DEVICE\_STATE\_XXX constants.</span></span>

<span data-ttu-id="7c108-127">不過，用戶端可以開啟串流 (例如，藉由取得裝置的 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，) 只在處於裝置狀態為作用中狀態的裝置 \_ 上 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7c108-127">However, a client can open a stream (for example, by obtaining an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface for the device) only on a device that is in the DEVICE\_STATE\_ACTIVE state.</span></span>

<span data-ttu-id="7c108-128">[Windows 多媒體] 控制台（Mmsys.cpl）會顯示系統中的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-128">The Windows multimedia control panel, Mmsys.cpl, displays the audio endpoint devices in the system.</span></span> <span data-ttu-id="7c108-129">在 Mmsys.cpl 中停用裝置，會從較高層級音訊 Api 中的裝置探索機制隱藏裝置，但是在停用裝置之前，用戶端可能已具現化的任何資料流程物件都不會失效。</span><span class="sxs-lookup"><span data-stu-id="7c108-129">Disabling a device in Mmsys.cpl hides the device from the device-discovery mechanisms in higher-level audio APIs, but it does not invalidate any stream objects that a client might have instantiated before the device was disabled.</span></span> <span data-ttu-id="7c108-130">例如，當使用者在 Mmsys.cpl 中停用資料流程時，如果在裝置上播放資料流程，資料流程會繼續播放不受干擾。</span><span class="sxs-lookup"><span data-stu-id="7c108-130">For example, if a stream is playing on the device when the user disables it in Mmsys.cpl, the stream continues to play uninterrupted.</span></span>

<span data-ttu-id="7c108-131">相反地，在裝置管理員中停用裝置，實際上會將裝置從系統中移除。</span><span class="sxs-lookup"><span data-stu-id="7c108-131">In contrast, disabling a device in Device Manager effectively removes the device from the system.</span></span>

<span data-ttu-id="7c108-132">若要使用 Mmsys.cpl 來查看轉譯裝置，請開啟命令提示字元視窗，然後輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="7c108-132">To use Mmsys.cpl to view the rendering devices, open a Command Prompt window and enter the following command:</span></span>

<span data-ttu-id="7c108-133">**control mmsys.cpl、0**</span><span class="sxs-lookup"><span data-stu-id="7c108-133">**control mmsys.cpl,,0**</span></span>

<span data-ttu-id="7c108-134">若要查看 capture 裝置，請輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="7c108-134">To view the capture devices, enter the following command:</span></span>

<span data-ttu-id="7c108-135">**control mmsys.cpl、，1**</span><span class="sxs-lookup"><span data-stu-id="7c108-135">**control mmsys.cpl,,1**</span></span>

<span data-ttu-id="7c108-136">或者，您也可以在 Mmsys.cpl 中，以滑鼠右鍵按一下位於工作列右邊的 [通知] 區域內的喇叭圖示，然後選取 [ **播放裝置** ] 或 [ **錄製裝置**]，以查看轉譯裝置或捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-136">Alternatively, you can view the rendering devices or the capture devices in Mmsys.cpl by right-clicking the speaker icon in the notification area, which is located on the right side of the taskbar, and selecting **Playback Devices** or **Recording Devices**.</span></span>

<span data-ttu-id="7c108-137">Mmsys.cpl 一律會顯示處於裝置狀態處於作用中狀態的端點裝置 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7c108-137">Mmsys.cpl always displays endpoint devices that are in the DEVICE\_STATE\_ACTIVE state.</span></span> <span data-ttu-id="7c108-138">此外，您可以將它設定為顯示已停用和已中斷連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="7c108-138">In addition, it can be configured to display disabled and disconnected devices.</span></span>

<span data-ttu-id="7c108-139">若要查看裝置狀態為 [ \_ \_ 已停用] 和 [裝置狀態] NOTPRESENT 狀態的端點裝置 \_ \_ ，請在 [Mmsys.cpl] 視窗中按一下滑鼠右鍵，然後選取 [ **顯示已停用的裝置** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="7c108-139">To view endpoint devices that are in the DEVICE\_STATE\_DISABLED and DEVICE\_STATE\_NOTPRESENT states, right-click in the Mmsys.cpl window and select the **Show Disabled Devices** option.</span></span>

<span data-ttu-id="7c108-140">若要查看處於「裝置狀態已中斷」狀態的端點裝置 \_ \_ ，請在 [Mmsys.cpl] 視窗上按一下滑鼠右鍵，然後選取 [ **顯示已中斷** 連線的裝置] 選項。</span><span class="sxs-lookup"><span data-stu-id="7c108-140">To view endpoint devices that are in the DEVICE\_STATE\_UNPLUGGED state, right-click in the Mmsys.cpl window and select the **Show Disconnected Devices** option.</span></span>

<span data-ttu-id="7c108-141">若只要查看處於裝置狀態為作用中狀態的端點裝置 \_ \_ ，請取消選取 [ **顯示已停用的裝置** ] 和 [ **顯示已中斷** 連線的裝置] 選項。</span><span class="sxs-lookup"><span data-stu-id="7c108-141">To view only endpoint devices that are in the DEVICE\_STATE\_ACTIVE state, deselect both the **Show Disabled Devices** and **Show Disconnected Devices** options.</span></span>

<span data-ttu-id="7c108-142">若要啟用或停用 Mmsys.cpl 中的端點裝置，請根據裝置是播放或錄製裝置，按一下 [ **播放** ] 或 [ **錄製**]。</span><span class="sxs-lookup"><span data-stu-id="7c108-142">To enable or disable an endpoint device in Mmsys.cpl, click **Playback** or **Recording**, depending on whether the device is a playback or recording device.</span></span> <span data-ttu-id="7c108-143">接下來，選取裝置，然後 **按一下 [** 內容]。</span><span class="sxs-lookup"><span data-stu-id="7c108-143">Next, select the device and click **Properties**.</span></span> <span data-ttu-id="7c108-144">在 [ **屬性** ] 視窗的 [ **裝置使用** 方式] 旁，選取 [ **使用此裝置] (啟用)** 或 [ **不要使用此裝置] (停用)**。</span><span class="sxs-lookup"><span data-stu-id="7c108-144">In the **Properties** window, next to **Device usage**, select either **Use this device (enable)** or **Don't use this device (disable)**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c108-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c108-145">Requirements</span></span>



| <span data-ttu-id="7c108-146">需求</span><span class="sxs-lookup"><span data-stu-id="7c108-146">Requirement</span></span> | <span data-ttu-id="7c108-147">值</span><span class="sxs-lookup"><span data-stu-id="7c108-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c108-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c108-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7c108-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c108-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c108-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c108-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7c108-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c108-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c108-152">標頭</span><span class="sxs-lookup"><span data-stu-id="7c108-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c108-153"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c108-153"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c108-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c108-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c108-155">核心音訊常數</span><span class="sxs-lookup"><span data-stu-id="7c108-155">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="7c108-156">**IMMDevice：： >getstate**</span><span class="sxs-lookup"><span data-stu-id="7c108-156">**IMMDevice::GetState**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[<span data-ttu-id="7c108-157">**IMMDeviceEnumerator 介面**</span><span class="sxs-lookup"><span data-stu-id="7c108-157">**IMMDeviceEnumerator Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="7c108-158">**IMMDeviceEnumerator::EnumAudioEndpoints**</span><span class="sxs-lookup"><span data-stu-id="7c108-158">**IMMDeviceEnumerator::EnumAudioEndpoints**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[<span data-ttu-id="7c108-159">**IMMNotificationClient::OnDeviceStateChanged**</span><span class="sxs-lookup"><span data-stu-id="7c108-159">**IMMNotificationClient::OnDeviceStateChanged**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




