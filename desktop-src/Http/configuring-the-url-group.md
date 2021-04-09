---
title: 設定 URL 群組
description: .
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d9be6969b2b197d0bdcb404ad6b8965c278235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932404"
---
# <a name="configuring-the-url-group"></a><span data-ttu-id="714b9-103">設定 URL 群組</span><span class="sxs-lookup"><span data-stu-id="714b9-103">Configuring the URL Group</span></span>

<span data-ttu-id="714b9-104">URL 群組識別碼會使用 [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) 函式建立，並用於 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="714b9-104">The URL group ID is created with the [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) function and used in the call to [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty).</span></span> <span data-ttu-id="714b9-105">*PPropertyInformation* 參數指向設定之屬性類型的設定結構。</span><span class="sxs-lookup"><span data-stu-id="714b9-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="714b9-106">**PropertyInformationLength** 參數會指定設定結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="714b9-106">The **PropertyInformationLength** parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="714b9-107">例如，在設定 **HttpServerTimeoutsProperty** 時， *pPropertyInformation* 參數必須指向不能小於 [**HTTP \_ TIMEOUT \_ 限制 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) 結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="714b9-107">For example, when setting the **HttpServerTimeoutsProperty** the *pPropertyInformation* parameter must point to a buffer that cannot be smaller than the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span> <span data-ttu-id="714b9-108">URL 群組設定是藉由呼叫 [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)來查詢。</span><span class="sxs-lookup"><span data-stu-id="714b9-108">The URL group configurations are queried by calling [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).</span></span>

<span data-ttu-id="714b9-109">建立 URL 群組之後，會使用 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)將 url 新增至群組。</span><span class="sxs-lookup"><span data-stu-id="714b9-109">After the URL Group is created, URLs are added to the group with [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span> <span data-ttu-id="714b9-110">URL 群組必須與2.0 版要求佇列相關聯，才能接收要求。</span><span class="sxs-lookup"><span data-stu-id="714b9-110">The URL group must be associated with a version 2.0 request queue to receive requests.</span></span> <span data-ttu-id="714b9-111">為了將 URL 群組與要求佇列產生關聯，應用程式會呼叫 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) ，並在 *Property* 參數中指定 **HttpServerBindingProperty** 。</span><span class="sxs-lookup"><span data-stu-id="714b9-111">To associate the URL group with a request queue, the application calls [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) and specifies **HttpServerBindingProperty** in the *Property* parameter.</span></span> <span data-ttu-id="714b9-112">如果未設定此屬性，則會將 URL 群組的要求傳遞至要求佇列，而 HTTP 伺服器 API 會產生503回應。</span><span class="sxs-lookup"><span data-stu-id="714b9-112">If this property is not set, matching requests for the URL group are not delivered to a request queue and the HTTP Server API generates a 503 response.</span></span> <span data-ttu-id="714b9-113">應用程式只能在以低許可權執行時，將先前以服務保留的 Url 新增至 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="714b9-113">The application can only add URLs that have been previously reserved with the service to a URL group when running with low privilege.</span></span> <span data-ttu-id="714b9-114">如需詳細資訊，請參閱 [命名空間保留、註冊和路由](namespace-reservations-registrations-and-routing.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="714b9-114">For more information, see the [Namespace Reservations, Registrations, and Routing](namespace-reservations-registrations-and-routing.md) topic.</span></span>

 

 




