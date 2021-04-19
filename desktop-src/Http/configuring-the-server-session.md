---
title: 設定伺服器會話
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967187"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="266b7-103">設定伺服器會話</span><span class="sxs-lookup"><span data-stu-id="266b7-103">Configuring the Server Session</span></span>

<span data-ttu-id="266b7-104">伺服器會話識別碼會使用 [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) 函式建立，並用於 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="266b7-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="266b7-105">*PPropertyInformation* 參數指向設定之屬性類型的設定結構。</span><span class="sxs-lookup"><span data-stu-id="266b7-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="266b7-106">*PropertyInformationLength* 參數會指定設定結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="266b7-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="266b7-107">例如，在設定 **HttpServerTimeoutsProperty** 時， **pPropertyInformation** 參數必須指向至少為 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="266b7-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="266b7-108">HTTP 應用程式通常會建立單一伺服器會話，而且可能會設定整個應用程式的屬性，例如全域頻寬節流限制，或啟用此伺服器會話的集中式記錄。</span><span class="sxs-lookup"><span data-stu-id="266b7-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="266b7-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) 會覆寫呼叫應用程式的 HTTP 伺服器 API 設定;它不會影響 HTTP 伺服器 API 範圍的屬性。</span><span class="sxs-lookup"><span data-stu-id="266b7-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="266b7-110">藉由呼叫 [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)來查詢伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="266b7-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




