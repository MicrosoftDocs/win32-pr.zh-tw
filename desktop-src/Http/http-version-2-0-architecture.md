---
title: " (HTTP 伺服器 API) 的架構"
description: 伺服器會話、要求佇列和 URL 群組設定物件可讓應用程式設定 HTTP 服務。
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc7a07cb5e0439ed82421dd413aee3b6688bc0f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383645"
---
# <a name="architecture-http-server-api"></a> (HTTP 伺服器 API) 的架構

伺服器會話、要求佇列和 URL 群組設定物件可讓應用程式設定 HTTP 服務。 這些物件上設定的屬性會覆寫 HTTP Server API 範圍的預設設定。

-   伺服器會話：最上層設定物件，此物件會定義在會話下建立之所有 URL 群組的設定。
-   URL 群組：在伺服器會話下建立的 URL 群組包含一組 Url，這些 Url 會繼承伺服器會話上設定的設定。 當應用程式設定時，URL 群組設定會覆寫伺服器會話設定。 URL 群組會定義應用程式正在接聽的命名空間部分，並設定該部分的命名空間。
-   要求佇列：此物件會設定要求佇列的特定設定。 這些設定會套用至與要求佇列相關聯之群組中的所有 Url。

下圖顯示設定物件和應用程式之間的關聯性。 通常會為每個應用程式建立單一伺服器會話，並在其下建立一或多個 URL 群組。 要求佇列的建立與 URL 群組或伺服器會話無關。 URL 群組必須與要求佇列相關聯，才能接收要求。

![configuration 物件和應用程式之間的關聯性](images/architecture.png)

HTTP 伺服器版本 2.0 API 的命名要求佇列功能，可讓多個背景工作進程接收要求佇列上的要求。 要求佇列是由控制器進程所建立，識別已授與要求佇列存取權的工作者進程。 如需詳細資訊，請參閱「 [命名要求佇列](named-request-queue.md) 」主題。

## <a name="property-configuration"></a>屬性設定

如需在設定物件上設定屬性的詳細資訊，請參閱下列主題：

-   [設定要求佇列](configuring-the-request-queue.md)
-   [設定伺服器會話](configuring-the-server-session.md)
-   [設定 URL 群組](configuring-the-url-group.md)

下表列出設定物件上設定的屬性。 如需屬性設定的詳細資訊，請參閱設定 [HTTP 2.0 版中的屬性](configuring-properties-in-http-version-2-0.md) 主題。



| Name           | 屬性                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 伺服器會話 | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| URL 群組      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| 要求佇列  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





