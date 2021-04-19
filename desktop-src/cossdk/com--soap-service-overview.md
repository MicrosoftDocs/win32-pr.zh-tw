---
description: HTTP 因應電腦的使用，讓使用者可以使用網頁瀏覽器輕鬆地透過網路存取遠端伺服器上的資訊。
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: COM + SOAP 服務總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986257"
---
# <a name="com-soap-service-overview"></a><span data-ttu-id="74b9d-103">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="74b9d-103">COM+ SOAP Service Overview</span></span>

<span data-ttu-id="74b9d-104">HTTP 因應電腦的使用，讓使用者可以使用網頁瀏覽器輕鬆地透過網路存取遠端伺服器上的資訊。</span><span class="sxs-lookup"><span data-stu-id="74b9d-104">HTTP revolutionized computer use by allowing people to use a Web browser for easy access to information on a remote server over a network.</span></span> <span data-ttu-id="74b9d-105">XML web service 現在已可讓用戶端應用程式透過網路輕鬆呼叫遠端方法，來徹底改變應用程式開發。</span><span class="sxs-lookup"><span data-stu-id="74b9d-105">XML web services have now revolutionized application development by allowing client applications to easily call remote methods over a network.</span></span>

<span data-ttu-id="74b9d-106">這通常適用于用戶端應用程式呼叫在遠端伺服器上執行的方法。</span><span class="sxs-lookup"><span data-stu-id="74b9d-106">It is often useful for a client application to be able to call a method implemented on a remote server.</span></span> <span data-ttu-id="74b9d-107">有時方法會利用儲存在遠端伺服器上的變動性資訊 (例如，會傳回與指定的指示器符號) 對應之庫存的目前價格的方法。</span><span class="sxs-lookup"><span data-stu-id="74b9d-107">Sometimes the method makes use of volatile information stored on the remote server (for example, a method that returns the current price of the stock corresponding to a given ticker symbol).</span></span> <span data-ttu-id="74b9d-108">有時候，開發人員想要能夠升級方法，而不需要重新部署使用它的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="74b9d-108">At other times, the developer wants the ability to upgrade the methods implementation without having to redeploy all the applications that use it.</span></span>

<span data-ttu-id="74b9d-109">就像網頁一樣，XML web service 可透過網頁伺服器（例如 IIS）使用 HTTP 來存取。</span><span class="sxs-lookup"><span data-stu-id="74b9d-109">Like webpages, XML web services are accessed via a web server, such as IIS, using HTTP.</span></span> <span data-ttu-id="74b9d-110">但是，這些 HTTP 封包不是以 HTML 編碼的網頁，而是包含對伺服器上所執行方法的呼叫輸入和輸出參數，並以 SOAP 編碼。</span><span class="sxs-lookup"><span data-stu-id="74b9d-110">However, instead of webpages encoded in HTML, these HTTP packets contain the input and output parameters of calls to a method implemented on the server, encoded in SOAP.</span></span>

