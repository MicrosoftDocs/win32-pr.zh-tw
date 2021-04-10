---
description: 深入瞭解：事件記錄檔參數
title: 事件記錄檔參數
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026931"
---
# <a name="event-log-parameters"></a><span data-ttu-id="241dd-103">事件記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="241dd-103">Event Log Parameters</span></span>


<span data-ttu-id="241dd-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="241dd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="241dd-105">事件記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="241dd-105">Event Log Parameters</span></span>

<span data-ttu-id="241dd-106">本主題包含事件記錄檔所使用的參數。</span><span class="sxs-lookup"><span data-stu-id="241dd-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="241dd-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="241dd-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="241dd-108">此參數會控制記錄檔訊息快取的大小 () （以位元組為單位），此訊息會保存資料庫引擎在 eventlog 服務停止時發出的 eventlog 訊息。</span><span class="sxs-lookup"><span data-stu-id="241dd-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="241dd-109">當服務變成可運作時，這些快取的訊息將會清除到 eventlog。</span><span class="sxs-lookup"><span data-stu-id="241dd-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="241dd-110">將會捨棄任何溢位的快取訊息。</span><span class="sxs-lookup"><span data-stu-id="241dd-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-111">預設值：3</span><span class="sxs-lookup"><span data-stu-id="241dd-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="241dd-112">0</span><span class="sxs-lookup"><span data-stu-id="241dd-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="241dd-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="241dd-114">整數</span><span class="sxs-lookup"><span data-stu-id="241dd-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-115">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="241dd-116">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="241dd-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-117">範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="241dd-118">全球</span><span class="sxs-lookup"><span data-stu-id="241dd-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-119">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-120">No</span><span class="sxs-lookup"><span data-stu-id="241dd-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-121">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-122">No</span><span class="sxs-lookup"><span data-stu-id="241dd-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-123">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="241dd-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="241dd-124">No</span><span class="sxs-lookup"><span data-stu-id="241dd-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-125">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="241dd-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-126">No</span><span class="sxs-lookup"><span data-stu-id="241dd-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-127">影響效能：</span><span class="sxs-lookup"><span data-stu-id="241dd-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="241dd-128">No</span><span class="sxs-lookup"><span data-stu-id="241dd-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-129">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="241dd-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="241dd-130">Yes</span><span class="sxs-lookup"><span data-stu-id="241dd-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-131">可用性：</span><span class="sxs-lookup"><span data-stu-id="241dd-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-132">全部</span><span class="sxs-lookup"><span data-stu-id="241dd-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="241dd-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="241dd-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="241dd-134">此參數會設定資料庫引擎發出給 eventlog 的 eventlog 訊息詳細層級。</span><span class="sxs-lookup"><span data-stu-id="241dd-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="241dd-135">較高的數位將會產生更詳細的事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="241dd-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-136">預設值：3</span><span class="sxs-lookup"><span data-stu-id="241dd-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="241dd-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="241dd-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-138">輸入：</span><span class="sxs-lookup"><span data-stu-id="241dd-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="241dd-139">整數</span><span class="sxs-lookup"><span data-stu-id="241dd-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-140">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="241dd-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="241dd-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-142">範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="241dd-143">執行個體</span><span class="sxs-lookup"><span data-stu-id="241dd-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-144">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-145">Yes</span><span class="sxs-lookup"><span data-stu-id="241dd-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-146">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-147">No</span><span class="sxs-lookup"><span data-stu-id="241dd-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-148">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="241dd-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="241dd-149">No</span><span class="sxs-lookup"><span data-stu-id="241dd-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-150">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="241dd-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-151">No</span><span class="sxs-lookup"><span data-stu-id="241dd-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-152">影響效能：</span><span class="sxs-lookup"><span data-stu-id="241dd-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="241dd-153">No</span><span class="sxs-lookup"><span data-stu-id="241dd-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-154">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="241dd-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="241dd-155">No</span><span class="sxs-lookup"><span data-stu-id="241dd-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-156">可用性：</span><span class="sxs-lookup"><span data-stu-id="241dd-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-157">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="241dd-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="241dd-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="241dd-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="241dd-159">4</span><span class="sxs-lookup"><span data-stu-id="241dd-159">4</span></span>  

