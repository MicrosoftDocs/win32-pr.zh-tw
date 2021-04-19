---
description: 深入瞭解：中繼參數
title: 中繼參數
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986314"
---
# <a name="meta-parameters"></a><span data-ttu-id="8f29c-103">中繼參數</span><span class="sxs-lookup"><span data-stu-id="8f29c-103">Meta Parameters</span></span>


<span data-ttu-id="8f29c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8f29c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="8f29c-105">中繼參數</span><span class="sxs-lookup"><span data-stu-id="8f29c-105">Meta Parameters</span></span>

<span data-ttu-id="8f29c-106">本主題包含用來控制其他參數的參數。</span><span class="sxs-lookup"><span data-stu-id="8f29c-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="8f29c-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f29c-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="8f29c-108">129</span><span class="sxs-lookup"><span data-stu-id="8f29c-108">129</span></span>  
<span data-ttu-id="8f29c-109">此參數會針對整組系統參數公開多組預設值。</span><span class="sxs-lookup"><span data-stu-id="8f29c-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="8f29c-110">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="8f29c-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="8f29c-111">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="8f29c-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="8f29c-112">此外，參數本身也可能對資料庫引擎的行為產生其他影響。</span><span class="sxs-lookup"><span data-stu-id="8f29c-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="8f29c-113">目前有兩個支援的設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="8f29c-114">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="8f29c-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="8f29c-115">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="8f29c-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="8f29c-116">Small Configuration 會將下列系統參數的預設值變更為指定的值：</span><span class="sxs-lookup"><span data-stu-id="8f29c-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8f29c-117">系統參數</span><span class="sxs-lookup"><span data-stu-id="8f29c-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="8f29c-118">新的預設值</span><span class="sxs-lookup"><span data-stu-id="8f29c-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="8f29c-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="8f29c-120">30000</span><span class="sxs-lookup"><span data-stu-id="8f29c-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="8f29c-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="8f29c-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="8f29c-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="8f29c-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="8f29c-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="8f29c-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="8f29c-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="8f29c-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="8f29c-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="8f29c-130">64</span><span class="sxs-lookup"><span data-stu-id="8f29c-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="8f29c-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="8f29c-132">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="8f29c-134">16</span><span class="sxs-lookup"><span data-stu-id="8f29c-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="8f29c-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="8f29c-136">14</span><span class="sxs-lookup"><span data-stu-id="8f29c-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="8f29c-138">16</span><span class="sxs-lookup"><span data-stu-id="8f29c-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="8f29c-140">65536</span><span class="sxs-lookup"><span data-stu-id="8f29c-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="8f29c-142">10</span><span class="sxs-lookup"><span data-stu-id="8f29c-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="8f29c-144">16</span><span class="sxs-lookup"><span data-stu-id="8f29c-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="8f29c-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="8f29c-146">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="8f29c-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="8f29c-148">2</span><span class="sxs-lookup"><span data-stu-id="8f29c-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="8f29c-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="8f29c-150">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="8f29c-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="8f29c-152">16</span><span class="sxs-lookup"><span data-stu-id="8f29c-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="8f29c-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="8f29c-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="8f29c-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="8f29c-156">0</span><span class="sxs-lookup"><span data-stu-id="8f29c-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="8f29c-158">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="8f29c-160">32</span><span class="sxs-lookup"><span data-stu-id="8f29c-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="8f29c-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="8f29c-162">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="8f29c-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="8f29c-164">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="8f29c-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="8f29c-166">1</span><span class="sxs-lookup"><span data-stu-id="8f29c-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="8f29c-168">1024</span><span class="sxs-lookup"><span data-stu-id="8f29c-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="8f29c-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="8f29c-170">0</span><span class="sxs-lookup"><span data-stu-id="8f29c-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="8f29c-172">8</span><span class="sxs-lookup"><span data-stu-id="8f29c-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f29c-173">Small Configuration 也有其他對資料庫引擎的影響，包括：</span><span class="sxs-lookup"><span data-stu-id="8f29c-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="8f29c-174">系統參數所管理的所有資源都會視需要從堆積進行配置</span><span class="sxs-lookup"><span data-stu-id="8f29c-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="8f29c-175">資料庫引擎所使用的其他內部資源大小縮小</span><span class="sxs-lookup"><span data-stu-id="8f29c-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="8f29c-176">將各種維護活動調整回來以避免背景執行緒活動</span><span class="sxs-lookup"><span data-stu-id="8f29c-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-177">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8f29c-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-178">1 (舊版) </span><span class="sxs-lookup"><span data-stu-id="8f29c-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-179">輸入：</span><span class="sxs-lookup"><span data-stu-id="8f29c-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-180">整數</span><span class="sxs-lookup"><span data-stu-id="8f29c-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-181">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8f29c-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-182">0-1</span><span class="sxs-lookup"><span data-stu-id="8f29c-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-183">範圍：</span><span class="sxs-lookup"><span data-stu-id="8f29c-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-184">執行個體</span><span class="sxs-lookup"><span data-stu-id="8f29c-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-185">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-186">Yes</span><span class="sxs-lookup"><span data-stu-id="8f29c-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-187">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-188">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-189">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8f29c-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-190">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-191">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8f29c-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-192">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-193">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8f29c-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-194">Yes</span><span class="sxs-lookup"><span data-stu-id="8f29c-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-195">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8f29c-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-196">Yes</span><span class="sxs-lookup"><span data-stu-id="8f29c-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-197">可用性：</span><span class="sxs-lookup"><span data-stu-id="8f29c-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-198">從 Windows Server 2008 和 Windows Vista 開始</span><span class="sxs-lookup"><span data-stu-id="8f29c-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8f29c-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="8f29c-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="8f29c-200">130</span><span class="sxs-lookup"><span data-stu-id="8f29c-200">130</span></span>  
<span data-ttu-id="8f29c-201">這個參數是用來控制 database engine 接受或拒絕系統參數子集之變更的時間。</span><span class="sxs-lookup"><span data-stu-id="8f29c-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="8f29c-202">此參數會搭配 JET_paramConfiguration 使用，以防止某些系統參數從選取的設定的預設值中移除。</span><span class="sxs-lookup"><span data-stu-id="8f29c-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="8f29c-203">當此參數設定為 False 時，將會保護下列系統參數，不要設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="8f29c-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="8f29c-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="8f29c-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="8f29c-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="8f29c-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="8f29c-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="8f29c-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="8f29c-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="8f29c-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="8f29c-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="8f29c-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="8f29c-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="8f29c-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="8f29c-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="8f29c-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="8f29c-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="8f29c-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="8f29c-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="8f29c-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="8f29c-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="8f29c-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="8f29c-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="8f29c-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="8f29c-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="8f29c-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="8f29c-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="8f29c-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="8f29c-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="8f29c-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="8f29c-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="8f29c-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="8f29c-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="8f29c-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="8f29c-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="8f29c-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="8f29c-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="8f29c-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="8f29c-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="8f29c-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="8f29c-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="8f29c-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="8f29c-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="8f29c-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="8f29c-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="8f29c-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="8f29c-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="8f29c-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="8f29c-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="8f29c-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="8f29c-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="8f29c-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="8f29c-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="8f29c-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="8f29c-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="8f29c-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="8f29c-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="8f29c-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="8f29c-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="8f29c-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="8f29c-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="8f29c-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="8f29c-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="8f29c-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="8f29c-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-244">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8f29c-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-245">對</span><span class="sxs-lookup"><span data-stu-id="8f29c-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-246">輸入：</span><span class="sxs-lookup"><span data-stu-id="8f29c-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="8f29c-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-248">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8f29c-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-249">False, True</span><span class="sxs-lookup"><span data-stu-id="8f29c-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-250">範圍：</span><span class="sxs-lookup"><span data-stu-id="8f29c-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-251">執行個體</span><span class="sxs-lookup"><span data-stu-id="8f29c-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-252">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-253">Yes</span><span class="sxs-lookup"><span data-stu-id="8f29c-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-254">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8f29c-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-255">Yes</span><span class="sxs-lookup"><span data-stu-id="8f29c-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-256">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8f29c-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-257">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-258">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8f29c-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-259">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-260">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8f29c-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-261">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-262">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8f29c-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-263">No</span><span class="sxs-lookup"><span data-stu-id="8f29c-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-264">可用性：</span><span class="sxs-lookup"><span data-stu-id="8f29c-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8f29c-265">從 Windows Server 2008 和 Windows Vista 開始</span><span class="sxs-lookup"><span data-stu-id="8f29c-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8f29c-266">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f29c-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-267"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8f29c-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8f29c-268">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="8f29c-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f29c-269"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8f29c-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8f29c-270">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="8f29c-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f29c-271"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8f29c-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8f29c-272">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8f29c-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8f29c-273">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f29c-273">See Also</span></span>

[<span data-ttu-id="8f29c-274">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="8f29c-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="8f29c-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="8f29c-275">JetInit</span></span>](./jetinit-function.md)
