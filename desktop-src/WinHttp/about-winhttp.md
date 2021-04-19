---
description: Microsoft Windows HTTP Services (WinHTTP) 提供伺服器支援的高階介面給 HTTP/2 和1.1 的網際網路通訊協定。
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: 關於 WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150c829410a1601a3ede7f115f4594276af7fead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000145"
---
# <a name="about-winhttp"></a>關於 WinHTTP

> [!NOTE]
> 針對應用程式容器和系統服務，自 Windows 10，版本1709，HTTP/2 (請參閱 [RFC7540](https://tools.ietf.org/html/rfc7540)) 預設為開啟。

Microsoft Windows HTTP Services (WinHTTP) 提供伺服器支援的高階介面給 HTTP/2 和1.1 的網際網路通訊協定。 在與 HTTP 伺服器通訊的伺服器應用程式中，WinHTTP 的設計主要是用於以伺服器為基礎的案例中。

[WinINet](/windows/desktop/WinInet/portal) 是設計為互動式桌面應用程式的 HTTP 用戶端平臺。 WinINet 會顯示某些作業的使用者介面，例如收集使用者認證。 但是，WinHTTP 會以程式設計的方式處理這些作業。 需要 HTTP 用戶端服務的伺服器應用程式應該使用 WinHTTP 而非 WinINet。 如需詳細資訊，請參閱 [將 WinINet 應用程式移植到 WinHTTP](porting-wininet-applications-to-winhttp.md)。

WinHTTP 也設計成用於系統服務和 HTTP 型用戶端應用程式。 不過，需要 FTP 通訊協定功能、cookie 持續性、快取、自動認證對話處理、Internet Explorer 相容性或舊版平臺支援的單一使用者應用程式，應該考慮使用 [WinINet](/windows/desktop/WinInet/portal)。

您可以使用 (API) 的 WinHTTP 應用程式設計介面，或使用 [**IWinHttpRequest**](iwinhttprequest-interface.md) 和 [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) 介面，從 C/c + + 存取這個介面。 WinHTTP 也可從腳本和 Microsoft Visual Basic 透過 WinHTTP 物件來存取。 如需個別函式的詳細資訊和描述，請參閱適用于特定語言的 WinHTTP 函數參考。

從 Windows 8 開始，WinHTTP 提供 Api 來啟用使用 [WebSocket 通訊協定](https://tools.ietf.org/html/rfc6455)l 的連接，例如 [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) 和 [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)。

> [!Caution]  
> 除非在非同步完成回呼期間，否則 WinHTTP 不可重新進入。 也就是說，當執行緒呼叫其中一個 WinHTTP 函式（例如 WinHttpSendRequest、WinHttpReceiveResponse、WinHttpQueryDataAvailable、WinHttpSendData 或 WinHttpWriteData）時，它永遠不會在第一次呼叫完成之前，第二次呼叫 WinHTTP。 發生第二次呼叫的其中一個案例如下：如果應用程式將非同步程序呼叫排入佇列， (APC) 至呼叫 WinHTTP 的執行緒，而且如果 WinHTTP 在內部執行可提供警示等候，則可以執行 APC。 如果 APC 常式也會呼叫 WinHTTP，它會重新進入 WinHTTP API，而 WinHTTP 的內部狀態可能會損毀。

## <a name="winhttp-51-features"></a>WinHTTP 5.1 功能

下列功能已新增至5.1 版的 WinHTTP：

-   IPv6 支援。
-   自動代理功能。
-   HTTP/1.0 通訊協定，包括支援 keep-alive (持續性) 連線和會話 cookie。
-   Http/1.1 區塊傳輸支援 HTTP 回應。
-   在會話之間保持匿名連接的保持運作狀態。
-   安全通訊端層 (SSL) 功能，包括用戶端憑證。 支援的 SSL 通訊協定包括下列各項： SSL 2.0、SSL 3.0 和傳輸層安全性 (TLS) 1.0。
-   支援伺服器和 proxy 驗證，包括 Microsoft Passport 1.4 與 Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md) 封裝的整合式支援。
-   除非隱藏，否則重新導向的自動處理。
-   可編寫腳本的介面，以及 API。
-   有助於疑難排解問題的追蹤公用程式。

WinHTTP 中不支援許多 [WinINet](/windows/desktop/WinInet/portal) 功能，包括 URL 快取和持續性 cookie、自動代理程式、autodialing、離線支援，以及檔案傳輸通訊協定 (FTP) 。

如需5.1 版中所引進之變更的詳細資訊，請參閱 [WinHTTP 5.1 中的新功能](what-s-new-in-winhttp-5-1.md)。

## <a name="getting-started-with-winhttp"></a>使用 WinHTTP 開始使用

如需 WinHTTP 的詳細資訊，請參閱下列主題。

* [WinINet 與 WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) 比較兩種用來存取 HTTP 的技術。
* [WinHTTP 版本](winhttp-versions.md) 說明 winHTTP 的版本歷程記錄。
* [WinHTTP 5.1 的新](what-s-new-in-winhttp-5-1.md) 功能說明 winHTTP 5.1 中的變更和新功能。
* [網路術語](network-terminology.md) 描述一般與網路功能相關的實用概念和術語，尤其是 HTTP 通訊協定。
* [選擇 WinHTTP 介面](choosing-a-winhttp-interface.md) 會描述適用于 WinHTTP 的 C/c + + API 和 COM 介面。
* [WinHTTP 安全性考慮](winhttp-security-considerations.md) 說明使用 winHTTP 時要注意的安全性問題。
* [將 WinINet 應用程式移植到 winHTTP](porting-wininet-applications-to-winhttp.md) ，說明如何修改現有的 [WinINet](/windows/desktop/WinInet/portal) 應用程式以使用 WinHTTP API。
