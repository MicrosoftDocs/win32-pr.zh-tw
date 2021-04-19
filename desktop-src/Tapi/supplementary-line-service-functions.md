---
description: 補充線服務函式依類別列于下列主題中。
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: 補充線服務功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992456"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="77d01-103">補充線服務功能</span><span class="sxs-lookup"><span data-stu-id="77d01-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="77d01-104">補充線服務函式依類別列于下列主題中。</span><span class="sxs-lookup"><span data-stu-id="77d01-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="77d01-105">如果函式會將回復訊息中的完成指出至應用程式，則會將函式識別為 [*非同步*](a-tapgloss.md) 。</span><span class="sxs-lookup"><span data-stu-id="77d01-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="77d01-106">如果函式一律會立即將其結果傳回給應用程式，則會將函數視為 [*同步*](s-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="77d01-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="77d01-107">以下是補充行服務功能的功能群組：</span><span class="sxs-lookup"><span data-stu-id="77d01-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="77d01-108">代理程式</span><span class="sxs-lookup"><span data-stu-id="77d01-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="77d01-109">應用程式優先順序</span><span class="sxs-lookup"><span data-stu-id="77d01-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="77d01-110">持有人模式和費率</span><span class="sxs-lookup"><span data-stu-id="77d01-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="77d01-111">呼叫接受和重新導向</span><span class="sxs-lookup"><span data-stu-id="77d01-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="77d01-112">呼叫完成</span><span class="sxs-lookup"><span data-stu-id="77d01-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="77d01-113">通話會議</span><span class="sxs-lookup"><span data-stu-id="77d01-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="77d01-114">來電轉接</span><span class="sxs-lookup"><span data-stu-id="77d01-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="77d01-115">通話保留</span><span class="sxs-lookup"><span data-stu-id="77d01-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="77d01-116">撥打公園</span><span class="sxs-lookup"><span data-stu-id="77d01-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="77d01-117">撥打取貨</span><span class="sxs-lookup"><span data-stu-id="77d01-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="77d01-118">拒絕呼叫</span><span class="sxs-lookup"><span data-stu-id="77d01-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="77d01-119">來電轉接</span><span class="sxs-lookup"><span data-stu-id="77d01-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="77d01-120">數位監視和收集</span><span class="sxs-lookup"><span data-stu-id="77d01-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="77d01-121">產生 inband 數位和音調</span><span class="sxs-lookup"><span data-stu-id="77d01-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="77d01-122">進行呼叫</span><span class="sxs-lookup"><span data-stu-id="77d01-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="77d01-123">媒體控制項</span><span class="sxs-lookup"><span data-stu-id="77d01-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="77d01-124">媒體監視</span><span class="sxs-lookup"><span data-stu-id="77d01-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="77d01-125">代理</span><span class="sxs-lookup"><span data-stu-id="77d01-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="77d01-126">服務品質</span><span class="sxs-lookup"><span data-stu-id="77d01-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="77d01-127">將資訊傳送給遠端當事人</span><span class="sxs-lookup"><span data-stu-id="77d01-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="77d01-128">服務提供者管理</span><span class="sxs-lookup"><span data-stu-id="77d01-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="77d01-129">設定電話通話的終端機</span><span class="sxs-lookup"><span data-stu-id="77d01-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="77d01-130">語氣監視</span><span class="sxs-lookup"><span data-stu-id="77d01-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="77d01-131">另外還有 [其他](#miscellaneous) 補充線服務功能。</span><span class="sxs-lookup"><span data-stu-id="77d01-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="77d01-132">持有人模式和費率</span><span class="sxs-lookup"><span data-stu-id="77d01-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="77d01-133">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-133">Function</span></span>                                       | <span data-ttu-id="77d01-134">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-135">**lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="77d01-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="77d01-136">要求現有呼叫的呼叫參數變更。</span><span class="sxs-lookup"><span data-stu-id="77d01-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="77d01-137">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="77d01-138">媒體監視</span><span class="sxs-lookup"><span data-stu-id="77d01-138">Media Monitoring</span></span>



| <span data-ttu-id="77d01-139">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-139">Function</span></span>                                     | <span data-ttu-id="77d01-140">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-141">**lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="77d01-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="77d01-142">啟用或停用指定之呼叫的媒體模式通知。</span><span class="sxs-lookup"><span data-stu-id="77d01-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="77d01-143">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="77d01-144">數位監視和收集</span><span class="sxs-lookup"><span data-stu-id="77d01-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="77d01-145">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-145">Function</span></span>                                       | <span data-ttu-id="77d01-146">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-147">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="77d01-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="77d01-148">啟用或停用指定之呼叫的數位偵測通知。</span><span class="sxs-lookup"><span data-stu-id="77d01-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="77d01-149">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-149">Synchronous.</span></span> |
| [<span data-ttu-id="77d01-150">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="77d01-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="77d01-151">在呼叫上執行已緩衝的數位收集。</span><span class="sxs-lookup"><span data-stu-id="77d01-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="77d01-152">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="77d01-153">語氣監視</span><span class="sxs-lookup"><span data-stu-id="77d01-153">Tone Monitoring</span></span>



| <span data-ttu-id="77d01-154">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-154">Function</span></span>                                     | <span data-ttu-id="77d01-155">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="77d01-156">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="77d01-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="77d01-157">指定要在指定的呼叫上偵測的色調。</span><span class="sxs-lookup"><span data-stu-id="77d01-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="77d01-158">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="77d01-159">媒體控制項</span><span class="sxs-lookup"><span data-stu-id="77d01-159">Media Control</span></span>



| <span data-ttu-id="77d01-160">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-160">Function</span></span>                                           | <span data-ttu-id="77d01-161">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-162">**lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="77d01-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="77d01-163">設定 media control 的呼叫媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="77d01-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="77d01-164">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="77d01-165">**lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="77d01-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="77d01-166">在 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) 結構中，設定指定之呼叫的媒體模式 (s) 。</span><span class="sxs-lookup"><span data-stu-id="77d01-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="77d01-167">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="77d01-168">產生 Inband 數位和音調</span><span class="sxs-lookup"><span data-stu-id="77d01-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="77d01-169">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-169">Function</span></span>                                         | <span data-ttu-id="77d01-170">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="77d01-171">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="77d01-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="77d01-172">在呼叫上產生 inband 位數。</span><span class="sxs-lookup"><span data-stu-id="77d01-172">Generates inband digits on a call.</span></span> <span data-ttu-id="77d01-173">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-173">Synchronous.</span></span>               |
| [<span data-ttu-id="77d01-174">**lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="77d01-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="77d01-175">在呼叫上產生一組指定的聲 inband。</span><span class="sxs-lookup"><span data-stu-id="77d01-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="77d01-176">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="77d01-177">呼叫接受和重新導向</span><span class="sxs-lookup"><span data-stu-id="77d01-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="77d01-178">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-178">Function</span></span>                             | <span data-ttu-id="77d01-179">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-180">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="77d01-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="77d01-181">接受提供的呼叫，並開始發出兩個呼叫者 (回電) 和呼叫方 (環形) 的警示。</span><span class="sxs-lookup"><span data-stu-id="77d01-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="77d01-182">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-182">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-183">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="77d01-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="77d01-184">將供應專案呼叫重新導向至另一個位址。</span><span class="sxs-lookup"><span data-stu-id="77d01-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="77d01-185">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="77d01-186">拒絕呼叫</span><span class="sxs-lookup"><span data-stu-id="77d01-186">Call Reject</span></span>



| <span data-ttu-id="77d01-187">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-187">Function</span></span>                     | <span data-ttu-id="77d01-188">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-189">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="77d01-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="77d01-190">中斷通話的連線，或放棄進行中的呼叫嘗試。</span><span class="sxs-lookup"><span data-stu-id="77d01-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="77d01-191">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="77d01-192">通話保留</span><span class="sxs-lookup"><span data-stu-id="77d01-192">Call Hold</span></span>



| <span data-ttu-id="77d01-193">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-193">Function</span></span>                         | <span data-ttu-id="77d01-194">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="77d01-195">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="77d01-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="77d01-196">放置指定的呼叫以進行硬保留。</span><span class="sxs-lookup"><span data-stu-id="77d01-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="77d01-197">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-197">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-198">**lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="77d01-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="77d01-199">抓取保留的呼叫。</span><span class="sxs-lookup"><span data-stu-id="77d01-199">Retrieves a held call.</span></span> <span data-ttu-id="77d01-200">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="77d01-201">保護呼叫的安全</span><span class="sxs-lookup"><span data-stu-id="77d01-201">Securing Calls</span></span>



| <span data-ttu-id="77d01-202">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-202">Function</span></span>                                 | <span data-ttu-id="77d01-203">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-204">**lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="77d01-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="77d01-205">保護現有的呼叫免于受到其他事件的干擾，例如資料連線上的呼叫等候嗶聲。</span><span class="sxs-lookup"><span data-stu-id="77d01-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="77d01-206">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="77d01-207">來電轉接</span><span class="sxs-lookup"><span data-stu-id="77d01-207">Call Transfer</span></span>



| <span data-ttu-id="77d01-208">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-208">Function</span></span>                                             | <span data-ttu-id="77d01-209">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="77d01-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="77d01-211">準備指定的呼叫，以傳送至其他位址。</span><span class="sxs-lookup"><span data-stu-id="77d01-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="77d01-212">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="77d01-213">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="77d01-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="77d01-214">傳送針對傳送到另一個呼叫所設定的呼叫，或進入三向會議。</span><span class="sxs-lookup"><span data-stu-id="77d01-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="77d01-215">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-215">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-216">**lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="77d01-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="77d01-217">將來電轉接給另一方。</span><span class="sxs-lookup"><span data-stu-id="77d01-217">Transfers a call to another party.</span></span> <span data-ttu-id="77d01-218">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="77d01-219">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="77d01-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="77d01-220">使用目前在諮詢上的呼叫來交換主動呼叫。</span><span class="sxs-lookup"><span data-stu-id="77d01-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="77d01-221">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="77d01-222">通話會議</span><span class="sxs-lookup"><span data-stu-id="77d01-222">Call Conference</span></span>



| <span data-ttu-id="77d01-223">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-223">Function</span></span>                                                         | <span data-ttu-id="77d01-224">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-225">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="77d01-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="77d01-226">準備指定的呼叫，以新增另一個合作物件。</span><span class="sxs-lookup"><span data-stu-id="77d01-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="77d01-227">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="77d01-228">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="77d01-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="77d01-229">準備新增合作物件到現有的會議通話，方法是將會議通話置於保存狀態，然後建立可稍後新增至會議通話的諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="77d01-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="77d01-230">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-230">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-231">**lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="77d01-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="77d01-232">將諮詢通話新增至現有的會議通話。</span><span class="sxs-lookup"><span data-stu-id="77d01-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="77d01-233">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="77d01-234">**lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="77d01-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="77d01-235">從會議通話中移除合作物件。</span><span class="sxs-lookup"><span data-stu-id="77d01-235">Removes a party from a conference call.</span></span> <span data-ttu-id="77d01-236">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="77d01-237">撥打公園</span><span class="sxs-lookup"><span data-stu-id="77d01-237">Call Park</span></span>



| <span data-ttu-id="77d01-238">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-238">Function</span></span>                         | <span data-ttu-id="77d01-239">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="77d01-240">**linePark**</span><span class="sxs-lookup"><span data-stu-id="77d01-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="77d01-241">在另一個位址公園指定的來電。</span><span class="sxs-lookup"><span data-stu-id="77d01-241">Parks a given call at another address.</span></span> <span data-ttu-id="77d01-242">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-242">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-243">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="77d01-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="77d01-244">抓取暫停的呼叫。</span><span class="sxs-lookup"><span data-stu-id="77d01-244">Retrieves a parked call.</span></span> <span data-ttu-id="77d01-245">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="77d01-246">呼叫轉送</span><span class="sxs-lookup"><span data-stu-id="77d01-246">Call Forwarding</span></span>



| <span data-ttu-id="77d01-247">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-247">Function</span></span>                           | <span data-ttu-id="77d01-248">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="77d01-249">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="77d01-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="77d01-250">設定或取消呼叫轉送要求。</span><span class="sxs-lookup"><span data-stu-id="77d01-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="77d01-251">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="77d01-252">撥打取貨</span><span class="sxs-lookup"><span data-stu-id="77d01-252">Call Pickup</span></span>



| <span data-ttu-id="77d01-253">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-253">Function</span></span>                         | <span data-ttu-id="77d01-254">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-255">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="77d01-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="77d01-256">在指定的目的地位址收取通話警示，並傳回所挑選呼叫的呼叫控制碼 ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) 也可用於呼叫等候) 。</span><span class="sxs-lookup"><span data-stu-id="77d01-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="77d01-257">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="77d01-258">將資訊傳送給遠端當事人</span><span class="sxs-lookup"><span data-stu-id="77d01-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="77d01-259">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-259">Function</span></span>                                                   | <span data-ttu-id="77d01-260">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-261">**lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="77d01-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="77d01-262">釋出使用者的使用者資訊，允許系統以新資訊覆寫此儲存體。</span><span class="sxs-lookup"><span data-stu-id="77d01-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="77d01-263">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-263">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-264">**lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="77d01-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="77d01-265">在指定的呼叫上，將使用者資訊傳送給遠端方。</span><span class="sxs-lookup"><span data-stu-id="77d01-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="77d01-266">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="77d01-267">呼叫完成</span><span class="sxs-lookup"><span data-stu-id="77d01-267">Call Completion</span></span>



| <span data-ttu-id="77d01-268">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-268">Function</span></span>                                         | <span data-ttu-id="77d01-269">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="77d01-270">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="77d01-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="77d01-271">放置通話完成要求。</span><span class="sxs-lookup"><span data-stu-id="77d01-271">Places a call completion request.</span></span> <span data-ttu-id="77d01-272">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="77d01-273">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="77d01-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="77d01-274">取消通話完成要求。</span><span class="sxs-lookup"><span data-stu-id="77d01-274">Cancels a call completion request.</span></span> <span data-ttu-id="77d01-275">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="77d01-276">設定電話通話的終端機</span><span class="sxs-lookup"><span data-stu-id="77d01-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="77d01-277">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-277">Function</span></span>                                   | <span data-ttu-id="77d01-278">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-279">**lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="77d01-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="77d01-280">指定要路由指定之行、位址事件或呼叫媒體串流事件的終端機裝置。</span><span class="sxs-lookup"><span data-stu-id="77d01-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="77d01-281">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="77d01-282">應用程式優先順序</span><span class="sxs-lookup"><span data-stu-id="77d01-282">Application Priority</span></span>



| <span data-ttu-id="77d01-283">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-283">Function</span></span>                                         | <span data-ttu-id="77d01-284">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-285">**lineGetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="77d01-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="77d01-286">抓取應用程式的遞交及/或輔助電話語音優先順序資訊。</span><span class="sxs-lookup"><span data-stu-id="77d01-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="77d01-287">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-287">Synchronous.</span></span> |
| [<span data-ttu-id="77d01-288">**lineSetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="77d01-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="77d01-289">設定應用程式的遞交及/或輔助電話語音優先順序。</span><span class="sxs-lookup"><span data-stu-id="77d01-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="77d01-290">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="77d01-291">服務提供者管理</span><span class="sxs-lookup"><span data-stu-id="77d01-291">Service Provider Management</span></span>



| <span data-ttu-id="77d01-292">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-292">Function</span></span>                                           | <span data-ttu-id="77d01-293">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="77d01-294">**lineAddProvider**</span><span class="sxs-lookup"><span data-stu-id="77d01-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="77d01-295">安裝電話語音服務提供者。</span><span class="sxs-lookup"><span data-stu-id="77d01-295">Installs a telephony service provider.</span></span> <span data-ttu-id="77d01-296">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="77d01-297">**lineConfigProvider**</span><span class="sxs-lookup"><span data-stu-id="77d01-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="77d01-298">顯示服務提供者的 [設定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="77d01-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="77d01-299">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-299">Synchronous.</span></span> |
| [<span data-ttu-id="77d01-300">**lineRemoveProvider**</span><span class="sxs-lookup"><span data-stu-id="77d01-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="77d01-301">移除現有的電話語音服務提供者。</span><span class="sxs-lookup"><span data-stu-id="77d01-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="77d01-302">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-302">Synchronous.</span></span>          |
| [<span data-ttu-id="77d01-303">**lineGetProviderList**</span><span class="sxs-lookup"><span data-stu-id="77d01-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="77d01-304">抓取已安裝的服務提供者清單。</span><span class="sxs-lookup"><span data-stu-id="77d01-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="77d01-305">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="77d01-306">代理程式</span><span class="sxs-lookup"><span data-stu-id="77d01-306">Agents</span></span>



| <span data-ttu-id="77d01-307">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-307">Function</span></span>                                                     | <span data-ttu-id="77d01-308">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-309">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="77d01-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="77d01-310">允許應用程式存取與位址相關聯之代理程式處理常式的專屬處理常式特定函式。</span><span class="sxs-lookup"><span data-stu-id="77d01-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="77d01-311">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-311">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-312">**lineGetAgentActivityList**</span><span class="sxs-lookup"><span data-stu-id="77d01-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="77d01-313">取得活動清單，應用程式會從該清單中選取代理程式所執行的函式。</span><span class="sxs-lookup"><span data-stu-id="77d01-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="77d01-314">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="77d01-315">**lineGetAgentCaps**</span><span class="sxs-lookup"><span data-stu-id="77d01-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="77d01-316">取得指定線路裝置上支援的代理程式相關功能。</span><span class="sxs-lookup"><span data-stu-id="77d01-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="77d01-317">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="77d01-318">**lineGetAgentGroupList**</span><span class="sxs-lookup"><span data-stu-id="77d01-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="77d01-319">取得代理程式群組的清單，代理程式可以在此清單中登入自動呼叫散發者。</span><span class="sxs-lookup"><span data-stu-id="77d01-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="77d01-320">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="77d01-321">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="77d01-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="77d01-322">取得指定位址上代理程式相關的狀態。</span><span class="sxs-lookup"><span data-stu-id="77d01-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="77d01-323">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="77d01-324">**lineSetAgentActivity**</span><span class="sxs-lookup"><span data-stu-id="77d01-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="77d01-325">設定與特定位址相關聯的代理程式活動代碼。</span><span class="sxs-lookup"><span data-stu-id="77d01-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="77d01-326">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="77d01-327">**lineSetAgentGroup**</span><span class="sxs-lookup"><span data-stu-id="77d01-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="77d01-328">設定代理程式用來登入特定位址的代理程式群組。</span><span class="sxs-lookup"><span data-stu-id="77d01-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="77d01-329">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="77d01-330">**lineSetAgentState**</span><span class="sxs-lookup"><span data-stu-id="77d01-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="77d01-331">設定與特定位址相關聯的代理程式狀態。</span><span class="sxs-lookup"><span data-stu-id="77d01-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="77d01-332">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="77d01-333">Proxy</span><span class="sxs-lookup"><span data-stu-id="77d01-333">Proxies</span></span>



| <span data-ttu-id="77d01-334">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-334">Function</span></span>                                       | <span data-ttu-id="77d01-335">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-336">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="77d01-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="77d01-337">由已註冊的 proxy 要求處理常式用來產生 TAPI 訊息。</span><span class="sxs-lookup"><span data-stu-id="77d01-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="77d01-338">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-338">Synchronous.</span></span>  |
| [<span data-ttu-id="77d01-339">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="77d01-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="77d01-340">表示已註冊的 proxy 處理常式完成 proxy 要求。</span><span class="sxs-lookup"><span data-stu-id="77d01-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="77d01-341">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="77d01-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="77d01-342">服務品質</span><span class="sxs-lookup"><span data-stu-id="77d01-342">Quality of Service</span></span>



| <span data-ttu-id="77d01-343">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-343">Function</span></span>                                                           | <span data-ttu-id="77d01-344">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-345">**lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="77d01-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="77d01-346">要求現有呼叫的服務參數品質變更。</span><span class="sxs-lookup"><span data-stu-id="77d01-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="77d01-347">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="77d01-348">其他</span><span class="sxs-lookup"><span data-stu-id="77d01-348">Miscellaneous</span></span>



| <span data-ttu-id="77d01-349">函式</span><span class="sxs-lookup"><span data-stu-id="77d01-349">Function</span></span>                                             | <span data-ttu-id="77d01-350">描述</span><span class="sxs-lookup"><span data-stu-id="77d01-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77d01-351">**lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="77d01-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="77d01-352">設定 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)結構的 **CallData** 成員。</span><span class="sxs-lookup"><span data-stu-id="77d01-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="77d01-353">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-353">Asynchronous.</span></span> |
| [<span data-ttu-id="77d01-354">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="77d01-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="77d01-355">設定當來電未接聽或保留時，使用者所聽到的聲音。</span><span class="sxs-lookup"><span data-stu-id="77d01-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="77d01-356">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="77d01-357">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="77d01-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="77d01-358">設定線路裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="77d01-358">Sets the line device status.</span></span> <span data-ttu-id="77d01-359">非同步：</span><span class="sxs-lookup"><span data-stu-id="77d01-359">Asynchronous.</span></span>                                                            |



 

 

 



