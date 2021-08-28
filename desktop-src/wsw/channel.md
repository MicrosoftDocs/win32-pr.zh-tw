---
title: '通道 (Windows Web 服務) '
description: 通道會在兩個或多個合作物件之間封裝通訊內容，用來傳送和接收訊息。
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Windows 的通道 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff11601f372416527f1d521f8fb9880c98821f9421b633f9eed059cc5b4f672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026646"
---
# <a name="channel-windows-web-services"></a>通道 (Windows Web 服務) 

通道會在兩個或多個合作物件之間封裝通訊內容，用來傳送和接收訊息。


在用戶端上，使用 [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) 來建立通道。 在伺服器上，使用 [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener)來建立可由用戶端使用接聽程式接受的 [通道。](listener.md)

當您建立通道時，您會指定下列資訊，以判斷通道的本機行為和要使用的網路通訊協定。

-   [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)，可識別通道的訊息交換模式。
-   [**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結，識別要使用的傳輸通訊協定。
-   [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)，指定用於通道的安全性。 建立要在伺服器中使用的通道時，會針對指定接聽程式接受的所有通道指定一次。
-   設定的 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s，指定其他選擇性設定 (針對這些設定的清單，請參閱 [**WS \_ 通道 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) 列舉) 。

使用通道之前，您必須先呼叫 [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) 函式來開啟它，並指定通道和 [端點位址](endpoint-address.md)，以及其他選擇性資訊。

如需通道狀態轉換的詳細資訊，請參閱 [**通道狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) 主題。

如需通道的詳細資訊，請參閱 [通道層級總覽](channel-layer-overview.md) 主題。

下列 API 元素會與通道搭配使用。

| 回呼                                                                                  | 描述                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 放棄 \_ 訊息 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | 使用自訂通道系結處理通道的 [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) 呼叫。                                              |
| [**WS \_ 中止 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | 使用自訂通道系結處理通道的 [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) 呼叫。                                                  |
| [**WS \_ 關閉 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | 使用自訂通道系結處理通道的 [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) 呼叫。                                                  |
| [**WS \_ 建立 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | 使用自訂通道系結處理通道的 [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) 呼叫。                                                  |
| [**WS \_ 建立 \_ 解碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | 處理建立解碼器實例的處理。                                                                                                                  |
| [**WS \_ 建立 \_ 編碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | 處理建立編碼器實例的程式。                                                                                                                 |
| [**WS \_ 解碼 \_ 解碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | 解碼訊息。                                                                                                                                    |
| [**WS \_ 解碼器 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | 解碼訊息的結尾。                                                                                                                         |
| [**WS \_ 解碼 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | 取得訊息的內容類型。                                                                                                                 |
| [**WS \_ 解碼 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | 開始解碼訊息。                                                                                                                            |
| [**WS \_ 編碼器 \_ 編碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | 編碼訊息。                                                                                                                                    |
| [**WS \_ 編碼器 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | 將訊息的結尾編碼。                                                                                                                         |
| [**WS \_ 編碼器 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | 取得訊息的內容類型。                                                                                                                 |
| [**WS \_ 編碼器 \_ 啟動 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | 開始編碼訊息。                                                                                                                            |
| [**WS \_ FREE \_ CHANNEL \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | 使用自訂通道系結處理通道的 [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) 呼叫。                                                    |
| [**WS \_ FREE \_ 解碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | 處理釋出的解碼器實例。                                                                                                                   |
| [**WS \_ 免費 \_ 編碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | 控制碼釋放編碼器實例。                                                                                                                  |
| [**WS \_ GET \_ 通道 \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | 使用自訂通道系結處理通道的 [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) 呼叫。                                      |
| [**WS \_ HTTP 重新 \_ 導向 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | 當訊息即將自動重新導向至使用 HTTP 自動重新導向功能的另一個服務時叫用，如 RFC2616 中所述。 |
| [**WS \_ 開啟 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | 使用自訂通道系結處理通道的 [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) 呼叫。                                                    |
| [**WS \_ 讀取 \_ 訊息 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | 使用自訂通道系結處理通道的 [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) 呼叫。                                              |
| [**WS \_ 讀取 \_ 訊息 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | 使用自訂通道系結處理通道的 [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) 呼叫。                                              |
| [**WS \_ 重設 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | 使用自訂通道系結處理通道的 [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) 呼叫。                                                  |
| [**WS \_ 設定 \_ 通道 \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | 使用自訂通道系結處理通道的 [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) 呼叫。                                      |
| [**WS \_ 關機 \_ 會話 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | 使用自訂通道系結處理通道的 [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) 呼叫。                              |
| [**WS \_ 寫入 \_ 訊息 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | 使用自訂通道系結處理通道的 [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) 呼叫。                                            |
| [**WS \_ 寫入 \_ 訊息 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | 使用自訂通道系結處理通道的 [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) 呼叫。                                        |



 



| 列舉型別                                                 | 描述                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 通道系結 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | 指出要用於通道的通訊協定堆疊。                                                                                      |
| [**WS \_ 通道 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | 依識別碼識別每個通道屬性。                                                                                                |
| [**WS \_ 通道 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | 通道的狀態。                                                                                                                 |
| [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | 指出通道的基本特性，例如它是否為會話，以及支援的通訊方向。 |
| [**WS \_ 編碼**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | 不同的編碼 (訊息格式) 。                                                                                                |
| [**WS \_ 接收 \_ 選項**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | 指定從通道接收時是否需要訊息。                                                                    |
| [**WS \_ 傳輸 \_ 模式**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | 指定傳送或接收的訊息是否經過資料流程處理或緩衝處理。                                                            |



 



| 函式                                                         | 描述                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | 略過通道的其餘訊息。                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | 中止指定通道上的所有暫止 i/o，並將通道狀態設定為 **WS \_ 通道 \_ 狀態 \_** 發生錯誤。 |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | 不再需要時關閉通道。                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | 建立通道。                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | 建立接聽程式的通道。                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | 釋放與通道相關聯的記憶體資源。                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | 抓取通道參數所參考之通道的屬性。                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | 開啟端點的通道。                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | 從通道讀取訊息的結尾元素。                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | 從通道讀取下一個訊息的標頭，並準備讀取主體元素。               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | 接收訊息，並將訊息主體還原序列化為值。                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | 傳送要求訊息，並接收相互關聯的回復訊息。                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | 重設通道，讓它可以重複使用。                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | 使用序列化在通道上傳送訊息，以撰寫主體專案。                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | 傳送訊息，此訊息是接收訊息的回復。                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | 設定通道的屬性。                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | 設定訊息的屬性。                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | 將訊息的結尾元素寫入通道。                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | 將訊息的標頭寫出至通道，並準備撰寫本文元素。                   |



 



| Handle                        | 描述                                 |
|-------------------------------|---------------------------------------------|
| [WS \_ 通道](ws-channel.md) | 用來參考通道的不透明類型。 |



 



| 結構                                                                          | 描述                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 通道 \_ 解碼**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | 一組回呼，可轉換所接收訊息的內容類型和編碼的位元組。                                                                                                      |
| [**WS \_ 通道 \_ 編碼器**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | 一組回呼，可轉換所傳送訊息的內容類型和編碼位元組。                                                                                                      |
| [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | 一組 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) 結構。                                                                                                                        |
| [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | 通道特定的設定。                                                                                                                                                                      |
| [**WS \_ 自訂 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | 一組回呼，可形成自訂通道的執行。                                                                                                                             |
| [**WS \_ 自訂 \_ HTTP \_ PROXY**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | 用來指定通道的自訂 proxy，使用 Ws 通道屬性識別碼列舉的 **\_ \_ \_ 自訂 \_ HTTP** \_ proxy 值 [**。 \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) |
| [**WS \_ HTTP \_ 標頭 \_ 對應**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | 表示對應為 [**WS \_ HTTP \_ 訊息 \_ 對應**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)一部分的個別標頭。                                                                         |
| [**WS \_ HTTP \_ 訊息 \_ 對應**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | 有關如何在訊息物件中表示 HTTP 要求或回應的資訊。                                                                                                     |
| [**WS \_ HTTP 重新 \_ 導向 \_ 回呼 \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | 指定回呼函數和狀態，以控制 HTTP 自動重新導向行為。                                                                                               |
| [**WS \_ 訊息 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | 給定作業描述之輸入和輸出 [WS \_ 訊息](ws-message.md) 的架構。                                                                                             |



 

 

 




