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
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="d6d7d-104">使用 WinHTTP 記錄來確認取得流量</span><span class="sxs-lookup"><span data-stu-id="d6d7d-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="d6d7d-105">如果泛型主機和用戶端成功，但實際的主機和用戶端仍失敗，則可能是中繼資料要求尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="d6d7d-106">您可以使用[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)記錄來確認是否已正確產生和傳送輸出訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="d6d7d-107">以 WSDAPI 為基礎的用戶端應用程式會使用 [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 連接到裝置。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="d6d7d-108">WSDAPI 型裝置主機不使用 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="d6d7d-109">此外，有些協力廠商 proxy 不會使用 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="d6d7d-110">針對不使用 WinHTTP 的主機或 proxy 進行疑難排解時，請略過此診斷程式，並遵循 [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)中的程式來繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="d6d7d-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 記錄不會顯示所有 TCP 層級的流量。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="d6d7d-112">如果有興趣 HTTP 流量以外的流量，請跳過 [檢查 Http 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md) 。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="d6d7d-113">**使用 WinHTTP 記錄來確認取得流量**</span><span class="sxs-lookup"><span data-stu-id="d6d7d-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="d6d7d-114">捕捉 WinHTTP 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="d6d7d-115">啟動「記事本」或其他文字編輯器。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="d6d7d-116">文字編輯器必須以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="d6d7d-117">開啟 WinHTTP 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="d6d7d-118">確認已傳送所需的 HTTP 要求和中繼資料訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="d6d7d-119">如果在 WinHTTP 記錄檔中找到主機的 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，則會成功將中繼資料要求傳送到 winHTTP。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="d6d7d-120">遵循 [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)中的程式，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="d6d7d-121">如果在 WinHTTP 記錄檔中找不到主機的 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，則不會起始中繼資料要求。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="d6d7d-122">當主機發佈不正確 XAddrs 時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="d6d7d-123">確認主機上的 XAddrs 符合 [XAddr 驗證規則](xaddr-validation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="d6d7d-124">確認已傳送所需的 HTTP 要求和中繼資料訊息</span><span class="sxs-lookup"><span data-stu-id="d6d7d-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="d6d7d-125">成功交換中繼資料時必須發生下列事件：</span><span class="sxs-lookup"><span data-stu-id="d6d7d-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="d6d7d-126">WSDAPI 用戶端會產生輸出 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="d6d7d-127">此要求會傳送至 WSDAPI 主機。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="d6d7d-128">用戶端會將 [Get](get--metadata-exchange--http-request-and-message.md) 訊息傳送至主機。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="d6d7d-129">這些事件會在 WinHTTP 記錄檔中捕捉。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="d6d7d-130">下列 WinHTTP 記錄檔程式碼片段顯示 WSDAPI 用戶端所產生的輸出 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

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

<span data-ttu-id="d6d7d-131">下列 WinHTTP 記錄檔程式碼片段顯示 [取得](get--metadata-exchange--http-request-and-message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d6d7d-132">此訊息應該緊接在 HTTP 要求之後。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-132">This message should immediately follow the HTTP request.</span></span>

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

<span data-ttu-id="d6d7d-133">**Action** 元素 (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) 將訊息識別為 [取得](get--metadata-exchange--http-request-and-message.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d6d7d-134">請確認 **To** 元素的值 (例如， `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) 符合原始 UDP WS-Discovery 訊息中主機所公告的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="d6d7d-135">您可以使用 WSD Debug 主機來檢查主機所公告的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="d6d7d-136">如需詳細資訊，請參閱 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="d6d7d-137">此外，主機對中繼資料要求的回應可以在用戶端的 WinHTTP 記錄檔中找到。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="d6d7d-138">主機會產生 [GetResponse](getresponse--metadata-exchange--message.md) 訊息，以回應用戶端的 [取得](get--metadata-exchange--http-request-and-message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="d6d7d-139">下列 WinHTTP 記錄檔程式碼片段顯示 WSDAPI 用戶端接收的輸入 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

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

<span data-ttu-id="d6d7d-140">**Action** 元素 (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) 將訊息識別為 [GetResponse](getresponse--metadata-exchange--message.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="d6d7d-141">確認 GetResponse 訊息的 **RelatesTo** 元素值符合 [Get](get--metadata-exchange--http-request-and-message.md)訊息的 **MessageID** 元素值。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="d6d7d-142">在此範例中， () 的 **RelatesTo** 元素值 `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` 符合 Get 訊息的 **MessageID** 元素值 (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`) 。</span><span class="sxs-lookup"><span data-stu-id="d6d7d-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6d7d-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6d7d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6d7d-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d6d7d-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="d6d7d-145">正在捕獲 WinHTTP 記錄檔</span><span class="sxs-lookup"><span data-stu-id="d6d7d-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="d6d7d-146">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="d6d7d-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="d6d7d-147">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="d6d7d-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
