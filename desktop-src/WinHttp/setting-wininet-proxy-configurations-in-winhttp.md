---
description: 從 WinINet 至 WinHTTP 的應用程式，可能需要使用可在 WinINet 或 Internet Explorer (IE) 中取得的相同自動代理程式設定。
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: 在 WinHTTP 中設定 WinINet Proxy 設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa060d24036a02752a5eefacc9ea6672dec9bb77bad30f653c8f382490a487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133051"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>在 WinHTTP 中設定 WinINet Proxy 設定

## <a name="setting-automatic-proxy-on-winhttp-51"></a>在 WinHTTP 5.1 上設定自動 Proxy

從 WinINet 至 WinHTTP 的應用程式，可能需要使用可在 WinINet 或 Internet Explorer (IE) 中取得的相同自動代理程式設定。 WinHTTP 5.1 版 API 可以取出並使用這些 proxy 設定。 一般而言，WinHTTP 會在建立會話時，指定每個會話的 proxy 和 proxy 略過伺服器。 您可以根據每個要求來覆寫這些設定。

若要使用與 WinINet 或 IE 相同的 proxy 設定，WinHTTP 用戶端應該設定會話的 proxy 設定。 此外，如果將 IE 或 WinINet 設定為使用 Web Proxy 自動探索 (WPAD) ，則使用這些設定的 WinHTTP 用戶端必須根據每個要求來設定 Proxy 設定。 下列各節說明如何指定會話和要求的 proxy 設定：

-   [設定會話的 Proxy 設定](#setting-the-proxy-configuration-on-a-session)
-   [在單一要求上設定 Proxy 設定](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>設定會話的 Proxy 設定

## <a name="the-application-is-running-on-a-user-account"></a>應用程式正在使用者帳戶上執行

在建立會話之前，應用程式會呼叫 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 以取得 IE proxy 設定。 應用程式必須以使用者帳戶的形式執行，才能取得這些設定。 *PProxyConfig* 參數是 [**WINHTTP \_ 目前 \_ 使用者的 \_ IE \_ PROXY \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)設定結構的指標，其中包含 proxy 名稱 (*lpszProxy*) 和 proxy 略過 (*lpszProxyBypass*) 伺服器。 接著會使用 **winHTTP \_ 目前 \_ 使用者 \_ IE \_ proxy \_** 設定結構的 proxy 名稱和 proxy 略過值來初始化 winHTTP 會話。 藉由呼叫 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)和從 **WINHTTP \_ 目前 \_ 使用者 \_ IE \_ PROXY \_** 設定結構的 **lpszProxy** 和 **lpszProxyBypass** 成員取得的 *pwszProxyName* 和 *pwszProxyBypass* 參數，初始化會話。

## <a name="the-application-is-running-as-a-service"></a>應用程式正在以服務方式執行

應用程式必須確保在呼叫 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)之前，將個別使用者的登錄設定載入登錄中。 如果這些設定未載入至登錄， **WinHttpGetIEProxyConfigForCurrentUser** 無法取得 proxy 設定。 您可以藉由呼叫 **LoadUserProfile** 函式，將個別使用者的登錄設定載入至登錄。 如果無法選擇載入使用者的登錄設定，則應用程式可以使用 *dwAcessType* 參數中指定的 **WINHTTP \_ 存取 \_ 類型 \_ 預設 \_ PROXY** 來呼叫 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 。 在 **WinHttpOpen** 的呼叫中指定預設 proxy，會指示 winHTTP API 使用 winHTTP [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) 公用程式來取得 proxy 設定集。 載入個別使用者的登錄設定之後，應用程式會遵循在 [使用者帳戶上執行的應用程式](#the-application-is-running-on-a-user-account) 所述的步驟，來設定 proxy 名稱和 proxy 略過伺服器。

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>在單一要求上設定 Proxy 設定

在建立會話之前，應用程式會呼叫 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 來判斷 WININET 和 IE 是否設定為使用 WPAD。 **WinHttpGetIEProxyConfigForCurrentUser** 會傳回 [**WINHTTP \_ 目前 \_ 使用者 \_ 的 \_ IE \_ PROXY**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) 設定結構，其中包含 **fAutoDetect** 成員。 此成員的 **TRUE** 值表示使用 wpad，且 **LPSZAUTOCONFIGURL** 成員包含 wpad URL。

## <a name="automatic-proxy-configuration-is-used"></a>使用自動 Proxy 設定

如果使用 WPAD，應用程式會呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 來取得要求的 proxy。 *LpwszUrl* 參數包含要將要求傳送至其中的 URL，而 *pAutoProxyOptions* 參數包含結構 (WINHTTP 自動 [**代理程式 \_ \_ 選項**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) 的指標，其中包含自動代理程式選項。 應用程式會使用 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)呼叫中 [**winHTTP \_ 目前 \_ 使用者的 \_ IE \_ PROXY \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)設定結構所傳回的設定，初始化 **WINHTTP 自動代理程式 \_ \_ 選項** 結構。 WinHTTP 自動代理程式設定 **\_ \_ \_ url** 旗標是在 winHTTP 自動代理程式 **\_ \_ 選項** 結構的 **DwFlags** 成員中指定， **lpszAutoconfigUrl** 成員則包含來自 **WINHTTP \_ 目前 \_ 使用者 \_ IE \_ proxy \_** 設定結構的 proxy 自動設定 url。 **WinHttpGetProxyForUrl** 函式會傳回 **lpszProxy** 中的 proxy 名稱和 proxy 略過清單，以及 [**WINHTTP \_ proxy \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)結構的 **lpszProxyBypass** 成員。

從 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)取得要求的 proxy 之後，應用程式會使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立要求。 然後藉由在 *hInternet* 參數中指定要求控制碼，呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)來設定要求的 proxy。 在 **WinHttpSetOption** 的呼叫中， *dwOption* 參數應該設定為 **WinHTTP \_ 選項 \_ PROXY** ，而 *lpBuffer* 參數則是包含用於要求的 proxy 和 proxy 略過之 [**winHTTP \_ proxy \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)結構的指標。

## <a name="automatic-proxy-configuration-is-not-used"></a>未使用自動 Proxy 設定

如果對 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) 的呼叫指出未使用自動代理程式，則應用程式可以直接使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立要求。 整個會話的 proxy 設定都相同，且不需要每個要求的變更。

 

 



