---
description: 媒體基礎宏
ms.assetid: c460b1cd-13d7-4b65-a755-23b2ea87864d
title: 媒體基礎宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bed83710f41957edc1b945fecd5d68b5550b4ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945604"
---
# <a name="media-foundation-macros"></a>媒體基礎宏

## <a name="in-this-section"></a>本節內容



| 屬性                                                                                              | 描述                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**定義 \_ 媒體 \_ GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid)<br/>                              | 從 FOURCC 程式碼、 **D3DFORMAT** 值或音訊格式類型定義媒體子類型 GUID。<br/>                                                                       |
| [**MFP \_ 取得 \_ \_ 使用者 \_ 認證 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event)<br/> | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ 取得 \_ 使用者 \_ 認證 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event) 指標。<br/> |
| [**MFP \_ 取得 \_ 錯誤 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event)<br/>                                       | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ 錯誤 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_error_event) 指標。<br/>                                       |
| [**MFP \_ 取得 \_ 畫面格 \_ 步驟 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_frame_step_event)<br/>                            | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成「 [**mfp \_ 框架步驟」 \_ \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_frame_step_event) 指標。<br/>                            |
| [**已 \_ \_ 清除 MEDIAITEM 的 MFP \_ \_ 活動**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_cleared_event)<br/>              | 將 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**MEDIAITEM \_ 清除的 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_cleared_event) 指標。<br/>                   |
| [**MFP \_ 取得 \_ MEDIAITEM \_ 建立的 \_ 活動**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event)<br/>              | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成已建立的 [**mfp \_ MEDIAITEM \_ 建立 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_created_event) 指標。<br/>              |
| [**MFP \_ 取得 \_ MEDIAITEM \_ 設定 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event)<br/>                      | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ MEDIAITEM \_ SET \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event) 指標。<br/>                      |
| [**MFP \_ 取得 \_ MF \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event)<br/>                                             | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ MF \_ 事件**](/windows/win32/api/mfplay/ns-mfplay-mfp_mf_event) 指標。<br/>                                              |
| [**MFP \_ 取得 \_ 暫停 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_pause_event)<br/>                                       | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ PAUSE \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_pause_event) 指標。<br/>                                       |
| [**MFP \_ 取得 \_ PLAY \_ 活動**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event)<br/>                                         | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ PLAY \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) 指標。<br/>                                         |
| [**MFP \_ 取得 \_ 播放 \_ 結束 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event)<br/>                    | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ 播放 \_ 結束 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_playback_ended_event) 指標。<br/>                    |
| [**MFP \_ 取得 \_ 位置 \_ 設定 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_position_set_event)<br/>                        | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ 位置 \_ 集 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event) 指標。<br/>                        |
| [**MFP \_ 取得 \_ 速率 \_ 設定 \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event)<br/>                                | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ RATE \_ SET \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_rate_set_event) 指標。<br/>                                |
| [**MFP \_ 取得 \_ 停止 \_ 活動**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_stop_event)<br/>                                         | 將 [**mfp \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉換成 [**mfp \_ 停止 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event) 指標。<br/>                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計參考](media-foundation-programming-reference.md)
</dt> </dl>

 

 
