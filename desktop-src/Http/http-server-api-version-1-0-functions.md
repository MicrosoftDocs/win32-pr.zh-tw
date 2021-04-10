---
title: HTTP 伺服器 API 版本1.0 函式
description: HTTP 伺服器 API 提供下列功能來撰寫應用程式。
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- HTTP 伺服器 API 版本1.0 函式
- 函數 HTTP，HTTP 伺服器 API 版本1。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183944"
---
# <a name="http-server-api-version-10-functions"></a>HTTP 伺服器 API 版本1.0 函式

HTTP 伺服器 API 提供下列功能來撰寫應用程式。

## <a name="general"></a>一般



| 函式                                             | 描述                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | 建立 HTTP 要求佇列，並將控制碼傳回給它。                                                                         |
| [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)             | 初始化 HTTP 伺服器 API，以供呼叫進程使用。                                                                   |
| [**HttpPrepareUrl**](/windows/desktop/api/Http/nf-http-httpprepareurl)             | 剖析、分析和正規化非正規化的 Unicode 或 punycode URL，以便安全且有效地在其他 HTTP 函數中使用。 |
| [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate)               | 指示 HTTP 伺服器 API 清除任何與特定進程相關聯的資源。                                       |



 

## <a name="cache-management"></a>快取管理



| 函式                                                       | 描述                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | 快取資料片段，讓它可以用來撰寫動態回應，而不需要從磁片讀取。 |
| [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | 從 HTTP 快取中移除指定的快取片段。                                                |
| [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | 抓取指定的快取回應片段。                                                        |



 

## <a name="configuration"></a>組態



| 函式                                                                 | 描述                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | 從 HTTP 設定存放區刪除指定的資訊。  |
| [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | 查詢 HTTP 設定存放區中的指定資訊。   |
| [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | 在 HTTP 伺服器 API 設定存放區中設定指定的值。 |



 

## <a name="input-and-output"></a>輸入和輸出



| 函式                                                             | 描述                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | 從指定的要求佇列中抓取 HTTP 要求。      |
| [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | 抓取特定 HTTP 要求的實體主體資料。       |
| [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | 傳送特定 HTTP 要求的 HTTP 回應。          |
| [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | 傳送 HTTP 回應的實體主體資料。                    |
| [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | 當 HTTP 用戶端中斷連線時，通知應用程式。 |



 

## <a name="ssl"></a>SSL



| 函式                                                             | 描述                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | 抓取 SSL 連線的用戶端憑證。 |



 

## <a name="url-registration"></a>URL 註冊



| 函式                               | 描述                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)       | 註冊 URL，讓它的 HTTP 要求會路由傳送至指定的要求佇列。           |
| [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl) | 取消註冊指定的 URL，使其要求不再路由傳送至指定的佇列。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HTTP 伺服器 API 版本1.0 結構](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




