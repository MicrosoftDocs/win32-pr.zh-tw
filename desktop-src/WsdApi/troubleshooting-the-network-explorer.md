---
description: 列出針對網路總管進行疑難排解時要使用的診斷程式。
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: 疑難排解網路總管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943415"
---
# <a name="troubleshooting-the-network-explorer"></a>疑難排解網路總管

網路總管：

-   一律使用 UDP WS-Discovery 進行裝置探索
-   一律起始中繼資料交換的 HTTP 或 HTTPS 連接
-   有時會使用安全通道 (HTTPS) 進行中繼資料交換

下列診斷程式應依序 (使用) ，以協助找出網路總管的問題。

**若要疑難排解網路總管**

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。
3.  [使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。
4.  [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。
5.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
6.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
7.  [檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。

網路總管使用 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) 來列舉網路裝置。 如需疑難排解的詳細資訊，請參閱 [疑難排解函數探索用戶端](troubleshooting-function-discovery-clients.md)。

如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[針對函數探索用戶端進行疑難排解](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
