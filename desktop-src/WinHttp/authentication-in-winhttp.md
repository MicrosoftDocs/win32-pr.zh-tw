---
description: 某些 HTTP 伺服器和 proxy 需要驗證，才能允許存取網際網路上的資源。 Microsoft Windows HTTP Services (WinHTTP) 函數支援 HTTP 會話的伺服器和 proxy 驗證。
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: WinHTTP 中的驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192916"
---
# <a name="authentication-in-winhttp"></a>WinHTTP 中的驗證

某些 HTTP 伺服器和 proxy 需要驗證，才能允許存取網際網路上的資源。 Microsoft Windows HTTP Services (WinHTTP) 函數支援 HTTP 會話的伺服器和 proxy 驗證。

## <a name="about-http-authentication"></a>關於 HTTP 驗證

如果需要驗證，HTTP 應用程式會收到狀態碼 401 (server 需要驗證) 或 407 (proxy 需要驗證) 。 除了狀態碼，proxy 或伺服器也會傳送一或多個驗證標頭： WWW-Authenticate (進行伺服器驗證) 或 Proxy-Authenticate (進行 proxy 驗證) 。

每個驗證標頭都包含支援的驗證配置，以及適用于基本和摘要式配置的領域。 如果支援多個驗證配置，伺服器會傳回多個驗證標頭。 領域值會區分大小寫，而且會定義一組接受相同認證的伺服器或 proxy。 例如，在需要伺服器驗證時，可能會傳回標頭 "WWW-驗證：基本領域 =" 範例 ""。 此標頭會指定必須提供「範例」網域的使用者認證。

HTTP 應用程式可包含授權標頭欄位，並將要求傳送至伺服器。 授權標頭包含驗證配置，以及該配置所需的適當回應。 例如，如果用戶端收到回應標頭 "WWW-驗證：基本領域 =" 範例 ""，就會將 "Authorization： Basic <username： password>" 標頭新增至要求，並傳送至伺服器。

> [!Note]  
> 雖然在此以純文字形式顯示，但使用者名稱和密碼實際上是以 [*base64 編碼*](glossary.md)。

 

驗證架構有兩種一般類型：

-   基本驗證配置，在此配置中，使用者名稱和密碼會以純文字傳送至伺服器。

    基本驗證配置是以用戶端必須用來識別每個領域的使用者名稱和密碼的模型為基礎。 只有在要求是以包含有效使用者名稱和密碼的授權標頭傳送時，伺服器才會為要求提供服務。

-   挑戰-回應配置（例如 Kerberos），伺服器會使用 [*驗證資料*](glossary.md)來挑戰用戶端。 用戶端會使用使用者認證來轉換資料，並將轉換後的資料傳送回伺服器進行驗證。

    挑戰-回應配置可啟用更安全的驗證。 在挑戰-回應配置中，使用者名稱和密碼永遠不會透過網路傳輸。 在用戶端選取挑戰回應配置之後，伺服器會傳回適當的狀態碼，其中包含該配置的 [*驗證資料*](glossary.md) 。 然後，用戶端會以適當的回應重新傳送要求，以取得所要求的服務。 挑戰-回應配置可能需要多個交換才能完成。

下表包含 WinHTTP 支援的驗證配置、驗證類型，以及配置的描述。



| 配置            | 類型               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 基本 (純文字)  | 基本              | 使用 [*base64 編碼*](glossary.md) 的字串，其中包含使用者名稱和密碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | 挑戰-回應 | 使用 nonce (伺服器指定的資料字串) 值的挑戰。 有效的回應包含使用者名稱、密碼、指定的 nonce 值、 [*HTTP 動詞*](glossary.md)命令，以及要求的統一資源識別項 (URI) 的總和檢查碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | 挑戰-回應 | 需要使用使用者認證來轉換 [*驗證資料*](glossary.md) ，以證明身分識別。 若要讓 NTLM 驗證正常運作，必須在相同的連接上進行數個交換。 因此，如果仲介 proxy 不支援 keep-alive 連接，則無法使用 NTLM 驗證。 如果 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 搭配 [**WINHTTP \_ 停用 \_ 保持 \_**](option-flags.md) 運作旗標來停用 keep-alive 語義，則 NTLM 驗證也會失敗。                                                                                                                                                                                                                                       |
| Passport          | 挑戰-回應 | 使用 [Microsoft Passport 1.4](passport-authentication-in-winhttp.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 交涉         | 挑戰-回應 | 如果伺服器和用戶端都使用 Windows 2000 或更新版本，則會使用 Kerberos 驗證。 否則會使用 NTLM 驗證。 Kerberos 適用于 Windows 2000 和更新版本的作業系統，而且會被視為比 NTLM 驗證更安全。 若要讓 Negotiate 驗證正常運作，必須在相同的連接上進行數個交換。 因此，如果仲介 proxy 不支援 keep-alive 連接，則無法使用 Negotiate 驗證。 如果使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 搭配 [**WINHTTP \_ 停用 \_ 保持 \_**](option-flags.md) 運作旗標來停用 keep-alive 語義，則協商驗證也會失敗。 「協商驗證」配置有時也稱為整合式 Windows 驗證。 |



 

## <a name="authentication-in-winhttp-applications"></a>WinHTTP 應用程式中的驗證

 (API) 的 WinHTTP 應用程式開發介面提供兩個函式，可在需要驗證的情況下用來存取網際網路資源： [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 和 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)。

收到具有401或407狀態碼的回應時， [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 可以用來剖析驗證標頭，以判斷支援的驗證配置和驗證目標。 驗證目標是要求驗證的伺服器或 proxy。 **WinHttpQueryAuthSchemes** 也會根據伺服器建議的驗證配置喜好設定，從可用的配置中判斷第一個驗證配置。 這種選擇驗證配置的方法，是 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)所建議的行為。

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 可讓應用程式指定驗證配置，搭配有效的使用者名稱和密碼使用於目標伺服器或 proxy。 設定認證並重新傳送要求之後，會自動產生必要的標頭，並將其新增至要求。 由於某些驗證配置需要多個交易 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) 可能會傳回錯誤，因此會發生錯誤的 \_ WINHTTP 重 \_ 送 \_ 要求。 遇到此錯誤時，應用程式應繼續重新傳送要求，直到收到未包含401或407狀態碼的回應為止。 200狀態碼表示資源可供使用，且要求成功。 請參閱 [**HTTP 狀態碼**](http-status-codes.md) ，以取得可傳回的其他狀態碼。

