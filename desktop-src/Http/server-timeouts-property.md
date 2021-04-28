---
title: 伺服器超時屬性
description: 伺服器超時屬性
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- 伺服器超時屬性 HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26fcd1376e8b7394a3a037bbbe00495466e32609
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090856"
---
# <a name="server-timeouts-property"></a><span data-ttu-id="410db-104">伺服器超時屬性</span><span class="sxs-lookup"><span data-stu-id="410db-104">Server Timeouts Property</span></span>

<span data-ttu-id="410db-105">HTTP 伺服器 API 可讓應用程式設定伺服器會話或 URL 群組的伺服器連接逾時限制。</span><span class="sxs-lookup"><span data-stu-id="410db-105">The HTTP Server API enables applications to set the server connection timeout limits on a server session or a URL group.</span></span> <span data-ttu-id="410db-106">HTTP 超時屬性是用來設定應用程式特定的所有超時。</span><span class="sxs-lookup"><span data-stu-id="410db-106">The HTTP timeouts property is used to set all timeouts on an application-specific basis.</span></span> <span data-ttu-id="410db-107">**IdleConnection** 和 **HeaderWait** 計時器也可以設定為「HTTP 伺服器 API 範圍」。</span><span class="sxs-lookup"><span data-stu-id="410db-107">The **IdleConnection** and **HeaderWait** timers can also be configured HTTP Server API-wide.</span></span> <span data-ttu-id="410db-108">當計時器設定為使用 HTTP 伺服器 API 時，它們會套用至電腦上的所有 HTTP 伺服器 API 應用程式，而設定會在服務重新開機時保存。</span><span class="sxs-lookup"><span data-stu-id="410db-108">When the timers are configured HTTP Server API-wide, they apply to all the HTTP Server API applications on the computer and the settings persist when the service is restarted.</span></span>

<span data-ttu-id="410db-109">如需設定計時器的詳細資訊，請參閱設定 [應用程式特定的超時](configuring-the-application-specific-timeouts.md)。</span><span class="sxs-lookup"><span data-stu-id="410db-109">For more information about configuring timers, see [Configuring the Application Specific Timeouts](configuring-the-application-specific-timeouts.md).</span></span>

<span data-ttu-id="410db-110">如果未針對 URL 群組或伺服器會話設定計時器，則會套用 HTTP 伺服器 API 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="410db-110">When the timers are not configured for a URL group or server session, the HTTP Server API default configurations apply.</span></span>

<span data-ttu-id="410db-111">執行超時的順序如下：</span><span class="sxs-lookup"><span data-stu-id="410db-111">The order of timeout enforcement is as follows:</span></span>

1.  <span data-ttu-id="410db-112">HTTP 伺服器 API 範圍的預設值適用于電腦上的所有 HTTP 伺服器 API 應用程式。</span><span class="sxs-lookup"><span data-stu-id="410db-112">The HTTP Server API-wide defaults apply to all the HTTP Server API applications on the computer.</span></span>
2.  <span data-ttu-id="410db-113">設定時，伺服器會話超時會覆寫 HTTP 伺服器 API 範圍的設定。</span><span class="sxs-lookup"><span data-stu-id="410db-113">The Server Session timeouts override the HTTP Server API-wide settings, when set.</span></span>
3.  <span data-ttu-id="410db-114">設定時，URL 群組設定會覆寫伺服器會話設定。</span><span class="sxs-lookup"><span data-stu-id="410db-114">The URL group settings override the server session configurations, when set.</span></span>

<span data-ttu-id="410db-115">下表列出預設的連接逾時限制</span><span class="sxs-lookup"><span data-stu-id="410db-115">The following table lists the default connection timeout limits</span></span>



