---
title: 設定和啟用伺服器端記錄
description: 設定和啟用伺服器端記錄
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372166"
---
# <a name="configuring-and-enabling-server-side-logging"></a>設定和啟用伺服器端記錄

應用程式會在使用 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)傳送回應之前，先在伺服器會話或 URL 群組上啟用記錄。 下列範例顯示如何設定和啟用 W3C 類型伺服器端記錄：

1.  應用程式會使用 **格式** 成員中指定的 **HttpLoggingTypeW3C** 來初始化 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)結構，並使用 **欄位** 成員中 [**HTTP \_ 記錄 \_ 欄位**](http-log-field--constants.md)常數的位元遮罩來初始化。
2.  應用程式會使用在 *Property* 參數中指定的 **HttpServerLoggingProperty** 來呼叫 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)或 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並呼叫 *pPropertyInformation* 參數中的 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)結構指標。

[**HTTP \_ 記錄 \_ 欄位**](http-log-field--constants.md)常數的位元遮罩包含可在 W3C 記錄檔中記錄的欄位。 請注意，在伺服器會話或 URL 群組上設定 **HttpServerLoggingProperty** 屬性，並不表示將會記錄 HTTP 回應。 當 W3C 在 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) 或 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)的呼叫中啟用時，會以每個要求為基礎執行記錄。

若要針對每個要求啟用 W3C 回應記錄，應用程式會執行下列步驟：

1.  應用程式會使用將針對該回應記錄的欄位資訊，初始化 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data) 的成員。
2.  [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data)結構的 **基底. 類型** 成員應初始化為 **HttpLogDataTypeFields**。 **Base. Type** 欄位可確保結構和 API 未來的擴充性。
3.  應用程式會使用 *pLogData* 參數中 [**HTTP \_ 記錄 \_ 欄位 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_fields_data)結構的指標，呼叫 [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)或 [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) 。 應用程式應該輸入轉換 [**PHTTP \_ 記錄 \_ 資料**](/windows/desktop/api/Http/ns-http-http_log_data)的指標。

 

 