<span data-ttu-id="74b9d-111">若要使用 XML web service，您需要知道公開服務的 URL，以及您想要呼叫的方法名稱，而且必須提供方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="74b9d-111">To use an XML web service, you need to know the URL where the service is exposed and the name of the method you want to call, and you must provide the input parameters to the method.</span></span> <span data-ttu-id="74b9d-112">[SOAP 1.1 標準](https://www.w3.org/TR/SOAP/) 提供下列 HTTP 封包範例，其中包含 XML web service 的遠端呼叫 https://www.stockquoteserver.com/StockQuote ，後者會傳回對應至指定之指示器符號的存貨目前價格。</span><span class="sxs-lookup"><span data-stu-id="74b9d-112">[The SOAP 1.1 standard](https://www.w3.org/TR/SOAP/) provides the following example of an HTTP packet containing a remote call to an XML web service at https://www.stockquoteserver.com/StockQuote, which returns the current price of the stock corresponding to a given ticker symbol.</span></span>

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="74b9d-113">如先前的範例所示，SOAP 是可以內嵌在 HTTP 要求中的 XML 實例。</span><span class="sxs-lookup"><span data-stu-id="74b9d-113">As the preceding example illustrates, SOAP is an XML instance that can be embedded in an HTTP request.</span></span> <span data-ttu-id="74b9d-114">同樣地，結果會以具有 SOAP 承載的 HTTP 封包傳回，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="74b9d-114">Similarly, the result is returned as an HTTP packet with a SOAP payload, as shown in the following example.</span></span>

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

<span data-ttu-id="74b9d-115">雖然對 XML web service 的基礎結構有一些瞭解很有説明，但 COM + 讓您很容易就能建立及使用 XML web service，而您通常不需要深入探究此層級。</span><span class="sxs-lookup"><span data-stu-id="74b9d-115">While it is helpful to have some understanding of the infrastructure that underlies XML web services, COM+ makes it so easy to create and use XML web services that you won't often have to delve to this level.</span></span>

<span data-ttu-id="74b9d-116">您可以將任何 COM + 應用程式中已設定 COM 元件的預設介面中的方法公開為 XML web service。</span><span class="sxs-lookup"><span data-stu-id="74b9d-116">You can expose the methods in the default interfaces of the configured COM components in any COM+ application as an XML web service.</span></span> <span data-ttu-id="74b9d-117">撰寫元件時，不需要任何特殊的程式設計考慮，不同之處在于您想要公開的方法必須在預設介面中，而且必須在伺服器的 COM + 目錄) 中設定 (元件。</span><span class="sxs-lookup"><span data-stu-id="74b9d-117">No special programming considerations are necessary when writing the components, except that the methods you want to expose must be in the default interface and the component must be configured (in your server's COM+ catalog).</span></span> <span data-ttu-id="74b9d-118">您不需要撰寫程式碼來透過網路介面進行通訊，或剖析 SOAP。</span><span class="sxs-lookup"><span data-stu-id="74b9d-118">You need not write code to communicate via a network interface or to parse SOAP.</span></span> <span data-ttu-id="74b9d-119">如需有關使用 COM + SOAP 服務來建立 XML web service 的詳細指示，請參閱 [建立 Xml Web 服務](creating-xml-web-services.md)。</span><span class="sxs-lookup"><span data-stu-id="74b9d-119">For detailed instructions about using the COM+ SOAP service to create an XML web service, see [Creating XML Web Services](creating-xml-web-services.md).</span></span>

<span data-ttu-id="74b9d-120">當您將 COM + 應用程式公開為 XML web service 時，會使用 Web 服務描述語言 (WSDL) ，自動發行 XML web service 所提供之所有方法語法的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="74b9d-120">When you expose a COM+ application as an XML web service, detailed information about the syntax of all the methods available from an XML web service is published automatically, using the Web Services Description Language (WSDL).</span></span> <span data-ttu-id="74b9d-121">使用您的 XML web service 的用戶端會使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="74b9d-121">This information is used by clients that use your XML web service.</span></span>

<span data-ttu-id="74b9d-122">COM + 提供兩種方式讓您存取和使用遠端 XML web 服務，如下所示：</span><span class="sxs-lookup"><span data-stu-id="74b9d-122">COM+ provides two ways for you to access and use a remote XML web service, as follows:</span></span>

-   <span data-ttu-id="74b9d-123">*已知的物件* (WKO) 模式可用來存取任何使用 WSDL 發行其語法的 xml web service，即使該 xml web service 不是使用 com + 或甚至是 Microsoft Windows 來建立也一樣。</span><span class="sxs-lookup"><span data-stu-id="74b9d-123">The *well-known object* (WKO) mode can be used to access any XML web service that publishes its syntax using WSDL, even if that XML web service was not created using COM+ or even Microsoft Windows.</span></span>
-   <span data-ttu-id="74b9d-124"> (CAO) 模式的 *用戶端啟始物件* 只能用來存取公開 com + 應用程式所建立的 XML web service。</span><span class="sxs-lookup"><span data-stu-id="74b9d-124">The *client-activated object* (CAO) mode can be used only to access XML web services created by exposing COM+ applications.</span></span> <span data-ttu-id="74b9d-125">CAO 模式使用持續連線（目前的 SOAP 標準不支援的功能）來提升效能。</span><span class="sxs-lookup"><span data-stu-id="74b9d-125">CAO mode increases performance by using persistent connections, a feature not supported by the current SOAP standard.</span></span>

<span data-ttu-id="74b9d-126">這兩種方法都可讓用戶端應用程式以直接的方式從遠端呼叫 XML web service 的方法，而不需要撰寫程式碼來透過網路介面進行通訊或剖析 SOAP。</span><span class="sxs-lookup"><span data-stu-id="74b9d-126">Both methods allow client applications to call the methods of XML web services remotely in a straightforward fashion, without having to write code to communicate via a network interface or parse SOAP.</span></span> <span data-ttu-id="74b9d-127">如需有關如何在任一模式中存取 XML web service 的詳細資訊，請參閱以 [CAO 模式存取 Xml Web service](accessing-xml-web-services-in-cao-mode.md) 和 [在 WKO 模式中存取 xml web service](accessing-xml-web-services-in-wko-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="74b9d-127">For details about how to access XML web services in either mode, see [Accessing XML Web Services in CAO Mode](accessing-xml-web-services-in-cao-mode.md) and [Accessing XML Web Services in WKO Mode](accessing-xml-web-services-in-wko-mode.md).</span></span>

> [!Note]  
> <span data-ttu-id="74b9d-128">COM + 僅支援 SOAP-RPC 規格，而不支援 SOAP-Document 規格。</span><span class="sxs-lookup"><span data-stu-id="74b9d-128">COM+ supports only the SOAP-RPC specification, not the SOAP-Document specification.</span></span>

 

<span data-ttu-id="74b9d-129">COM + 可讓您以完全透明的方式使用現有的 COM + 應用程式作為 CAO 模式的 XML web 服務，讓您更輕鬆地使用 XML web service。</span><span class="sxs-lookup"><span data-stu-id="74b9d-129">COM+ makes using XML web services especially easy by allowing you to use existing COM+ applications as XML web services in CAO mode in a completely transparent fashion.</span></span> <span data-ttu-id="74b9d-130">如果您 [匯出](exporting-a-soap-enabled-application.md) 的 com + 應用程式已從伺服器公開為 XML web service，則任何 [匯入應用](importing-a-soap-enabled-application.md) 程式的用戶端都可以在每次使用匯入的應用程式時，以透明的方式使用伺服器的 XML web service。</span><span class="sxs-lookup"><span data-stu-id="74b9d-130">If you [export](exporting-a-soap-enabled-application.md) a COM+ application that has been exposed as an XML web service from your server, any client that [imports](importing-a-soap-enabled-application.md) the application can transparently use the server's XML web service whenever the imported application is used.</span></span> <span data-ttu-id="74b9d-131">這項功能可讓現有的 COM + 應用程式轉換為 XML web 服務，並透過網路部署這些服務非常簡單。</span><span class="sxs-lookup"><span data-stu-id="74b9d-131">This facility makes the conversion of existing COM+ applications to XML web services and the deployment of those services over a network very easy.</span></span>

<span data-ttu-id="74b9d-132">使用 XML web service 有幾個獨特的優點，也就是遠端程序呼叫的替代執行 (RPC) ，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="74b9d-132">Using XML web services has several unique advantages over alternative implementations of remote procedure calls (RPC), including the following:</span></span>

-   <span data-ttu-id="74b9d-133">SOAP 是真正的跨平臺 RPC 實施，可提高互通性。</span><span class="sxs-lookup"><span data-stu-id="74b9d-133">SOAP is a true cross-platform RPC implementation, which increases interoperability.</span></span>
-   <span data-ttu-id="74b9d-134">XML web service 支援具有輸入和輸出參數的方法。</span><span class="sxs-lookup"><span data-stu-id="74b9d-134">XML web services support methods with both input and output parameters.</span></span>
-   <span data-ttu-id="74b9d-135">XML web service 會透過 HTTP 執行，通常會滲透可能封鎖其他 RPC 執行的防火牆。</span><span class="sxs-lookup"><span data-stu-id="74b9d-135">XML web services run over HTTP, which can usually penetrate firewalls that might block other RPC implementations.</span></span>
-   <span data-ttu-id="74b9d-136">使用 COM + 執行 XML web service 時，開發人員不需要撰寫任何特製化的程式碼;這是優於替代 RPC 機制的巨大優勢。</span><span class="sxs-lookup"><span data-stu-id="74b9d-136">When an XML web service is implemented using COM+, the developer does not have to write any specialized code; this is a tremendous advantage over alternative RPC mechanisms.</span></span>

> [!Note]  
> <span data-ttu-id="74b9d-137">XML web service 不支援非同步或透明的交易式呼叫。</span><span class="sxs-lookup"><span data-stu-id="74b9d-137">XML web services do not support asynchronous or transparently transactional calls.</span></span> <span data-ttu-id="74b9d-138">當您需要這種功能時，請使用 [Com + 佇列的元件](com--queued-components.md) 服務。</span><span class="sxs-lookup"><span data-stu-id="74b9d-138">Use the [COM+ Queued Components](com--queued-components.md) service when you require this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="74b9d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="74b9d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b9d-140">COM + SOAP 服務安全性考慮</span><span class="sxs-lookup"><span data-stu-id="74b9d-140">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



