---
title: HTTP 伺服器 API 總覽
description: 本主題會識別使用 HTTP 伺服器 API 的一般作業順序。
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d24defe190c073f7ca359309baf6731d466459d9bb7cfbd9ffc05268ded11ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150331"
---
# <a name="http-server-api-overview"></a>HTTP 伺服器 API 總覽

下列清單會識別使用 HTTP 伺服器 API 的一般作業順序：

-   使用 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) 函數來初始化 HTTP 伺服器 API。
-   使用 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) 函數建立要求佇列。
-   使用 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函數註冊一或多個 url。
-   使用 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函式來接收導向至已註冊之 url 的連入要求，並使用 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 函數傳送這些要求的 HTTP 回應。
-    (選擇性) 傳送回應時，請使用 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 函數傳送額外的實體主體。
-   使用 [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)、 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 和 [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) 函數來執行清除作業。

在使用 Url 的作業中，請注意，它是已處理的 URL，其包含在應使用之 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1)結構的 **CookedUrl** 成員中。 請勿在 **pRawUrl** 成員中使用未處理的 URL，這僅適用于追蹤和統計用途。

每個應用程式都會建立自己的要求佇列。 應用程式從 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)取得其要求佇列控制碼。 它會將此控制碼傳遞至 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式，以將 URL 新增至要求佇列。 應用程式會接收傳入要求的通知，然後藉由呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函式與要求佇列控制碼，從要求佇列中抓取該要求。 您可以使用此函式來接收要求標頭或標頭和實體主體。 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 也會針對要求控制碼唯一的接收要求，傳回 (RequestId) 的要求識別碼。

> [!Note]  
> 應用程式必須負責檢查所有相關的要求標頭，包括使用中的內容協調標頭，並根據標頭內容適當地使要求失敗。 HTTP 伺服器 API 可確保只會正確地終止每個標頭行，且不會包含不合法的字元。

 

使用 [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) 函式搭配要求佇列控制碼，以抓取要求的實體主體的後續部分（如果有的話）。

> [!Note]  
> HTTP 伺服器 API 會在接收端解碼區塊的訊息，但不會在傳送端執行區塊編碼。 如果傳送端需要區塊化，應用程式必須加以執行。 如需區塊編碼的詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。

 

使用 [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) 函式搭配提供 url 的應用程式，方法是使用 ( "**HTTPs**" ) 的安全配置，以選擇性地取出用戶端的憑證資訊。

[**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)函式會傳送回應。 此函式會使用來自對應要求的 RequestId 來傳送回應。 藉由呼叫 HttpSendResponseEntityBody 函式，並從原始接收的要求呼叫[](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)函式，就可以在數次 API 呼叫中傳送回應。

> [!Note]  
> 根據預設， [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 會使用 "MICROSOFT-HTTPapi.dll/1.0" 作為 "Server：" 標頭。 如果應用程式在回應中指定伺服器標頭，該值會被放在伺服器標頭的第一個部分，後面接著一個空格，然後是 "Microsoft-HTTPAPI.DLL/1.0"。

 

一般而言，HTTP 伺服器 API 會隱藏連接管理的詳細資料，以及從應用程式建立和卸載的詳細資料。 不過，應用程式可以藉由呼叫 [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)，選擇性地偵測連接的終止。

應用程式必須使用下列步驟來清除：

-   當應用程式未接聽或回應 URL 時，會使用 [**HttpRemoveURL**](/windows/desktop/api/Http/nf-http-httpremoveurl) 函數來移除 url。
-   當應用程式使用完要求佇列時，請使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數關閉要求佇列控制碼。
-   當應用程式使用 HTTP 伺服器 API 完成時，請呼叫 [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) 函數。

 

 