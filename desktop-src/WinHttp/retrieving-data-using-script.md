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
ms.openlocfilehash: 9e018aa680808feddc021c7c03937d085b0d0f787c3213720cbb5e94a46a85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133061"
---
# <a name="retrieving-data-using-script"></a>使用腳本來抓取資料

本主題包含的範例會示範如何撰寫腳本，以同步或非同步方式透過 Microsoft Windows HTTP 服務 (WinHTTP) 取得資料。 在此範例中示範的概念，可提供撰寫需要使用 HTTP 通訊協定存取資料之用戶端或仲介層伺服器應用程式的基礎。

-   [必要條件和需求](#prerequisites-and-requirements)
-   [同步取出資料](#retrieving-data-synchronously)
-   [非同步地取出資料](#retrieving-data-asynchronously)
-   [相關主題](#related-topics)

## <a name="prerequisites-and-requirements"></a>必要條件和需求

除了 Microsoft JScript 的工作知識之外，此範例還需要下列各項：

-   Microsoft Windows 軟體開發套件 (SDK 的最新版本) 。
-   如果您的網際網路連線是透過 proxy 伺服器，則可使用 proxy 設定工具來建立 Microsoft Windows HTTP 服務 (WinHTTP) 的 proxy 設定。 如需詳細資訊，請參閱 [ProxyCfg.exe Proxy 設定工具](proxycfg-exe--a-proxy-configuration-tool.md)。
-   熟悉 [網路術語](network-terminology.md) 和概念。

## <a name="retrieving-data-synchronously"></a>同步取出資料

**若要建立可同步從網頁取得文字的腳本，請執行下列動作：**

1.  開啟文字編輯器。
2.  將下列程式碼複製到文字編輯器中。

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

    

3.  將檔案儲存為「Retrieve.js」。
4.  從命令提示字元輸入 "cscript Retrieve.js"，然後按 ENTER 鍵。

您現在有一個腳本，它會使用 [**WinHttpRequest**](winhttprequest.md) 物件來取得網頁的 HTML 原始程式碼 https://www.microsoft.com 。 您可能必須等候幾秒鐘的時間才會顯示程式碼。

應用程式只包含一個函式 "getText"。 腳本的第一行會建立 [**WinHttpRequest**](winhttprequest.md) 物件。


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



當 JScript 引擎遇到這一行時，它會建立這個物件的實例。 如果您收到錯誤訊息：「ActiveX 元件無法建立物件」，這一行很可能是因為 WinHttp.dll 未正確註冊或不存在於系統上。

腳本的下一行會呼叫 [**Open**](iwinhttprequest-open.md) 方法。


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



三個參數指定要使用的 [*HTTP 指令動詞*](glossary.md) 、資源的名稱，以及是否要以同步或非同步方式使用 WinHTTP。 在此範例中，方法會使用 *HTTP 指令動詞*"GET" 來取得資料 https://www.microsoft.com 。 針對最後一個參數指定 **FALSE** ，會決定交易是以同步方式進行。 [**Open**](iwinhttprequest-open.md)方法不會建立與資源的連接，因為名稱可能暗示。 相反地，它會初始化維護會話、連接和要求之相關資訊的內部資料結構。

Send 方法會將要求標頭組合在一起，並 [**傳送**](iwinhttprequest-send.md) 要求。 在同步模式下呼叫時， [**傳送**](iwinhttprequest-send.md) 方法也會等候回應，然後才允許應用程式繼續進行。


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



傳送要求之後，腳本會傳回 [**WinHttpRequest**](winhttprequest.md)物件的 [**ResponseText**](iwinhttprequest-responsetext.md)屬性值。 此屬性包含回應的實體主體，在此案例中為檔的來源。


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



當資源的整個文字都被抓取時，腳本的執行就會暫停。 資源文字會從函式傳回並顯示。

[**WinHttpRequest**](winhttprequest.md)物件可確保任何針對 HTTP 交易配置的內部資源都會釋出。

## <a name="retrieving-data-asynchronously"></a>非同步地取出資料

使用 WinHTTP 以非同步方式非同步地取出資料，與以同步方式抓取資料非常類似。 進行兩項小變更，以修改上一節中的腳本。

1.  將 [**Open**](iwinhttprequest-open.md) 方法的第三個參數設定為 "true" 而不是 "false"，以指定應該以非同步方式執行 WinHTTP 方法。
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  先叫用 [**WaitForResponse**](iwinhttprequest-waitforresponse.md) 方法，再存取 [**ResponseText**](iwinhttprequest-responsetext.md) 屬性，以確保已收到整個回應。
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

在腳本中以非同步方式使用 WinHTTP 的主要優點是 [**傳送**](iwinhttprequest-send.md) 方法會立即傳回。 要求是由工作者執行緒準備和傳送。 這可讓您的應用程式在等候回應時進行其他作業。 在嘗試存取回應之前，請先呼叫 [**WaitForResponse**](iwinhttprequest-waitforresponse.md) 方法，確定已收到整個回應。 否則可能會發生錯誤。

[**WaitForResponse**](iwinhttprequest-waitforresponse.md)方法也可以用來指定交易的超時值。 選擇性的參數可讓您指定超時值（以秒為單位）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[ (RFC 2616) 的 HTTP/1.1 要求批註 ](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



