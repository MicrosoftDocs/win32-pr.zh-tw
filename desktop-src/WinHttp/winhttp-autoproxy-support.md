---
description: 為了簡化 proxy 設定的設定，WinHTTP 5.1 會 (WPAD) 通訊協定（也稱為自動代理程式）來實行 Web Proxy 自動探索。
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: WinHTTP 自動代理支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973848"
---
# <a name="winhttp-autoproxy-support"></a>WinHTTP 自動代理支援

為了簡化 proxy 設定的設定，WinHTTP 5.1 會 (WPAD) 通訊協定（也稱為自動代理程式）來實行 Web Proxy 自動探索。

## <a name="overview-of-autoproxy"></a>自動代理程式總覽

使用 WinHTTP 傳送 HTTP 要求的應用程式和元件應確定已正確設定 proxy 設定。 除非用戶端有直接的網際網路連線，否則 HTTP 要求通常會透過將用戶端區域網路連線到網際網路的 web proxy 伺服器傳送 (例如，通常是在公司 LAN 上的 Web 用戶端) 的情況。 若是以伺服器為基礎的應用程式，則 proxy 設定通常是由伺服器的系統管理員使用 WinHTTP ProxyCfg.exe 公用程式來管理。 伺服器管理員事先知道 proxy 伺服器的名稱，並使用 ProxyCfg.exe 將此設定記錄在 WinHTTP 可以查詢的登錄中。 不過，要求用戶端桌面使用者手動設定 WinHTTP proxy 設定有問題。 終端使用者可能不知道 proxy 伺服器的名稱;要求終端使用者執行 ProxyCfg.exe 公用程式，可能是組織的支援負擔。 為了支援絕佳的使用者體驗，有 web 功能的用戶端應用程式應該判斷 proxy 設定，而不需要使用者介入。

為了讓您更輕鬆地設定以 WinHTTP 為基礎之應用程式的 proxy 設定，WinHTTP 現在會將 [Web Proxy 自動探索 (WPAD) 通訊協定](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)，通常稱為自動 *代理* 程式。 這是 web 瀏覽器所執行的相同通訊協定，可自動探索 proxy 設定，而不需要使用者手動指定 proxy 伺服器。 從 Windows 2000 Service Pack 3、Windows XP Service Pack 1 和 Windows Server 2003 中的 WinHTTP 5.1 版開始，可以使用這項功能。 請注意，雖然 Microsoft Internet Explorer 和 Microsoft WinHTTP 都支援 WPAD，但該規格絕不會超過「網際網路草稿」階段，並于2001年5月過期。

WPAD 通訊協定的運作方式如下：

1.  使用 DHCP 和（或） DNS 網路通訊協定時，會探索 Proxy 自動設定 (PAC) 檔的 URL。 URL 會在用戶端的區域網路上識別 PAC 檔案。 WinHTTP 只支援 "HTTP：" 和 "HTTPs：" PAC Url;例如，它不支援 "file：" URL。
2.  PAC 檔案會下載並選擇性地快取在用戶端的電腦上。 PAC 檔案是可執行檔腳本，它會根據指定的目標主機名稱和 URL，產生一或多個 proxy 伺服器的清單。 WinHTTP 只支援 ECMAScript 型 PAC 檔案。
3.  在每個 HTTP 要求中，會執行 PAC 腳本程式碼，並將 HTTP 要求的主機名稱和 URL 當作參數傳入。 WinHTTP 預期 PAC 腳本程式碼必須包含名為 **FindProxyForURL** 的函式，格式如下：
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    此函式會計算可供 HTTP 用戶端用來傳輸要求的一或多個 proxy 伺服器的清單。 如果 PAC 腳本判斷 HTTP 用戶端可以直接連線到目標伺服器而不需要通過 proxy 伺服器，則會使用特殊的傳回值來指出這一點。

## <a name="autoproxy-topics"></a>自動代理主題

-   [WinHTTP 自動代理函數](winhttp-autoproxy-api.md)
-   [沒有自動設定檔的探索](discovery-without-an-auto-config-file.md)
-   [WinHTTP 中的自動代理問題](autoproxy-issues-in-winhttp.md)
-   [在 WinHTTP 中設定 WinInet Proxy 設定](setting-wininet-proxy-configurations-in-winhttp.md)
-   [自動代理快取](autoproxy-cache.md)
-   [瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



