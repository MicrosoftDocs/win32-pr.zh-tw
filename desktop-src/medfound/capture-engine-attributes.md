---
description: 您可以使用下列屬性來設定「捕獲引擎」。
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Capture 引擎屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e79d0410407d12b46c0577615088f0f925b8558169d02140486b9fdc8fb303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959148"
---
# <a name="capture-engine-attributes"></a>Capture 引擎屬性

您可以使用下列屬性來設定「捕獲引擎」。

下列是與 capture 裝置相關的屬性：



| 屬性                                                                                                                              | 描述                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [已 \_ 封鎖 MF 捕獲 \_ 引擎 \_ 相機 \_ 串流 \_](mf-capture-engine-camera-stream-blocked.md)                                            | 發出驅動程式封鎖視頻捕捉的信號。                                                         |
| [已 \_ \_ 解除封鎖 MF 捕獲引擎 \_ 相機 \_ 串流 \_](mf-capture-engine-camera-stream-unblocked.md)                                        | 通知影片捕捉在封鎖後會還原。                                                        |
| [MF \_ 捕獲 \_ 引擎 \_ D3D \_ 管理員](mf-capture-engine-d3d-manager.md)                                                                 | 在 capture 引擎上設定 DXGI 裝置管理員的指標。                                                   |
| [MF \_ CAPTURE \_ ENGINE \_ 解碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | 讓 capture engine 使用具有使用規定限制的解碼器。                                    |
| [MF \_ 捕獲 \_ 引擎 \_ 停用 \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | 指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。                    |
| [MF \_ 捕獲 \_ 停用 \_ 硬體 \_ 轉換](mf-capture-engine-disable-hardware-transforms.md)                                        | 停用在 capture 引擎中 (MFTs) 的硬體媒體基礎轉換。                       |
| [MF \_ 捕獲 \_ 引擎 \_ 啟用 \_ 攝影機 \_ STREAMSTATE \_ 通知](mf-capture-engine-enable-camera-streamstate-notification.md)         | 指出是否應該啟用資料流程狀態通知。                                                    |
| [MF \_ 捕獲 \_ 引擎 \_ 編碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | 讓 capture engine 使用具有使用規定限制的編碼器。                                   |
| [MF \_ 捕獲 \_ 引擎 \_ 事件產生器 \_ \_ GUID](mf-capture-engine-event-generator-guid.md)                                              | 識別產生 capture 事件的元件。                                                           |
| [MF \_ 捕獲 \_ 引擎 \_ 事件 \_ 資料流程 \_ 索引](mf-capture-engine-event-stream-index.md)                                                  | 識別哪個資料流程產生了捕捉事件。                                                                 |
| [MF \_ CAPTURE \_ ENGINE \_ MEDIASOURCE \_ CONFIG](mf-capture-engine-mediasource-config.md)                                                   | 包含 capture 來源的設定屬性。                                                          |
| [MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最大 \_ 處理 \_ 範例](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | 設定可在記錄接收音訊路徑中緩衝處理之已處理樣本的最大數目。                   |
| [MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 音訊 \_ 最 \_ 大 \_ 未處理範例](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | 設定可在記錄接收音訊路徑中進行緩衝處理的未處理樣本數上限。 |
| [MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 影片的 \_ 最大 \_ 處理 \_ 範例](mf-capture-engine-record-sink-video-max-processed-samples.md)     | 設定可在記錄接收影片路徑中緩衝處理之已處理樣本的最大數目。                   |
| [MF \_ 捕獲 \_ 引擎 \_ 記錄 \_ 接收 \_ 影片的 \_ 最大 \_ \_ 未處理範例](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | 設定可在記錄接收影片路徑中緩衝處理的未處理樣本數上限。  |
| [MF \_ 捕獲 \_ 引擎 \_ 接收 \_ 類型](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | 指定捕捉接收的類型。                                                                                  |
| [MF \_ 捕獲 \_ 引擎 \_ \_ 僅使用音訊 \_ 裝置 \_](mf-capture-engine-use-audio-device-only.md)                                           | 指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。                                                 |
| [MF \_ 捕獲 \_ 引擎 \_ \_ 僅使用影片 \_ 裝置 \_](mf-capture-engine-use-video-device-only.md)                                           | 指定捕捉引擎是否要捕獲影片，而非音訊。                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



