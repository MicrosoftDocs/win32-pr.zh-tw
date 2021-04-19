---
description: 列出針對投影機 Wizard 進行疑難排解時要使用的診斷程式。
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: 針對投影機 Wizard 進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972405"
---
# <a name="troubleshooting-the-projector-wizard"></a>針對投影機 Wizard 進行疑難排解

投影機 Wizard：

-   一律使用 UDP WS-Discovery 進行裝置探索
-   一律使用 HTTP 進行中繼資料交換
-   有時會使用導向的探索

下列診斷程式應依序 (使用，) 協助您找出投影機 Wizard 的問題。

**針對投影機 Wizard 進行疑難排解**

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

 

 



