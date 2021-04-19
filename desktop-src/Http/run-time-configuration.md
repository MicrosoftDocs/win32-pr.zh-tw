---
title: Run-Time 設定
description: HTTP API 可讓應用程式在執行時間執行動態設定。
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b0a310f9fe86b2e6972aa2dff3d3b7fc05965
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968240"
---
# <a name="run-time-configuration"></a>Run-Time 設定

HTTP API 可讓應用程式在執行時間執行動態設定。 執行時間設定不是持續性，只需要低層級的許可權，而且只會影響您的應用程式。 執行時間設定可以包含下列任何活動：

-   初始化 HTTP 服務和建立伺服器會話。 應用程式會藉由呼叫 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) 函數來初始化 HTTP 服務。 伺服器必須先初始化，才能呼叫任何其他伺服器函數。 然後，應用程式會藉由呼叫 [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) 函數來建立伺服器會話。 伺服器會話是屬性的容器，適用于屬於該伺服器會話的所有 URL 群組。 一般來說，每個 allication 只能有一個伺服器會話。 如需有關設定伺服器會話屬性及其範圍的詳細資訊，請參閱 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)。
-   註冊 Url。 建立伺服器會話之後，應用程式可以藉由建立一或多個 URL 群組來註冊 Url。 URL 群組是將套用相同屬性的 Url 群組。 應用程式會藉由呼叫 [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) 函式來建立 URL 群組，然後藉由呼叫 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) 函數來新增所需的 url。 在應用程式透過建立 URL 群組來註冊 url，並將 URL 群組與要求佇列建立關聯之後 (請參閱 [建立和系結至要求佇列](creating-and-binding-to-a-request-queue.md)) ，來自這些 url 的所有要求都會路由傳送至與該應用程式相關聯的要求佇列。 如需時發生 URL 群組屬性的詳細資訊，請參閱 [ **HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   藉由設定 HTTP 伺服器屬性來啟用功能，例如 [驗證](authentication-in-http-version-2-0.md)、 [記錄](server-side-logging-in-http-version-2-0.md)、QOS 設定、超時、啟用狀態和系結資訊。 如需設定屬性的詳細資訊，請參閱 [**HTTP \_ 伺服器 \_ 屬性**](/windows/desktop/api/Http/ne-http-http_server_property)。

 

 




