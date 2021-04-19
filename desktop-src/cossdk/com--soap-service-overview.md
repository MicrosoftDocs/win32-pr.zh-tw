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
# <a name="com-soap-service-overview"></a>COM + SOAP 服務總覽

HTTP 因應電腦的使用，讓使用者可以使用網頁瀏覽器輕鬆地透過網路存取遠端伺服器上的資訊。 XML web service 現在已可讓用戶端應用程式透過網路輕鬆呼叫遠端方法，來徹底改變應用程式開發。

這通常適用于用戶端應用程式呼叫在遠端伺服器上執行的方法。 有時方法會利用儲存在遠端伺服器上的變動性資訊 (例如，會傳回與指定的指示器符號) 對應之庫存的目前價格的方法。 有時候，開發人員想要能夠升級方法，而不需要重新部署使用它的所有應用程式。

就像網頁一樣，XML web service 可透過網頁伺服器（例如 IIS）使用 HTTP 來存取。 但是，這些 HTTP 封包不是以 HTML 編碼的網頁，而是包含對伺服器上所執行方法的呼叫輸入和輸出參數，並以 SOAP 編碼。

若要使用 XML web service，您需要知道公開服務的 URL，以及您想要呼叫的方法名稱，而且必須提供方法的輸入參數。 [SOAP 1.1 標準](https://www.w3.org/TR/SOAP/) 提供下列 HTTP 封包範例，其中包含 XML web service 的遠端呼叫 https://www.stockquoteserver.com/StockQuote ，後者會傳回對應至指定之指示器符號的存貨目前價格。

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

如先前的範例所示，SOAP 是可以內嵌在 HTTP 要求中的 XML 實例。 同樣地，結果會以具有 SOAP 承載的 HTTP 封包傳回，如下列範例所示。

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

雖然對 XML web service 的基礎結構有一些瞭解很有説明，但 COM + 讓您很容易就能建立及使用 XML web service，而您通常不需要深入探究此層級。

您可以將任何 COM + 應用程式中已設定 COM 元件的預設介面中的方法公開為 XML web service。 撰寫元件時，不需要任何特殊的程式設計考慮，不同之處在于您想要公開的方法必須在預設介面中，而且必須在伺服器的 COM + 目錄) 中設定 (元件。 您不需要撰寫程式碼來透過網路介面進行通訊，或剖析 SOAP。 如需有關使用 COM + SOAP 服務來建立 XML web service 的詳細指示，請參閱 [建立 Xml Web 服務](creating-xml-web-services.md)。

當您將 COM + 應用程式公開為 XML web service 時，會使用 Web 服務描述語言 (WSDL) ，自動發行 XML web service 所提供之所有方法語法的詳細資訊。 使用您的 XML web service 的用戶端會使用這項資訊。

COM + 提供兩種方式讓您存取和使用遠端 XML web 服務，如下所示：

-   *已知的物件* (WKO) 模式可用來存取任何使用 WSDL 發行其語法的 xml web service，即使該 xml web service 不是使用 com + 或甚至是 Microsoft Windows 來建立也一樣。
-    (CAO) 模式的 *用戶端啟始物件* 只能用來存取公開 com + 應用程式所建立的 XML web service。 CAO 模式使用持續連線（目前的 SOAP 標準不支援的功能）來提升效能。

這兩種方法都可讓用戶端應用程式以直接的方式從遠端呼叫 XML web service 的方法，而不需要撰寫程式碼來透過網路介面進行通訊或剖析 SOAP。 如需有關如何在任一模式中存取 XML web service 的詳細資訊，請參閱以 [CAO 模式存取 Xml Web service](accessing-xml-web-services-in-cao-mode.md) 和 [在 WKO 模式中存取 xml web service](accessing-xml-web-services-in-wko-mode.md)。

> [!Note]  
> COM + 僅支援 SOAP-RPC 規格，而不支援 SOAP-Document 規格。

 

COM + 可讓您以完全透明的方式使用現有的 COM + 應用程式作為 CAO 模式的 XML web 服務，讓您更輕鬆地使用 XML web service。 如果您 [匯出](exporting-a-soap-enabled-application.md) 的 com + 應用程式已從伺服器公開為 XML web service，則任何 [匯入應用](importing-a-soap-enabled-application.md) 程式的用戶端都可以在每次使用匯入的應用程式時，以透明的方式使用伺服器的 XML web service。 這項功能可讓現有的 COM + 應用程式轉換為 XML web 服務，並透過網路部署這些服務非常簡單。

使用 XML web service 有幾個獨特的優點，也就是遠端程序呼叫的替代執行 (RPC) ，包括下列各項：

-   SOAP 是真正的跨平臺 RPC 實施，可提高互通性。
-   XML web service 支援具有輸入和輸出參數的方法。
-   XML web service 會透過 HTTP 執行，通常會滲透可能封鎖其他 RPC 執行的防火牆。
-   使用 COM + 執行 XML web service 時，開發人員不需要撰寫任何特製化的程式碼;這是優於替代 RPC 機制的巨大優勢。

> [!Note]  
> XML web service 不支援非同步或透明的交易式呼叫。 當您需要這種功能時，請使用 [Com + 佇列的元件](com--queued-components.md) 服務。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + SOAP 服務安全性考慮](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



