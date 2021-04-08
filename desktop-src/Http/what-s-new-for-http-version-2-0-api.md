---
title: HTTP Server 2.0 版 API 的新功能
description: HTTP 伺服器版本 2.0 API 提供下列功能。
ms.assetid: 236fdbb0-dead-4b73-9ef6-be2d502b5243
keywords:
- HTTP Server 2.0 版 API 的新功能
- HTTP 伺服器版本 2.0 API，新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 932a27a45768d0cb00cde4cb89fc4e5d424d1f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021065"
---
# <a name="whats-new-for-http-server-version-20-api"></a><span data-ttu-id="7101e-105">HTTP Server 2.0 版 API 的新功能</span><span class="sxs-lookup"><span data-stu-id="7101e-105">What's New for HTTP Server Version 2.0 API</span></span>

<span data-ttu-id="7101e-106">HTTP 伺服器版本 2.0 API 新增了屬性設定物件和 advanced request queue management。</span><span class="sxs-lookup"><span data-stu-id="7101e-106">The HTTP Server version 2.0 API adds property configuration objects and advanced request queue management.</span></span> <span data-ttu-id="7101e-107">如需詳細資訊和函式的完整清單，請參閱 [HTTP 伺服器版本2.0 參考](http-server-api-version-2-0-reference.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-107">For more information and a complete list of functions, see the [HTTP Server Version 2.0 Reference](http-server-api-version-2-0-reference.md) topic.</span></span> <span data-ttu-id="7101e-108">HTTP 伺服器版本 2.0 API 提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="7101e-108">The following features are available in the HTTP Server version 2.0 API.</span></span>

## <a name="configuration-objects"></a><span data-ttu-id="7101e-109">設定物件</span><span class="sxs-lookup"><span data-stu-id="7101e-109">Configuration Objects</span></span>

<span data-ttu-id="7101e-110">伺服器會話和 URL 群組設定物件可讓應用程式設定 HTTP 服務。</span><span class="sxs-lookup"><span data-stu-id="7101e-110">The server session and URL group configuration objects enable applications to configure the HTTP service.</span></span> <span data-ttu-id="7101e-111">伺服器會話是最上層的設定物件，它會覆寫會話下建立之所有 URL 群組的 HTTP 伺服器 API 預設設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-111">The server session is the top-level configuration object that overrides the HTTP Server API default settings for all the URL groups created under the session.</span></span> <span data-ttu-id="7101e-112">在伺服器會話下建立的 URL 群組會維護一組可接收群組設定的 Url。</span><span class="sxs-lookup"><span data-stu-id="7101e-112">The URL group, created under a server session, maintains a set of URLs that receive the configuration settings for the group.</span></span> <span data-ttu-id="7101e-113">如需詳細資訊，請參閱 [HTTP 版本2.0 架構](http-version-2-0-architecture.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-113">For more information, see the [HTTP Version 2.0 Architecture](http-version-2-0-architecture.md) topic.</span></span>

## <a name="property-configuration-in-version-20"></a><span data-ttu-id="7101e-114">2.0 版中的屬性設定</span><span class="sxs-lookup"><span data-stu-id="7101e-114">Property Configuration in Version 2.0</span></span>

<span data-ttu-id="7101e-115">設定是在伺服器會話或 URL 群組物件上執行。</span><span class="sxs-lookup"><span data-stu-id="7101e-115">Configuration is performed on the server session, or URL group objects.</span></span> <span data-ttu-id="7101e-116">伺服器會話設定物件上會設定整個伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-116">Server-wide configurations are set on the server session configuration object.</span></span> <span data-ttu-id="7101e-117">在伺服器會話下建立的 URL 群組會繼承伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-117">The URL groups, created under the server session, inherit the server session configurations.</span></span> <span data-ttu-id="7101e-118">在 URL 群組上設定的設定會覆寫伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-118">Configurations set on the URL group override the server session configurations.</span></span> <span data-ttu-id="7101e-119">應用程式可以設定的設定包括連接逾時、連線限制、驗證和記錄。</span><span class="sxs-lookup"><span data-stu-id="7101e-119">Configurations that can be set by the application include connection timeouts, connections limits, authentication, and logging.</span></span> <span data-ttu-id="7101e-120">如需詳細資訊，請參閱設定 [HTTP 2.0 版中的屬性](configuring-properties-in-http-version-2-0.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-120">For more information, see the [Configuring Properties in HTTP Version 2.0](configuring-properties-in-http-version-2-0.md) topic.</span></span>

## <a name="process-isolation-on-request-queues"></a><span data-ttu-id="7101e-121">要求佇列上的進程隔離</span><span class="sxs-lookup"><span data-stu-id="7101e-121">Process Isolation on Request Queues</span></span>

<span data-ttu-id="7101e-122">2.0 版要求佇列支援進程隔離，可讓多個背景工作進程在要求佇列上執行 IO。</span><span class="sxs-lookup"><span data-stu-id="7101e-122">The version 2.0 request queue supports process isolation, allowing multiple worker processes to perform IO on the request queue.</span></span> <span data-ttu-id="7101e-123">在要求佇列上設定的設定屬性，可讓應用程式更充分掌控服務。</span><span class="sxs-lookup"><span data-stu-id="7101e-123">Configuration properties set on the request queue allow applications to have more control over the service.</span></span> <span data-ttu-id="7101e-124">命名的要求佇列功能可讓應用程式建立要求佇列，並使用 (ACL) 的存取控制清單來保護它們。</span><span class="sxs-lookup"><span data-stu-id="7101e-124">The named request queue feature allows applications to create request queues and secure them with Access Control Lists (ACL).</span></span> <span data-ttu-id="7101e-125">在建立要求佇列的帳戶以外的使用者帳戶下操作的應用程式，可以開啟要求佇列、接收要求和傳送回應。</span><span class="sxs-lookup"><span data-stu-id="7101e-125">Applications operating under user accounts other than the account that created the request queue are able to open the request queue, receive requests, and send responses.</span></span> <span data-ttu-id="7101e-126">如需詳細資訊，請參閱 [進程隔離](process-isolation.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-126">For more information, see the [Process Isolation](process-isolation.md) topic.</span></span>

## <a name="full-kernel-mode-ssl"></a><span data-ttu-id="7101e-127">完整核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="7101e-127">Full Kernel Mode SSL</span></span>

<span data-ttu-id="7101e-128">預設會啟用核心模式 SSL 安全性;也支援相互驗證的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7101e-128">Kernel mode SSL security is enabled by default; client certificates for mutual authentication are also supported.</span></span> <span data-ttu-id="7101e-129">藉由在核心模式中完成 SSL 作業來提高效能，進而減少核心和使用者模式之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="7101e-129">Performance is increased by completing SSL operations in kernel mode, thus reducing transitions between kernel and user mode.</span></span> <span data-ttu-id="7101e-130">如需詳細資訊，請參閱 [核心模式 SSL](kernel-mode-ssl.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-130">For more information, see the [Kernel Mode SSL](kernel-mode-ssl.md) topic.</span></span>

## <a name="kernel-mode-response-cache"></a><span data-ttu-id="7101e-131">核心模式回應快取</span><span class="sxs-lookup"><span data-stu-id="7101e-131">Kernel mode response cache</span></span>

<span data-ttu-id="7101e-132">具有靜態內容的回應可在核心模式中快取，以提供比使用者模式快取更高的效能。</span><span class="sxs-lookup"><span data-stu-id="7101e-132">Responses with static content can be cached in kernel mode providing increased performance over the user mode cache.</span></span> <span data-ttu-id="7101e-133">快取原則結構會隨著回應傳送。</span><span class="sxs-lookup"><span data-stu-id="7101e-133">The cache policy structure is sent with the response.</span></span> <span data-ttu-id="7101e-134">如需詳細資訊，請參閱 [HTTP 2.0 中的核心模式](kernel-mode-cache-in-http-2-0.md) 快取主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-134">For more information, see the [Kernel Mode Cache in HTTP 2.0](kernel-mode-cache-in-http-2-0.md) topic.</span></span>

## <a name="authentication"></a><span data-ttu-id="7101e-135">驗證</span><span class="sxs-lookup"><span data-stu-id="7101e-135">Authentication</span></span>

<span data-ttu-id="7101e-136">HTTP \_ 回應和 HTTP \_ 要求結構會更新以包含驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="7101e-136">The HTTP\_RESPONSE and HTTP\_REQUEST structures are updated to include authentication information.</span></span> <span data-ttu-id="7101e-137">下列配置支援伺服器端驗證： Negotiate、NTLM、Basic 和 Digest。</span><span class="sxs-lookup"><span data-stu-id="7101e-137">Server-side authentication is supported for the following schemes: Negotiate, NTLM, Basic, and Digest.</span></span> <span data-ttu-id="7101e-138">應用程式可以指定支援的驗證配置，並設定這些配置的喜好設定順序。</span><span class="sxs-lookup"><span data-stu-id="7101e-138">Applications can specify the supported authentication schemes and set the order of preference for those schemes.</span></span>

## <a name="object-scoped-versioning"></a><span data-ttu-id="7101e-139">物件範圍版本控制</span><span class="sxs-lookup"><span data-stu-id="7101e-139">Object Scoped Versioning</span></span>

<span data-ttu-id="7101e-140">HTTP 伺服器版本 1.0 API 在 HTTPInitialize 的呼叫中傳遞了版本資訊。</span><span class="sxs-lookup"><span data-stu-id="7101e-140">The HTTP Server version 1.0 API passed version information in the call to HTTPInitialize.</span></span> <span data-ttu-id="7101e-141">此版本已針對相同進程中的所有應用程式設定為全域。</span><span class="sxs-lookup"><span data-stu-id="7101e-141">The version was set globally for all applications in the same process.</span></span> <span data-ttu-id="7101e-142">在 HTTP 伺服器版本 2.0 API 中，會在建立物件時提供版本資訊。</span><span class="sxs-lookup"><span data-stu-id="7101e-142">In the HTTP Server version 2.0 API, the version information is supplied when the object is created.</span></span> <span data-ttu-id="7101e-143">如需詳細資訊，請參閱 [HTTP Server 2.0 版 API 中](versioning-in-http-2-0.md)的版本設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-143">For more information, see [Versioning in HTTP Server Version 2.0 API](versioning-in-http-2-0.md).</span></span>

## <a name="logging"></a><span data-ttu-id="7101e-144">記錄</span><span class="sxs-lookup"><span data-stu-id="7101e-144">Logging</span></span>

<span data-ttu-id="7101e-145">從2.0 版開始，記錄可透過 HTTP 伺服器 API 來設定。</span><span class="sxs-lookup"><span data-stu-id="7101e-145">Starting with version 2.0, logging is configurable through the HTTP Server API.</span></span> <span data-ttu-id="7101e-146">在伺服器會話上啟用記錄可做為服務的集中式記錄形式。</span><span class="sxs-lookup"><span data-stu-id="7101e-146">Logging enabled on a server session serves as centralized form of logging for the service.</span></span> <span data-ttu-id="7101e-147">您也可以在個別記錄檔的 URL 群組上啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="7101e-147">Logging can also be enabled on a URL group for individualized log files.</span></span> <span data-ttu-id="7101e-148">應用程式會指定記錄檔的格式，以及針對錯誤和成功交易記錄的欄位。</span><span class="sxs-lookup"><span data-stu-id="7101e-148">The application specifies the format for the log files as well as the fields that are logged for errors and successful transactions.</span></span>

## <a name="graceful-request-queue-shutdown"></a><span data-ttu-id="7101e-149">正常要求佇列關閉</span><span class="sxs-lookup"><span data-stu-id="7101e-149">Graceful Request Queue Shutdown</span></span>

<span data-ttu-id="7101e-150">應用程式可以關閉要求佇列，並在終止要求佇列進程之前，正常處理佇列中的未處理要求。</span><span class="sxs-lookup"><span data-stu-id="7101e-150">Applications can shut down the request queue and gracefully handle outstanding requests in the queue before terminating the request queue process.</span></span> <span data-ttu-id="7101e-151">當要求佇列關閉時，HTTP 伺服器 API 會停止佇列要求，並在要求佇列中重新路由未處理的要求。</span><span class="sxs-lookup"><span data-stu-id="7101e-151">When the request queue is shutdown, the HTTP Server API stops queuing requests and re-routes outstanding requests in the request queue.</span></span>

## <a name="demand-start-on-a-request-queue"></a><span data-ttu-id="7101e-152">要求佇列上的要求開始</span><span class="sxs-lookup"><span data-stu-id="7101e-152">Demand Start on a Request Queue</span></span>

<span data-ttu-id="7101e-153">要求佇列上的需求啟動功能可讓控制器應用程式延遲工作者進程具現化，直到第一個要求抵達要求佇列為止。</span><span class="sxs-lookup"><span data-stu-id="7101e-153">The demand start feature on the request queue allows the controller application to delay worker process instantiation until the first request arrives on the request queue.</span></span> <span data-ttu-id="7101e-154">因此，應用程式可以避免耗用資源，直到需要它們為止。</span><span class="sxs-lookup"><span data-stu-id="7101e-154">Thus, applications can avoid consuming resources until they are required.</span></span> <span data-ttu-id="7101e-155">如需詳細資訊，請參閱 [2.0 版要求佇列主題的「需求開始」](demand-start-on-version-2-0-request-queues.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7101e-155">For more information, see the [Demand Start on Version 2.0 Request Queues](demand-start-on-version-2-0-request-queues.md) topic.</span></span>

## <a name="port-sharing"></a><span data-ttu-id="7101e-156">埠共用</span><span class="sxs-lookup"><span data-stu-id="7101e-156">Port Sharing</span></span>

<span data-ttu-id="7101e-157">以 HTTP Server API 為基礎的應用程式會自動與電腦上其他非 HTTP 伺服器 API 型應用程式共用 IP 接聽空間;不再需要 IP 接聽清單。</span><span class="sxs-lookup"><span data-stu-id="7101e-157">HTTP Server API-based applications automatically share the IP listen space with other non-HTTP Server API-based applications on the computer; the IP listen list is no longer required.</span></span> <span data-ttu-id="7101e-158">當應用程式註冊 URL 時，HTTP 伺服器 API 只會在指定的 IP 位址和埠配對上接聽。</span><span class="sxs-lookup"><span data-stu-id="7101e-158">When the application registers a URL, the HTTP Server API listens only on the specified IP address and port pair.</span></span>

## <a name="etw-support"></a><span data-ttu-id="7101e-159">ETW 支援</span><span class="sxs-lookup"><span data-stu-id="7101e-159">ETW Support</span></span>

<span data-ttu-id="7101e-160">使用「Windows 事件追蹤」 (ETW) 的 Advanced 追蹤可讓應用程式獲得更高的診斷能力。</span><span class="sxs-lookup"><span data-stu-id="7101e-160">Advanced tracing using the Event Tracing for Windows (ETW) allows applications greater diagnostic abilities.</span></span> <span data-ttu-id="7101e-161">事件追蹤適用于 URL 註冊和保留、屬性設定、快取事件、驗證以及記錄等等。</span><span class="sxs-lookup"><span data-stu-id="7101e-161">Event tracing is available for URL registrations and reservations, property configuration, cache events, authentication, and logging to name a few.</span></span>

## <a name="performance-counters"></a><span data-ttu-id="7101e-162">效能計數器</span><span class="sxs-lookup"><span data-stu-id="7101e-162">Performance Counters</span></span>

<span data-ttu-id="7101e-163">效能計數器工具可讓應用程式取出服務計數器，並診斷服務效能。</span><span class="sxs-lookup"><span data-stu-id="7101e-163">The performance counter tool allows applications to retrieve service counters and diagnose service performance.</span></span> <span data-ttu-id="7101e-164">全域計數器會追蹤服務的效能、site 計數器追蹤 URL 群組效能，以及要求佇列計數器會追蹤要求佇列的效能。</span><span class="sxs-lookup"><span data-stu-id="7101e-164">Global counters track performance for the service, site counters track URL group performance, and request queue counters track performance of the request queue.</span></span>

## <a name="international-domain-names-idn"></a><span data-ttu-id="7101e-165"> (IDN) 的國際功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="7101e-165">International Domain Names (IDN)</span></span>

<span data-ttu-id="7101e-166">URL 的國際化主機和路徑部分允許註冊非 ASCII 功能變數名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="7101e-166">Internationalized host and path portions of the URL allow registration of non-ASCII domain names and paths.</span></span> <span data-ttu-id="7101e-167">HTTP 伺服器 API 會處理 Unicode Url，以符合 IDN 標準。</span><span class="sxs-lookup"><span data-stu-id="7101e-167">The HTTP Server API processes Unicode URLs to comply with IDN standards.</span></span>

## <a name="netsh-extensions"></a><span data-ttu-id="7101e-168">NetSH 擴充功能</span><span class="sxs-lookup"><span data-stu-id="7101e-168">NetSH Extensions</span></span>

<span data-ttu-id="7101e-169">Netsh 公用程式會取代 Windows Server 2003 和 Windows XP Service Pack 2 中提供的 HttpCfg.exe 工具 (SP2) 。</span><span class="sxs-lookup"><span data-stu-id="7101e-169">The netsh utility replaces the HttpCfg.exe tool available in Windows Server 2003 and Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="7101e-170">Netsh 擴充功能提供管理、診斷和設定 HTTP 服務的方法。</span><span class="sxs-lookup"><span data-stu-id="7101e-170">The netsh extension provides a means of managing, diagnosing, and configuring the HTTP service.</span></span> <span data-ttu-id="7101e-171">系統管理員可以查詢和設定整個伺服器的設定，例如命名空間註冊和 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="7101e-171">Administrators can query and configure server-wide settings such as namespace registrations and SSL certificates.</span></span>

 

 




