---
description: 指定用戶端在初始化串流期間可以指派給音訊串流的特性。
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: 'AUDCLNT_STREAMFLAGS_XXX 常數 (Audiosessiontypes) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84817607092c179286f47eb35ef51f5e0f82d44211bcd2345ca3d27ee06b0e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407361"
---
# <a name="audclnt_streamflags_xxx-constants"></a>AUDCLNT \_ STREAMFLAGS \_ XXX 常數

指定用戶端在初始化串流期間可以指派給音訊串流的特性。



| 常數/值                                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | 音訊串流將會是跨進程音訊會話的成員。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ 回送**</dt> <dt>0x00020000</dt> </dl>                                                   | 音訊串流將以回送模式運作。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ >app >eventcallback**</dt> <dt>0x00040000</dt> </dl>                                    | 用戶端處理音訊緩衝區會是事件驅動的。 如需詳細資訊，請參閱＜備註＞。 <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ NOPERSIST**</dt> <dt>0x00080000</dt> </dl>                                                | 音訊會話的音量和靜音設定在應用程式重新開機時不會持續保存。 如需詳細資訊，請參閱＜備註＞。<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | 這個常數是 Windows 7 的新功能。 資料流程的取樣率會調整為應用程式所指定的速率。 如需詳細資訊，請參閱＜備註＞。 <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | 您可以視需要插入通道 matrixer 和取樣率轉換器，以在提供給 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 和音訊引擎混合格式的未壓縮格式之間進行轉換。<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_STREAMFLAGS \_ SRC \_ 預設 \_ 品質**</dt> <dt>0x08000000</dt> </dl>                | 與 **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM** 搭配使用時，會使用比預設轉換更高品質的取樣率轉換器，但會使用較高的效能成本。 如果音訊最終是要讓人類聽到，而非其他案例（例如，提取無回應或擴展計量），就應該使用這項功能。<br/> |



## <a name="remarks"></a>備註

[**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)方法和 [**DIRECTX \_ 音訊 \_ 啟用 \_ 參數**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params)結構使用 AUDCLNT \_ STREAMFLAGS \_ XXX 常數。

AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS 旗標表示資料流程的音訊會話是跨進程會話。 跨進程會話可以接受來自多個進程的資料流程。 如果兩個不同進程中的兩個應用程式呼叫 **IAudioClient：： Initialize** （具有相同的會話 guid），而這兩個應用程式都設定了 AUDCLNT \_ SHAREMODE \_ CROSSPROCESS 旗標，則音訊引擎會將其串流指派給相同的跨進程會話。 此旗標會覆寫預設行為，也就是將資料流程指派給進程特定的會話，而不是跨進程會話。 AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS 旗標位與獨佔模式不相容。 如需跨進程會話的詳細資訊，請參閱 [音訊會話](audio-sessions.md)。

AUDCLNT \_ STREAMFLAGS \_ 回送旗標可啟用回送記錄。 在回送記錄中，音訊引擎會將轉譯端點裝置播放的音訊串流複製到音訊端點緩衝區，讓 [WASAPI](wasapi.md) 用戶端可以捕獲資料流程。 如果設定此旗標， **IAudioClient：： Initialize** 方法會嘗試在轉譯裝置上開啟擷取緩衝區。 此旗標只適用于轉譯裝置，而且只有在 **Initialize** 呼叫將 *ShareMode* 參數設定為 AUDCLNT ShareMode SHARED 時才有效 \_ \_ 。 否則 **初始化** 呼叫將會失敗。 如果呼叫成功，用戶端可以呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法來取得轉譯裝置上的 [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) 介面。 如需詳細資訊，請參閱 [回送記錄](loopback-recording.md)。

AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback 旗標可啟用事件驅動的緩衝。 如果用戶端在初始化資料流程的 **IAudioClient：： Initialize** 呼叫中設定這個旗標，則用戶端必須接著呼叫 [**IAudioClient：： SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) 方法，以提供資料流程的事件控制碼。 資料流程啟動之後，音訊引擎會通知事件控制碼，在每次緩衝區準備好供用戶端處理時通知用戶端。 WASAPI 支援轉譯和擷取緩衝區的事件驅動緩衝。 共用模式和獨佔模式串流都可以使用事件驅動的緩衝。 如需使用 AUDCLNT STREAMFLAGS >app >eventcallback 旗標的程式碼範例 \_ \_ ，請參閱 [獨佔模式資料流程](exclusive-mode-streams.md)。

AUDCLNT \_ STREAMFLAGS \_ NOPERSIST 旗標會停用包含轉譯資料流程之會話的磁片區和靜音設定的持續性。 根據預設，轉譯會話的音量層級和靜音狀態會在應用程式重新開機時持續存在。 捕捉會話的磁片區層級和靜音狀態永遠不會持續。 如需會話磁片區和靜音設定持續性的詳細資訊，請參閱 [音訊會話](audio-sessions.md)。

AUDCLNT \_ STREAMFLAGS \_ RATEADJUST 旗標可讓應用程式取得 [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) 介面的參考，該介面是用來設定資料流程的取樣率。 若要取得此介面的指標，應用程式必須使用此旗標來初始化音訊用戶端，然後藉由指定 **IID \_ IAudioClockAdjustment** 識別碼來呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 。 若要設定新的取樣率，請呼叫 [**IAudioClockAdjustment：： SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate)。 此旗標只對轉譯裝置有效。 否則， **GetService** 呼叫會失敗，並出現錯誤碼 AUDCLNT \_ E \_ 錯誤的 \_ 端點 \_ 類型。 應用程式也必須將 *ShareMode* 參數設定為在 \_ \_ [**INITIALIZE**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 呼叫期間共用的 AUDCLNT ShareMode。 如果音訊用戶端不在共用模式中， **SetSampleRate** 就會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Audiosessiontypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心音訊常數](core-audio-constants.md)
</dt> <dt>

[**IAudioCaptureClient 介面**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




