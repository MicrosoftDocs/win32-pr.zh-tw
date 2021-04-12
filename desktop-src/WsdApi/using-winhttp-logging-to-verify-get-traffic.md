---
description: 如果泛型主機和用戶端成功，但實際的主機和用戶端仍失敗，則可能是中繼資料要求尚未初始化。 您可以使用 WinHTTP 記錄來確認是否已正確產生和傳送輸出訊息。
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: 使用 WinHTTP 記錄來確認取得流量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192904"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>使用 WinHTTP 記錄來確認取得流量

如果泛型主機和用戶端成功，但實際的主機和用戶端仍失敗，則可能是中繼資料要求尚未初始化。 您可以使用[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)記錄來確認是否已正確產生和傳送輸出訊息。

以 WSDAPI 為基礎的用戶端應用程式會使用 [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 連接到裝置。 WSDAPI 型裝置主機不使用 WinHTTP。 此外，有些協力廠商 proxy 不會使用 WinHTTP。 針對不使用 WinHTTP 的主機或 proxy 進行疑難排解時，請略過此診斷程式，並遵循 [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)中的程式來繼續進行疑難排解。

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 記錄不會顯示所有 TCP 層級的流量。 如果有興趣 HTTP 流量以外的流量，請跳過 [檢查 Http 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md) 。

**使用 WinHTTP 記錄來確認取得流量**

1.  [捕捉 WinHTTP 記錄檔。](capturing-winhttp-logs.md)
2.  啟動「記事本」或其他文字編輯器。 文字編輯器必須以系統管理員身分執行。
3.  開啟 WinHTTP 記錄檔。
4.  確認已傳送所需的 HTTP 要求和中繼資料訊息。

如果在 WinHTTP 記錄檔中找到主機的 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，則會成功將中繼資料要求傳送到 winHTTP。 遵循 [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)中的程式，繼續進行疑難排解。

如果在 WinHTTP 記錄檔中找不到主機的 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，則不會起始中繼資料要求。 當主機發佈不正確 XAddrs 時，就會發生這種情況。 確認主機上的 XAddrs 符合 [XAddr 驗證規則](xaddr-validation-rules.md)。

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>確認已傳送所需的 HTTP 要求和中繼資料訊息

成功交換中繼資料時必須發生下列事件：

-   WSDAPI 用戶端會產生輸出 HTTP 要求。 此要求會傳送至 WSDAPI 主機。
-   用戶端會將 [Get](get--metadata-exchange--http-request-and-message.md) 訊息傳送至主機。

這些事件會在 WinHTTP 記錄檔中捕捉。

下列 WinHTTP 記錄檔程式碼片段顯示 WSDAPI 用戶端所產生的輸出 HTTP 要求。

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

下列 WinHTTP 記錄檔程式碼片段顯示 [取得](get--metadata-exchange--http-request-and-message.md) 訊息。 此訊息應該緊接在 HTTP 要求之後。

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

**Action** 元素 (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) 將訊息識別為 [取得](get--metadata-exchange--http-request-and-message.md)訊息。 請確認 **To** 元素的值 (例如， `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) 符合原始 UDP WS-Discovery 訊息中主機所公告的裝置識別碼。 您可以使用 WSD Debug 主機來檢查主機所公告的裝置識別碼。 如需詳細資訊，請參閱 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。

此外，主機對中繼資料要求的回應可以在用戶端的 WinHTTP 記錄檔中找到。 主機會產生 [GetResponse](getresponse--metadata-exchange--message.md) 訊息，以回應用戶端的 [取得](get--metadata-exchange--http-request-and-message.md) 訊息。

下列 WinHTTP 記錄檔程式碼片段顯示 WSDAPI 用戶端接收的輸入 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

**Action** 元素 (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) 將訊息識別為 [GetResponse](getresponse--metadata-exchange--message.md)訊息。 確認 GetResponse 訊息的 **RelatesTo** 元素值符合 [Get](get--metadata-exchange--http-request-and-message.md)訊息的 **MessageID** 元素值。 在此範例中， () 的 **RelatesTo** 元素值 `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` 符合 Get 訊息的 **MessageID** 元素值 (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[正在捕獲 WinHTTP 記錄檔](capturing-winhttp-logs.md)
</dt> <dt>

[WSDAPI 診斷程式](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
