---
description: XAudio2 常數，可指定預設參數、最大值和旗標。
ms.assetid: 074ac40e-a17e-7366-1954-6699407b82f7
title: 'XAudio2 界限值和旗標 (Xaudio2 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59f229ea406eb5bf6c6b3f5c124d6d0d19c047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984340"
---
# <a name="xaudio2-boundary-values-and-flags"></a>XAudio2 界限值和旗標

XAudio2 常數，可指定預設參數、最大值和旗標。

**XAudio2 界限值**



| 常數                                                                                                                                                                                                     | 描述                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_MAX_BUFFER_BYTES"></span><span id="xaudio2_max_buffer_bytes"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 緩衝區 \_ 位元組數**</dt> </dl>             | [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)允許的最大值。AudioBytes.<br/>                                                      |
| <span id="XAUDIO2_MAX_QUEUED_BUFFERS"></span><span id="xaudio2_max_queued_buffers"></span><dl> <dt>**XAUDIO2 \_ \_ 佇列 \_ 緩衝區上限**</dt> </dl>       | 語音佇列中允許的最大緩衝區。<br/>                                                                                            |
| <span id="XAUDIO2_MAX_BUFFERS_SYSTEM"></span><span id="xaudio2_max_buffers_system"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 緩衝區 \_ 系統**</dt> </dl>       | 系統執行緒 (只 Xbox 360) 的緩衝區數目上限。<br/>                                                                          |
| <span id="XAUDIO2_MAX_AUDIO_CHANNELS"></span><span id="xaudio2_max_audio_channels"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 音訊 \_ 頻道**</dt> </dl>       | **WAVEFORMATEX. nChannels** 允許的最大值。<br/>                                                                                |
| <span id="XAUDIO2_MIN_SAMPLE_RATE"></span><span id="xaudio2_min_sample_rate"></span><dl> <dt>**XAUDIO2 \_ MIN \_ 取樣 \_ 率**</dt> </dl>                | 支援的最小音訊取樣率。<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_SAMPLE_RATE"></span><span id="xaudio2_max_sample_rate"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 取樣 \_ 率**</dt> </dl>                | 支援的最大音訊取樣率。<br/>                                                                                                 |
| <span id="XAUDIO2_MAX_VOLUME_LEVEL"></span><span id="xaudio2_max_volume_level"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 磁片區 \_ 層級**</dt> </dl>             | 允許的磁片區層級上限。<br/>                                                                                                        |
| <span id="XAUDIO2_MIN_FREQ_RATIO"></span><span id="xaudio2_min_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ 最小 \_ 頻率 \_ 比率**</dt> </dl>                   | 來源語音中允許的最小頻率比率。<br/>                                                                                   |
| <span id="XAUDIO2_MAX_FREQ_RATIO"></span><span id="xaudio2_max_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 頻率 \_ 比率**</dt> </dl>                   | 來源語音中允許的最大頻率比率。<br/>                                                                                   |
| <span id="XAUDIO2_DEFAULT_FREQ_RATIO"></span><span id="xaudio2_default_freq_ratio"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ 頻率 \_ 比率**</dt> </dl>       | [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)的 **MaxFrequencyRatio** 引數的預設值。<br/> |
| <span id="XAUDIO2_MAX_FILTER_ONEOVERQ"></span><span id="xaudio2_max_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ MAX \_ FILTER \_ ONEOVERQ**</dt> </dl>    | [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)的最大值。**OneOverQ**。<br/>                                     |
| <span id="XAUDIO2_MAX_FILTER_FREQUENCY"></span><span id="xaudio2_max_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 篩選 \_ 頻率**</dt> </dl> | [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)的最大值。**頻率**。<br/>                                    |
| <span id="XAUDIO2_MAX_LOOP_COUNT"></span><span id="xaudio2_max_loop_count"></span><dl> <dt>**XAUDIO2 \_ 最大 \_ 迴圈 \_ 計數**</dt> </dl>                   | 不會被視為 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)無限迴圈的最大值。**LoopCount**。<br/>              |
| <span id="XAUDIO2_MAX_INSTANCES"></span><span id="xaudio2_max_instances"></span><dl> <dt>**XAUDIO2 \_ 實例數目上限 \_**</dt> </dl>                       | Xbox 360 上允許的 XAudio2 並行實例數上限。<br/>                                                                       |



**XAudio2 具有特殊意義的值**



| 常數                                                                                                                                                                                              | 描述                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_COMMIT_NOW"></span><span id="xaudio2_commit_now"></span><dl> <dt>**\_立即 XAUDIO2 認可 \_**</dt> </dl>                         | 當做具有 OperationSet 引數之方法的參數使用。 如需詳細資訊，請參閱 [XAudio2 操作集合](xaudio2-operation-sets.md) 。<br/>                  |
| <span id="XAUDIO2_COMMIT_ALL"></span><span id="xaudio2_commit_all"></span><dl> <dt>**XAUDIO2 \_ 認可 \_ 全部**</dt> </dl>                         | 當做 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)中的參數使用。<br/>                                                                   |
| <span id="XAUDIO2_INVALID_OPSET"></span><span id="xaudio2_invalid_opset"></span><dl> <dt>**XAUDIO2 \_ 不正確 \_ OPSET**</dt> </dl>                | 指定不正確 OperationSet 引數值。 如需詳細資訊，請參閱 [XAudio2 操作集合](xaudio2-operation-sets.md) 。<br/>                         |
| <span id="XAUDIO2_NO_LOOP_REGION"></span><span id="xaudio2_no_loop_region"></span><dl> <dt>**XAUDIO2 \_ 無 \_ 迴圈 \_ 區域**</dt> </dl>            | 指定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)中未使用的迴圈區域。**LoopCount**。<br/>                                                                    |
| <span id="XAUDIO2_LOOP_INFINITE"></span><span id="xaudio2_loop_infinite"></span><dl> <dt>**XAUDIO2 \_ 迴圈 \_ 無限**</dt> </dl>                | 指定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)中使用的無限迴圈。**LoopCount**。<br/>                                                                  |
| <span id="XAUDIO2_DEFAULT_CHANNELS"></span><span id="xaudio2_default_channels"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ 通道**</dt> </dl>       | 指定目前平臺的預設通道數目（用於 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)）。<br/> |
| <span id="XAUDIO2_DEFAULT_SAMPLERATE"></span><span id="xaudio2_default_samplerate"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ SAMPLERATE**</dt> </dl> | 指定目前平臺的預設取樣率，用於 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)。<br/>        |



