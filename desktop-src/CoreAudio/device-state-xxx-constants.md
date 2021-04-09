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
# <a name="device_state_xxx-constants"></a>裝置 \_ 狀態 \_ XXX 常數

裝置 \_ 狀態 \_ XXX 常數指出音訊端點裝置的目前狀態。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**裝置 \_狀態為 \_ ACTIVE**</dt> <dt>0x00000001</dt> </dl>             | 音訊端點裝置處於作用中狀態。 亦即，連接至端點裝置的音訊介面卡已存在並已啟用。 此外，如果端點裝置插到介面卡上的插座，則會插入端點裝置。<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**裝置 \_狀態 \_ 停用**</dt> <dt>0x00000002</dt> </dl>       | 音訊端點裝置已停用。 使用者已在 [Windows 多媒體] 控制台中停用裝置，Mmsys.cpl。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**裝置 \_狀態 \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | 音訊端點裝置不存在，因為連接至端點裝置的音訊介面卡已從系統中移除，或使用者已在裝置管理員中停用介面卡裝置。<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**裝置 \_狀態未 \_ 插**</dt> <dt>0x00000008</dt> </dl>    | 音訊端點裝置已插上。 包含端點裝置之插孔的音訊介面卡已存在並已啟用，但端點裝置未插入至該插座。 只有具有插座狀態偵測的裝置才會處於此狀態。 如需有關插座是否存在偵測的詳細資訊，請參閱 [音訊端點裝置](audio-endpoint-devices.md)。<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**裝置 \_STATEMASK \_ 所有**</dt> <dt>0x0000000F</dt> </dl>          | 包含處於作用中、已停用、不存在和已插即用狀態的音訊端點裝置。<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>備註

[**IMMDeviceEnumerator：： EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)、 [**IMMDevice：： >getstate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)和 [**IMMNotificationClient：： OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)方法會使用裝置 \_ 狀態 \_ XXX 常數。 這些方法可讓用戶端取得裝置 \_ 狀態 XXX 常數所代表之任何狀態的端點裝置相關資訊 \_ 。

不過，用戶端可以開啟串流 (例如，藉由取得裝置的 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面，) 只在處於裝置狀態為作用中狀態的裝置 \_ 上 \_ 。

[Windows 多媒體] 控制台（Mmsys.cpl）會顯示系統中的音訊端點裝置。 在 Mmsys.cpl 中停用裝置，會從較高層級音訊 Api 中的裝置探索機制隱藏裝置，但是在停用裝置之前，用戶端可能已具現化的任何資料流程物件都不會失效。 例如，當使用者在 Mmsys.cpl 中停用資料流程時，如果在裝置上播放資料流程，資料流程會繼續播放不受干擾。

相反地，在裝置管理員中停用裝置，實際上會將裝置從系統中移除。

若要使用 Mmsys.cpl 來查看轉譯裝置，請開啟命令提示字元視窗，然後輸入下列命令：

**control mmsys.cpl、0**

若要查看 capture 裝置，請輸入下列命令：

**control mmsys.cpl、，1**

或者，您也可以在 Mmsys.cpl 中，以滑鼠右鍵按一下位於工作列右邊的 [通知] 區域內的喇叭圖示，然後選取 [ **播放裝置** ] 或 [ **錄製裝置**]，以查看轉譯裝置或捕獲裝置。

Mmsys.cpl 一律會顯示處於裝置狀態處於作用中狀態的端點裝置 \_ \_ 。 此外，您可以將它設定為顯示已停用和已中斷連線的裝置。

若要查看裝置狀態為 [ \_ \_ 已停用] 和 [裝置狀態] NOTPRESENT 狀態的端點裝置 \_ \_ ，請在 [Mmsys.cpl] 視窗中按一下滑鼠右鍵，然後選取 [ **顯示已停用的裝置** ] 選項。

若要查看處於「裝置狀態已中斷」狀態的端點裝置 \_ \_ ，請在 [Mmsys.cpl] 視窗上按一下滑鼠右鍵，然後選取 [ **顯示已中斷** 連線的裝置] 選項。

若只要查看處於裝置狀態為作用中狀態的端點裝置 \_ \_ ，請取消選取 [ **顯示已停用的裝置** ] 和 [ **顯示已中斷** 連線的裝置] 選項。

若要啟用或停用 Mmsys.cpl 中的端點裝置，請根據裝置是播放或錄製裝置，按一下 [ **播放** ] 或 [ **錄製**]。 接下來，選取裝置，然後 **按一下 [** 內容]。 在 [ **屬性** ] 視窗的 [ **裝置使用** 方式] 旁，選取 [ **使用此裝置] (啟用)** 或 [ **不要使用此裝置] (停用)**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心音訊常數](core-audio-constants.md)
</dt> <dt>

[**IMMDevice：： >getstate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**IMMDeviceEnumerator 介面**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 




