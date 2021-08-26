---
description: 本主題說明如何使用 Microsoft Windows HTTP 服務 (WinHTTP) proxy 設定工具，&\# 0034; ProxyCfg.exe&\# 0034;。
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe 和 ProxyCfg.exe Proxy 組態工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64c952db59fb4709614c498b4d9c732403798e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885829"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe 和 ProxyCfg.exe Proxy 組態工具

* * Windows Vista 和 Windows Server 2008： * *

ProxyCfg.exe 已被取代。 它是由 [Netsh.exe winHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) 命令所取代。

本主題說明如何使用[Microsoft Windows HTTP 服務 (WinHTTP) ](about-winhttp.md) proxy 設定工具「ProxyCfg.exe」。

有兩種方式可透過使用 Microsoft Windows HTTP Services (WinHTTP) 的 proxy，來存取 HTTP 和安全超文字傳輸通訊協定 (HTTPS) 伺服器。 首先，您可以從 WinHTTP 應用程式內指定 proxy 設定。 其次，您可以使用位於% windir% system32 目錄中的 proxy 設定公用程式，從您的應用程式外部指定預設 proxy 設定 \\ 。

您可以透過程式設計方式，從您的應用程式或腳本內設定 proxy 資料。 如果您使用 WinHTTP API 來撰寫應用程式，請使用下列兩種方法之一來變更 proxy 設定。

-   使用 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 函數。 在第二個參數中指定存取類型、第三個參數中指定 proxy 的名稱，並在第四個參數中指定 [略過] 清單。 下列範例會示範如何使用 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 函數來設定 proxy 資料。

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數。 [**WinHTTP \_ 選項 \_ PROXY**](option-flags.md)旗標可讓您使用 [**winHTTP \_ proxy \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)結構來指定 PROXY 設定。 下列範例程式碼顯示如何使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數來設定 proxy 資料。

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

如果您是使用 [**WinHttpRequest**](winhttprequest.md) 物件來撰寫腳本或應用程式，請使用下列技巧來變更 proxy 設定。

-   使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法。 指定第一個參數的存取類型、第二個參數中的 proxy 名稱，以及第三個參數中的 [略過] 清單。 下列範例顯示如何在腳本中使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法來設定 proxy 資料。

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

若要指定預設設定，而不需要使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數，請使用 proxy 設定公用程式。 您可以使用此公用程式，指定您的應用程式透過 proxy 直接存取網路，或透過指定略過清單來透過直接和 proxy 存取的組合來存取網路。 當您使用 WinHTTP API 時，proxy 設定工具只會決定當您將 **winHTTP \_ 存取 \_ 類型 \_ 預設** 旗標傳遞給 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) API 時的設定。 根據預設， [**WinHttpRequest**](winhttprequest.md) 物件會使用 proxy 設定工具設定。

WinHTTP 的 proxy 設定不是 Microsoft Internet Explorer 的 proxy 設定。 您無法在 Microsoft Windows 主控台中設定 WinHTTP 的 proxy 設定。 使用 WinHTTP proxy 設定公用程式並不會改變您用來 Internet Explorer 的設定。

> [!Note]  
> 如果您嘗試使用 WinHTTP 開啟和傳送 HTTP 要求，但 proxy 設定不正確，就會發生錯誤。

 

## <a name="command-line-parameters"></a>命令列參數

下表列出可搭配 ProxyCfg.exe 工具使用的命令列參數。



| 參數 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 無      | 如果未指定任何參數，則會顯示目前的 WinHTTP proxy 設定。                                                                                                                                                                                                                                                                                                                                               |
| ?         | 說明資訊隨即顯示。                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | 指定 WinHTTP 應用程式直接存取網路，而不使用 proxy。                                                                                                                                                                                                                                                                                                                                                 |
| p         | 指定 proxy 伺服器。 您也可以指定不使用 proxy 存取的選擇性伺服器清單。                                                                                                                                                                                                                                                                                                                   |
| u         | 指定 WinHTTP 應用程式使用目前使用者的 proxy 設定進行 Internet Explorer。 如果 Internet Explorer 自動偵測 proxy 設定，或使用自動設定 URL 來設定 proxy 資訊，則此參數無法運作。                                                                                                                                                      |
| i         | 指定 WinHTTP 應用程式使用目前使用者的 proxy 設定進行 Internet Explorer。 這僅適用于先前未使用 ProxyCfg.exe 時。 如果已安裝 ProxyCfg.exe，請指定 "u" 命令列參數使用手動設定。 如果 Internet Explorer 自動偵測 proxy 設定，或使用自動設定 URL 來設定 proxy 資訊，則此參數無法運作。 |



 

