---
description: 深入瞭解：資料庫快取參數
title: 資料庫快取參數
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974548"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="8d0b6-103">資料庫快取參數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-103">Database Cache Parameters</span></span>


<span data-ttu-id="8d0b6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8d0b6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="8d0b6-105">資料庫快取參數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-105">Database Cache Parameters</span></span>

<span data-ttu-id="8d0b6-106">本主題包含用於資料庫快取的參數。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="8d0b6-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="8d0b6-108">22</span><span class="sxs-lookup"><span data-stu-id="8d0b6-108">22</span></span>  

<span data-ttu-id="8d0b6-109">此參數會控制資料庫頁面快取的輔助部分大小，該部分在其他情況下無法使用時，用來模擬散佈收集 i/o。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="8d0b6-110">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-110">The size is in database pages.</span></span>

<span data-ttu-id="8d0b6-111">**WINDOWS XP 和更新版本：**  此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-112">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-113">256</span><span class="sxs-lookup"><span data-stu-id="8d0b6-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-114">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-115">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-116">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-117">0、2-2147483647</span><span class="sxs-lookup"><span data-stu-id="8d0b6-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-118">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-119">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-120">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-121">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-122">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-123">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-124">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-125">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-126">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-127">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-128">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-129">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-130">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-131">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-132">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-133">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="8d0b6-135">41</span><span class="sxs-lookup"><span data-stu-id="8d0b6-135">41</span></span>  

