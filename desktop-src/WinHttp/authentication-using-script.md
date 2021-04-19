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
# <a name="authentication-using-script"></a><span data-ttu-id="78ae3-103">使用腳本進行驗證</span><span class="sxs-lookup"><span data-stu-id="78ae3-103">Authentication Using Script</span></span>

<span data-ttu-id="78ae3-104">本節示範如何撰寫腳本，以使用 [**WinHttpRequest**](winhttprequest.md) 物件從需要 HTTP 驗證的伺服器存取資料。</span><span class="sxs-lookup"><span data-stu-id="78ae3-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="78ae3-105">必要條件和需求</span><span class="sxs-lookup"><span data-stu-id="78ae3-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="78ae3-106">使用驗證存取網站</span><span class="sxs-lookup"><span data-stu-id="78ae3-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="78ae3-107">檢查狀態碼</span><span class="sxs-lookup"><span data-stu-id="78ae3-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="78ae3-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="78ae3-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="78ae3-109">必要條件和需求</span><span class="sxs-lookup"><span data-stu-id="78ae3-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="78ae3-110">除了使用 Microsoft JScript 的知識之外，此範例還需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="78ae3-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="78ae3-111">Microsoft Windows 軟體開發套件 (SDK 的最新版本) 。</span><span class="sxs-lookup"><span data-stu-id="78ae3-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="78ae3-112">如果您的網際網路連線是透過 proxy 伺服器，則 proxy 設定工具可建立 Microsoft Windows HTTP Services (WinHTTP) 的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="78ae3-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="78ae3-113">如需詳細資訊，請參閱 [Proxycfg.exe 的 Proxy 設定工具](proxycfg-exe--a-proxy-configuration-tool.md) 。</span><span class="sxs-lookup"><span data-stu-id="78ae3-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="78ae3-114">熟悉 [網路術語](network-terminology.md) 和概念。</span><span class="sxs-lookup"><span data-stu-id="78ae3-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="78ae3-115">使用驗證存取網站</span><span class="sxs-lookup"><span data-stu-id="78ae3-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="78ae3-116">**若要建立示範驗證的腳本，請執行下列動作：**</span><span class="sxs-lookup"><span data-stu-id="78ae3-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="78ae3-117">開啟文字編輯器，例如 Microsoft 記事本。</span><span class="sxs-lookup"><span data-stu-id="78ae3-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="78ae3-118">使用適當的文字來取代 "authenticationSite"，將下列程式碼複製到文字編輯器中， \[ \] 以指定需要 HTTP 驗證之網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="78ae3-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

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

    

3.  <span data-ttu-id="78ae3-119">將檔案儲存為「Auth.js」。</span><span class="sxs-lookup"><span data-stu-id="78ae3-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="78ae3-120">從命令提示字元輸入 "cscript Auth.js"，然後按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="78ae3-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="78ae3-121">您現在有一個程式要求資源兩種不同的方式。</span><span class="sxs-lookup"><span data-stu-id="78ae3-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="78ae3-122">第一個方法會要求資源，而不提供認證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="78ae3-123">傳回401狀態碼，表示伺服器需要驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="78ae3-124">回應標頭也會顯示，且看起來應該類似下列內容：</span><span class="sxs-lookup"><span data-stu-id="78ae3-124">The response headers are also displayed and should look similar to the following:</span></span>

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

