---
description: 本主題包含的範例會示範如何撰寫腳本，以同步或非同步方式透過 Microsoft Windows HTTP 服務 (WinHTTP) 取得資料。
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: 使用腳本來抓取資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936577"
---
# <a name="retrieving-data-using-script"></a><span data-ttu-id="5a6da-103">使用腳本來抓取資料</span><span class="sxs-lookup"><span data-stu-id="5a6da-103">Retrieving Data Using Script</span></span>

<span data-ttu-id="5a6da-104">本主題包含的範例會示範如何撰寫腳本，以同步或非同步方式透過 Microsoft Windows HTTP 服務 (WinHTTP) 取得資料。</span><span class="sxs-lookup"><span data-stu-id="5a6da-104">This topic includes an example of how to write a script that obtains data through Microsoft Windows HTTP Services (WinHTTP) either synchronously or asynchronously.</span></span> <span data-ttu-id="5a6da-105">在此範例中示範的概念，可提供撰寫需要使用 HTTP 通訊協定存取資料之用戶端或仲介層伺服器應用程式的基礎。</span><span class="sxs-lookup"><span data-stu-id="5a6da-105">The concepts demonstrated in this example provide the basis for writing client or middle-tier server applications that require access to data using the HTTP protocol.</span></span>

-   [<span data-ttu-id="5a6da-106">必要條件和需求</span><span class="sxs-lookup"><span data-stu-id="5a6da-106">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="5a6da-107">同步取出資料</span><span class="sxs-lookup"><span data-stu-id="5a6da-107">Retrieving Data Synchronously</span></span>](#retrieving-data-synchronously)
-   [<span data-ttu-id="5a6da-108">非同步地取出資料</span><span class="sxs-lookup"><span data-stu-id="5a6da-108">Retrieving Data Asynchronously</span></span>](#retrieving-data-asynchronously)
-   [<span data-ttu-id="5a6da-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a6da-109">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="5a6da-110">必要條件和需求</span><span class="sxs-lookup"><span data-stu-id="5a6da-110">Prerequisites and Requirements</span></span>

<span data-ttu-id="5a6da-111">除了使用 Microsoft JScript 的知識之外，此範例還需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="5a6da-111">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="5a6da-112">Microsoft Windows 軟體開發套件 (SDK 的最新版本) 。</span><span class="sxs-lookup"><span data-stu-id="5a6da-112">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="5a6da-113">如果您的網際網路連線是透過 proxy 伺服器，則 proxy 設定工具可建立 Microsoft Windows HTTP Services (WinHTTP) 的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="5a6da-113">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="5a6da-114">如需詳細資訊，請參閱 [ProxyCfg.exe Proxy 設定工具](proxycfg-exe--a-proxy-configuration-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="5a6da-114">For more information, see [ProxyCfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md).</span></span>
-   <span data-ttu-id="5a6da-115">熟悉 [網路術語](network-terminology.md) 和概念。</span><span class="sxs-lookup"><span data-stu-id="5a6da-115">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="5a6da-116">同步取出資料</span><span class="sxs-lookup"><span data-stu-id="5a6da-116">Retrieving Data Synchronously</span></span>

<span data-ttu-id="5a6da-117">**若要建立可同步從網頁取得文字的腳本，請執行下列動作：**</span><span class="sxs-lookup"><span data-stu-id="5a6da-117">**To create a script that obtains the text from a Web page synchronously, do the following:**</span></span>

1.  <span data-ttu-id="5a6da-118">開啟文字編輯器。</span><span class="sxs-lookup"><span data-stu-id="5a6da-118">Open a text editor.</span></span>
2.  <span data-ttu-id="5a6da-119">將下列程式碼複製到文字編輯器中。</span><span class="sxs-lookup"><span data-stu-id="5a6da-119">Copy the following code into the text editor.</span></span>

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  <span data-ttu-id="5a6da-120">將檔案儲存為「Retrieve.js」。</span><span class="sxs-lookup"><span data-stu-id="5a6da-120">Save the file as "Retrieve.js".</span></span>
4.  <span data-ttu-id="5a6da-121">從命令提示字元輸入 "cscript Retrieve.js"，然後按 ENTER 鍵。</span><span class="sxs-lookup"><span data-stu-id="5a6da-121">From a command prompt, type "cscript Retrieve.js" and press ENTER.</span></span>

<span data-ttu-id="5a6da-122">您現在有一個腳本，它會使用 [**WinHttpRequest**](winhttprequest.md) 物件來取得網頁的 HTML 原始程式碼 https://www.microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="5a6da-122">You now have a script that uses a [**WinHttpRequest**](winhttprequest.md) object to obtain the HTML source code for the Web page at https://www.microsoft.com.</span></span> <span data-ttu-id="5a6da-123">您可能必須等候幾秒鐘的時間才會顯示程式碼。</span><span class="sxs-lookup"><span data-stu-id="5a6da-123">You might have to wait several seconds for the code to appear.</span></span>

<span data-ttu-id="5a6da-124">應用程式只包含一個函式 "getText"。</span><span class="sxs-lookup"><span data-stu-id="5a6da-124">The application contains only one function, "getText".</span></span> <span data-ttu-id="5a6da-125">腳本的第一行會建立 [**WinHttpRequest**](winhttprequest.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5a6da-125">The first line of the script creates the [**WinHttpRequest**](winhttprequest.md) object.</span></span>


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



<span data-ttu-id="5a6da-126">當 JScript 引擎遇到這一行時，它會建立這個物件的實例。</span><span class="sxs-lookup"><span data-stu-id="5a6da-126">When the JScript engine encounters this line, it creates an instance of this object.</span></span> <span data-ttu-id="5a6da-127">如果您收到錯誤訊息：「ActiveX 元件無法建立物件」，在這一行中，很可能是 WinHttp.dll 未正確註冊或不存在於系統上。</span><span class="sxs-lookup"><span data-stu-id="5a6da-127">If you get the error message, "ActiveX component can't create object", on this line, most likely the WinHttp.dll was not properly registered or is not present on the system.</span></span>

<span data-ttu-id="5a6da-128">腳本的下一行會呼叫 [**Open**](iwinhttprequest-open.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a6da-128">The next line of the script calls the [**Open**](iwinhttprequest-open.md) method.</span></span>


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



<span data-ttu-id="5a6da-129">三個參數指定要使用的 [*HTTP 指令動詞*](glossary.md) 、資源的名稱，以及是否要以同步或非同步方式使用 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="5a6da-129">Three parameters specify which [*HTTP verb*](glossary.md) to use, the name of the resource, and whether to use WinHTTP synchronously or asynchronously.</span></span> <span data-ttu-id="5a6da-130">在此範例中，方法會使用 *HTTP 指令動詞*"GET" 來取得資料 https://www.microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="5a6da-130">In this example, the method is using the *HTTP verb*"GET" to obtain data from https://www.microsoft.com.</span></span> <span data-ttu-id="5a6da-131">針對最後一個參數指定 **FALSE** ，會決定交易是以同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="5a6da-131">Specifying **FALSE** for the last parameter determines that the transaction occurs synchronously.</span></span> <span data-ttu-id="5a6da-132">[**Open**](iwinhttprequest-open.md)方法不會建立與資源的連接，因為名稱可能暗示。</span><span class="sxs-lookup"><span data-stu-id="5a6da-132">The [**Open**](iwinhttprequest-open.md) method does not establish a connection to the resource as the name might imply.</span></span> <span data-ttu-id="5a6da-133">相反地，它會初始化維護會話、連接和要求之相關資訊的內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="5a6da-133">Rather, it initializes the internal data structures that maintain information about the session, connection, and request.</span></span>

<span data-ttu-id="5a6da-134">Send 方法會將要求標頭組合在一起，並 [**傳送**](iwinhttprequest-send.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="5a6da-134">The [**Send**](iwinhttprequest-send.md) method assembles the request headers and sends the request.</span></span> <span data-ttu-id="5a6da-135">在同步模式下呼叫時， [**傳送**](iwinhttprequest-send.md) 方法也會等候回應，然後才允許應用程式繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5a6da-135">When called in synchronous mode, the [**Send**](iwinhttprequest-send.md) method also waits for a response before allowing the application to continue.</span></span>


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



<span data-ttu-id="5a6da-136">傳送要求之後，腳本會傳回 [**WinHttpRequest**](winhttprequest.md)物件的 [**ResponseText**](iwinhttprequest-responsetext.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="5a6da-136">After sending the request, the script returns the value of the [**ResponseText**](iwinhttprequest-responsetext.md) property of the [**WinHttpRequest**](winhttprequest.md) object.</span></span> <span data-ttu-id="5a6da-137">此屬性包含回應的實體主體，在此案例中為檔的來源。</span><span class="sxs-lookup"><span data-stu-id="5a6da-137">This property contains the entity body of the response, in this case, the source of a document.</span></span>


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



<span data-ttu-id="5a6da-138">當資源的整個文字都被抓取時，腳本的執行就會暫停。</span><span class="sxs-lookup"><span data-stu-id="5a6da-138">Execution of the script pauses while the entire text of the resource is retrieved.</span></span> <span data-ttu-id="5a6da-139">資源文字會從函式傳回並顯示。</span><span class="sxs-lookup"><span data-stu-id="5a6da-139">The resource text is returned from the function and displayed.</span></span>

<span data-ttu-id="5a6da-140">[**WinHttpRequest**](winhttprequest.md)物件可確保任何針對 HTTP 交易配置的內部資源都會釋出。</span><span class="sxs-lookup"><span data-stu-id="5a6da-140">The [**WinHttpRequest**](winhttprequest.md) object ensures that any internal resources that are allocated for the HTTP transaction are released.</span></span>

## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="5a6da-141">非同步地取出資料</span><span class="sxs-lookup"><span data-stu-id="5a6da-141">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="5a6da-142">使用 WinHTTP 以非同步方式非同步地取出資料，與以同步方式抓取資料非常類似。</span><span class="sxs-lookup"><span data-stu-id="5a6da-142">Retrieving data asynchronously using WinHTTP is very similar to retrieving data synchronously.</span></span> <span data-ttu-id="5a6da-143">進行兩項小變更，以修改上一節中的腳本。</span><span class="sxs-lookup"><span data-stu-id="5a6da-143">Modify the script from the previous section by making two small changes.</span></span>

1.  <span data-ttu-id="5a6da-144">將 [**Open**](iwinhttprequest-open.md) 方法的第三個參數設定為 "true" 而不是 "false"，以指定應該以非同步方式執行 WinHTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="5a6da-144">Set the third parameter of the [**Open**](iwinhttprequest-open.md) method to "true" instead of "false" to specify that WinHTTP methods should be performed asynchronously.</span></span>
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  <span data-ttu-id="5a6da-145">先叫用 [**WaitForResponse**](iwinhttprequest-waitforresponse.md) 方法，再存取 [**ResponseText**](iwinhttprequest-responsetext.md) 屬性，以確保已收到整個回應。</span><span class="sxs-lookup"><span data-stu-id="5a6da-145">Invoke the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method before accessing the [**ResponseText**](iwinhttprequest-responsetext.md) property to ensure that the entire response has been received.</span></span>
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

<span data-ttu-id="5a6da-146">在腳本中以非同步方式使用 WinHTTP 的主要優點是 [**傳送**](iwinhttprequest-send.md) 方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="5a6da-146">The main advantage to using WinHTTP asynchronously in script is that the [**Send**](iwinhttprequest-send.md) method returns immediately.</span></span> <span data-ttu-id="5a6da-147">要求是由工作者執行緒準備和傳送。</span><span class="sxs-lookup"><span data-stu-id="5a6da-147">The request is prepared and sent by a worker thread.</span></span> <span data-ttu-id="5a6da-148">這可讓您的應用程式在等候回應時進行其他作業。</span><span class="sxs-lookup"><span data-stu-id="5a6da-148">This enables your application to do other things while it is waiting for the response.</span></span> <span data-ttu-id="5a6da-149">在嘗試存取回應之前，請先呼叫 [**WaitForResponse**](iwinhttprequest-waitforresponse.md) 方法，確定已收到整個回應。</span><span class="sxs-lookup"><span data-stu-id="5a6da-149">Before attempting to access the response, ensure that the entire response has been received by calling the [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method.</span></span> <span data-ttu-id="5a6da-150">否則可能會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a6da-150">Otherwise an error can occur.</span></span>

<span data-ttu-id="5a6da-151">[**WaitForResponse**](iwinhttprequest-waitforresponse.md)方法也可以用來指定交易的超時值。</span><span class="sxs-lookup"><span data-stu-id="5a6da-151">The [**WaitForResponse**](iwinhttprequest-waitforresponse.md) method can also be used to specify a time-out value for the transaction.</span></span> <span data-ttu-id="5a6da-152">選擇性的參數可讓您指定超時值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a6da-152">An optional parameter enables you to specify the time-out value in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a6da-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a6da-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a6da-154">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5a6da-154">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="5a6da-155"> (RFC 2616) 的 HTTP/1.1 要求批註 </span><span class="sxs-lookup"><span data-stu-id="5a6da-155">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



