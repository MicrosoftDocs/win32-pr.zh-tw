---
description: 列出針對 [新增印表機嚮導] 進行疑難排解時要使用的診斷程式。
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: 針對新增印表機嚮導進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979079"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>針對新增印表機嚮導進行疑難排解

[新增印表機] 嚮導：

-   一律使用 UDP WS-Discovery 進行裝置探索
-   一律起始中繼資料交換的 HTTP 或 HTTPS 連接
-   有時會使用導向的探索
-   有時會使用安全通道 (HTTPS) 進行中繼資料交換

下列診斷程式應依序 (使用，) 協助您找出 [新增印表機嚮導] 的問題。

**若要針對新增印表機嚮導進行疑難排解**

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
</dt> <dt>

[使用導向探索針對應用程式進行疑難排解](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



