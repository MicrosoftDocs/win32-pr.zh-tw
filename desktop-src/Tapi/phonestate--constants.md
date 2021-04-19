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
# <a name="phonestate_-constants"></a>PHONESTATE \_ 常數

**PHONESTATE \_** 位旗標常數描述電話裝置的各種狀態專案。

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



指出，由於使用者或其他情況所做的設定變更， [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 結構中的一或多個成員已經變更。 應用程式應該使用 [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) 來讀取更新的結構。 如果服務提供者將包含此值的 [**電話 \_ 狀態**](phone-state.md) 消息傳送給 tapi，tapi 會將它傳遞給已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式將會收到 \_ 指定 PHONESTATE 重新初始化的電話狀態訊息 \_ ，要求他們關閉並重新初始化連線到 TAPI 以取得更新的資訊。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ 已連線**
</dt> <dd> <dl> <dt>



手機裝置與 TAPI 之間的連線剛剛進行。 這會發生在第一次叫用 TAPI 時，或連接電話與電腦的連線已插入 TAPI 作用中時。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



手機的裝置特定資訊已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE 已 \_ 中斷連線**
</dt> <dd> <dl> <dt>



電話裝置與 TAPI 之間的連線已中斷。 當 TAPI 正在使用中時，將電話設定連接到電腦的連線將會發生。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE \_ 顯示**
</dt> <dd> <dl> <dt>



手機的顯示已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**
</dt> <dd> <dl> <dt>



話筒的麥克風增益設定已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



話筒 hookswitch 狀態已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**
</dt> <dd> <dl> <dt>



話筒的喇叭音量設定已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



耳機的 hookswitch 狀態已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**
</dt> <dd> <dl> <dt>



耳機的麥克風增益設定已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**
</dt> <dd> <dl> <dt>



耳機的喇叭音量設定已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE \_ 燈**
</dt> <dd> <dl> <dt>



電話指示燈已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE \_ 監視器**
</dt> <dd> <dl> <dt>



電話裝置的監視器數目。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ 其他**
</dt> <dd> <dl> <dt>



以下列出的電話狀態專案已變更。 應用程式應該檢查目前的電話狀態，以判斷哪些專案已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE \_ 擁有者**
</dt> <dd> <dl> <dt>



電話裝置的擁有者數目。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE \_ 重新初始化**
</dt> <dd> <dl> <dt>



手機裝置設定中的專案已變更。 為了留意這些變更 (當) 的新電話裝置外觀時，應用程式應該重新初始化其使用的 TAPI。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ 已移除**
</dt> <dd> <dl> <dt>



指出服務提供者已將裝置從系統中移除 (很可能透過 [控制台] 或類似的公用程式) ，透過使用者動作。 具有此值的 [**電話 \_ 狀態**](phone-state.md) 消息通常會緊接在裝置上的 [**電話 \_ 關閉**](phone-close.md) 訊息後面。 後續在 TAPI 重新初始化之前存取裝置的嘗試，將會導致 PHONEERR \_ NODEVICE 傳回給應用程式。 如果服務提供者將 \_ 包含此值的電話狀態訊息傳送給 tapi，tapi 會將它傳遞到已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式不會收到任何通知。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE \_ RESUME**
</dt> <dd> <dl> <dt>



在暫停一段時間之後，應用程式會繼續使用手機裝置。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**
</dt> <dd> <dl> <dt>



手機的響鈴模式已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**
</dt> <dd> <dl> <dt>



手機的響鈴音量已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**
</dt> <dd> <dl> <dt>



話筒的 hookswitch 狀態已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**
</dt> <dd> <dl> <dt>



話筒的麥克風增益設定狀態已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**
</dt> <dd> <dl> <dt>



話筒的喇叭音量設定已變更。


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE \_ 暫停**
</dt> <dd> <dl> <dt>



應用程式的電話使用已暫時暫止。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**電話 \_ 關閉**](phone-close.md)
</dt> <dt>

[**電話 \_ 狀態**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




