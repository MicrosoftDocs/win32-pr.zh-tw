---
description: 使用導向探索的應用程式會透過 HTTP 或 HTTPS 傳送探查訊息以探索裝置。
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: 使用導向探索針對 WSDAPI 應用程式進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513044"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>使用導向探索針對 WSDAPI 應用程式進行疑難排解

使用導向探索的應用程式會透過 HTTP 或 HTTPS 傳送 [探查](probe-message.md) 訊息以探索裝置。 在回應中傳送的對應 [ProbeMatches](probematches-message.md) 訊息也會透過 HTTP 或 HTTPS 傳送。 [新增印表機嚮導]、[函式探索用戶端] 或 [WSDAPI 應用程式] 可以起始導向探索。 探查和 ProbeMatches 訊息的結構與透過 UDP 傳送的訊息相同。 訊息前面會加上適當的 HTTP 或 HTTPS 標頭。

下列診斷程式應依序 (使用，) 協助您使用導向探索來識別應用程式的問題。

**使用導向探索針對 WSDAPI 應用程式進行疑難排解**

1.  [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。
2.  [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。
3.  [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。
4.  [使用導向探索來檢查應用程式的網路追蹤](inspecting-network-traces-for-applications-using-directed-discovery.md)。

如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WSDAPI 進行疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[針對新增印表機嚮導進行疑難排解](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[針對 WSDAPI 應用程式進行疑難排解](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



