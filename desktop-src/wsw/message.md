---
title: 訊息 (Windows Web 服務)
description: 訊息是封裝傳輸或接收之資料的物件。
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Windows 的訊息 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657091"
---
# <a name="message-windows-web-services"></a>訊息 (Windows Web 服務)

訊息是封裝傳輸或接收之資料的物件。 訊息的結構由 SOAP 定義，並包含一組標頭和主體。 標頭一定會在記憶體中進行緩衝處理，但是主體是使用串流 API 來讀取和寫入。

![此圖顯示具有正在緩衝處理之標頭的訊息，以及要進行資料流程處理的主體。](images/messageenvelope.png)


訊息有一組屬性，可用來指定控制訊息行為的選擇性設定，並提供方法來取得所接收訊息的其他資訊 (例如) 安全性資訊。 如需完整的訊息屬性清單，請參閱 [**WS \_ 訊息 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) 。

訊息會定址至特定的 [端點位址](endpoint-address.md)。

[**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)是一種特殊的訊息內容，用來表示從遠端端點傳回的錯誤。

訊息會經過編碼，以在傳輸之前將 XML 轉換成線性電傳格式。

如需訊息的詳細資訊，請參閱 [通道層級總覽](channel-layer-overview.md) 主題。

下列範例說明如何使用 WWSAPI 中的訊息。

| 範例                                              | 描述                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | 說明如何使用自訂訊息標頭。    |
| [MessageEncodingExample](messageencodingexample.md) | 說明編碼和解碼訊息。 |
| [ForwardMessageExample](forwardmessageexample.md)   | 說明如何轉送訊息。            |



 

下列 API 元素會與訊息一起使用。

| 回呼                                                        | 描述                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 訊息 \_ 完成 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | 通知呼叫端訊息已完成使用提供給 WsReadEnvelopeStart 函式的 WS \_ xml \_ 讀取器結構，或 \_ \_ 提供給 WsWriteEnvelopeStart 函數的 ws xml 寫入器結構。 |



 



| 列舉型別                                                      | 描述                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**WS \_ 定址 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | 用於定址標頭的規格版本。                                        |
| [**WS \_ 信封 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | 用於信封結構的規格版本。                                        |
| [**WS \_ 標頭 \_ 屬性**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | 一組旗標，代表標頭的 SOAP mustUnderstand 和轉送屬性。                    |
| [**WS \_ 標頭 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | 標頭的型別。                                                                                  |
| [**WS-MANAGEMENT \_ 訊息 \_ 初始化**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | 指定 [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) 應新增至訊息的標頭。 |
| [**WS \_ 訊息 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | 每個訊息屬性的識別碼。                                                                         |
| [**WS \_ 訊息 \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | 訊息的狀態。                                                                                |



 



| 函式                                                             | 描述                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | 將目的地位址指派給訊息。                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | 確認接收者已適當理解指定的標頭。                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | 建立 [WS \_ MESSAGE](ws-message.md) 物件的實例。                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | 建立適合搭配特定通道使用的訊息。                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | 確定訊息中有足夠的位元組數目可供讀取。                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | 清除所有已寫入的累積訊息主體資料。                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | 釋放與訊息相關聯的記憶體資源。                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | 尋找訊息的應用程式定義標頭，並將其還原序列化。                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | 在訊息中尋找特定的標準標頭，並將其還原序列化。                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | 從讀取器所在位置的標頭專案中，將 [**WS \_ 標頭 \_ 屬性**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) 填入至 ULONG 參數。 |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | 抓取指定的訊息物件屬性。                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | 初始化訊息的標頭，以準備進行處理。                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | 標記應用程式所瞭解的標頭。                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | 從訊息的 XML 讀取器還原序列化值。                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | 讀取訊息的結尾元素。                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | 讀取訊息的標頭，並準備讀取主體元素。                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | 從訊息移除自訂標頭。                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | 從訊息中移除標準 [**WS \_ 標頭 \_ 型**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) 別物件。                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | 將訊息狀態設定回「 **WS \_ 訊息 \_ 狀態 \_ 空白**」。                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | 在訊息中新增或取代指定的標準標頭。                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | 在訊息主體中寫入值。                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | 寫入訊息的結尾元素。                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | 寫入訊息的開頭，包括訊息的目前標頭集，並準備撰寫本文元素。                           |



 



| Handle                        | 描述                                         |
|-------------------------------|-----------------------------------------------------|
| [WS \_ 訊息](ws-message.md) | 用來參考訊息物件的不透明類型。 |



 



| 結構                                                | 描述                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**WS \_ 錯誤**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | 在訊息本文中攜帶的錯誤值，指出處理失敗。 |
| [**WS \_ \_ 錯誤碼**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | 代表錯誤碼。                                                             |
| [**WS \_ 錯誤 \_ 原因**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | 包含錯誤的說明。                                                |
| [**WS \_ 訊息 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | 指定一組 [**WS \_ 訊息 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) 結構。  |
| [**WS \_ MESSAGE \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | 指定訊息特定設定。                                                |



 

 

 




