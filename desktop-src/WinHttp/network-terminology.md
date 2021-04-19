---
description: 在開發使用 Microsoft Windows HTTP Services (WinHTTP) 的應用程式時，請務必瞭解下列與一般網路功能相關的概念和術語，尤其是 HTTP 通訊協定。
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: " (WinHTTP) 的網路術語"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998124"
---
# <a name="network-terminology-winhttp"></a> (WinHTTP) 的網路術語

在開發使用 Microsoft Windows HTTP Services (WinHTTP) 的應用程式時，請務必瞭解下列與一般網路功能相關的概念和術語，尤其是 HTTP 通訊協定。

-   [HTTP 交易](#http-transactions)
-   [Proxy 伺服器](#proxy-servers)
-   [同步和非同步模式](#synchronous-and-asynchronous-modes)
-   [驗證](#authentication)

## <a name="http-transactions"></a>HTTP 交易

當您使用 HTTP 交易時，會與網路上其他位置的其他電腦交換資訊。 交換的資訊可以是包含文字或多媒體的檔案，也可以是資料庫查詢的結果。 透過網路交換的部分資訊稱為 *資源*。 通常傳送資源的電腦是伺服器，而接收該資源的電腦是用戶端。 不過，用戶端也可以將資料張貼至伺服器。 有時 HTTP 交易牽涉到仲介層伺服器。 仲介層伺服器會收集來自其他伺服器的數個資源、將資訊編譯成一個資源，然後將該資源傳送給用戶端。

使用 HTTP 通訊協定取得資源的程式需要在用戶端與伺服器之間交換一系列的訊息。 用戶端會傳送要求資源的訊息來開始交易。 此訊息稱為 HTTP 要求，或有時只是要求。 HTTP 要求是由下列元件所組成。

-   方法、統一資源識別項 (URI) 、通訊協定版本號碼
-   標題
-   實體主體

當伺服器收到要求時，它會藉由將訊息傳送回用戶端來回應。 伺服器所傳送的訊息稱為 HTTP 回應。 HTTP 回應是由下列元件所組成。

-   通訊協定版本號碼、狀態碼和狀態文字
-   標題
-   實體主體

回應可能表示無法處理要求，或提供要求的資訊。 根據要求的類型而定，這可能是資源的相關資訊，例如其大小和類型，或者可以是部分或全部資源本身。 回應的部分（包括部分或全部要求的資源）稱為「回應資料」或「實體主體」，在收到所有回應資料之前，回應都不會完成。

如需有關 HTTP 交易與 HTTP 通訊協定的詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)、超文字傳輸通訊協定（HTTP/1.1）。

## <a name="proxy-servers"></a>Proxy 伺服器

雖然目標伺服器最後會收到用戶端傳送的要求，但有時候交易會先通過 proxy 伺服器。 Proxy 會攔截要求，甚至可以修改要求，再將它傳送至伺服器。 當伺服器回應時，回應也會在轉送至用戶端之前通過 proxy。 Proxy 可以修改此回應中的標頭。

藉由攔截和轉譯網路交易，proxy 可以：

-   藉由監視潛在的危險交易來保護用戶端。
-   讓用戶端使用用戶端軟體可能不會執行的通訊協定進行通訊。
-   作為私人網路與公用網路之間的閘道。

WinHTTP API 包含 proxy 設定工具，可讓您為 WinHTTP 提供任何會攔截 HTTP 交易之 proxy 伺服器的相關資訊。 如需使用 proxy 設定工具的詳細資訊，請參閱 [ProxyCfg.exe proxy 設定工具](proxycfg-exe--a-proxy-configuration-tool.md)。

## <a name="synchronous-and-asynchronous-modes"></a>同步和非同步模式

有兩種程式設計模型可讓您透過網路使用 WinHTTP （同步和非同步模型）來取得資源。 在同步模型中，在要求的作業完成或發生錯誤之前，對函式或方法的呼叫不會完成。 例如，當您的應用程式以同步方式使用 WinHTTP 要求資源時，除非收到要求的資料，否則不會繼續下一個步驟。

另一方面，非同步模型可讓應用程式在等候資源被抓取時執行其他工作。 如果呼叫另一個 WinHTTP 函數或方法，但先前的作業尚未完成，則函式會傳回錯誤。 以非同步方式使用 WinHTTP 時，元件物件模型 (COM) 事件和回呼可用來通知應用程式在 HTTP 操作中的進度。

## <a name="authentication"></a>驗證

驗證是 HTTP proxy 或 HTTP 伺服器在允許存取資源之前，用來驗證使用者登入資訊的處理常式。 在網際網路上使用各種不同的驗證配置。 使用者的名稱和密碼通常會與授權清單進行比較，如果系統偵測到相符項，則會將存取權授與使用者的許可權清單中指定的範圍。

WinHTTP 函數支援 HTTP 會話的伺服器和 proxy 驗證。 WinHTTP 支援下列驗證配置：基本、摘要 (請參閱 [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)) 、 [NTLM 驗證](../com/ntlmssp.md)、Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)和 Microsoft Passport 1.4。 如需驗證的詳細資訊，以及在 Microsoft Visual C++ 應用程式中使用驗證的範例，請參閱 [WinHTTP 中的驗證](authentication-in-winhttp.md)。

如需有關基本和 Passport 驗證之安全性考慮的詳細資訊，請參閱 [WinHTTP 安全性考慮](winhttp-security-considerations.md)。

 

 