<span data-ttu-id="78ae3-125">雖然回應表示拒絕存取資源，但仍會傳回數個標頭，以提供資源的一些相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78ae3-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="78ae3-126">名為「WWW-驗證」的標頭表示伺服器需要此資源的驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="78ae3-127">如果有名為「Proxy-驗證」的標頭，則表示 Proxy 伺服器需要驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="78ae3-128">每個驗證標頭都包含可用的驗證配置，有時也包含領域。</span><span class="sxs-lookup"><span data-stu-id="78ae3-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="78ae3-129">領域值會區分大小寫，而且會定義一組應接受相同認證的伺服器或 proxy。</span><span class="sxs-lookup"><span data-stu-id="78ae3-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="78ae3-130">有兩個標頭名為「WWW-驗證」，這表示支援多個驗證配置。</span><span class="sxs-lookup"><span data-stu-id="78ae3-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="78ae3-131">如果您呼叫 [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) 方法來尋找「WWW 驗證」標頭，則方法只會傳回該名稱之第一個標頭的內容。</span><span class="sxs-lookup"><span data-stu-id="78ae3-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="78ae3-132">在此情況下，它會傳回值 "NTLM"。</span><span class="sxs-lookup"><span data-stu-id="78ae3-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="78ae3-133">為了確保所有出現的標頭都已處理，請改用 [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="78ae3-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="78ae3-134">第二個方法呼叫會要求相同的資源，但會先藉由呼叫 [**SetCredentials**](iwinhttprequest-setcredentials.md) 方法提供驗證認證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="78ae3-135">下列程式碼區段會顯示如何使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="78ae3-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="78ae3-136">這個方法會將使用者名稱設定為 "UserName"，將密碼設定為 "Password"，並指出授權認證適用于資源伺服器。</span><span class="sxs-lookup"><span data-stu-id="78ae3-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="78ae3-137">驗證認證也可以傳送到 proxy。</span><span class="sxs-lookup"><span data-stu-id="78ae3-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="78ae3-138">當提供認證時，伺服器會傳回200狀態碼，指出可以取出檔。</span><span class="sxs-lookup"><span data-stu-id="78ae3-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="78ae3-139">檢查狀態碼</span><span class="sxs-lookup"><span data-stu-id="78ae3-139">Checking the Status Codes</span></span>

<span data-ttu-id="78ae3-140">上述範例是教學課程，但需要使用者明確提供認證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="78ae3-141">在必要時提供認證的應用程式，如果不需要，則不提供認證會更有用。</span><span class="sxs-lookup"><span data-stu-id="78ae3-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="78ae3-142">若要執行執行這項工作的功能，您必須修改範例以檢查回應所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="78ae3-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="78ae3-143">如需可能狀態碼的完整清單和描述，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="78ae3-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="78ae3-144">不過，在此範例中，您應該只會遇到三個程式碼中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="78ae3-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="78ae3-145">狀態碼200表示資源可供使用，且正在與回應一起傳送。</span><span class="sxs-lookup"><span data-stu-id="78ae3-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="78ae3-146">狀態碼401表示伺服器需要驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="78ae3-147">狀態碼407表示 proxy 需要驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="78ae3-148">以下列程式碼取代 "getText2" 函式，以修改您在上一節中建立的範例 (將 " \[ authenticationSite" 取代為 \] 您自己的文字，以指定需要 HTTP 驗證的網站 URL) ：</span><span class="sxs-lookup"><span data-stu-id="78ae3-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


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



<span data-ttu-id="78ae3-149">同樣地，儲存並執行該檔案。</span><span class="sxs-lookup"><span data-stu-id="78ae3-149">Again, save and run the file.</span></span> <span data-ttu-id="78ae3-150">第二種方法仍會抓取檔，但它只會在必要時提供認證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="78ae3-151">"GetText2" 函式會執行 [**開啟**](iwinhttprequest-open.md) 和 [**傳送**](iwinhttprequest-send.md) 方法，如同不需要驗證。</span><span class="sxs-lookup"><span data-stu-id="78ae3-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="78ae3-152">狀態會使用 [**status**](iwinhttprequest-status.md) 屬性抓取，而 switch 語句則會回應產生的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="78ae3-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="78ae3-153">如果狀態為 401 (server 需要驗證) 或 407 (proxy 需要驗證) ，則會再次執行 [**Open**](iwinhttprequest-open.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="78ae3-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="78ae3-154">後面接著 [**SetCredentials**](iwinhttprequest-setcredentials.md) 方法，它會設定使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="78ae3-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="78ae3-155">然後，程式碼會迴圈回 [**傳送**](iwinhttprequest-send.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="78ae3-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="78ae3-156">如果在三次嘗試之後，無法成功抓取資源，則函數會停止執行。</span><span class="sxs-lookup"><span data-stu-id="78ae3-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78ae3-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="78ae3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ae3-158">WinHTTP 中的驗證</span><span class="sxs-lookup"><span data-stu-id="78ae3-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="78ae3-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="78ae3-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="78ae3-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="78ae3-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="78ae3-161"> (RFC 2616) 的 HTTP/1.1 要求批註 </span><span class="sxs-lookup"><span data-stu-id="78ae3-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



