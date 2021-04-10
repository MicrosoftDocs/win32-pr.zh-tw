---
title: " (HTTP 伺服器 API) 的版本控制"
description: HTTP 伺服器版本 2.0 API 會套用物件範圍版本設定，以判斷 API 的版本。
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- HTTP Server 2.0 版 API 中的版本設定
- HTTP 伺服器版本 2.0 API，版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221ff7a93bb24e7e0b8a1b9f7c2399012cdbe95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093635"
---
# <a name="versioning-http-server-api"></a> (HTTP 伺服器 API) 的版本控制

HTTP 伺服器版本 2.0 API 使版本1.0 要求佇列和 URL 關聯與要求佇列過時。 物件範圍的版本控制可讓應用程式提供應用程式特定的版本資訊。 應用程式可以針對執行所在的作業系統，自動呼叫正確的結構版本。

## <a name="request-queues"></a>要求佇列

從 HTTP Server 2.0 版 API 開始，會建立要求佇列，並讓 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 淘汰 1.0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) 函式版本。 使用 [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) 函式時，會在2.0 版中引進 URL 群組。 使用 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) 將 url 新增至群組，以使1.0 版 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式過時。 版本 2.0 URL 群組不得搭配1.0 版要求佇列使用。

從2.0 版開始，下列1.0 版函式已過時，無法搭配版本2.0 要求佇列使用：

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

如需設定 URL 群組的詳細資訊，請參閱設定 [Url 群組](configuring-the-url-group.md) 主題。 如需2.0 版要求佇列的詳細資訊，請參閱「 [命名要求佇列](named-request-queue.md) 」主題。

## <a name="object-scoped-versioning"></a>Object-Scoped 版本控制

在1.0 版中，應用程式會在呼叫 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)時提供 HTTP 伺服器 API 版本。 只有呼叫 **HttpInitialize** 的第一個應用程式會接受版本資訊，並且會在相同的進程中套用至所有 HTTP 伺服器 API 應用程式。 從2.0 版 API 開始，不會使用 **HttpInitialize** 呼叫中提供的全域版本資訊。 針對2.0 版的應用程式，當要求佇列或伺服器會話由 [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) 或 [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession)所建立時，會在 VERSION 參數中傳遞 HTTP 伺服器 API 版本。 使用1.0 版 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)建立要求佇列時，會自動將它標示為1.0 版。 版本1.0 和2.0 版應用程式都可以在相同的進程中執行。

[**Http \_ 要求**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))和 [**HTTP \_ 回應**](http-response.md)結構會更新，以包含 HTTP 伺服器2.0 版 API 中的驗證資訊。 [**HTTP \_要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) 和 [**HTTP \_ 要求 \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) 是應用程式所使用的 API 版本專用的。 不過，應用程式不應該直接在程式碼中使用這些結構;相反地，他們應該使用 **HTTP \_ 要求** ，根據收到要求的要求佇列版本取得正確的版本。 此外，請注意 **HTTP \_ 要求** 結構的大小是以編譯器代碼所用的作業系統版本為基礎。

 

 
