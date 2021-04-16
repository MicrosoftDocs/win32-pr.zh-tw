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
# <a name="architecture-http-server-api"></a><span data-ttu-id="fb403-103"> (HTTP 伺服器 API) 的架構</span><span class="sxs-lookup"><span data-stu-id="fb403-103">Architecture (HTTP Server API)</span></span>

<span data-ttu-id="fb403-104">伺服器會話、要求佇列和 URL 群組設定物件可讓應用程式設定 HTTP 服務。</span><span class="sxs-lookup"><span data-stu-id="fb403-104">The server session, request queue, and URL group configuration objects enable applications to configure the HTTP service.</span></span> <span data-ttu-id="fb403-105">這些物件上設定的屬性會覆寫 HTTP Server API 範圍的預設設定。</span><span class="sxs-lookup"><span data-stu-id="fb403-105">The properties set on these objects override the HTTP Server API wide default configurations.</span></span>

-   <span data-ttu-id="fb403-106">伺服器會話：最上層設定物件，此物件會定義在會話下建立之所有 URL 群組的設定。</span><span class="sxs-lookup"><span data-stu-id="fb403-106">Server Session: The top-level configuration object that defines configurations for all the URL groups created under the session.</span></span>
-   <span data-ttu-id="fb403-107">URL 群組：在伺服器會話下建立的 URL 群組包含一組 Url，這些 Url 會繼承伺服器會話上設定的設定。</span><span class="sxs-lookup"><span data-stu-id="fb403-107">URL Group: The URL group, created under the server session, contains a set of URLs that inherit the configurations set on the server session.</span></span> <span data-ttu-id="fb403-108">當應用程式設定時，URL 群組設定會覆寫伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="fb403-108">The URL group configurations override the server session configurations when set by the application.</span></span> <span data-ttu-id="fb403-109">URL 群組會定義應用程式正在接聽的命名空間部分，並設定該部分的命名空間。</span><span class="sxs-lookup"><span data-stu-id="fb403-109">The URL group defines a portion of the namespace that the application is listening on and configures that portion of the namespace.</span></span>
-   <span data-ttu-id="fb403-110">要求佇列：此物件會設定要求佇列的特定設定。</span><span class="sxs-lookup"><span data-stu-id="fb403-110">Request Queue: This object configures settings specific to the request queue.</span></span> <span data-ttu-id="fb403-111">這些設定會套用至與要求佇列相關聯之群組中的所有 Url。</span><span class="sxs-lookup"><span data-stu-id="fb403-111">These configurations are applied to all the URLs in the groups associated with the request queue.</span></span>

<span data-ttu-id="fb403-112">下圖顯示設定物件和應用程式之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="fb403-112">The diagram below shows the relationship between the configuration objects and the application.</span></span> <span data-ttu-id="fb403-113">通常會為每個應用程式建立單一伺服器會話，並在其下建立一或多個 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="fb403-113">Typically, a single server session is created for each application with one or more URL groups created under it.</span></span> <span data-ttu-id="fb403-114">要求佇列的建立與 URL 群組或伺服器會話無關。</span><span class="sxs-lookup"><span data-stu-id="fb403-114">The request queues are created independent of the URL group or server session.</span></span> <span data-ttu-id="fb403-115">URL 群組必須與要求佇列相關聯，才能接收要求。</span><span class="sxs-lookup"><span data-stu-id="fb403-115">URL groups must be associated with a request queue to receive requests.</span></span>

![configuration 物件和應用程式之間的關聯性](images/architecture.png)

