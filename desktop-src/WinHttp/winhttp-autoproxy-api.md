---
description: WinHTTP 使用 WinHttpGetProxyForUrl 函式，以及兩個支援公用程式函式（WinHttpDetectAutoProxyConfigUrl 和 WinHttpGetIEProxyConfigForCurrentUser）來執行 WPAD 通訊協定。
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: WinHTTP 自動代理函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955708"
---
# <a name="winhttp-autoproxy-functions"></a>WinHTTP 自動代理函數

WinHTTP 使用 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 函式，以及兩個支援公用程式函式（ [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) 和 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)）來執行 WPAD 通訊協定。

自動代理程式支援並未完全整合到 WinHTTP 中的 HTTP 堆疊。 在傳送要求之前，應用程式必須呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)來取得 proxy 伺服器的名稱，然後使用 **WINHTTP \_ 選項 \_ proxy** 呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ，以在 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)所建立的 WINHTTP 要求控制碼上設定 proxy 設定。

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)函式可以執行上一步中所述之 WPAD 通訊協定的三個步驟： (1) 探索 pac URL， (2) 下載 pac 腳本檔案， (3) 執行腳本，並傳回 **WINHTTP \_ proxy \_ 資訊** 結構中的 proxy 設定。 （選擇性）如果應用程式事先知道 PAC URL，它可以將它指定為 **WinHttpGetProxyForUrl**。

下列範例程式碼使用自動代理程式。 它會先建立 WinHTTP 會話連接和要求控制碼，以設定 HTTP GET 要求。 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)呼叫會為初始 PROXY 設定指定 **WINHTTP \_ 存取 \_ 類型 \_ NO \_ proxy** ，以指出依預設會將要求直接傳送到目標伺服器。 接著，它會使用自動代理，在要求控制碼上直接設定 proxy 設定。


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



在提供的範例程式碼中，對 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)的呼叫會指示函式在 [**winHTTP 自動代理程式 \_ \_ 選項**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)結構中指定 winHTTP 自動代理程式 **\_ \_ 自動 \_** 偵測旗標，以自動探索 proxy 自動設定檔案。 使用「 **winHTTP 自動 \_ 代理程式 \_ 自動 \_** 偵測」旗標需要程式碼指定一或兩個自動偵測旗標 (**WINHTTP 自動偵測型別 \_ \_ \_ \_ DHCP**、 **winHTTP 自動偵測型別 \_ \_ \_ \_ DNS \_ A**) 。 範例程式碼會使用 **WinHttpGetProxyForUrl** 的自動偵測功能，因為 PAC URL 事先不知道。 在此案例中，如果無法在網路上找到 PAC URL， **WinHttpGetProxyForUrl** 會失敗 ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **錯誤 WINHTTP 自動偵測 \_ \_ \_ 失敗**) 。

## <a name="if-the-pac-url-is-known-in-advance"></a>如果事先知道 PAC URL

如果應用程式知道 PAC URL，它可以在 WINHTTP 自動代理程式選項結構中指定它， \_ \_ 並設定 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 略過自動偵測階段。

例如，如果可在區域網路的 URL "" 上取得 PAC 檔案，則 https://InternalSite/proxy-config.pac 呼叫 [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 會如下所示。


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



如果 [**winHTTP 自動 \_ 代理程式 \_ 選項**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) 結構同時指定了 winHTTP 自動偵測自動偵測和 winHTTP **\_ \_ 自動 \_** 代理程式設定 **\_ \_ \_ URL** 旗標 (並指定自動 detction 旗標和自動設定 url) ， [**WINHTTPGETPROXYFORURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 會先嘗試自動偵測，然後如果自動偵測找不到 PAC URL，則會「回復」至應用程式所提供的自動設定 URL。

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>WinHttpDetectAutoProxyConfigUrl 函式

[**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)函式會執行 WPAD 通訊協定的子集：它會嘗試自動偵測 proxy 自動設定檔案的 URL，而不需要下載或執行 PAC 檔案。 在 Web 用戶端應用程式必須處理 PAC 檔案本身的下載和執行的特殊情況下，此函式很有用。

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>WinHttpGetIEProxyConfigForCurrentUser 函式

[**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)函式會傳回目前使用中網路連線的目前使用者 Internet Explorer proxy 設定，而不需要呼叫 "WinInet.dll"。 只有在以互動式使用者帳戶身分識別執行的進程內呼叫時，此函式才有用處，因為在其他情況下，可能不會有 Internet Explorer proxy 設定。 例如，從 IIS 服務處理常式中執行的 ISAPI DLL 呼叫這個函式會很有用。 如需以 WinHTTP 為基礎的應用程式會使用 **WinHttpGetIEProxyConfigForCurrentUser** 的詳細資訊和案例，請參閱 [不含自動設定檔的探索](discovery-without-an-auto-config-file.md)。

 

 
