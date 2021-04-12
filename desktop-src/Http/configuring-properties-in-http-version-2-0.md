---
title: 設定屬性
description: 設定屬性
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372163"
---
# <a name="configuring-properties"></a><span data-ttu-id="6677d-103">設定屬性</span><span class="sxs-lookup"><span data-stu-id="6677d-103">Configuring Properties</span></span>

<span data-ttu-id="6677d-104">HTTP 伺服器版本 2.0 API 可讓應用程式手動設定要求佇列、伺服器會話和 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="6677d-104">The HTTP Server version 2.0 API allows applications to manually configure request queues, server sessions, and URL groups.</span></span> <span data-ttu-id="6677d-105">伺服器會話是最上層的物件，其中包含適用于所有在其下建立之 URL 群組的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="6677d-105">The server session is the top-level object that contains configuration information that applies to all the URL groups created under them.</span></span> <span data-ttu-id="6677d-106">應用程式會建立具有一或多個 URL 群組的伺服器會話，然後將 URL 群組與要求佇列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="6677d-106">The application creates a server session with one or more URL groups under it, and then associates the URL group with a request queue.</span></span>

<span data-ttu-id="6677d-107">如需有關 HTTP Server 2.0 版 API 中特定設定物件的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="6677d-107">For more information about specific configuration objects in HTTP Server version 2.0 API, see:</span></span>

-   [<span data-ttu-id="6677d-108">設定伺服器會話</span><span class="sxs-lookup"><span data-stu-id="6677d-108">Configuring the Server Session</span></span>](configuring-the-server-session.md)
-   [<span data-ttu-id="6677d-109">設定 URL 群組</span><span class="sxs-lookup"><span data-stu-id="6677d-109">Configuring the URL Group</span></span>](configuring-the-url-group.md)
-   [<span data-ttu-id="6677d-110">設定 HTTP Server API 寬計時器</span><span class="sxs-lookup"><span data-stu-id="6677d-110">Configuring the HTTP Server API Wide Timers</span></span>](configuring-the-http-server-api-wide-timers.md)

<span data-ttu-id="6677d-111">設定物件的屬性會以 [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)、 [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) 和 [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) 設定，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="6677d-111">Properties for the configuration objects are set with the [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), the [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) and the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) as shown in the diagram below.</span></span> <span data-ttu-id="6677d-112">要求佇列與 URL 群組之間的關聯可以隨需變更，而伺服器會話與 URL 群組之間的關聯則無法變更。</span><span class="sxs-lookup"><span data-stu-id="6677d-112">The association between the request queue and the URL Group can be changed on demand whereas the association between the Server Session and the URL Groups cannot be changed.</span></span> <span data-ttu-id="6677d-113">URL 群組必須與要求佇列相關聯，才能接收要求。</span><span class="sxs-lookup"><span data-stu-id="6677d-113">The URL Groups must be associated with a request queue to receive requests.</span></span>

![設定物件的屬性](images/configpropinv2.png)

<span data-ttu-id="6677d-115">下表列出可在每個設定物件上設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="6677d-115">The following table lists the properties that can be set on each configuration object.</span></span> <span data-ttu-id="6677d-116">一般情況下，如果應用程式未設定屬性設定，則會套用 HTTP 伺服器 API 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="6677d-116">In general, if no property configuration is set by the application, the HTTP Server API default configurations apply.</span></span> <span data-ttu-id="6677d-117">應用程式在伺服器會話上設定的設定屬性會覆寫 HTTP 伺服器 API 範圍的設定。</span><span class="sxs-lookup"><span data-stu-id="6677d-117">The configuration properties set by the application on the server session override the HTTP Server API-wide configurations.</span></span> <span data-ttu-id="6677d-118">在 URL 群組上設定的設定會覆寫伺服器會話設定，而要求佇列設定會覆寫 HTTP 伺服器 API 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="6677d-118">The configurations set on the URL group override the server session configurations and the request queue configurations override the HTTP Server API default configurations.</span></span>



