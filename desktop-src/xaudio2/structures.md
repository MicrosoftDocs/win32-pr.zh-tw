---
title: XAudio2 結構
description: 本節包含 Microsoft XAudio2 API 所提供之結構的相關資訊。
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcbdf454f282ca696a040aa7c1a3fe84c372ca4e0607c0a60f18b59d5f5e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962587"
---
# <a name="xaudio2-structures"></a>XAudio2 結構

本節包含 Microsoft XAudio2 API 所提供之結構的相關資訊。



| 結構                                                                                 | Description                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | 代表音訊資料緩衝區。<br/>                                                                                                    |
| [**XAUDIO2 \_ 緩衝區 \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | 表示 WMA 音訊資料緩衝區。<br/>                                                                                                 |
| [**XAUDIO2 \_ DEBUG \_ 設定**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | 當 SetDebugConfiguration 函數使用時，為 XAudio2 設定新的全域偵錯工具設定。                                             |
| [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | 定義效果鏈。<br/>                                                                                                            |
| [**XAUDIO2 \_ 效果 \_ 描述項**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | 定義效果。<br/>                                                                                                                  |
| [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | 定義來源語音的篩選參數。<br/>                                                                                       |
| [**XAUDIO2 \_ 效能 \_ 資料**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | 捕獲效能資訊。<br/>                                                                                                  |
| [**XAUDIO2 \_ 傳送 \_ 描述元**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | 描述語音傳送目的地。<br/>                                                                                                 |
| [**XAUDIO2 \_ VOICE \_ 詳細資料**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | 包含建立旗標、輸入通道和語音取樣率的相關資訊。<br/>                                          |
| [**XAUDIO2 \_ 語音 \_ 傳送**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | 定義一組用來接收單一輸出語音資料的語音。<br/>                                                                 |
| [**XAUDIO2 \_ VOICE \_ 州**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | 傳回語音的目前狀態和游標位置資料。<br/>                                                                         |
| [**XAUDIO2FX \_ 回音 \_ I3DL2 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | 描述 I3DL2 (互動式3D 音訊轉譯指導方針層級 2.0) 參數，以在 ReverbConvertI3DL2ToNative 函式中使用。           |
| [**XAUDIO2FX 的 \_ 回音 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | 描述在 [回音] APO 中使用的參數。                                                                                                |
| [**XAUDIO2FX \_ VOLUMEMETER \_ 層級**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | 描述用於磁片區計量 APO 的參數。                                                                                        |
| [**XAPO \_ LOCKFORPROCESS \_ 緩衝區 \_ 參數**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | 定義鎖定 XAPO 時保持不變的緩衝區參數。<br/>                                                             |
| [**XAPO \_ 進程 \_ 緩衝區 \_ 參數**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | 定義可能會從一個呼叫變更為下一個呼叫的緩衝區參數。<br/>                                                                |
| [**XAPO \_ 註冊 \_ 屬性**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | 描述 XAPO 的一般特性。<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | 用於 FXECHO XAPO 的初始化參數。<br/>                                                                             |
| [**FXECHO \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | 搭配 FXECHO XAPO 使用的參數。<br/>                                                                                            |
| [**FXEQ \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | 搭配 FXEQ XAPO 使用的參數。<br/>                                                                                              |
| [**FXMASTERINGLIMITER \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | 搭配 FXMasteringLimiter XAPO 使用的參數。<br/>                                                                                |
| [**FXREVERB \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | 搭配 FXReverb XAPO 使用的參數。<br/>                                                                                          |
| [**X3DAUDIO \_ 圓錐**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | 藉由根據發射器的方向來調整 DSP 行為，以指定單一通道非 LFE 發射器的方向。<br/>    |
| [**X3DAUDIO \_ 距離 \_ 曲線**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | 定義由線性區段組成的明確分段曲線，直接定義與標準化距離相關的 DSP 行為。<br/> |
| [**X3DAUDIO \_ 距離 \_ 曲線 \_ 點**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | 在指定的正規化距離定義 DSP 設定。<br/>                                                                               |
| [**X3DAUDIO \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | 接收 X3DAudioCalculate 呼叫的結果。<br/>                                                                              |
| [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | 定義與任意數量的音效頻道搭配使用的單一或多點3D 音訊來源。<br/>                                    |
| [**X3DAUDIO \_ 接聽程式**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | 定義3D 音訊接收的點。<br/>                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> </dl>

 

 




