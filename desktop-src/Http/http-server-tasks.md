---
title: HTTP 伺服器工作
description: HTTP 伺服器工作通常會以特定循序執行;也就是說，必須完成一項工作，並在下一個工作開始之前取得輸出。
ms.assetid: 08f8e7e9-23b9-403f-b00c-8912919d65b1
keywords:
- HTTP 伺服器工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d89f72074ba870981421e228b0ff271505b3fce1e30cd49e79d58463570c0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830058"
---
# <a name="http-server-tasks"></a>HTTP 伺服器工作

HTTP 伺服器工作通常會以特定循序執行;也就是說，必須完成一項工作，並在下一個工作開始之前取得輸出。

系統會建立工作頁面，以顯示有關 HTTP 伺服器應用程式所執行之特定工作的範例程式碼。 工作頁面會連結至 HTTP 伺服器範例的 C 擴充檔。 當您在本機電腦的 C：磁片磁碟機上安裝 PSDK 時 \\ ，會在 c： \\ Program FILES \\ Microsoft SDK \\ 範例 \\ netds \\ HTTP \\ 伺服器上安裝完整的伺服器範例應用程式。

下列清單會識別 HTTP 伺服器工作：

-   [初始化 HTTP 服務](#initialize-the-http-service)
-   [註冊要接聽的 Url](#register-the-urls-to-listen-on)
-   [呼叫常式以接收要求](#call-the-routine-to-receive-a-request)
-   [接收要求](#receive-the-request)
-   [處理 HTTP 要求](#handle-the-http-request)
-   [傳送 HTTP 回應](#send-the-http-response)
-   [傳送 HTTP POST 回應](#send-the-http-post-response)
-   [清除 HTTP 伺服器 API](#clean-up-the-http-server-api)

## <a name="initialize-the-http-service"></a>初始化 HTTP 服務

HTTP 服務是使用 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) 函式來初始化，而要求佇列的控制碼則是使用 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)所建立。 伺服器必須先初始化，才能呼叫任何其他伺服器函數。 必須先建立要求佇列，服務才能註冊 Url 來接聽傳入的 HTTP 要求。

如需詳細資訊和程式碼範例，請參閱 [初始化 HTTP 服務](http-server-sample-application.md)。

## <a name="register-the-urls-to-listen-on"></a>註冊要接聽的 Url

為了讓 HTTP 伺服器 API 接聽傳入的要求，會藉由呼叫 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式，向 API 註冊特定的 url。 符合這些 Url 的連入要求會路由傳送到此呼叫中指定的要求佇列。

如需詳細資訊和程式碼範例，請參閱 [註冊要接聽的 url](http-server-sample-application.md)。

## <a name="call-the-routine-to-receive-a-request"></a>呼叫常式以接收要求

DoReceiveRequest 函式會配置要求緩衝區、初始化要求識別碼，並啟動迴圈來接收要求。

如需詳細資訊和程式碼範例，請參閱 [呼叫常式以接收要求](http-server-sample-application.md)。

## <a name="receive-the-request"></a>接收要求

HTTP 伺服器 API 會提供一個要求結構來儲存剖析的連入要求。 此結構是由應用程式所配置，並在收到傳入要求時初始化。 應用程式會呼叫 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) 函數來接收要求。 如果要求緩衝區太小而無法接收要求，應用程式可以增加緩衝區大小，然後再次呼叫 **HttpReceiveHttpRequest** ，以接收整個要求。

如需詳細資訊和程式碼範例，請參閱 [接收要求](http-server-sample-application.md)。

## <a name="handle-the-http-request"></a>處理 HTTP 要求

範例應用程式會示範如何處理 HTTP GET 和 POST 要求動詞。 如果應用程式未處理的要求中出現動詞命令，則應用程式會傳送 503 (**未 \_ 執行**) 錯誤。

請注意，用來處理要求的 URL 是已處理的 URL，其包含在 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1)結構的 **CookedUrl** 成員中。 請勿在 **pRawUrl** 成員中使用未處理的 URL，這僅適用于追蹤和統計用途。

如需詳細資訊和程式碼範例，請參閱 [處理 HTTP 要求](http-server-sample-application.md)。

## <a name="send-the-http-response"></a>傳送 HTTP 回應

回應結構會以狀態碼和 INITIALIZE \_ HTTP 回應宏中的原因片語進行配置和初始化 \_ 。 已知的 HTTP 標頭會新增至「加入已知標頭」宏的回應結構中 \_ \_ ，而實體主體會加入至來自記憶體之資料區塊的回應。 呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 函數以傳送回應。 在此範例中，應用程式會將簡單的200正常回應傳送給 GET 要求。

如需詳細資訊和程式碼範例，請參閱 [傳送 HTTP 回應](http-server-sample-application.md)。

## <a name="send-the-http-post-response"></a>傳送 HTTP POST 回應

POST 要求需要比 GET 要求更多的處理。 藉由呼叫 [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) 函數來接收要求實體主體。 應用程式會在 HTTP 伺服器 API 的個別呼叫中傳送回應和回應實體主體。 回應標頭會與 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)一起傳送。 實體主體會使用 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 函式，從檔案控制代碼傳送到資料區塊中。

如需詳細資訊和程式碼範例，請參閱 [傳送 HTTP POST 回應](http-server-sample-application.md)。

## <a name="clean-up-the-http-server-api"></a>清除 HTTP 伺服器 API

HTTP 伺服器 API 的清除作業包括：

-   正在移除所有已註冊的 Url。
-   關閉要求佇列的控制碼。
-   終止 HTTP 伺服器 API 所建立的資源。

應用程式會呼叫 [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) 函式，將初始 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式所註冊的 url 取消註冊。 應用程式也會針對具有相符旗標設定的每個 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)呼叫呼叫 [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) 。 此呼叫會結束通話 **HttpInitialize** 所建立的所有資源。

如需詳細資訊和程式碼範例，請參閱 [清除 HTTP 伺服器 API](http-server-sample-application.md)。

 

 