**XAudio2 旗標**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_DEBUG_ENGINE"></span><span id="xaudio2_debug_engine"></span><dl> <dt><strong>XAUDIO2_DEBUG_ENGINE</strong></dt> </dl></td>
<td style="text-align: left;">指定應使用音訊引擎的 debug/checked 版本，而不是發行版本。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。<br/>
<blockquote>
[!Note]<br />
Windows 8 或 Windows 10 不支援此旗標。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOPITCH"></span><span id="xaudio2_voice_nopitch"></span><dl> <dt><strong>XAUDIO2_VOICE_NOPITCH</strong></dt> </dl></td>
<td style="text-align: left;">指定來源語音不會使用移動音調，請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_NOSRC"></span><span id="xaudio2_voice_nosrc"></span><dl> <dt><strong>XAUDIO2_VOICE_NOSRC</strong></dt> </dl></td>
<td style="text-align: left;">指定來源語音上沒有可用的取樣率轉換，語音的輸出必須具有相同的取樣率。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_VOICE_USEFILTER"></span><span id="xaudio2_voice_usefilter"></span><dl> <dt><strong>XAUDIO2_VOICE_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">指定要在語音上使用篩選效果。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice"><strong>IXAudio2：： CreateSourceVoice</strong></a> 和 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice"><strong>IXAudio2：： CreateSubmixVoice</strong></a>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_PLAY_TAILS"></span><span id="xaudio2_play_tails"></span><dl> <dt><strong>XAUDIO2_PLAY_TAILS</strong></dt> </dl></td>
<td style="text-align: left;">指定語音在停止之後，應繼續發出效果輸出。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop"><strong>IXAudio2SourceVoice：： Stop</strong></a>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_END_OF_STREAM"></span><span id="xaudio2_end_of_stream"></span><dl> <dt><strong>XAUDIO2_END_OF_STREAM</strong></dt> </dl></td>
<td style="text-align: left;">表示資料流程中的最後一個緩衝區。 請參閱 <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer"><strong>XAUDIO2_BUFFER</strong></a>。<strong>旗標</strong>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_STOP_ENGINE_WHEN_IDLE"></span><span id="xaudio2_stop_engine_when_idle"></span><dl> <dt><strong>XAUDIO2_STOP_ENGINE_WHEN_IDLE</strong></dt> </dl></td>
<td style="text-align: left;">指定當語音啟動時，音訊引擎應該停止，並在啟動時啟動。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_SEND_USEFILTER"></span><span id="xaudio2_send_usefilter"></span><dl> <dt><strong>XAUDIO2_SEND_USEFILTER</strong></dt> </dl></td>
<td style="text-align: left;">表示篩選準則應該用於語音傳送。 請參閱 <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor"><strong>XAUDIO2_SEND_DESCRIPTOR</strong></a>。<strong>旗標</strong>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="XAUDIO2_1024_QUANTUM"></span><span id="xaudio2_1024_quantum"></span><dl> <dt><strong>XAUDIO2_1024_QUANTUM</strong></dt> </dl></td>
<td style="text-align: left;">在 48KHz) 指定非預設的處理量子 21.33 ms (1024 範例。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create"><strong>XAudio2Create</strong></a>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT"></span><span id="xaudio2_no_virtual_audio_client"></span><dl> <dt><strong>XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT</strong></dt> </dl></td>
<td style="text-align: left;">指定不應使用虛擬音訊用戶端。 請參閱 <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice"><strong>IXAudio2：： CreateMasteringVoice</strong></a>。<br/>
<blockquote>
[!Note]<br />
在行動裝置家族中的裝置上，一律會使用虛擬音訊用戶端，不論是否使用此旗標。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



**XAudio2 內建聲音篩選器的預設參數**



| 常數                                                                                                                                                                                                                 | 描述                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_DEFAULT_FILTER_TYPE"></span><span id="xaudio2_default_filter_type"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ 類型**</dt> </dl>                | 指定要搭配語音和語音傳送使用的預設篩選類型。<br/>          |
| <span id="XAUDIO2_DEFAULT_FILTER_FREQUENCY"></span><span id="xaudio2_default_filter_frequency"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ 頻率**</dt> </dl> | 指定要搭配語音和語音傳送使用的預設篩選頻率。<br/>     |
| <span id="XAUDIO2_DEFAULT_FILTER_ONEOVERQ"></span><span id="xaudio2_default_filter_oneoverq"></span><dl> <dt>**XAUDIO2 \_ 預設 \_ 篩選 \_ ONEOVERQ**</dt> </dl>    | 指定要搭配語音和語音傳送使用之衰減的預設篩選速率。<br/> |



## <a name="remarks"></a>備註

### <a name="platform-requirements"></a>平台需求

Windows 10 (XAudio 2.9) ;Windows 8、Windows Phone 8 (XAudio 2.8) ;DirectX SDK (XAudio 2.7) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Xaudio2。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XAudio2：：常數](constants.md)
</dt> </dl>

 

 
