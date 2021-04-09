---
description: 在裝置 API (WSDAPI) 的 Web 服務上建立的偵錯工具集可在 Windows SDK 和 Windows 驅動程式套件 (WDK) 中提供。
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: 偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115708"
---
# <a name="debugging-tools"></a>偵錯工具

在裝置 API (WSDAPI) 的 Web 服務上建立的偵錯工具集可在 Windows SDK 和 Windows 驅動程式套件 (WDK) 中提供。 這些工具可用來測試在 WSDAPI 上撰寫的自訂應用程式的功能，或使用 Web 服務的其他裝置設定檔所撰寫的裝置和用戶端 (DPWS) 堆疊。

WSD Debug Host (wsddebug \_host.exe) 和 Wsd Debug Client (wsddebug \_client.exe) tools 可以用來檢查 DPWS 用戶端或主機的特性。 它們也可以用來針對連線能力或設定問題進行疑難排解。 如需詳細資訊，請參閱 [WSDAPI 疑難排解指南](wsdapi-troubleshooting-guide.md)。 這些工具僅適用于 SDK。 SDK 工具位於下列目錄： <Windows SDK Install Folder> \\ Bin。

[ [WSDAPI 基本互通性] 工具 (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx) 可用來測試 SOAP 層級或傳輸層級的互通性 (也就是確保訊息的格式正確) 。 此工具僅適用于 WDK。

## <a name="the-wsd-debug-client"></a>WSD Debug 用戶端

WSD Debug Client (wsddebug \_client.exe) 提供互動式主控台，可用來傳送和接收 WS-Discovery 訊息，以及取得中繼資料。 它也可以用來產生和取用原始多播訊息。

WSD Debug 用戶端會以三種模式的其中一種方式運作：多播、探索和中繼資料。



| [模式]      | 描述                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 多點傳送 | 在多播模式中，WSD Debug 用戶端會在 UDP 埠3702上傳送和接收未格式化的多播訊息，如 WS-MANAGEMENT 中所定義。 使用者可將這些 SOAP 訊息儲存在文字檔中，並可使用 WSD Debug 用戶端來修改和重新廣播訊息。                                                                                                                                 |
| 探索 | 在探索模式中，WSD Debug 用戶端會傳送和接收格式化的 WS-Discovery 訊息。 它可以顯示收到的 [Hello](hello-message.md)、 [再見](bye-message.md)、 [ProbeMatches](probematches-message.md)和 [ResolveMatches](resolvematches-message.md) 訊息。 它可以透過 UDP 或 HTTP 傳送 [探查](probe-message.md) 訊息，以及透過 Udp 來 [解析](resolve-message.md) 訊息。 |
| 中繼資料  | 除了執行探索模式的所有功能之外，中繼資料模式也會嘗試從裝置取得中繼資料。                                                                                                                                                                                                                                                                    |



 

如需詳細資訊，請參閱 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)、 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)，以及 [使用 WSD 偵錯工具用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。

## <a name="the-wsd-debug-host"></a>WSD Debug 主機

WSD Debug Host (wsddebug \_host.exe) 提供一個互動式主控台，用來宣告主機、回應用戶端要求，以及列印診斷資訊。

WSD Debug 主機會以兩種模式的其中一種方式運作：探索和中繼資料。



| [模式]      | 描述                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 探索 | 在探索模式中，WSD Debug 主機會印出格式化的 WS-Discovery 訊息。 它也會傳送 [Hello](hello-message.md) 和 [再見](bye-message.md) 的訊息，並自動回應 [探查](probe-message.md) 和 [解決](resolve-message.md) 訊息。 |
| 中繼資料  | 除了執行探索模式的所有功能之外，中繼資料模式還會通告中繼資料服務，並允許用戶端連接和執行中繼資料交換。                                                                                       |



 

如需詳細資訊，請參閱 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md) ，以及 [使用一般主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 上的 WSD 應用程式開發](wsd-application-development-on-windows.md)
</dt> <dt>

[WSDAPI 開發工具](wsdapi-development-tools.md)
</dt> <dt>

[WSDAPI 疑難排解指南](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



