---
description: 深入瞭解：備份和還原參數
title: 備份和還原參數
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514072"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="d49da-103">備份和還原參數</span><span class="sxs-lookup"><span data-stu-id="d49da-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="d49da-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d49da-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="d49da-105">備份和還原參數</span><span class="sxs-lookup"><span data-stu-id="d49da-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="d49da-106">本主題包含用於備份和還原的參數。</span><span class="sxs-lookup"><span data-stu-id="d49da-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="d49da-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="d49da-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="d49da-108">113</span><span class="sxs-lookup"><span data-stu-id="d49da-108">113</span></span>  

<span data-ttu-id="d49da-109">在執行時間，會將每個資料庫的完整路徑保存在交易記錄中。</span><span class="sxs-lookup"><span data-stu-id="d49da-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="d49da-110">一般來說，這些資料庫必須保留在原始位置，才能讓交易重新執行正常運作。</span><span class="sxs-lookup"><span data-stu-id="d49da-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="d49da-111">這個參數可以用來強制損毀復原或還原作業，以便在指定的資料夾中，尋找交易記錄中所參考的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d49da-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-112">預設值：3</span><span class="sxs-lookup"><span data-stu-id="d49da-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="d49da-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="d49da-114">資料夾路徑 (字串) </span><span class="sxs-lookup"><span data-stu-id="d49da-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-115">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d49da-116">0–246個字元</span><span class="sxs-lookup"><span data-stu-id="d49da-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-117">範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d49da-118">執行個體</span><span class="sxs-lookup"><span data-stu-id="d49da-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-119">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-120">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-121">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-122">No</span><span class="sxs-lookup"><span data-stu-id="d49da-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-123">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="d49da-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d49da-124">No</span><span class="sxs-lookup"><span data-stu-id="d49da-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-125">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="d49da-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-126">No</span><span class="sxs-lookup"><span data-stu-id="d49da-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-127">影響效能：</span><span class="sxs-lookup"><span data-stu-id="d49da-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d49da-128">No</span><span class="sxs-lookup"><span data-stu-id="d49da-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-129">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="d49da-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d49da-130">No</span><span class="sxs-lookup"><span data-stu-id="d49da-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-131">可用性：</span><span class="sxs-lookup"><span data-stu-id="d49da-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-132">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d49da-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d49da-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="d49da-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="d49da-134">77</span><span class="sxs-lookup"><span data-stu-id="d49da-134">77</span></span>  

<span data-ttu-id="d49da-135">此參數可控制當資料庫引擎設定為在磁片上的交易記錄檔，與設定的大小不同時， [JetInit](./jetinit-function.md) 的結果。</span><span class="sxs-lookup"><span data-stu-id="d49da-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="d49da-136">一般來說， [JetInit](./jetinit-function.md) 會成功復原資料庫，但會失敗，並 JET_errLogFileSizeMismatchDatabasesConsistent 指出記錄檔大小設定不正確。</span><span class="sxs-lookup"><span data-stu-id="d49da-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="d49da-137">但是，當這個參數設定為 true 時，資料庫引擎將會以無訊息模式刪除所有舊的記錄檔、使用設定的記錄檔大小來啟動一組新的交易記錄檔，然後再傳回 JET_errSuccess。</span><span class="sxs-lookup"><span data-stu-id="d49da-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="d49da-138">當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。</span><span class="sxs-lookup"><span data-stu-id="d49da-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-139">預設值：3</span><span class="sxs-lookup"><span data-stu-id="d49da-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d49da-140">否</span><span class="sxs-lookup"><span data-stu-id="d49da-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-141">輸入：</span><span class="sxs-lookup"><span data-stu-id="d49da-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="d49da-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="d49da-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-143">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d49da-144">False, True</span><span class="sxs-lookup"><span data-stu-id="d49da-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-145">範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d49da-146">執行個體</span><span class="sxs-lookup"><span data-stu-id="d49da-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-147">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-148">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-149">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-150">No</span><span class="sxs-lookup"><span data-stu-id="d49da-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-151">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="d49da-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d49da-152">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-153">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="d49da-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-154">No</span><span class="sxs-lookup"><span data-stu-id="d49da-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-155">影響效能：</span><span class="sxs-lookup"><span data-stu-id="d49da-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d49da-156">No</span><span class="sxs-lookup"><span data-stu-id="d49da-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-157">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="d49da-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d49da-158">No</span><span class="sxs-lookup"><span data-stu-id="d49da-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-159">可用性：</span><span class="sxs-lookup"><span data-stu-id="d49da-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-160">全部</span><span class="sxs-lookup"><span data-stu-id="d49da-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d49da-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="d49da-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="d49da-162">52</span><span class="sxs-lookup"><span data-stu-id="d49da-162">52</span></span>  