| <span data-ttu-id="6677d-119">Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="6677d-119">Configuration Object</span></span> | <span data-ttu-id="6677d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="6677d-120">Property</span></span>                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6677d-121">伺服器會話</span><span class="sxs-lookup"><span data-stu-id="6677d-121">Server Session</span></span>       | <span data-ttu-id="6677d-122">HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-122">HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty</span></span>                           |
| <span data-ttu-id="6677d-123">URL 群組</span><span class="sxs-lookup"><span data-stu-id="6677d-123">URL Group</span></span>            | <span data-ttu-id="6677d-124">HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-124">HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty</span></span> |
| <span data-ttu-id="6677d-125">要求佇列</span><span class="sxs-lookup"><span data-stu-id="6677d-125">Request Queue</span></span>        | <span data-ttu-id="6677d-126">HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-126">HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty</span></span>                                                                          |



 

<span data-ttu-id="6677d-127">伺服器會話屬性是在 [HTTP \_ 伺服器 \_ 屬性](/windows/desktop/api/Http/ne-http-http_server_property) 列舉中定義。</span><span class="sxs-lookup"><span data-stu-id="6677d-127">The server session properties are defined in the [HTTP\_SERVER\_PROPERTY](/windows/desktop/api/Http/ne-http-http_server_property) enumeration.</span></span> <span data-ttu-id="6677d-128">下表列出當應用程式未設定這些屬性時，針對每個屬性類型所設定的屬性結構，以及 HTTP 伺服器 API 預設值。</span><span class="sxs-lookup"><span data-stu-id="6677d-128">The following table lists the property structures that are set for each property type and the HTTP Server API default when these properties are not set by the application.</span></span>



