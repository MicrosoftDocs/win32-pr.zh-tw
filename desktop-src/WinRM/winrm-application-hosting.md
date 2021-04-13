---
title: 管理託管服務的基礎結構
description: Windows 遠端管理 2.0 (WinRM) 引進了裝載架構。 為了使用此架構，會撰寫 WinRM 外掛程式，以公開 WinRM 基礎結構內應用程式的管理資料。
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311307"
---
# <a name="infrastructure-for-managing-hosted-services"></a><span data-ttu-id="8de43-104">管理託管服務的基礎結構</span><span class="sxs-lookup"><span data-stu-id="8de43-104">Infrastructure for Managing Hosted Services</span></span>

<span data-ttu-id="8de43-105">Windows 遠端管理 2.0 (WinRM) 引進了裝載架構。</span><span class="sxs-lookup"><span data-stu-id="8de43-105">Windows Remote Management 2.0 (WinRM) introduces a hosting framework.</span></span> <span data-ttu-id="8de43-106">為了使用此架構，會撰寫 WinRM 外掛程式，以公開 WinRM 基礎結構內應用程式的管理資料。</span><span class="sxs-lookup"><span data-stu-id="8de43-106">To use the framework, WinRM plug-ins are written that expose management data of an application within the WinRM infrastructure.</span></span> <span data-ttu-id="8de43-107">支援兩種裝載模型。</span><span class="sxs-lookup"><span data-stu-id="8de43-107">Two hosting models are supported.</span></span> <span data-ttu-id="8de43-108">其中一個是 Internet Information Services (IIS) 「基礎」，另一個則是「以服務為基礎的 WinRMâ」。</span><span class="sxs-lookup"><span data-stu-id="8de43-108">One is Internet Information Services (IIS)â€“based and the other is WinRMâ€“service based.</span></span> <span data-ttu-id="8de43-109">以 WinRM 為基礎的模型會使用 HTTP.sys，且不會相依于 IIS。</span><span class="sxs-lookup"><span data-stu-id="8de43-109">The WinRM-based model uses HTTP.sys and does not depend on IIS.</span></span>

<span data-ttu-id="8de43-110">下列各節說明裝載模型：</span><span class="sxs-lookup"><span data-stu-id="8de43-110">The following sections describe the hosting models:</span></span>