<span data-ttu-id="8d0b6-136">這個參數可以用來控制執行時間的資料庫頁面快取大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="8d0b6-137">一般來說，快取會自動將其大小調整為資料庫和電腦活動層級的功能。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="8d0b6-138">如果應用程式將此參數設定為零，則快取會以這種方式調整其本身的大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="8d0b6-139">但是，如果應用程式將此參數設定為非零值，則快取會將其本身調整為資料庫頁面)  (的目標大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="8d0b6-140">然後，快取會將其大小保留為該閾值，直到指定新的大小或釋放它以選擇其本身的大小為止。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="8d0b6-141">**注意**  快取大小仍受限於 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所加諸的限制。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="8d0b6-142">讀取此參數時，會傳回資料庫頁面中的實際快取大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="8d0b6-143">應用程式可使用此大小做為輸入，以驅動其手動調整快取大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-144">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-145">特殊</span><span class="sxs-lookup"><span data-stu-id="8d0b6-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-146">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-147">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-148">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-149"><strong>Windows 2000：</strong>  1 –1048575</span><span class="sxs-lookup"><span data-stu-id="8d0b6-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="8d0b6-150"><strong>WINDOWS XP：</strong>  1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-151">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-152">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-153">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-154">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-155">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-156">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-157">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-158">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-159">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-160">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-161">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-162">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-163">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-164">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-165">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-166">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="8d0b6-168">60</span><span class="sxs-lookup"><span data-stu-id="8d0b6-168">60</span></span>  

<span data-ttu-id="8d0b6-169">此參數會設定資料庫頁面快取的大小下限。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="8d0b6-170">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-170">The size is in database pages.</span></span>

<span data-ttu-id="8d0b6-171">根據預設，資料庫快取會在 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所設定的限制之間自動調整其大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="8d0b6-172">**Windows 2000：**  在 Windows 2000 上，此參數的值應該設定為大約等於四倍的執行緒數目，這些執行緒會同時位於 ESE API 內。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="8d0b6-173">這是為了避免資料庫頁面快取緩衝區數目不足所造成的鎖死，以執行像 B + 樹狀結構分割的複雜作業。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="8d0b6-174">**WINDOWS XP 和更新版本：**  快取管理員會自動設定自己的最小快取大小，以避免鎖死。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-175">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-176"><strong>Windows 2000：</strong>  64</span><span class="sxs-lookup"><span data-stu-id="8d0b6-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="8d0b6-177"><strong>WINDOWS XP：</strong>  1</span><span class="sxs-lookup"><span data-stu-id="8d0b6-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-178">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-179">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-180">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-181"><strong>Windows 2000：</strong>  1 –1048575</span><span class="sxs-lookup"><span data-stu-id="8d0b6-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="8d0b6-182"><strong>WINDOWS XP：</strong>  1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-183">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-184">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-185">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-186"><strong>Windows 2000：</strong>  不</span><span class="sxs-lookup"><span data-stu-id="8d0b6-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="8d0b6-187"><strong>WINDOWS XP：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="8d0b6-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-188">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-189"><strong>Windows 2000：</strong>  不</span><span class="sxs-lookup"><span data-stu-id="8d0b6-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="8d0b6-190"><strong>WINDOWS XP：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="8d0b6-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-191">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-192">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-193">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-194">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-195">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-196">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-197">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-198">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-199">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-200">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="8d0b6-202">23</span><span class="sxs-lookup"><span data-stu-id="8d0b6-202">23</span></span>  

<span data-ttu-id="8d0b6-203">此參數會設定資料庫頁面快取的大小上限。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="8d0b6-204">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-204">The size is in database pages.</span></span>

<span data-ttu-id="8d0b6-205">根據預設，資料庫快取會在 **JET_paramCacheSizeMin** 和 **JET_paramCacheSizeMax** 所設定的限制之間自動調整其大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="8d0b6-206">**注意**   如果此參數保留為其預設值，則在呼叫 [JetInit](./jetinit-function.md) 時，會將快取的大小上限設定為實體記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="8d0b6-207">**Windows Vista：**  在 Windows Vista 中，此參數的預設值已變更，以闡明此行為。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-208">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-209"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  512</span><span class="sxs-lookup"><span data-stu-id="8d0b6-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="8d0b6-210"><strong>Windows Vista：</strong>  2000000000</span><span class="sxs-lookup"><span data-stu-id="8d0b6-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-211">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-212">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-213">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-214"><strong>Windows 2000：</strong>  1 –1048575</span><span class="sxs-lookup"><span data-stu-id="8d0b6-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="8d0b6-215"><strong>WINDOWS XP：</strong>  1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-216">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-217">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-218">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-219"><strong>Windows 2000：</strong>  不</span><span class="sxs-lookup"><span data-stu-id="8d0b6-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="8d0b6-220"><strong>WINDOWS XP：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="8d0b6-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-221">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-222"><strong>WINDOWS XP 和 windows 2000：</strong>  不</span><span class="sxs-lookup"><span data-stu-id="8d0b6-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="8d0b6-223"><strong>Windows Vista 和 Windows Server 2003：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="8d0b6-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-224">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-225">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-226">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-227">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-228">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-229">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-230">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-231">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-232">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-233">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="8d0b6-235">24</span><span class="sxs-lookup"><span data-stu-id="8d0b6-235">24</span></span> 

<span data-ttu-id="8d0b6-236">此參數會控制從資料庫頁面快取清除資料庫頁面的方式，以將從損毀復原所需的時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="8d0b6-237">參數是一種閾值，以位元組為單位，表示在損毀之後必須重新執行的交易記錄檔數目。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="8d0b6-238">如果使用 [JET_paramCircularLog](./transaction-log-parameters.md) 啟用迴圈記錄，此參數也會控制要保留在磁片上的交易記錄檔大約數量。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="8d0b6-239">此參數的設定必須太低。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="8d0b6-240">因為這個參數的值接近零，所以快取在將資料庫頁面排清至磁片時，會變得越來越多。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="8d0b6-241">這並不只會導致資料庫檔案的寫入數目增加，也會間接造成這些檔案的讀取次數增加。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="8d0b6-242">在某些情況下，這可能會造成極大的效能問題。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="8d0b6-243">可惜的是，為此參數設定最小的最佳值只能透過目標應用程式的實驗來完成。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-244">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-245">20971520</span><span class="sxs-lookup"><span data-stu-id="8d0b6-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-246">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-247">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-248">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-249"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  0 –2147483647</span><span class="sxs-lookup"><span data-stu-id="8d0b6-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="8d0b6-250"><strong>Windows Vista：</strong>  所有值</span><span class="sxs-lookup"><span data-stu-id="8d0b6-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-251">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-252"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong> 此參數為 global。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="8d0b6-253"><strong>Windows Vista：</strong>  此參數為每個實例。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-254">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-255">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-256">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-257">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-258">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-259">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-260">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-261">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-262">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-263">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-264">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-265">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-266">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-267">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="8d0b6-269">135</span><span class="sxs-lookup"><span data-stu-id="8d0b6-269">135</span></span>  

<span data-ttu-id="8d0b6-270">此參數會控制資料庫引擎將用來排清修改過的資料庫頁面，以使檢查點前進的最大並行寫入數目。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="8d0b6-271">此參數的值可用來平衡檢查點的速度，以及此進程對保存資料庫的磁片之其他 i/o 作業的回應時間所造成的負面影響。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-272">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-273">96</span><span class="sxs-lookup"><span data-stu-id="8d0b6-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-274">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-275">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-276">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-277">8–1024</span><span class="sxs-lookup"><span data-stu-id="8d0b6-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-278">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-279">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-280">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-281">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-282">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-283">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-284">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-285">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-286">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-287">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-288">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-289">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-290">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-291">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-292">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-293">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8d0b6-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="8d0b6-295">127</span><span class="sxs-lookup"><span data-stu-id="8d0b6-295">127</span></span>  

<span data-ttu-id="8d0b6-296">當此參數為 **True** 時，資料庫引擎將直接從 Windows 檔案快取使用資料庫資料，而不是將快取的資料複製到它自己的私用記憶體中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="8d0b6-297">任何修改過的資料庫資料仍會快取在私用記憶體中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="8d0b6-298">這種模式的目的是要進一步減少 database engine 用來快取資料庫資料的私用記憶體量。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="8d0b6-299">只有在使用 Windows 檔案快取時，您可以將 JET_paramEnableFileCache 設定為 **True**，才能使用 view cache。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-300">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-301">否</span><span class="sxs-lookup"><span data-stu-id="8d0b6-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-302">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="8d0b6-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-304">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-305">False, True</span><span class="sxs-lookup"><span data-stu-id="8d0b6-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-306">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-307">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-308">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-309">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-310">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-311">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-312">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-313">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-314">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-315">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-316">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-317">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-318">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-319">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-320">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-321">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="8d0b6-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="8d0b6-323">25</span><span class="sxs-lookup"><span data-stu-id="8d0b6-323">25</span></span>  

<span data-ttu-id="8d0b6-324">此參數會設定以微秒為單位的時間間隔，這會將兩個資料庫頁面存取視為相互關聯。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="8d0b6-325">此相互關聯間隔可控制快取頁面取代演算法的敏感度， (LRU-K) 至後續的頁面存取。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="8d0b6-326">接著，這會影響其選擇要保持快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-327">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-328">128000</span><span class="sxs-lookup"><span data-stu-id="8d0b6-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-329">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-330">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-331">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-332"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>    0 –2147483647</span><span class="sxs-lookup"><span data-stu-id="8d0b6-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="8d0b6-333"><strong>Windows Vista：</strong>  所有值</span><span class="sxs-lookup"><span data-stu-id="8d0b6-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-334">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-335">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-336">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-337">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-338">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-339">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-340">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-341">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-342">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-343">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-344">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-345">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-346">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-347">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-348">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-349">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="8d0b6-351">26</span><span class="sxs-lookup"><span data-stu-id="8d0b6-351">26</span></span>  

<span data-ttu-id="8d0b6-352">此參數會設定將保留資料庫頁面存取時間的非快取資料庫頁面數目上限。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="8d0b6-353">這些記錄可讓快取的頁面取代演算法 (LRU-K) ，更精確地偵測錯誤地從資料庫頁面快取中收回的熱門頁面。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="8d0b6-354">**WINDOWS XP 和 Windows Server 2003：**  Windows XP 和 Windows Server 2003 會忽略此參數，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-355">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-356"><strong>Windows 2000：</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="8d0b6-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="8d0b6-357"><strong>Windows Vista：</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="8d0b6-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-358">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-359">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-360">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-361"><strong>Windows 2000：</strong>  0 –4194303</span><span class="sxs-lookup"><span data-stu-id="8d0b6-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="8d0b6-362"><strong>Windows Vista：</strong>  所有值</span><span class="sxs-lookup"><span data-stu-id="8d0b6-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-363">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-364">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-365">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-366">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-367">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-368">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-369">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-370">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-371">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-372">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-373">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-374">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-375">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-376">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-377">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-378">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="8d0b6-380">27</span><span class="sxs-lookup"><span data-stu-id="8d0b6-380">27</span></span>  

<span data-ttu-id="8d0b6-381">此參數會設定視為用來判斷頁面實用性的資料庫頁面存取數目。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="8d0b6-382">此參數基本上是 LRU-K 中的 K，也就是資料庫頁面快取的頁面取代演算法。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-383">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-384">2</span><span class="sxs-lookup"><span data-stu-id="8d0b6-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-385">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-386">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-387">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-388">1 - 2</span><span class="sxs-lookup"><span data-stu-id="8d0b6-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-389">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-390">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-391">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-392">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-393">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-394">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-395">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-396">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-397">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-398">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-399">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-400">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-401">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-402">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-403">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-404">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="8d0b6-406">28</span><span class="sxs-lookup"><span data-stu-id="8d0b6-406">28</span></span>

<span data-ttu-id="8d0b6-407">此參數表示以秒為單位的時間間隔，在這段時間之後，資料庫頁面快取中的頁面會被視為已遺失頁面存取權，目的是考慮頁面的實用性。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-408">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-409">100</span><span class="sxs-lookup"><span data-stu-id="8d0b6-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-410">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-411">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-412">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-413"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  1 –2147483647</span><span class="sxs-lookup"><span data-stu-id="8d0b6-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="8d0b6-414"><strong>Windows Vista：</strong>   1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-415">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-416">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-417">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-418">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-419">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-420">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-421">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-422">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-423">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-424">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-425">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-426">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-427">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-428">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-429">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-430">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="8d0b6-432">29</span><span class="sxs-lookup"><span data-stu-id="8d0b6-432">29</span></span>  

<span data-ttu-id="8d0b6-433">此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="8d0b6-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="8d0b6-435">31</span><span class="sxs-lookup"><span data-stu-id="8d0b6-435">31</span></span>  

<span data-ttu-id="8d0b6-436">此參數會控制當資料庫頁面快取開始從快取收回頁面，以騰出空間給未快取的頁面時。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="8d0b6-437">當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="8d0b6-438">此臨界值一律相對於 **JET_paramCacheSizeMax** 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="8d0b6-439">此臨界值也必須小於 **JET_paramStopFlushThreshold** 所設定的停止閾值。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="8d0b6-440">開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="8d0b6-441">高啟動臨界值可讓背景進程更有時間回應。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="8d0b6-442">不過，高啟動閾值表示較高的停止閾值，而且會減少修改過的頁面的資料庫頁面快取大小 (Windows 2000) 或 (Windows XP 及更新版本) 的所有頁面。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-443">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-444"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  5 (1% ) </span><span class="sxs-lookup"><span data-stu-id="8d0b6-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="8d0b6-445"><strong>Windows Vista：</strong>  20000000 (1% ) </span><span class="sxs-lookup"><span data-stu-id="8d0b6-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-446">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-447">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-448">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-449"><strong>Windows 2000：</strong>  1 –1048575</span><span class="sxs-lookup"><span data-stu-id="8d0b6-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="8d0b6-450"><strong>WINDOWS XP：</strong>  1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="8d0b6-451"><strong>Windows Vista：</strong>  所有值</span><span class="sxs-lookup"><span data-stu-id="8d0b6-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-452">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-453">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-454">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-455">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-456">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-457">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-458">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-459">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-460">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-461">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-462">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-463">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-464">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-465">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-466">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-467">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d0b6-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="8d0b6-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="8d0b6-469">32</span><span class="sxs-lookup"><span data-stu-id="8d0b6-469">32</span></span>  

<span data-ttu-id="8d0b6-470">此參數會控制資料庫頁面快取何時結束從快取收回頁面，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="8d0b6-471">當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="8d0b6-472">此臨界值一律相對於 **JET_paramCacheSizeMax** 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="8d0b6-473">此臨界值也必須大於 **JET_paramStartFlushThreshold** 所設定的 [開始] 閾值。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="8d0b6-474">開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="8d0b6-475">較大的間距將可讓您更有可能合併對相鄰頁面的寫入。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="8d0b6-476">不過，高停止閾值會減少修改過的頁面的資料庫頁面快取大小 (Windows 2000) 或 (Windows XP 及更新版本) 的所有頁面。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-477">預設值：3</span><span class="sxs-lookup"><span data-stu-id="8d0b6-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-478"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  10 (2% ) </span><span class="sxs-lookup"><span data-stu-id="8d0b6-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="8d0b6-479"><strong>Windows Vista：</strong>  40000000 (2% ) </span><span class="sxs-lookup"><span data-stu-id="8d0b6-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-480">輸入：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-481">整數</span><span class="sxs-lookup"><span data-stu-id="8d0b6-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-482">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-483"><strong>Windows 2000：</strong>  1 –1048575</span><span class="sxs-lookup"><span data-stu-id="8d0b6-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="8d0b6-484"><strong>WINDOWS XP：</strong>  1-4294967295</span><span class="sxs-lookup"><span data-stu-id="8d0b6-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="8d0b6-485"><strong>Windows Vista：</strong>  所有值</span><span class="sxs-lookup"><span data-stu-id="8d0b6-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-486">範圍：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-487">全球</span><span class="sxs-lookup"><span data-stu-id="8d0b6-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-488">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-489">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-490">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-491">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-492">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-493">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-494">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-495">No</span><span class="sxs-lookup"><span data-stu-id="8d0b6-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-496">影響效能：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-497">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-498">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-499">Yes</span><span class="sxs-lookup"><span data-stu-id="8d0b6-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-500">可用性：</span><span class="sxs-lookup"><span data-stu-id="8d0b6-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="8d0b6-501">全部</span><span class="sxs-lookup"><span data-stu-id="8d0b6-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8d0b6-502">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d0b6-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-503"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8d0b6-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8d0b6-504">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d0b6-505"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8d0b6-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8d0b6-506">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d0b6-507"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8d0b6-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8d0b6-508">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8d0b6-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8d0b6-509">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d0b6-509">See Also</span></span>

[<span data-ttu-id="8d0b6-510">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="8d0b6-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="8d0b6-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="8d0b6-511">JetInit</span></span>](./jetinit-function.md)
