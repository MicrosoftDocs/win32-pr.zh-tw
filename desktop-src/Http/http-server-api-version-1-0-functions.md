---
title: HTTP 伺服器 API 版本1.0 函式
description: HTTP 伺服器 API 提供下列功能來撰寫應用程式。
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- HTTP 伺服器 API 版本1.0 函式
- 函數 HTTP，HTTP 伺服器 API 版本1。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183944"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="c78b4-105">HTTP 伺服器 API 版本1.0 函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="c78b4-106">HTTP 伺服器 API 提供下列功能來撰寫應用程式。</span><span class="sxs-lookup"><span data-stu-id="c78b4-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="c78b4-107">一般</span><span class="sxs-lookup"><span data-stu-id="c78b4-107">General</span></span>



| <span data-ttu-id="c78b4-108">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-108">Function</span></span>                                             | <span data-ttu-id="c78b4-109">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c78b4-110">**HttpCreateHttpHandle**</span><span class="sxs-lookup"><span data-stu-id="c78b4-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="c78b4-111">建立 HTTP 要求佇列，並將控制碼傳回給它。</span><span class="sxs-lookup"><span data-stu-id="c78b4-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="c78b4-112">**HttpInitialize**</span><span class="sxs-lookup"><span data-stu-id="c78b4-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="c78b4-113">初始化 HTTP 伺服器 API，以供呼叫進程使用。</span><span class="sxs-lookup"><span data-stu-id="c78b4-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="c78b4-114">**HttpPrepareUrl**</span><span class="sxs-lookup"><span data-stu-id="c78b4-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="c78b4-115">剖析、分析和正規化非正規化的 Unicode 或 punycode URL，以便安全且有效地在其他 HTTP 函數中使用。</span><span class="sxs-lookup"><span data-stu-id="c78b4-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="c78b4-116">**HttpTerminate**</span><span class="sxs-lookup"><span data-stu-id="c78b4-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="c78b4-117">指示 HTTP 伺服器 API 清除任何與特定進程相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c78b4-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="c78b4-118">快取管理</span><span class="sxs-lookup"><span data-stu-id="c78b4-118">Cache Management</span></span>



| <span data-ttu-id="c78b4-119">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-119">Function</span></span>                                                       | <span data-ttu-id="c78b4-120">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c78b4-121">**HttpAddFragmentToCache**</span><span class="sxs-lookup"><span data-stu-id="c78b4-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="c78b4-122">快取資料片段，讓它可以用來撰寫動態回應，而不需要從磁片讀取。</span><span class="sxs-lookup"><span data-stu-id="c78b4-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="c78b4-123">**HttpFlushResponseCache**</span><span class="sxs-lookup"><span data-stu-id="c78b4-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="c78b4-124">從 HTTP 快取中移除指定的快取片段。</span><span class="sxs-lookup"><span data-stu-id="c78b4-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="c78b4-125">**HttpReadFragmentFromCache**</span><span class="sxs-lookup"><span data-stu-id="c78b4-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="c78b4-126">抓取指定的快取回應片段。</span><span class="sxs-lookup"><span data-stu-id="c78b4-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="c78b4-127">組態</span><span class="sxs-lookup"><span data-stu-id="c78b4-127">Configuration</span></span>



| <span data-ttu-id="c78b4-128">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-128">Function</span></span>                                                                 | <span data-ttu-id="c78b4-129">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="c78b4-130">**HttpDeleteServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="c78b4-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="c78b4-131">從 HTTP 設定存放區刪除指定的資訊。</span><span class="sxs-lookup"><span data-stu-id="c78b4-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="c78b4-132">**HttpQueryServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="c78b4-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="c78b4-133">查詢 HTTP 設定存放區中的指定資訊。</span><span class="sxs-lookup"><span data-stu-id="c78b4-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="c78b4-134">**HttpSetServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="c78b4-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="c78b4-135">在 HTTP 伺服器 API 設定存放區中設定指定的值。</span><span class="sxs-lookup"><span data-stu-id="c78b4-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="c78b4-136">輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="c78b4-136">Input and Output</span></span>



| <span data-ttu-id="c78b4-137">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-137">Function</span></span>                                                             | <span data-ttu-id="c78b4-138">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c78b4-139">**HttpReceiveHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c78b4-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="c78b4-140">從指定的要求佇列中抓取 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="c78b4-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="c78b4-141">**HttpReceiveRequestEntityBody**</span><span class="sxs-lookup"><span data-stu-id="c78b4-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="c78b4-142">抓取特定 HTTP 要求的實體主體資料。</span><span class="sxs-lookup"><span data-stu-id="c78b4-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="c78b4-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="c78b4-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="c78b4-144">傳送特定 HTTP 要求的 HTTP 回應。</span><span class="sxs-lookup"><span data-stu-id="c78b4-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="c78b4-145">**HttpSendResponseEntityBody**</span><span class="sxs-lookup"><span data-stu-id="c78b4-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="c78b4-146">傳送 HTTP 回應的實體主體資料。</span><span class="sxs-lookup"><span data-stu-id="c78b4-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="c78b4-147">**HttpWaitForDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c78b4-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="c78b4-148">當 HTTP 用戶端中斷連線時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="c78b4-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="c78b4-149">SSL</span><span class="sxs-lookup"><span data-stu-id="c78b4-149">SSL</span></span>



| <span data-ttu-id="c78b4-150">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-150">Function</span></span>                                                             | <span data-ttu-id="c78b4-151">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="c78b4-152">**HttpReceiveClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="c78b4-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="c78b4-153">抓取 SSL 連線的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="c78b4-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="c78b4-154">URL 註冊</span><span class="sxs-lookup"><span data-stu-id="c78b4-154">URL Registration</span></span>



| <span data-ttu-id="c78b4-155">函式</span><span class="sxs-lookup"><span data-stu-id="c78b4-155">Function</span></span>                               | <span data-ttu-id="c78b4-156">描述</span><span class="sxs-lookup"><span data-stu-id="c78b4-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c78b4-157">**HttpAddUrl**</span><span class="sxs-lookup"><span data-stu-id="c78b4-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="c78b4-158">註冊 URL，讓它的 HTTP 要求會路由傳送至指定的要求佇列。</span><span class="sxs-lookup"><span data-stu-id="c78b4-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="c78b4-159">**HttpRemoveUrl**</span><span class="sxs-lookup"><span data-stu-id="c78b4-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="c78b4-160">取消註冊指定的 URL，使其要求不再路由傳送至指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="c78b4-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c78b4-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="c78b4-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c78b4-162">HTTP 伺服器 API 版本1.0 結構</span><span class="sxs-lookup"><span data-stu-id="c78b4-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