-   [<span data-ttu-id="8de43-111">WinRM IIS 擴充功能裝載模型</span><span class="sxs-lookup"><span data-stu-id="8de43-111">WinRM IIS Extension Hosting Model</span></span>](#winrm-iis-extension-hosting-model)
    -   [<span data-ttu-id="8de43-112">WinRM IIS 擴充功能裝載模型中的負載平衡</span><span class="sxs-lookup"><span data-stu-id="8de43-112">Load Balancing in the WinRM IIS Extension Hosting Model</span></span>](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [<span data-ttu-id="8de43-113">WinRM IIS 擴充功能裝載模型中的 HTTP 重新導向</span><span class="sxs-lookup"><span data-stu-id="8de43-113">HTTP Redirection in the WinRM IIS Extension Hosting Model</span></span>](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [<span data-ttu-id="8de43-114">WinRM 服務裝載模型</span><span class="sxs-lookup"><span data-stu-id="8de43-114">WinRM Service Hosting Model</span></span>](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a><span data-ttu-id="8de43-115">WinRM IIS 擴充功能裝載模型</span><span class="sxs-lookup"><span data-stu-id="8de43-115">WinRM IIS Extension Hosting Model</span></span>

<span data-ttu-id="8de43-116">WinRM IIS 延伸模組是使用 **伺服器管理員** 安裝的選用元件。</span><span class="sxs-lookup"><span data-stu-id="8de43-116">The WinRM IIS extension module is an optional component that is installed using the **Server Manager**.</span></span> <span data-ttu-id="8de43-117">WinRM IIS 延伸模組是用來從 IIS 服務內建立 WinRMâ€「啟用的端點」。</span><span class="sxs-lookup"><span data-stu-id="8de43-117">The WinRM IIS extension module is used to create WinRMâ€“enabled endpoints from within the IIS service.</span></span> <span data-ttu-id="8de43-118">您可以在網站或虛擬目錄層級啟用此模組。</span><span class="sxs-lookup"><span data-stu-id="8de43-118">This module can be enabled at either the website or virtual directory level.</span></span> <span data-ttu-id="8de43-119">其運作方式是攔截連入要求，並將其重新導向至關聯的網站或虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="8de43-119">It works by intercepting and redirecting incoming requests to the associated website or virtual directory.</span></span> <span data-ttu-id="8de43-120">系統會將要求重新導向至可分析內容的 WinRM 模組，然後判斷哪些 WinRM 外掛程式設定為處理每個要求。</span><span class="sxs-lookup"><span data-stu-id="8de43-120">The requests are redirected to a WinRM module that analyzes the content and then determines which WinRM plug-in is configured to handle each request.</span></span> <span data-ttu-id="8de43-121">如需詳細資訊，請參閱 [IIS 主機外掛程式](iis-host-plug-in-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="8de43-121">For more information, see [IIS Host Plug-in Configuration](iis-host-plug-in-configuration.md).</span></span>

<span data-ttu-id="8de43-122">WinRM IIS 擴充功能裝載模型是設計來處理大量的要求。</span><span class="sxs-lookup"><span data-stu-id="8de43-122">The WinRM IIS extension hosting model is designed to handle a large volume of requests.</span></span> <span data-ttu-id="8de43-123">如果以 IIS 為基礎的模型做為裝載架構，則可使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="8de43-123">If the IIS-based model is used as the hosting framework, the following features are available:</span></span>

-   <span data-ttu-id="8de43-124">標準 IIS 驗證模組。</span><span class="sxs-lookup"><span data-stu-id="8de43-124">The standard IIS authentication modules.</span></span>
-   <span data-ttu-id="8de43-125">裝載所有外掛程式的 IIS 應用程式集區進程。</span><span class="sxs-lookup"><span data-stu-id="8de43-125">The IIS application pool process for hosting all plug-ins.</span></span>
-   <span data-ttu-id="8de43-126">節流管理系統的大量使用者。</span><span class="sxs-lookup"><span data-stu-id="8de43-126">Quota management for throttling heavy users of the system.</span></span> <span data-ttu-id="8de43-127">如需詳細資訊，請參閱 [遠端 shell 的配額管理](quotas.md)。</span><span class="sxs-lookup"><span data-stu-id="8de43-127">For more information, see [Quota Management for Remote Shells](quotas.md).</span></span>
-   <span data-ttu-id="8de43-128">Shell 外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="8de43-128">A shell plug-in model.</span></span> <span data-ttu-id="8de43-129">請參閱 [WinRM 用戶端 SHELL API](client-shell-api.md)。</span><span class="sxs-lookup"><span data-stu-id="8de43-129">See [WinRM Client Shell API](client-shell-api.md).</span></span>
-   <span data-ttu-id="8de43-130">彈性的授權模型。</span><span class="sxs-lookup"><span data-stu-id="8de43-130">A flexible authorization model.</span></span> <span data-ttu-id="8de43-131">請參閱 [WinRM 外掛程式 API](winrm-plugin-api.md)。</span><span class="sxs-lookup"><span data-stu-id="8de43-131">See [WinRM Plugin API](winrm-plugin-api.md).</span></span>

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a><span data-ttu-id="8de43-132">WinRM IIS 擴充功能裝載模型中的負載平衡</span><span class="sxs-lookup"><span data-stu-id="8de43-132">Load Balancing in the WinRM IIS Extension Hosting Model</span></span>

<span data-ttu-id="8de43-133">大部分的負載平衡器 (磅) 支援以 cookie 為基礎的粘性模型。</span><span class="sxs-lookup"><span data-stu-id="8de43-133">Most load balancers (LBs) support a cookie-based stickiness model.</span></span> <span data-ttu-id="8de43-134">LB 會將 cookie 插入至用戶端的第一個要求的回應中。</span><span class="sxs-lookup"><span data-stu-id="8de43-134">The LB inserts a cookie into the response to the first request from the client.</span></span> <span data-ttu-id="8de43-135">針對所有後續的要求，cookie 會在要求中傳輸，而 LB 會使用 cookie 將要求路由傳送至適當的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8de43-135">For all subsequent requests, the cookie is transmitted in the request and the LB uses the cookie to route the request to the appropriate server.</span></span>

<span data-ttu-id="8de43-136">在將 WinRM 2.0 裝載于 LB 後方的環境中，LB 應設定為以 MS-WSMAN 作為 cookie 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8de43-136">In environments where WinRM 2.0 is hosted behind an LB, the LB should be configured to prefix MS-WSMAN to the name of the cookie.</span></span> <span data-ttu-id="8de43-137">此外，您必須設定 LB，讓 cookie 的存留期成為無限的，因為 WinRM 用戶端應該控制 cookie 的有效時間長度。</span><span class="sxs-lookup"><span data-stu-id="8de43-137">In addition, the LB needs to be configured to allow the lifetime of the cookie to be infinite, because the WinRM client should control how long the cookie is valid.</span></span>

<span data-ttu-id="8de43-138">以下是 cookie 名稱的範例：</span><span class="sxs-lookup"><span data-stu-id="8de43-138">The following is an example of a cookie name:</span></span>

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a><span data-ttu-id="8de43-139">WinRM IIS 擴充功能裝載模型中的 HTTP 重新導向</span><span class="sxs-lookup"><span data-stu-id="8de43-139">HTTP Redirection in the WinRM IIS Extension Hosting Model</span></span>

<span data-ttu-id="8de43-140">WinRM 2.0 可處理 HTTP 重新導向。</span><span class="sxs-lookup"><span data-stu-id="8de43-140">WinRM 2.0 can handle HTTP redirection.</span></span> <span data-ttu-id="8de43-141">建議所有重新導向都使用安全通訊端層 (SSL) ，而且所有應用程式會在建立新的會話之前驗證重新導向的 URI。</span><span class="sxs-lookup"><span data-stu-id="8de43-141">It is recommended that all redirection use Secure Sockets Layer (SSL), and that all applications validate the redirected URI before creating a new session.</span></span>

## <a name="winrm-service-hosting-model"></a><span data-ttu-id="8de43-142">WinRM 服務裝載模型</span><span class="sxs-lookup"><span data-stu-id="8de43-142">WinRM Service Hosting Model</span></span>

<span data-ttu-id="8de43-143">以 WinRM 服務為基礎的模型會在 HTTP.sys 上執行。</span><span class="sxs-lookup"><span data-stu-id="8de43-143">The WinRM service-based model runs on top of HTTP.sys.</span></span> <span data-ttu-id="8de43-144">WinRM 服務是向 WinRM 用戶端處理要求的網路面向服務。</span><span class="sxs-lookup"><span data-stu-id="8de43-144">The WinRM service is a network facing service that handles requests from WinRM clients.</span></span> <span data-ttu-id="8de43-145">服務會判斷要求是否會路由至在主要服務中執行的外掛程式，或是透過執行協力廠商外掛程式的主機進行路由傳送。</span><span class="sxs-lookup"><span data-stu-id="8de43-145">The service determines whether the request is routed to a plug-in that runs in the main service or is routed through a host where the third-party plug-in is run.</span></span> <span data-ttu-id="8de43-146">此模型適用于受管理節點上的負載偏低的案例。</span><span class="sxs-lookup"><span data-stu-id="8de43-146">This model is intended for scenarios where the load on the managed node is low.</span></span> <span data-ttu-id="8de43-147">此外，此模型適用于 IIS 裝載不是選項的情況。</span><span class="sxs-lookup"><span data-stu-id="8de43-147">Moreover, this model is intended for scenarios where IIS hosting is not an option.</span></span> <span data-ttu-id="8de43-148">如需詳細資訊，請參閱 [WinRM 服務外掛程式](wsman-service-plug-in-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="8de43-148">For more information, see [WinRM Service Plug-in Configuration](wsman-service-plug-in-configuration.md).</span></span>

 

 




