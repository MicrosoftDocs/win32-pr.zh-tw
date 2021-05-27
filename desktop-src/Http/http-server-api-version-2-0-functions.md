---
title: HTTP 伺服器 API 版本2.0 函式
description: HTTP 伺服器 API 2.0 版提供下列功能。
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- HTTP 伺服器 API 版本2.0 函式
- 函數 HTTP，HTTP 伺服器 API 版本2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549073"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="a912b-105">HTTP 伺服器 API 版本2.0 函式</span><span class="sxs-lookup"><span data-stu-id="a912b-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="a912b-106">HTTP 伺服器 API 2.0 版提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="a912b-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="a912b-107">函式</span><span class="sxs-lookup"><span data-stu-id="a912b-107">Function</span></span> | <span data-ttu-id="a912b-108">描述</span><span class="sxs-lookup"><span data-stu-id="a912b-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="a912b-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="a912b-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="a912b-110">將要求從來源要求佇列委派至目標要求佇列。</span><span class="sxs-lookup"><span data-stu-id="a912b-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="a912b-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="a912b-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="a912b-112">抓取 URL 的 URL 群組識別碼和要求佇列。</span><span class="sxs-lookup"><span data-stu-id="a912b-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="a912b-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="a912b-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="a912b-114">檢查是否支援特定功能。</span><span class="sxs-lookup"><span data-stu-id="a912b-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="a912b-115">伺服器會話</span><span class="sxs-lookup"><span data-stu-id="a912b-115">Server session</span></span>

| <span data-ttu-id="a912b-116">函式</span><span class="sxs-lookup"><span data-stu-id="a912b-116">Function</span></span> | <span data-ttu-id="a912b-117">描述</span><span class="sxs-lookup"><span data-stu-id="a912b-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="a912b-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="a912b-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="a912b-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="a912b-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="a912b-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="a912b-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="a912b-122">URL 群組</span><span class="sxs-lookup"><span data-stu-id="a912b-122">URL Groups</span></span>

| <span data-ttu-id="a912b-123">函式</span><span class="sxs-lookup"><span data-stu-id="a912b-123">Function</span></span> | <span data-ttu-id="a912b-124">描述</span><span class="sxs-lookup"><span data-stu-id="a912b-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="a912b-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a912b-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="a912b-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a912b-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="a912b-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a912b-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="a912b-128">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="a912b-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a912b-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="a912b-130">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="a912b-131">要求佇列</span><span class="sxs-lookup"><span data-stu-id="a912b-131">Request Queue</span></span>

| <span data-ttu-id="a912b-132">函式</span><span class="sxs-lookup"><span data-stu-id="a912b-132">Function</span></span> | <span data-ttu-id="a912b-133">描述</span><span class="sxs-lookup"><span data-stu-id="a912b-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="a912b-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a912b-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="a912b-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a912b-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="a912b-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="a912b-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="a912b-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="a912b-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a912b-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="a912b-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="a912b-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="a912b-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="a912b-140">Related topics</span></span>

[<span data-ttu-id="a912b-141">HTTP 伺服器 API 版本2.0 結構</span><span class="sxs-lookup"><span data-stu-id="a912b-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