<span data-ttu-id="d49da-163">當此參數為 true 時， [JetInit](./jetinit-function.md)就會刪除在磁片上找到的任何非目前記錄檔順序的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d49da-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="d49da-164">這可用來在還原作業之後，自動清除多餘的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d49da-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="d49da-165">**WINDOWS XP：**  在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="d49da-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-166">預設值：3</span><span class="sxs-lookup"><span data-stu-id="d49da-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d49da-167">否</span><span class="sxs-lookup"><span data-stu-id="d49da-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-168">輸入：</span><span class="sxs-lookup"><span data-stu-id="d49da-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="d49da-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="d49da-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-170">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d49da-171">False, True</span><span class="sxs-lookup"><span data-stu-id="d49da-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-172">範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d49da-173">執行個體</span><span class="sxs-lookup"><span data-stu-id="d49da-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-174">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-175">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-176">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-177">No</span><span class="sxs-lookup"><span data-stu-id="d49da-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-178">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="d49da-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d49da-179">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-180">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="d49da-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-181">No</span><span class="sxs-lookup"><span data-stu-id="d49da-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-182">影響效能：</span><span class="sxs-lookup"><span data-stu-id="d49da-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d49da-183">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-184">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="d49da-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d49da-185">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-186">可用性：</span><span class="sxs-lookup"><span data-stu-id="d49da-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-187">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d49da-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d49da-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="d49da-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="d49da-189">82</span><span class="sxs-lookup"><span data-stu-id="d49da-189">82</span></span>  

<span data-ttu-id="d49da-190">此參數會設定在發生超時之前呼叫 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 之間允許的時間量。</span><span class="sxs-lookup"><span data-stu-id="d49da-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="d49da-191">如需詳細資訊，請參閱 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="d49da-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="d49da-192">Timeout 是以毫秒為單位。</span><span class="sxs-lookup"><span data-stu-id="d49da-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-193">預設值：3</span><span class="sxs-lookup"><span data-stu-id="d49da-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d49da-194">20000 (Windows XP 和 Windows Server 2003) ;</span><span class="sxs-lookup"><span data-stu-id="d49da-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="d49da-195">70000 (Windows Server 2003 SP1) </span><span class="sxs-lookup"><span data-stu-id="d49da-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-196">輸入：</span><span class="sxs-lookup"><span data-stu-id="d49da-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="d49da-197">整數</span><span class="sxs-lookup"><span data-stu-id="d49da-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-198">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d49da-199">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="d49da-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-200">範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d49da-201">全球</span><span class="sxs-lookup"><span data-stu-id="d49da-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-202">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-203">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-204">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-205">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-206">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="d49da-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d49da-207">No</span><span class="sxs-lookup"><span data-stu-id="d49da-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-208">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="d49da-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-209">No</span><span class="sxs-lookup"><span data-stu-id="d49da-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-210">影響效能：</span><span class="sxs-lookup"><span data-stu-id="d49da-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d49da-211">No</span><span class="sxs-lookup"><span data-stu-id="d49da-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-212">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="d49da-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d49da-213">No</span><span class="sxs-lookup"><span data-stu-id="d49da-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-214">可用性：</span><span class="sxs-lookup"><span data-stu-id="d49da-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-215">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d49da-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d49da-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="d49da-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="d49da-217">71</span><span class="sxs-lookup"><span data-stu-id="d49da-217">71</span></span>  

<span data-ttu-id="d49da-218">當此參數為 true 時，資料庫中正在進行串流備份的每個頁面將會清除已刪除的資料。</span><span class="sxs-lookup"><span data-stu-id="d49da-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="d49da-219">請務必注意，要清除的資料庫頁面是在磁片上。</span><span class="sxs-lookup"><span data-stu-id="d49da-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="d49da-220">在清除程式之前，會備份完整的資料集。</span><span class="sxs-lookup"><span data-stu-id="d49da-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-221">預設值：3</span><span class="sxs-lookup"><span data-stu-id="d49da-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="d49da-222">否</span><span class="sxs-lookup"><span data-stu-id="d49da-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-223">輸入：</span><span class="sxs-lookup"><span data-stu-id="d49da-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="d49da-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="d49da-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-225">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="d49da-226">False, True</span><span class="sxs-lookup"><span data-stu-id="d49da-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-227">範圍：</span><span class="sxs-lookup"><span data-stu-id="d49da-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="d49da-228">執行個體</span><span class="sxs-lookup"><span data-stu-id="d49da-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-229">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-230">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-231">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="d49da-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="d49da-232">No</span><span class="sxs-lookup"><span data-stu-id="d49da-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-233">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="d49da-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="d49da-234">No</span><span class="sxs-lookup"><span data-stu-id="d49da-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-235">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="d49da-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-236">No</span><span class="sxs-lookup"><span data-stu-id="d49da-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-237">影響效能：</span><span class="sxs-lookup"><span data-stu-id="d49da-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="d49da-238">Yes</span><span class="sxs-lookup"><span data-stu-id="d49da-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-239">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="d49da-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="d49da-240">No</span><span class="sxs-lookup"><span data-stu-id="d49da-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-241">可用性：</span><span class="sxs-lookup"><span data-stu-id="d49da-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="d49da-242">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="d49da-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d49da-243">規格需求</span><span class="sxs-lookup"><span data-stu-id="d49da-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d49da-244"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d49da-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d49da-245">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="d49da-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d49da-246"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d49da-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d49da-247">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="d49da-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d49da-248"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d49da-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d49da-249">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d49da-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d49da-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d49da-250">See Also</span></span>

[<span data-ttu-id="d49da-251">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="d49da-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="d49da-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="d49da-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="d49da-253">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="d49da-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="d49da-254">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="d49da-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
