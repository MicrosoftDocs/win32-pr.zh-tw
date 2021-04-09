---
description: 列出針對函數探索用戶端進行疑難排解時要使用的診斷程式。
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: 針對函數探索用戶端進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691511"
---
# <a name="troubleshooting-function-discovery-clients"></a>針對函數探索用戶端進行疑難排解

函數探索用戶端：

-   一律使用 UDP WS-Discovery 進行裝置探索
-   一律起始中繼資料交換的 HTTP 或 HTTPS 連接
-   有時使用導向探索
-   有時使用安全通道 (HTTPS) 進行中繼資料交換

下列清單顯示功能探索用戶端傳送和接收的一般訊息順序。 並非所有的訊息都是強制性的。

1.  用戶端會傳送 [探查](probe-message.md) 訊息以探索裝置和服務。 如果用戶端使用導向探索，則會透過 HTTP 或 HTTPS 傳送此訊息;否則，UDP 多播會將訊息傳送到埠3702。
2.  用戶端會接收來自相符裝置或服務的 [ProbeMatches](probematches-message.md) 訊息。 導向的探索訊息會透過 HTTP 或 HTTPS 傳送;否則，這些訊息會由 UDP 單播傳送，並源自埠3702。
3.  如果 ProbeMatches 訊息中未包含任何 XAddrs，則用戶端會透過 UDP 多播將 [解析](resolve-message.md) 訊息傳送到埠3702。
4.  如果傳送了 [解析](resolve-message.md) 訊息，則用戶端會收到相符服務的 [ResolveMatches](resolvematches-message.md) 訊息。 此訊息是由 UDP 單播從埠3702傳送到解析訊息來源的埠。
5.  用戶端會傳送 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，以從裝置或服務要求中繼資料。 此訊息是由 HTTP 或 HTTPS 傳送。
6.  用戶端會收到具有裝置或服務中繼資料的 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。 此訊息是由 HTTP 或 HTTPS 傳送。

下列診斷程式應依序 (使用) ，以協助找出函式探索用戶端的問題。

**針對函數探索用戶端進行疑難排解**

1.  如果使用導向探索，請 [針對導向探索進行疑難排解](troubleshooting-applications-using-directed-discovery.md)。
2.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
3.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
4.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
5.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。
6.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
7.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
8.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