<span data-ttu-id="241dd-160">此參數會提供應用程式特定的字串，該字串將會新增至 database engine 發出的任何事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="241dd-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="241dd-161">這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。</span><span class="sxs-lookup"><span data-stu-id="241dd-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="241dd-162">如果指定了空字串 (預設) 則會使用主應用程式的可執行檔名稱。</span><span class="sxs-lookup"><span data-stu-id="241dd-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-163">預設值：3</span><span class="sxs-lookup"><span data-stu-id="241dd-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-164">輸入：</span><span class="sxs-lookup"><span data-stu-id="241dd-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="241dd-165">String</span><span class="sxs-lookup"><span data-stu-id="241dd-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-166">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="241dd-167">0–259個字元</span><span class="sxs-lookup"><span data-stu-id="241dd-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-168">範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="241dd-169">執行個體</span><span class="sxs-lookup"><span data-stu-id="241dd-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-170">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-171">Yes</span><span class="sxs-lookup"><span data-stu-id="241dd-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-172">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-173">No</span><span class="sxs-lookup"><span data-stu-id="241dd-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-174">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="241dd-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="241dd-175">No</span><span class="sxs-lookup"><span data-stu-id="241dd-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-176">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="241dd-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-177">No</span><span class="sxs-lookup"><span data-stu-id="241dd-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-178">影響效能：</span><span class="sxs-lookup"><span data-stu-id="241dd-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="241dd-179">No</span><span class="sxs-lookup"><span data-stu-id="241dd-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-180">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="241dd-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="241dd-181">No</span><span class="sxs-lookup"><span data-stu-id="241dd-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-182">可用性：</span><span class="sxs-lookup"><span data-stu-id="241dd-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-183">全部</span><span class="sxs-lookup"><span data-stu-id="241dd-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="241dd-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="241dd-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="241dd-185">49</span><span class="sxs-lookup"><span data-stu-id="241dd-185">49</span></span>  

<span data-ttu-id="241dd-186">這個參數可以用來控制 database engine 針對其事件記錄檔訊息所使用的事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="241dd-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="241dd-187">依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="241dd-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="241dd-188">如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。</span><span class="sxs-lookup"><span data-stu-id="241dd-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-189">預設值：3</span><span class="sxs-lookup"><span data-stu-id="241dd-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-190">輸入：</span><span class="sxs-lookup"><span data-stu-id="241dd-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="241dd-191">String</span><span class="sxs-lookup"><span data-stu-id="241dd-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-192">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="241dd-193">0–259個字元</span><span class="sxs-lookup"><span data-stu-id="241dd-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-194">範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="241dd-195">執行個體</span><span class="sxs-lookup"><span data-stu-id="241dd-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-196">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-197">Yes</span><span class="sxs-lookup"><span data-stu-id="241dd-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-198">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-199">No</span><span class="sxs-lookup"><span data-stu-id="241dd-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-200">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="241dd-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="241dd-201">No</span><span class="sxs-lookup"><span data-stu-id="241dd-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-202">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="241dd-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-203">No</span><span class="sxs-lookup"><span data-stu-id="241dd-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-204">影響效能：</span><span class="sxs-lookup"><span data-stu-id="241dd-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="241dd-205">No</span><span class="sxs-lookup"><span data-stu-id="241dd-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-206">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="241dd-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="241dd-207">No</span><span class="sxs-lookup"><span data-stu-id="241dd-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-208">可用性：</span><span class="sxs-lookup"><span data-stu-id="241dd-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-209">全部</span><span class="sxs-lookup"><span data-stu-id="241dd-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="241dd-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="241dd-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="241dd-211">50</span><span class="sxs-lookup"><span data-stu-id="241dd-211">50</span></span>  

<span data-ttu-id="241dd-212">當此參數為 true 時，將會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="241dd-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-213">預設值：3</span><span class="sxs-lookup"><span data-stu-id="241dd-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="241dd-214">否</span><span class="sxs-lookup"><span data-stu-id="241dd-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-215">輸入：</span><span class="sxs-lookup"><span data-stu-id="241dd-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="241dd-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="241dd-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-217">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="241dd-218">False, True</span><span class="sxs-lookup"><span data-stu-id="241dd-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-219">範圍：</span><span class="sxs-lookup"><span data-stu-id="241dd-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="241dd-220">執行個體</span><span class="sxs-lookup"><span data-stu-id="241dd-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-221">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-222">Yes</span><span class="sxs-lookup"><span data-stu-id="241dd-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-223">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="241dd-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="241dd-224">No</span><span class="sxs-lookup"><span data-stu-id="241dd-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-225">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="241dd-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="241dd-226">No</span><span class="sxs-lookup"><span data-stu-id="241dd-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-227">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="241dd-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-228">No</span><span class="sxs-lookup"><span data-stu-id="241dd-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-229">影響效能：</span><span class="sxs-lookup"><span data-stu-id="241dd-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="241dd-230">No</span><span class="sxs-lookup"><span data-stu-id="241dd-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-231">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="241dd-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="241dd-232">No</span><span class="sxs-lookup"><span data-stu-id="241dd-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-233">可用性：</span><span class="sxs-lookup"><span data-stu-id="241dd-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="241dd-234">全部</span><span class="sxs-lookup"><span data-stu-id="241dd-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="241dd-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="241dd-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241dd-236"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="241dd-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="241dd-237">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="241dd-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241dd-238"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="241dd-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="241dd-239">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="241dd-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241dd-240"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="241dd-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="241dd-241">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="241dd-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="241dd-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="241dd-242">See Also</span></span>

[<span data-ttu-id="241dd-243">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="241dd-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="241dd-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="241dd-244">JetInit</span></span>](./jetinit-function.md)