<span data-ttu-id="fb403-117">HTTP 伺服器版本 2.0 API 的命名要求佇列功能，可讓多個背景工作進程接收要求佇列上的要求。</span><span class="sxs-lookup"><span data-stu-id="fb403-117">The named request queue feature of the HTTP Server version 2.0 API allows multiple worker processes to receive requests on a request queue.</span></span> <span data-ttu-id="fb403-118">要求佇列是由控制器進程所建立，識別已授與要求佇列存取權的工作者進程。</span><span class="sxs-lookup"><span data-stu-id="fb403-118">The request queue is created by a controller process that identifies the worker processes granted access to the request queue.</span></span> <span data-ttu-id="fb403-119">如需詳細資訊，請參閱「 [命名要求佇列](named-request-queue.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="fb403-119">For more information, see the [Named Request Queue](named-request-queue.md) topic</span></span>

## <a name="property-configuration"></a><span data-ttu-id="fb403-120">屬性設定</span><span class="sxs-lookup"><span data-stu-id="fb403-120">Property Configuration</span></span>

<span data-ttu-id="fb403-121">如需在設定物件上設定屬性的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="fb403-121">For more information about setting properties on the configuration objects, see the following topics:</span></span>

-   [<span data-ttu-id="fb403-122">設定要求佇列</span><span class="sxs-lookup"><span data-stu-id="fb403-122">Configuring the Request Queue</span></span>](configuring-the-request-queue.md)
-   [<span data-ttu-id="fb403-123">設定伺服器會話</span><span class="sxs-lookup"><span data-stu-id="fb403-123">Configuring the Server Session</span></span>](configuring-the-server-session.md)
-   [<span data-ttu-id="fb403-124">設定 URL 群組</span><span class="sxs-lookup"><span data-stu-id="fb403-124">Configuring the URL Group</span></span>](configuring-the-url-group.md)

<span data-ttu-id="fb403-125">下表列出設定物件上設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="fb403-125">The following table lists properties that are set on the configuration objects.</span></span> <span data-ttu-id="fb403-126">如需屬性設定的詳細資訊，請參閱設定 [HTTP 2.0 版中的屬性](configuring-properties-in-http-version-2-0.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="fb403-126">For more information about property configurations, see the [Configuring Properties in HTTP Version 2.0](configuring-properties-in-http-version-2-0.md) topic.</span></span>



| <span data-ttu-id="fb403-127">Name</span><span class="sxs-lookup"><span data-stu-id="fb403-127">Name</span></span>           | <span data-ttu-id="fb403-128">屬性</span><span class="sxs-lookup"><span data-stu-id="fb403-128">Property</span></span>                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb403-129">伺服器會話</span><span class="sxs-lookup"><span data-stu-id="fb403-129">Server Session</span></span> | <span data-ttu-id="fb403-130">HttpServerStateProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-130">HttpServerStateProperty</span></span><br/> <span data-ttu-id="fb403-131">HttpServerLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-131">HttpServerLoggingProperty</span></span><br/> <span data-ttu-id="fb403-132">HttpServerBandwidthProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-132">HttpServerBandwidthProperty</span></span><br/> <span data-ttu-id="fb403-133">HttpServerTimeoutsProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-133">HttpServerTimeoutsProperty</span></span><br/> <span data-ttu-id="fb403-134">HttpServerAuthenticatonProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-134">HttpServerAuthenticatonProperty</span></span><br/>                                                                               |
| <span data-ttu-id="fb403-135">URL 群組</span><span class="sxs-lookup"><span data-stu-id="fb403-135">URL Group</span></span>      | <span data-ttu-id="fb403-136">HttpServerStateProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-136">HttpServerStateProperty</span></span><br/> <span data-ttu-id="fb403-137">HttpServerAuthenticatonProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-137">HttpServerAuthenticatonProperty</span></span><br/> <span data-ttu-id="fb403-138">HttpServerLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-138">HttpServerLoggingProperty</span></span><br/> <span data-ttu-id="fb403-139">HttpServerConnectionsProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-139">HttpServerConnectionsProperty</span></span><br/> <span data-ttu-id="fb403-140">HttpServerBandwidthProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-140">HttpServerBandwidthProperty</span></span><br/> <span data-ttu-id="fb403-141">HttpServerBindingProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-141">HttpServerBindingProperty</span></span><br/> <span data-ttu-id="fb403-142">HttpServerTimeoutsProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-142">HttpServerTimeoutsProperty</span></span><br/> |
| <span data-ttu-id="fb403-143">要求佇列</span><span class="sxs-lookup"><span data-stu-id="fb403-143">Request Queue</span></span>  | <span data-ttu-id="fb403-144">HttpServerStateProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-144">HttpServerStateProperty</span></span><br/> <span data-ttu-id="fb403-145">HttpServerQueueLengthProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-145">HttpServerQueueLengthProperty</span></span><br/> <span data-ttu-id="fb403-146">HttpServer503VerbosityProperty</span><span class="sxs-lookup"><span data-stu-id="fb403-146">HttpServer503VerbosityProperty</span></span><br/>                                                                                                                                                         |



 

 

 