| <span data-ttu-id="6677d-129">屬性</span><span class="sxs-lookup"><span data-stu-id="6677d-129">Property</span></span>                                                    | <span data-ttu-id="6677d-130">結構</span><span class="sxs-lookup"><span data-stu-id="6677d-130">Structure</span></span>                                                                     | <span data-ttu-id="6677d-131">HTTP 伺服器 API 預設值</span><span class="sxs-lookup"><span data-stu-id="6677d-131">HTTP Server API Default</span></span>    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="6677d-132">HttpServerAuthenticatonProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-132">HttpServerAuthenticatonProperty</span></span>                             | [<span data-ttu-id="6677d-133">**HTTP \_ 伺服器 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-133">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | <span data-ttu-id="6677d-134">不需要驗證</span><span class="sxs-lookup"><span data-stu-id="6677d-134">No Authentication</span></span>          |
| <span data-ttu-id="6677d-135">HttpServerLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-135">HttpServerLoggingProperty</span></span>                                   | [<span data-ttu-id="6677d-136">**HTTP \_ 記錄 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-136">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)                              | <span data-ttu-id="6677d-137">無記錄</span><span class="sxs-lookup"><span data-stu-id="6677d-137">No Logging</span></span>                 |
| <span data-ttu-id="6677d-138">HttpServerQosProperty->HttpQosSettingTypeConnectionLimit</span><span class="sxs-lookup"><span data-stu-id="6677d-138">HttpServerQosProperty->HttpQosSettingTypeConnectionLimit</span></span> | [<span data-ttu-id="6677d-139">**HTTP \_ 連接 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-139">**HTTP\_CONNECTION\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | <span data-ttu-id="6677d-140">沒有限制</span><span class="sxs-lookup"><span data-stu-id="6677d-140">No Limit</span></span>                   |
| <span data-ttu-id="6677d-141">HttpServerTimeoutsProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-141">HttpServerTimeoutsProperty</span></span>                                  | [<span data-ttu-id="6677d-142">**HTTP \_ 超時 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-142">**HTTP\_TIMEOUT\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | <span data-ttu-id="6677d-143">120秒。</span><span class="sxs-lookup"><span data-stu-id="6677d-143">120 sec.</span></span>                   |
| <span data-ttu-id="6677d-144">HttpServerQosProperty->HttpQosSettingTypeBandwidth</span><span class="sxs-lookup"><span data-stu-id="6677d-144">HttpServerQosProperty->HttpQosSettingTypeBandwidth</span></span>       | [<span data-ttu-id="6677d-145">**HTTP \_ 頻寬 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-145">**HTTP\_BANDWIDTH\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | <span data-ttu-id="6677d-146">沒有限制</span><span class="sxs-lookup"><span data-stu-id="6677d-146">No Limit</span></span>                   |
| <span data-ttu-id="6677d-147">HttpServerQueueLengthProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-147">HttpServerQueueLengthProperty</span></span>                               | <span data-ttu-id="6677d-148">ULONG</span><span class="sxs-lookup"><span data-stu-id="6677d-148">ULONG</span></span>                                                                         | <span data-ttu-id="6677d-149">1000</span><span class="sxs-lookup"><span data-stu-id="6677d-149">1000</span></span>                       |
| <span data-ttu-id="6677d-150">HttpServerStateProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-150">HttpServerStateProperty</span></span>                                     | [<span data-ttu-id="6677d-151">**HTTP \_ 狀態 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-151">**HTTP\_STATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_state_info)                                  | <span data-ttu-id="6677d-152">已啟用</span><span class="sxs-lookup"><span data-stu-id="6677d-152">Enabled</span></span>                    |
| <span data-ttu-id="6677d-153">HttpServer503VerbosityProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-153">HttpServer503VerbosityProperty</span></span>                              | [<span data-ttu-id="6677d-154">**HTTP \_ 503 \_ 回應 \_ 詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-154">**HTTP\_503\_RESPONSE\_VERBOSITY**</span></span>](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | <span data-ttu-id="6677d-155">HttpResponseVerbosityBasic</span><span class="sxs-lookup"><span data-stu-id="6677d-155">HttpResponseVerbosityBasic</span></span> |
| <span data-ttu-id="6677d-156">HttpServerBindingProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-156">HttpServerBindingProperty</span></span>                                   | [<span data-ttu-id="6677d-157">**HTTP 系結 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6677d-157">**HTTP\_BINDING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_binding_info)                              | <span data-ttu-id="6677d-158">無</span><span class="sxs-lookup"><span data-stu-id="6677d-158">None</span></span>                       |



 

<span data-ttu-id="6677d-159">下表列出 HTTP 伺服器 API 設定的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="6677d-159">The following table lists the minimum and and maximum values for the HTTP Server API configurations.</span></span>



| <span data-ttu-id="6677d-160">屬性</span><span class="sxs-lookup"><span data-stu-id="6677d-160">Property</span></span>                                              | <span data-ttu-id="6677d-161">HTTP 伺服器 API 最大值和最小值</span><span class="sxs-lookup"><span data-stu-id="6677d-161">HTTP Server API Maximum and Minimum</span></span>                        |
|-------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6677d-162">HttpServerQosProperty->HttpQosSettingTypeBandwidth</span><span class="sxs-lookup"><span data-stu-id="6677d-162">HttpServerQosProperty->HttpQosSettingTypeBandwidth</span></span> | <span data-ttu-id="6677d-163">最小值 = 允許的最小 \_ \_ 頻寬 \_ 節流 \_ 速率上限 = 無</span><span class="sxs-lookup"><span data-stu-id="6677d-163">Min = MIN\_ALLOWED\_BANDWIDTH\_THROTTLING\_RATE Max = none</span></span> |
| <span data-ttu-id="6677d-164">HttpServerQueueLengthProperty</span><span class="sxs-lookup"><span data-stu-id="6677d-164">HttpServerQueueLengthProperty</span></span>                         | <span data-ttu-id="6677d-165">最小值 = 0xA Max = 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="6677d-165">Min = 0xA Max = 0xFFFF</span></span>                                     |



 

 

 




