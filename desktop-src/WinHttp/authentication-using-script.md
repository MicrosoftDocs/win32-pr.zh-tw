---
description: 本節示範如何撰寫腳本，以使用 WinHttpRequest 物件從需要 HTTP 驗證的伺服器存取資料。
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: 使用腳本進行驗證
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981589"
---
# <a name="authentication-using-script"></a>使用腳本進行驗證

本節示範如何撰寫腳本，以使用 [**WinHttpRequest**](winhttprequest.md) 物件從需要 HTTP 驗證的伺服器存取資料。

-   [必要條件和需求](#prerequisites-and-requirements)
-   [使用驗證存取網站](#accessing-a-web-site-with-authentication)
-   [檢查狀態碼](#checking-the-status-codes)
-   [相關主題](#related-topics)

## <a name="prerequisites-and-requirements"></a>必要條件和需求

除了使用 Microsoft JScript 的知識之外，此範例還需要下列各項：

-   Microsoft Windows 軟體開發套件 (SDK 的最新版本) 。
-   如果您的網際網路連線是透過 proxy 伺服器，則 proxy 設定工具可建立 Microsoft Windows HTTP Services (WinHTTP) 的 proxy 設定。 如需詳細資訊，請參閱 [Proxycfg.exe 的 Proxy 設定工具](proxycfg-exe--a-proxy-configuration-tool.md) 。
-   熟悉 [網路術語](network-terminology.md) 和概念。

## <a name="accessing-a-web-site-with-authentication"></a>使用驗證存取網站

**若要建立示範驗證的腳本，請執行下列動作：**

1.  開啟文字編輯器，例如 Microsoft 記事本。
2.  使用適當的文字來取代 "authenticationSite"，將下列程式碼複製到文字編輯器中， \[ \] 以指定需要 HTTP 驗證之網站的 URL。

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  將檔案儲存為「Auth.js」。
4.  從命令提示字元輸入 "cscript Auth.js"，然後按 ENTER 鍵。

您現在有一個程式要求資源兩種不同的方式。 第一個方法會要求資源，而不提供認證。 傳回401狀態碼，表示伺服器需要驗證。 回應標頭也會顯示，且看起來應該類似下列內容：

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

雖然回應表示拒絕存取資源，但仍會傳回數個標頭，以提供資源的一些相關資訊。 名為「WWW-驗證」的標頭表示伺服器需要此資源的驗證。 如果有名為「Proxy-驗證」的標頭，則表示 Proxy 伺服器需要驗證。 每個驗證標頭都包含可用的驗證配置，有時也包含領域。 領域值會區分大小寫，而且會定義一組應接受相同認證的伺服器或 proxy。

有兩個標頭名為「WWW-驗證」，這表示支援多個驗證配置。 如果您呼叫 [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) 方法來尋找「WWW 驗證」標頭，則方法只會傳回該名稱之第一個標頭的內容。 在此情況下，它會傳回值 "NTLM"。 為了確保所有出現的標頭都已處理，請改用 [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) 方法。

第二個方法呼叫會要求相同的資源，但會先藉由呼叫 [**SetCredentials**](iwinhttprequest-setcredentials.md) 方法提供驗證認證。 下列程式碼區段會顯示如何使用這個方法。


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



這個方法會將使用者名稱設定為 "UserName"，將密碼設定為 "Password"，並指出授權認證適用于資源伺服器。 驗證認證也可以傳送到 proxy。

當提供認證時，伺服器會傳回200狀態碼，指出可以取出檔。

## <a name="checking-the-status-codes"></a>檢查狀態碼

上述範例是教學課程，但需要使用者明確提供認證。 在必要時提供認證的應用程式，如果不需要，則不提供認證會更有用。 若要執行執行這項工作的功能，您必須修改範例以檢查回應所傳回的狀態碼。

如需可能狀態碼的完整清單和描述，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。 不過，在此範例中，您應該只會遇到三個程式碼中的其中一個。 狀態碼200表示資源可供使用，且正在與回應一起傳送。 狀態碼401表示伺服器需要驗證。 狀態碼407表示 proxy 需要驗證。

以下列程式碼取代 "getText2" 函式，以修改您在上一節中建立的範例 (將 " \[ authenticationSite" 取代為 \] 您自己的文字，以指定需要 HTTP 驗證的網站 URL) ：


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



同樣地，儲存並執行該檔案。 第二種方法仍會抓取檔，但它只會在必要時提供認證。 "GetText2" 函式會執行 [**開啟**](iwinhttprequest-open.md) 和 [**傳送**](iwinhttprequest-send.md) 方法，如同不需要驗證。 狀態會使用 [**status**](iwinhttprequest-status.md) 屬性抓取，而 switch 語句則會回應產生的狀態碼。 如果狀態為 401 (server 需要驗證) 或 407 (proxy 需要驗證) ，則會再次執行 [**Open**](iwinhttprequest-open.md) 方法。 後面接著 [**SetCredentials**](iwinhttprequest-setcredentials.md) 方法，它會設定使用者名稱和密碼。 然後，程式碼會迴圈回 [**傳送**](iwinhttprequest-send.md) 方法。 如果在三次嘗試之後，無法成功抓取資源，則函數會停止執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinHTTP 中的驗證](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[ (RFC 2616) 的 HTTP/1.1 要求批註 ](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



