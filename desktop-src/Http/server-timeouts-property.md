---
title: 伺服器超時屬性
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- 伺服器超時屬性 HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372349"
---
# <a name="server-timeouts-property"></a><span data-ttu-id="337b7-104">伺服器超時屬性</span><span class="sxs-lookup"><span data-stu-id="337b7-104">Server Timeouts Property</span></span>

<span data-ttu-id="337b7-105">HTTP 伺服器 API 可讓應用程式設定伺服器會話或 URL 群組的伺服器連接逾時限制。</span><span class="sxs-lookup"><span data-stu-id="337b7-105">The HTTP Server API enables applications to set the server connection timeout limits on a server session or a URL group.</span></span> <span data-ttu-id="337b7-106">HTTP 超時屬性是用來設定應用程式特定的所有超時。</span><span class="sxs-lookup"><span data-stu-id="337b7-106">The HTTP timeouts property is used to set all timeouts on an application-specific basis.</span></span> <span data-ttu-id="337b7-107">**IdleConnection** 和 **HeaderWait** 計時器也可以設定為「HTTP 伺服器 API 範圍」。</span><span class="sxs-lookup"><span data-stu-id="337b7-107">The **IdleConnection** and **HeaderWait** timers can also be configured HTTP Server API-wide.</span></span> <span data-ttu-id="337b7-108">當計時器設定為使用 HTTP 伺服器 API 時，它們會套用至電腦上的所有 HTTP 伺服器 API 應用程式，而設定會在服務重新開機時保存。</span><span class="sxs-lookup"><span data-stu-id="337b7-108">When the timers are configured HTTP Server API-wide, they apply to all the HTTP Server API applications on the computer and the settings persist when the service is restarted.</span></span>

<span data-ttu-id="337b7-109">如需設定計時器的詳細資訊，請參閱設定 [應用程式特定的超時](configuring-the-application-specific-timeouts.md)。</span><span class="sxs-lookup"><span data-stu-id="337b7-109">For more information about configuring timers, see [Configuring the Application Specific Timeouts](configuring-the-application-specific-timeouts.md).</span></span>

<span data-ttu-id="337b7-110">如果未針對 URL 群組或伺服器會話設定計時器，則會套用 HTTP 伺服器 API 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="337b7-110">When the timers are not configured for a URL group or server session, the HTTP Server API default configurations apply.</span></span>

<span data-ttu-id="337b7-111">執行超時的順序如下：</span><span class="sxs-lookup"><span data-stu-id="337b7-111">The order of timeout enforcement is as follows:</span></span>

1.  <span data-ttu-id="337b7-112">HTTP 伺服器 API 範圍的預設值適用于電腦上的所有 HTTP 伺服器 API 應用程式。</span><span class="sxs-lookup"><span data-stu-id="337b7-112">The HTTP Server API-wide defaults apply to all the HTTP Server API applications on the computer.</span></span>
2.  <span data-ttu-id="337b7-113">設定時，伺服器會話超時會覆寫 HTTP 伺服器 API 範圍的設定。</span><span class="sxs-lookup"><span data-stu-id="337b7-113">The Server Session timeouts override the HTTP Server API-wide settings, when set.</span></span>
3.  <span data-ttu-id="337b7-114">設定時，URL 群組設定會覆寫伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="337b7-114">The URL group settings override the server session configurations, when set.</span></span>

<span data-ttu-id="337b7-115">下表列出預設的連接逾時限制</span><span class="sxs-lookup"><span data-stu-id="337b7-115">The following table lists the default connection timeout limits</span></span>