| <span data-ttu-id="410db-116">計時器</span><span class="sxs-lookup"><span data-stu-id="410db-116">Timer</span></span>           | <span data-ttu-id="410db-117">定義</span><span class="sxs-lookup"><span data-stu-id="410db-117">Definition</span></span>                                                                                                        | <span data-ttu-id="410db-118">HTTP 伺服器 API 預設值</span><span class="sxs-lookup"><span data-stu-id="410db-118">HTTP Server API default</span></span> | <span data-ttu-id="410db-119">可設定為 HTTP 伺服器 API 寬</span><span class="sxs-lookup"><span data-stu-id="410db-119">Configurable as HTTP Server API wide</span></span> | <span data-ttu-id="410db-120">可設定為應用程式特定</span><span class="sxs-lookup"><span data-stu-id="410db-120">Configurable as Application specific</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="410db-121">IdleConnection</span><span class="sxs-lookup"><span data-stu-id="410db-121">IdleConnection</span></span>  | <span data-ttu-id="410db-122">連接會在保持閒置狀態時過期。</span><span class="sxs-lookup"><span data-stu-id="410db-122">The connection expired while staying idle.</span></span>                                                                        | <span data-ttu-id="410db-123">120秒</span><span class="sxs-lookup"><span data-stu-id="410db-123">120 Sec</span></span>                 | <span data-ttu-id="410db-124">是</span><span class="sxs-lookup"><span data-stu-id="410db-124">Yes</span></span>                                  | <span data-ttu-id="410db-125">限制</span><span class="sxs-lookup"><span data-stu-id="410db-125">Limited</span></span>                              |
| <span data-ttu-id="410db-126">HeaderWait</span><span class="sxs-lookup"><span data-stu-id="410db-126">HeaderWait</span></span>      | <span data-ttu-id="410db-127">在等候 HTTP 伺服器 API 剖析標頭時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="410db-127">The connection expired while waiting for the HTTP Server API to parse the header.</span></span>                                 | <span data-ttu-id="410db-128">120秒</span><span class="sxs-lookup"><span data-stu-id="410db-128">120 Sec</span></span>                 | <span data-ttu-id="410db-129">是</span><span class="sxs-lookup"><span data-stu-id="410db-129">Yes</span></span>                                  | <span data-ttu-id="410db-130">限制</span><span class="sxs-lookup"><span data-stu-id="410db-130">Limited</span></span>                              |
| <span data-ttu-id="410db-131">EntityBody</span><span class="sxs-lookup"><span data-stu-id="410db-131">EntityBody</span></span>      | <span data-ttu-id="410db-132">等待要求實體內容到達時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="410db-132">The connection expired while waiting for the request entity body to arrive.</span></span>                                       | <span data-ttu-id="410db-133">120秒</span><span class="sxs-lookup"><span data-stu-id="410db-133">120 Sec</span></span>                 | <span data-ttu-id="410db-134">否</span><span class="sxs-lookup"><span data-stu-id="410db-134">No</span></span>                                   | <span data-ttu-id="410db-135">是</span><span class="sxs-lookup"><span data-stu-id="410db-135">Yes</span></span>                                  |
| <span data-ttu-id="410db-136">DrainEntityBody</span><span class="sxs-lookup"><span data-stu-id="410db-136">DrainEntityBody</span></span> | <span data-ttu-id="410db-137">在等候 HTTP 伺服器 API 將實體主體清空 Keep-Alive 連接時，連接已過期。</span><span class="sxs-lookup"><span data-stu-id="410db-137">The connection expired while waiting for the HTTP Server API to drain the entity body on a Keep-Alive connection.</span></span> | <span data-ttu-id="410db-138">120秒</span><span class="sxs-lookup"><span data-stu-id="410db-138">120 Sec</span></span>                 | <span data-ttu-id="410db-139">否</span><span class="sxs-lookup"><span data-stu-id="410db-139">No</span></span>                                   | <span data-ttu-id="410db-140">是</span><span class="sxs-lookup"><span data-stu-id="410db-140">Yes</span></span>                                  |
| <span data-ttu-id="410db-141">MinSendRate</span><span class="sxs-lookup"><span data-stu-id="410db-141">MinSendRate</span></span>     | <span data-ttu-id="410db-142">連接已過期，因為回應傳送速率低於預設值150位元組/秒。</span><span class="sxs-lookup"><span data-stu-id="410db-142">The connection expired because the response send rate was slower than the default of 150 bytes/sec.</span></span>               | <span data-ttu-id="410db-143">150秒</span><span class="sxs-lookup"><span data-stu-id="410db-143">150 Sec</span></span>                 | <span data-ttu-id="410db-144">否</span><span class="sxs-lookup"><span data-stu-id="410db-144">No</span></span>                                   | <span data-ttu-id="410db-145">是</span><span class="sxs-lookup"><span data-stu-id="410db-145">Yes</span></span>                                  |
| <span data-ttu-id="410db-146">RequestQueue</span><span class="sxs-lookup"><span data-stu-id="410db-146">RequestQueue</span></span>    | <span data-ttu-id="410db-147">連接已過期，因為要求會在應用程式挑選之前保留在要求佇列中。</span><span class="sxs-lookup"><span data-stu-id="410db-147">The connection expired because the request remained in the request queue before the application picked it up.</span></span>     | <span data-ttu-id="410db-148">120位元組/秒</span><span class="sxs-lookup"><span data-stu-id="410db-148">120 Bytes/Sec</span></span>           | <span data-ttu-id="410db-149">否</span><span class="sxs-lookup"><span data-stu-id="410db-149">No</span></span>                                   | <span data-ttu-id="410db-150">是</span><span class="sxs-lookup"><span data-stu-id="410db-150">Yes</span></span>                                  |



 

 

 