您可以在以空格分隔的字串中指定 proxy。 Proxy 清單可以包含用來存取 proxy 的埠號碼。 若要列出特定通訊協定的 proxy，字串必須遵循下列格式： &lt; protocol &gt; = HTTPs://<proxy \_ 名稱>。 有效的通訊協定為 HTTP 和 HTTPS。 例如，若要列出 HTTP proxy，有效的字串為 HTTP = https://http\_proxy\_name:80 ，其中 HTTP \_ proxy \_ 名稱是 proxy 伺服器的名稱，而80則是您必須用來存取 proxy 的埠號碼。 如果 proxy 使用該通訊協定的預設通訊埠號碼，則您可以省略埠號碼。 如果 proxy 名稱本身列出，您可以使用它做為任何沒有指定 proxy 之通訊協定的預設 proxy。 例如，HTTP = https://http\_proxy 其他 \_ proxy 會 \_ 對任何 HTTP 作業使用 HTTP PROXY，而 HTTPS 通訊協定會使用名為其他 \_ proxy 的 proxy。

您可以在 [proxy 略過] 清單中列出本機已知的主機名稱或 IP 位址。 這份清單可以包含萬用字元，例如 " \* "，這會導致應用程式針對符合指定模式的位址略過 proxy 伺服器，例如 " \* . microsoft.com" 或 " \* org"。 萬用字元必須是清單中最左邊的字元。 例如，"aaa"。 \*不受支援。 若要列出多個位址和主機名稱，請在 proxy 略過字串中使用空格或分號分隔。 如果您指定 &lt; 本機 &gt; 宏，函式會略過不包含句號的任何主機名稱。

> [!WARNING]
> Proxycfg.exe 執行之後，您就無法還原先前的 proxy 設定。 不過，您可以完全移除 proxy 設定。

 

## <a name="usage"></a>使用方式

若要使用 proxy 設定工具，請開啟命令提示字元視窗，然後使用適當的命令列參數來執行 proxy 設定公用程式。 下一節提供語法範例。

## <a name="example-syntax"></a>範例語法

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>範例1：僅針對外部資源使用 proxy

以下是最常見的 Proxycfg.exe 用途。 此命令會指定透過名為「proxy 伺服器」的 proxy 伺服器來存取 HTTP 和 HTTPS 伺服器 \_ ，但不包含句點的主機名稱除外。

**proxycfg.exe-p proxy \_ 伺服器 " &lt; local &gt; "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>範例2：針對所有資源使用 proxy

下列範例會指定透過名為「proxy 伺服器」的 proxy 伺服器來存取 HTTP 和 HTTPS 伺服器 \_ 。 未指定任何略過清單。

**proxycfg.exe-p proxy \_ 伺服器**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>範例3：針對安全資源使用不同的 proxy

下列範例會指定透過 HTTP proxy proxy 存取 HTTP 伺服器 \_ ，並透過 HTTPs proxy 存取 HTTPs 伺服器 \_ 。 近端內部網路網站與 microsoft.com 網域中的任何網站都會 \* 略過 proxy。

**proxycfg.exe-p "HTTP = HTTP \_ proxy HTTPs = HTTPs \_ proxy" " &lt; local &gt; ; \* 。microsoft.com "**

## <a name="removing-proxycfgexe"></a>移除 ProxyCfg.exe

使用 proxy 設定工具之後，您就無法還原原始 proxy 設定。 不過，如有必要，您可以移除公用程式所建立的登錄設定。 若要移除 ProxyCfg.exe 建立的登錄專案，您必須從下列登錄機碼中刪除 **WinHttpSettings** 值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet 設定** \\ **Connections** \\ **WinHttpSettings**

刪除 *WinHttpSettings* 值會移除所有的 proxy 設定。

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe 和驗證

Proxy 設定公用程式會設定預設的驗證原則。 因為您不應該使用不受信任的主機執行 NTLM 驗證，所以根據預設，NTLM 驗證只會自動在 proxy 略過清單上與主機一起進行。 如果沒有 proxy，您仍然可以使用 ProxyCfg.exe 來指定您信任用來執行 NTLM 驗證之主機的略過清單。 基於此目的使用 ProxyCfg.exe 時需要 proxy 名稱，但您可以使用任何有效的字串來取代實際的 proxy 名稱。

如需有關自動登入原則的詳細資訊，請參閱 [自動登入原則](authentication-in-winhttp.md)。

 

 