| <span data-ttu-id="337b7-116">計時器</span><span class="sxs-lookup"><span data-stu-id="337b7-116">Timer</span></span>           | <span data-ttu-id="337b7-117">定義</span><span class="sxs-lookup"><span data-stu-id="337b7-117">Definition</span></span>                                                                                                        | <span data-ttu-id="337b7-118">HTTP 伺服器 API 預設值</span><span class="sxs-lookup"><span data-stu-id="337b7-118">HTTP Server API default</span></span> | <span data-ttu-id="337b7-119">可設定為 HTTP 伺服器 API 寬</span><span class="sxs-lookup"><span data-stu-id="337b7-119">Configurable as HTTP Server API wide</span></span> | <span data-ttu-id="337b7-120">可設定為應用程式特定</span><span class="sxs-lookup"><span data-stu-id="337b7-120">Configurable as Application specific</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="337b7-121">IdleConnection</span><span class="sxs-lookup"><span data-stu-id="337b7-121">IdleConnection</span></span>  | <span data-ttu-id="337b7-122">連接會在保持閒置狀態時過期。</span><span class="sxs-lookup"><span data-stu-id="337b7-122">The connection expired while staying idle.</span></span>                                                                        | <span data-ttu-id="337b7-123">120秒</span><span class="sxs-lookup"><span data-stu-id="337b7-123">120 Sec</span></span>                 | <span data-ttu-id="337b7-124">Yes</span><span class="sxs-lookup"><span data-stu-id="337b7-124">Yes</span></span>                                  | <span data-ttu-id="337b7-125">限制</span><span class="sxs-lookup"><span data-stu-id="337b7-125">Limited</span></span>                              |
| <span data-ttu-id="337b7-126">HeaderWait</span><span class="sxs-lookup"><span data-stu-id="337b7-126">HeaderWait</span></span>      | <span data-ttu-id="337b7-127">在等候 HTTP 伺服器 API 剖析標頭時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="337b7-127">The connection expired while waiting for the HTTP Server API to parse the header.</span></span>                                 | <span data-ttu-id="337b7-128">120秒</span><span class="sxs-lookup"><span data-stu-id="337b7-128">120 Sec</span></span>                 | <span data-ttu-id="337b7-129">Yes</span><span class="sxs-lookup"><span data-stu-id="337b7-129">Yes</span></span>                                  | <span data-ttu-id="337b7-130">限制</span><span class="sxs-lookup"><span data-stu-id="337b7-130">Limited</span></span>                              |
| <span data-ttu-id="337b7-131">EntityBody</span><span class="sxs-lookup"><span data-stu-id="337b7-131">EntityBody</span></span>      | <span data-ttu-id="337b7-132">等待要求實體內容到達時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="337b7-132">The connection expired while waiting for the request entity body to arrive.</span></span>                                       | <span data-ttu-id="337b7-133">120秒</span><span class="sxs-lookup"><span data-stu-id="337b7-133">120 Sec</span></span>                 | <span data-ttu-id="337b7-134">否</span><span class="sxs-lookup"><span data-stu-id="337b7-134">No</span></span>                                   | <span data-ttu-id="337b7-135">是</span><span class="sxs-lookup"><span data-stu-id="337b7-135">Yes</span></span>                                  |
| <span data-ttu-id="337b7-136">DrainEntityBody</span><span class="sxs-lookup"><span data-stu-id="337b7-136">DrainEntityBody</span></span> | <span data-ttu-id="337b7-137">在等候 HTTP 伺服器 API 將實體主體清空 Keep-Alive 連接時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="337b7-137">The connection expired while waiting for the HTTP Server API to drain the entity body on a Keep-Alive connection.</span></span> | <span data-ttu-id="337b7-138">120秒</span><span class="sxs-lookup"><span data-stu-id="337b7-138">120 Sec</span></span>                 | <span data-ttu-id="337b7-139">否</span><span class="sxs-lookup"><span data-stu-id="337b7-139">No</span></span>                                   | <span data-ttu-id="337b7-140">是</span><span class="sxs-lookup"><span data-stu-id="337b7-140">Yes</span></span>                                  |
| <span data-ttu-id="337b7-141">MinSendRate</span><span class="sxs-lookup"><span data-stu-id="337b7-141">MinSendRate</span></span>     | <span data-ttu-id="337b7-142">連接已過期，因為回應傳送速率低於預設值150位元組/秒。</span><span class="sxs-lookup"><span data-stu-id="337b7-142">The connection expired because the response send rate was slower than the default of 150 bytes/sec.</span></span>               | <span data-ttu-id="337b7-143">150秒</span><span class="sxs-lookup"><span data-stu-id="337b7-143">150 Sec</span></span>                 | <span data-ttu-id="337b7-144">否</span><span class="sxs-lookup"><span data-stu-id="337b7-144">No</span></span>                                   | <span data-ttu-id="337b7-145">是</span><span class="sxs-lookup"><span data-stu-id="337b7-145">Yes</span></span>                                  |
| <span data-ttu-id="337b7-146">RequestQueue</span><span class="sxs-lookup"><span data-stu-id="337b7-146">RequestQueue</span></span>    | <span data-ttu-id="337b7-147">連接已過期，因為要求會在應用程式挑選之前保留在要求佇列中。</span><span class="sxs-lookup"><span data-stu-id="337b7-147">The connection expired because the request remained in the request queue before the application picked it up.</span></span>     | <span data-ttu-id="337b7-148">120位元組/秒</span><span class="sxs-lookup"><span data-stu-id="337b7-148">120 Bytes/Sec</span></span>           | <span data-ttu-id="337b7-149">否</span><span class="sxs-lookup"><span data-stu-id="337b7-149">No</span></span>                                   | <span data-ttu-id="337b7-150">是</span><span class="sxs-lookup"><span data-stu-id="337b7-150">Yes</span></span>                                  |



 

 

 




