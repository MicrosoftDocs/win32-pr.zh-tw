---
title: 設定屬性
description: 設定屬性
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d5707840634f86da41d3e67a1014e93b8450c668cae9ea6f3129a0fe021f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047450"
---
# <a name="configuring-properties"></a>設定屬性

HTTP 伺服器版本 2.0 API 可讓應用程式手動設定要求佇列、伺服器會話和 URL 群組。 伺服器會話是最上層的物件，其中包含適用于所有在其下建立之 URL 群組的設定資訊。 應用程式會建立具有一或多個 URL 群組的伺服器會話，然後將 URL 群組與要求佇列產生關聯。

如需有關 HTTP Server 2.0 版 API 中特定設定物件的詳細資訊，請參閱：

-   [設定伺服器會話](configuring-the-server-session.md)
-   [設定 URL 群組](configuring-the-url-group.md)
-   [設定 HTTP Server API 寬計時器](configuring-the-http-server-api-wide-timers.md)

設定物件的屬性會以 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)、 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) 和 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 設定，如下圖所示。 要求佇列與 URL 群組之間的關聯可以隨需變更，而伺服器會話與 URL 群組之間的關聯則無法變更。 URL 群組必須與要求佇列相關聯，才能接收要求。

![設定物件的屬性](images/configpropinv2.png)

下表列出可在每個設定物件上設定的屬性。 一般情況下，如果應用程式未設定屬性設定，則會套用 HTTP 伺服器 API 的預設設定。 應用程式在伺服器會話上設定的設定屬性會覆寫 HTTP 伺服器 API 範圍的設定。 在 URL 群組上設定的設定會覆寫伺服器會話設定，而要求佇列設定會覆寫 HTTP 伺服器 API 的預設設定。



| Configuration 物件 | 屬性                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 伺服器會話       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| URL 群組            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| 要求佇列        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

伺服器會話屬性是在 [HTTP \_ 伺服器 \_ 屬性](/windows/desktop/api/Http/ne-http-http_server_property) 列舉中定義。 下表列出當應用程式未設定這些屬性時，針對每個屬性類型所設定的屬性結構，以及 HTTP 伺服器 API 預設值。



| 屬性                                                    | 結構                                                                     | HTTP 伺服器 API 預設值    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | 不需要驗證          |
| HttpServerLoggingProperty                                   | [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | 無記錄                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**HTTP \_ 連接 \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | 沒有限制                   |
| HttpServerTimeoutsProperty                                  | [**HTTP \_ 超時 \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120秒。                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**HTTP \_ 頻寬 \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | 沒有限制                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**HTTP \_ 狀態 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | 啟用                    |
| HttpServer503VerbosityProperty                              | [**HTTP \_ 503 \_ 回應 \_ 詳細資訊**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**HTTP 系結 \_ \_ 資訊**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | 無                       |



 

下表列出 HTTP 伺服器 API 設定的最小值和最大值。



| 屬性                                              | HTTP 伺服器 API 最大值和最小值                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | 最小值 = 允許的最小 \_ \_ 頻寬 \_ 節流 \_ 速率上限 = 無 |
| HttpServerQueueLengthProperty                         | 最小值 = 0xA Max = 0xFFFF                                     |



 

 

 