如果在將要求傳送到伺服器之前，已知可接受的驗證配置和認證，則應用程式可以呼叫 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ，然後再呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)。 在此情況下，WinHTTP 會在伺服器的初始要求中提供認證或 [*驗證資料*](glossary.md) ，以嘗試向伺服器進行預先驗證。 預先驗證可以減少驗證程式中的交換次數，進而改善應用程式效能。

預先驗證可搭配下列驗證配置使用：

-   基本-永遠可行。
-   將解析成 Kerberos-可能很可能;唯一的例外狀況是用戶端與網域控制站之間的時間誤差已關閉。
-    (協商進入 NTLM) -永遠不可能發生。
-   只有在 Windows Server 2008 R2 中可以進行 NTLM。
-   摘要-永遠不可能。
-   Passport-永不可能;在最初的挑戰回應之後，WinHTTP 會使用 cookie 預先驗證 Passport。

一般的 WinHTTP 應用程式會完成下列步驟，才能處理驗證。

-   使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) 和 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)來要求資源。
-   使用 [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)檢查回應標頭。
-   如果傳回401或407狀態碼，表示需要驗證，請呼叫 [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) 來尋找可接受的配置。
-   使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)設定 [驗證配置]、[使用者名稱] 和 [密碼]。
-   藉由呼叫 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)，以相同的要求控制碼重新傳送要求。

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)所設定的認證只會用於一個要求。 WinHTTP 不會快取要在其他要求中使用的認證，這表示必須撰寫應用程式來回應多個要求。 如果重複使用已驗證的連線，其他要求可能不會有挑戰，但您的程式碼應該隨時都能回應要求。

### <a name="example-retrieving-a-document"></a>範例：抓取檔

下列範例程式碼會嘗試從 HTTP 伺服器取出指定的檔。 狀態碼會從回應中取出，以判斷是否需要驗證。 如果找到200狀態碼，則可以使用檔。 如果發現狀態碼401或407，則必須先進行驗證，然後才能抓取檔。 若為任何其他狀態碼，則會顯示錯誤訊息。 如需可能的狀態代碼清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md) 。


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>自動登入原則

自動登入 (自動登入) 原則會決定 WinHTTP 在要求中包含預設認證時，可接受的時間。 預設認證是目前的執行緒權杖或會話權杖，取決於是否在同步或非同步模式中使用 WinHTTP。 執行緒 token 是在同步模式中使用，而會話權杖則是在非同步模式中使用。 這些預設認證通常是用來登入 Microsoft Windows 的使用者名稱和密碼。

已執行自動登入原則，以避免將這些認證用於對不受信任的伺服器進行驗證。 根據預設，安全性層級會設定為 WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中等，這可讓預設認證僅用於內部網路要求。 自動登入原則僅適用于 NTLM 和協商驗證配置。 認證永遠不會與其他配置自動傳輸。

您可以使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式搭配 WINHTTP 選項自動登入 [**\_ \_ \_ 原則**](option-flags.md) 旗標來設定自動登入原則。 此旗標只適用于要求控制碼。 當原則設定為 WINHTTP 自動登 \_ 入 \_ 安全性 \_ 等級時 \_ ，預設認證可以傳送至所有伺服器。 當原則設定為 WINHTTP 自動登 \_ 入 \_ 安全性 \_ 等級 \_ 高時，預設認證無法用於驗證。 強烈建議您在中層級使用自動登入。

## <a name="stored-user-names-and-passwords"></a>儲存的使用者名稱與密碼

Windows XP 引進了預存使用者名稱和密碼的概念。 如果使用者的 Passport 認證是透過 **Passport 註冊嚮導** 或標準 **認證對話方塊** 來儲存，則會儲存在儲存的使用者名稱和密碼中。 在 Windows XP 或更新版本上使用 WinHTTP 時，如果未明確設定認證，WinHTTP 會自動使用預存使用者名稱和密碼中的認證。 這類似于支援 NTLM/Kerberos 的預設登入認證。 不過，使用預設的 Passport 認證並不受自動登入原則設定的規定。

 

 



