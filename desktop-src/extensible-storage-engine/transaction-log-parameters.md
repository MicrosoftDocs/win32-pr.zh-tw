---
description: 深入瞭解：交易記錄參數
title: 交易記錄檔參數
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997856"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="868aa-103">交易記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="868aa-103">Transaction Log Parameters</span></span>


<span data-ttu-id="868aa-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="868aa-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="868aa-105">**本文內容**</span><span class="sxs-lookup"><span data-stu-id="868aa-105">**In this article**</span></span>  
<span data-ttu-id="868aa-106">交易記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="868aa-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="868aa-107">需求</span><span class="sxs-lookup"><span data-stu-id="868aa-107">Requirements</span></span>  
<span data-ttu-id="868aa-108">另請參閱</span><span class="sxs-lookup"><span data-stu-id="868aa-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="868aa-109">交易記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="868aa-109">Transaction Log Parameters</span></span>

<span data-ttu-id="868aa-110">本主題包含用於交易記錄的參數。</span><span class="sxs-lookup"><span data-stu-id="868aa-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="868aa-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="868aa-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="868aa-112">3</span><span class="sxs-lookup"><span data-stu-id="868aa-112">3</span></span>  

<span data-ttu-id="868aa-113">此參數會設定用於資料庫引擎所使用之許多檔案的三個字母前置詞。</span><span class="sxs-lookup"><span data-stu-id="868aa-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="868aa-114">例如，檢查點檔案稱為「EDB」。因為 EDB 是預設的基底名稱，所以預設為使用 .CHK。</span><span class="sxs-lookup"><span data-stu-id="868aa-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="868aa-115">基底名稱可以用來輕鬆區分屬於不同實例或不同應用程式的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="868aa-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-116">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-117">&quot;edb.log&quot;</span><span class="sxs-lookup"><span data-stu-id="868aa-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-118">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-119">String</span><span class="sxs-lookup"><span data-stu-id="868aa-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-120">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-121">3個字元</span><span class="sxs-lookup"><span data-stu-id="868aa-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-122">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-123">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-124">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-125">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-126">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-127">No</span><span class="sxs-lookup"><span data-stu-id="868aa-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-128">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-129">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-130">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-131">No</span><span class="sxs-lookup"><span data-stu-id="868aa-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-132">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-133">No</span><span class="sxs-lookup"><span data-stu-id="868aa-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-134">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-135">No</span><span class="sxs-lookup"><span data-stu-id="868aa-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-136">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-137">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="868aa-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="868aa-139">17</span><span class="sxs-lookup"><span data-stu-id="868aa-139">17</span></span>  

<span data-ttu-id="868aa-140">此參數會設定資料庫引擎管理交易記錄檔的方式。</span><span class="sxs-lookup"><span data-stu-id="868aa-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="868aa-141">當迴圈記錄關閉時，所產生的所有交易記錄檔都會保留在磁片上，直到不再需要該檔案，因為已執行資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="868aa-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="868aa-142">在此模式中，您可以從較舊的備份進行還原，並在所有保留的交易記錄檔中向前播放，如此一來，萬一發生強制還原的損毀，就不會遺失任何資料。</span><span class="sxs-lookup"><span data-stu-id="868aa-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="868aa-143">需要定期完整備份，以防止磁片填滿交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="868aa-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="868aa-144">當迴圈記錄開啟時，只有小於目前檢查點的交易記錄檔會保留在磁片上。</span><span class="sxs-lookup"><span data-stu-id="868aa-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="868aa-145">這種模式的好處是，備份不需要淘汰舊的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="868aa-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="868aa-146">缺點是已不再有零的資料遺失還原。</span><span class="sxs-lookup"><span data-stu-id="868aa-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-147">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-148">否</span><span class="sxs-lookup"><span data-stu-id="868aa-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-149">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="868aa-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-151">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-152">False, True</span><span class="sxs-lookup"><span data-stu-id="868aa-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-153">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-154">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-155">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-156">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-157">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-158">No</span><span class="sxs-lookup"><span data-stu-id="868aa-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-159">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-160">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-161">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-162">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-163">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-164">No</span><span class="sxs-lookup"><span data-stu-id="868aa-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-165">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-166">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-167">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-168">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="868aa-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="868aa-170">16</span><span class="sxs-lookup"><span data-stu-id="868aa-170">16</span></span>  

<span data-ttu-id="868aa-171">此參數會控制在會話上認可最外層交易時所採取的預設動作。</span><span class="sxs-lookup"><span data-stu-id="868aa-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="868aa-172">任何可以傳遞給 [JetCommitTransaction](./jetcommittransaction-function.md) 的有效選項，也可以做為實例中所有會話的預設值和/或特定會話的預設值。</span><span class="sxs-lookup"><span data-stu-id="868aa-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="868aa-173">如需這些選項的詳細資訊，請參閱 [JetCommitTransaction](./jetcommittransaction-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="868aa-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="868aa-174">此參數會影響交易的可靠性和效能。</span><span class="sxs-lookup"><span data-stu-id="868aa-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="868aa-175">如需詳細資訊，請參閱 [JetCommitTransaction](./jetcommittransaction-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="868aa-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-176">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-177">0</span><span class="sxs-lookup"><span data-stu-id="868aa-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-178">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-179">JET_GRBIT (整數) </span><span class="sxs-lookup"><span data-stu-id="868aa-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-180">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-181">適用于 JetCommitTransaction 的有效選項</span><span class="sxs-lookup"><span data-stu-id="868aa-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-182">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-183">實例或會話</span><span class="sxs-lookup"><span data-stu-id="868aa-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-184">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-185">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-186">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-187">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-188">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-189">No</span><span class="sxs-lookup"><span data-stu-id="868aa-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-190">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-191">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-192">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-193">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-194">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-195">No</span><span class="sxs-lookup"><span data-stu-id="868aa-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-196">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-197">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="868aa-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="868aa-199">48</span><span class="sxs-lookup"><span data-stu-id="868aa-199">48</span></span>  

<span data-ttu-id="868aa-200">當此參數為 true，且記錄檔路徑所指向的交易記錄檔 (**JET_paramLogFilePath**) 都是過時的版本，則這些交易記錄檔將會自動刪除。</span><span class="sxs-lookup"><span data-stu-id="868aa-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="868aa-201">**Windows 2000：**  將資料庫從 Windows NT 升級到 Windows 2000 時，必須小心使用此參數。</span><span class="sxs-lookup"><span data-stu-id="868aa-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="868aa-202">如果資料庫不是處於一致的狀態，而且舊的記錄檔遭到刪除，則資料庫的內容將會遺失。</span><span class="sxs-lookup"><span data-stu-id="868aa-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-203">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-204"><strong>Windows 2000：</strong>  假</span><span class="sxs-lookup"><span data-stu-id="868aa-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="868aa-205"><strong>WINDOWS XP：</strong>  真</span><span class="sxs-lookup"><span data-stu-id="868aa-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-206">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="868aa-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-208">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-209">False, True</span><span class="sxs-lookup"><span data-stu-id="868aa-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-210">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-211">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-212">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-213">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-214">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-215">No</span><span class="sxs-lookup"><span data-stu-id="868aa-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-216">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-217">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-218">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-219">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-220">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-221">No</span><span class="sxs-lookup"><span data-stu-id="868aa-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-222">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-223">No</span><span class="sxs-lookup"><span data-stu-id="868aa-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-224">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-225">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="868aa-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="868aa-227">47</span><span class="sxs-lookup"><span data-stu-id="868aa-227">47</span></span>  

<span data-ttu-id="868aa-228">如果此參數為 true，則資料庫引擎將不會在 [JetInit](./jetinit-function.md)期間驗證交易記錄檔的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="868aa-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="868aa-229">**WINDOWS XP：**  從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="868aa-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-230">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-231">否</span><span class="sxs-lookup"><span data-stu-id="868aa-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-232">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="868aa-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-234">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-235">False, True</span><span class="sxs-lookup"><span data-stu-id="868aa-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-236">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-237">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-238">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-239">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-240">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-241">No</span><span class="sxs-lookup"><span data-stu-id="868aa-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-242">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-243">No</span><span class="sxs-lookup"><span data-stu-id="868aa-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-244">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-245">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-246">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-247">No</span><span class="sxs-lookup"><span data-stu-id="868aa-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-248">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-249">No</span><span class="sxs-lookup"><span data-stu-id="868aa-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-250">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-251">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="868aa-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="868aa-253">136</span><span class="sxs-lookup"><span data-stu-id="868aa-253">136</span></span>  

<span data-ttu-id="868aa-254">此參數提供舊版資料庫引擎的檔案命名慣例回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="868aa-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="868aa-255">目前支援下列選項：</span><span class="sxs-lookup"><span data-stu-id="868aa-255">The following options are currently supported:</span></span>

<span data-ttu-id="868aa-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="868aa-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="868aa-257">當這個選項存在時，database engine 會針對其檔案使用下列命名慣例：</span><span class="sxs-lookup"><span data-stu-id="868aa-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="868aa-258">交易記錄檔將會使用。記錄檔的副檔名</span><span class="sxs-lookup"><span data-stu-id="868aa-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="868aa-259">檢查點檔案將會使用。副檔名的 .CHK</span><span class="sxs-lookup"><span data-stu-id="868aa-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-260">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="868aa-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-262">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-263">JET_GRBIT (整數) </span><span class="sxs-lookup"><span data-stu-id="868aa-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-264">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-265">0、JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="868aa-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-266">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-267">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-268">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-269">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-270">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-271">No</span><span class="sxs-lookup"><span data-stu-id="868aa-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-272">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-273">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-274">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-275">No</span><span class="sxs-lookup"><span data-stu-id="868aa-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-276">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-277">No</span><span class="sxs-lookup"><span data-stu-id="868aa-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-278">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-279">No</span><span class="sxs-lookup"><span data-stu-id="868aa-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-280">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-281">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="868aa-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="868aa-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="868aa-283">12</span><span class="sxs-lookup"><span data-stu-id="868aa-283">12</span></span>  

<span data-ttu-id="868aa-284">此參數會設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="868aa-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="868aa-285">此參數的單位是保存交易記錄檔之磁片區的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="868aa-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="868aa-286">磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。</span><span class="sxs-lookup"><span data-stu-id="868aa-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="868aa-287">此參數會對效能造成影響。</span><span class="sxs-lookup"><span data-stu-id="868aa-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="868aa-288">當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。</span><span class="sxs-lookup"><span data-stu-id="868aa-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="868aa-289">交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。</span><span class="sxs-lookup"><span data-stu-id="868aa-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="868aa-290">在此情況下，已知的預設值太小。</span><span class="sxs-lookup"><span data-stu-id="868aa-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="868aa-291">**WINDOWS XP 和 windows 2000：**  在 Windows XP 和舊版中，不建議將此參數設定為較大 (位元組數的緩衝區，) 超過交易記錄檔大小的一半。</span><span class="sxs-lookup"><span data-stu-id="868aa-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-292">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-293"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  80</span><span class="sxs-lookup"><span data-stu-id="868aa-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="868aa-294"><strong>Windows Vista：</strong>  126</span><span class="sxs-lookup"><span data-stu-id="868aa-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-295">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-296">整數</span><span class="sxs-lookup"><span data-stu-id="868aa-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-297">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-298"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  80 –2147483647</span><span class="sxs-lookup"><span data-stu-id="868aa-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="868aa-299"><strong>Windows Vista：</strong>  1-2147483647</span><span class="sxs-lookup"><span data-stu-id="868aa-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-300">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-301">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-302">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-303">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-304">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-305">No</span><span class="sxs-lookup"><span data-stu-id="868aa-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-306">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-307">No</span><span class="sxs-lookup"><span data-stu-id="868aa-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-308">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-309">No</span><span class="sxs-lookup"><span data-stu-id="868aa-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-310">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-311">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-312">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-313">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-314">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-315">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="868aa-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="868aa-317">14</span><span class="sxs-lookup"><span data-stu-id="868aa-317">14</span></span>  

<span data-ttu-id="868aa-318">此參數會設定資料庫引擎在產生指定的記錄檔磁區數目時，採取檢查點。</span><span class="sxs-lookup"><span data-stu-id="868aa-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="868aa-319">**WINDOWS XP：**  從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="868aa-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-320">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-321">1024</span><span class="sxs-lookup"><span data-stu-id="868aa-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-322">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-323">整數</span><span class="sxs-lookup"><span data-stu-id="868aa-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-324">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-325">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="868aa-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-326">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-327">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-328">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-329">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-330">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-331">No</span><span class="sxs-lookup"><span data-stu-id="868aa-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-332">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-333">No</span><span class="sxs-lookup"><span data-stu-id="868aa-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-334">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-335">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-336">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-337">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-338">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-339">No</span><span class="sxs-lookup"><span data-stu-id="868aa-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-340">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-341">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="868aa-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="868aa-343">69</span><span class="sxs-lookup"><span data-stu-id="868aa-343">69</span></span>  

<span data-ttu-id="868aa-344">當這個參數設定為 true 時，資料庫引擎會建立下一個交易記錄檔，因為目前的交易記錄檔已被取用。</span><span class="sxs-lookup"><span data-stu-id="868aa-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="868aa-345">其目的是要將從一個交易記錄檔切換至下一個交易記錄檔所花費的時間降至最低，以大幅更新負載。</span><span class="sxs-lookup"><span data-stu-id="868aa-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-346">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-347">對</span><span class="sxs-lookup"><span data-stu-id="868aa-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-348">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="868aa-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-350">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-351">False, True</span><span class="sxs-lookup"><span data-stu-id="868aa-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-352">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-353">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-354">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-355">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-356">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-357">No</span><span class="sxs-lookup"><span data-stu-id="868aa-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-358">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-359">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-360">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-361">No</span><span class="sxs-lookup"><span data-stu-id="868aa-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-362">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-363">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-364">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-365">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-366">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-367">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="868aa-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="868aa-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="868aa-369">2</span><span class="sxs-lookup"><span data-stu-id="868aa-369">2</span></span> 

<span data-ttu-id="868aa-370">此參數表示將包含實例之交易記錄之資料夾的相對或絕對檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="868aa-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="868aa-371">路徑必須以反斜線字元結束，表示目標路徑是資料夾。</span><span class="sxs-lookup"><span data-stu-id="868aa-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="868aa-372">交易記錄檔包含在損毀之後將資料庫檔案帶入一致狀態所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="868aa-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="868aa-373">它們通常名為 EDB \* 。日誌。</span><span class="sxs-lookup"><span data-stu-id="868aa-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="868aa-374">交易記錄檔的內容就和資料庫檔案本身一樣，)  (也一樣重要。</span><span class="sxs-lookup"><span data-stu-id="868aa-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="868aa-375">每個努力都應該進行保護。</span><span class="sxs-lookup"><span data-stu-id="868aa-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="868aa-376">此外也會有名為 RES1 的其他保留記錄檔。記錄檔和 RES2。連同一般記錄檔一起儲存的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="868aa-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="868aa-377">這些檔案的內容並不重要，因為其唯一的目的是保留磁碟空間，以允許引擎在低磁片案例中正常關機。</span><span class="sxs-lookup"><span data-stu-id="868aa-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="868aa-378">這些也會是暫時的記錄檔，通常名為 EDBTMP。登入相同的資料夾。</span><span class="sxs-lookup"><span data-stu-id="868aa-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="868aa-379">這兩個檔案的內容並不重要。</span><span class="sxs-lookup"><span data-stu-id="868aa-379">The contents of this file are not important either.</span></span> <span data-ttu-id="868aa-380">這個檔案是準備好使用的新記錄檔。</span><span class="sxs-lookup"><span data-stu-id="868aa-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="868aa-381">交易記錄檔之主機磁片區的屬性及其相對於資料庫引擎所使用之其他檔案的位置，可能會大幅影響效能。</span><span class="sxs-lookup"><span data-stu-id="868aa-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="868aa-382">**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。</span><span class="sxs-lookup"><span data-stu-id="868aa-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-383">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-384">&quot;.\&q</span><span class="sxs-lookup"><span data-stu-id="868aa-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-385">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-386">資料夾路徑 (字串) </span><span class="sxs-lookup"><span data-stu-id="868aa-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-387">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-388">0–246個字元</span><span class="sxs-lookup"><span data-stu-id="868aa-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-389">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-390">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-391">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-392">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-393">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-394">No</span><span class="sxs-lookup"><span data-stu-id="868aa-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-395">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-396">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-397">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-398">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-399">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-400">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-401">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-402">No</span><span class="sxs-lookup"><span data-stu-id="868aa-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-403">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-404">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="868aa-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="868aa-406">11</span><span class="sxs-lookup"><span data-stu-id="868aa-406">11</span></span>  

<span data-ttu-id="868aa-407">此參數會設定交易記錄檔的大小。</span><span class="sxs-lookup"><span data-stu-id="868aa-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="868aa-408">每個交易記錄檔都是固定的大小。</span><span class="sxs-lookup"><span data-stu-id="868aa-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="868aa-409">大小等於這個系統參數的設定（單位為1024個位元組）。</span><span class="sxs-lookup"><span data-stu-id="868aa-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="868aa-410">此參數會對可靠性造成影響。</span><span class="sxs-lookup"><span data-stu-id="868aa-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="868aa-411">如果設定太小，則會更快達到 (1048575) 的記錄檔數目上限。</span><span class="sxs-lookup"><span data-stu-id="868aa-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="868aa-412">發生這種情況時，必須完全關閉實例、必須刪除現有的記錄檔，而且必須重新開機實例。</span><span class="sxs-lookup"><span data-stu-id="868aa-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="868aa-413">此動作不僅會降低應用程式的可用性，也會使應用程式資料庫的任何先前備份失效。</span><span class="sxs-lookup"><span data-stu-id="868aa-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="868aa-414">此參數會對效能造成影響。</span><span class="sxs-lookup"><span data-stu-id="868aa-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="868aa-415">如果設定非常大，則 [JetInit](./jetinit-function.md) 會變慢，因為資料庫引擎在初始化時，至少必須讀取最年輕記錄檔 (的) 。</span><span class="sxs-lookup"><span data-stu-id="868aa-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="868aa-416">如果設定非常大，則在記錄檔之間切換時也需要較長的時間。</span><span class="sxs-lookup"><span data-stu-id="868aa-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="868aa-417">如果設定非常小，則需要為指定的更新數目建立更多記錄檔，這樣會增加額外負荷。</span><span class="sxs-lookup"><span data-stu-id="868aa-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-418">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-419">5120</span><span class="sxs-lookup"><span data-stu-id="868aa-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-420">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-421">整數</span><span class="sxs-lookup"><span data-stu-id="868aa-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-422">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-423"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  128 –32768</span><span class="sxs-lookup"><span data-stu-id="868aa-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="868aa-424"><strong>Windows Vista：</strong>  64 –32768</span><span class="sxs-lookup"><span data-stu-id="868aa-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-425">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-426">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-427">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-428">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-429">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-430">No</span><span class="sxs-lookup"><span data-stu-id="868aa-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-431">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-432">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-433">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-434">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-435">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-436">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-437">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-438">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-439">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-440">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="868aa-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="868aa-442">15</span><span class="sxs-lookup"><span data-stu-id="868aa-442">15</span></span>  

<span data-ttu-id="868aa-443">此參數會嘗試將長期認可所造成的記錄緩衝區排清優化，方法是在希望另一個交易共用排清的情況下，等候指定的會話數目等待永久性認可。</span><span class="sxs-lookup"><span data-stu-id="868aa-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="868aa-444">**WINDOWS XP：**  從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="868aa-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-445">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-446">3</span><span class="sxs-lookup"><span data-stu-id="868aa-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-447">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-448">整數</span><span class="sxs-lookup"><span data-stu-id="868aa-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-449">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-450">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="868aa-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-451">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-452">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-453">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-454">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-455">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-456">No</span><span class="sxs-lookup"><span data-stu-id="868aa-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-457">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-458">No</span><span class="sxs-lookup"><span data-stu-id="868aa-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-459">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-460">No</span><span class="sxs-lookup"><span data-stu-id="868aa-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-461">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-462">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-463">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-464">No</span><span class="sxs-lookup"><span data-stu-id="868aa-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-465">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-466">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="868aa-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="868aa-468">34</span><span class="sxs-lookup"><span data-stu-id="868aa-468">34</span></span>  

<span data-ttu-id="868aa-469">此參數是控制實例損毀復原的主切換。</span><span class="sxs-lookup"><span data-stu-id="868aa-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="868aa-470">如果此參數設定為 "On"，則會使用 >ARIES 樣式復原，在進程或電腦損毀時，將實例中的所有資料庫帶到一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="868aa-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="868aa-471">如果此參數設定為 "Off"，則會管理實例中的所有資料庫，而不會有損毀復原的優點。</span><span class="sxs-lookup"><span data-stu-id="868aa-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="868aa-472">也就是說，如果實例未在進程結束或電腦關機之前使用 [JetTerm](./jetterm-function.md) 完全關閉，則該實例中所有資料庫的內容將會損毀。</span><span class="sxs-lookup"><span data-stu-id="868aa-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="868aa-473">在特殊情況下，停用復原會很有用，因為在這種情況下，資料庫的內容在發生損毀的情況下不會很有用。</span><span class="sxs-lookup"><span data-stu-id="868aa-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="868aa-474">所有其他情況都應啟用復原。</span><span class="sxs-lookup"><span data-stu-id="868aa-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-475">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-476">&quot;開啟&quot;</span><span class="sxs-lookup"><span data-stu-id="868aa-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-477">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-478">String</span><span class="sxs-lookup"><span data-stu-id="868aa-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-479">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-480">0–259個字元</span><span class="sxs-lookup"><span data-stu-id="868aa-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-481">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-482">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-483">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-484">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-485">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-486">No</span><span class="sxs-lookup"><span data-stu-id="868aa-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-487">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-488">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-489">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-490">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-491">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-492">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-493">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-494">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-495">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-496">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="868aa-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="868aa-498">0</span><span class="sxs-lookup"><span data-stu-id="868aa-498">0</span></span>  

<span data-ttu-id="868aa-499">此參數表示將包含實例之檢查點檔案之資料夾的相對或絕對檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="868aa-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="868aa-500">路徑必須以反斜線字元結束，表示目標路徑是資料夾。</span><span class="sxs-lookup"><span data-stu-id="868aa-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="868aa-501">檢查點檔案是每個實例維護的簡單檔案，可記住必須重新執行的最舊交易記錄檔，以便在損毀之後將該實例中的所有資料庫帶到一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="868aa-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="868aa-502">檢查點檔案通常名為 EDB。.CHK.</span><span class="sxs-lookup"><span data-stu-id="868aa-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="868aa-503">**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。</span><span class="sxs-lookup"><span data-stu-id="868aa-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-504">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-505">&quot;.\&q</span><span class="sxs-lookup"><span data-stu-id="868aa-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-506">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-507">資料夾路徑 (字串) </span><span class="sxs-lookup"><span data-stu-id="868aa-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-508">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-509">0–246個字元</span><span class="sxs-lookup"><span data-stu-id="868aa-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-510">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-511">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-512">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-513">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-514">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-515">No</span><span class="sxs-lookup"><span data-stu-id="868aa-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-516">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-517">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-518">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-519">No</span><span class="sxs-lookup"><span data-stu-id="868aa-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-520">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-521">No</span><span class="sxs-lookup"><span data-stu-id="868aa-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-522">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-523">No</span><span class="sxs-lookup"><span data-stu-id="868aa-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-524">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-525">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="868aa-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="868aa-527">13</span><span class="sxs-lookup"><span data-stu-id="868aa-527">13</span></span> 

<span data-ttu-id="868aa-528">此參數會嘗試將長期認可所造成之記錄緩衝區的排清優化，方法是在希望另一個交易共用排清之前等候一段指定的時間。</span><span class="sxs-lookup"><span data-stu-id="868aa-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="868aa-529">**WINDOWS XP：**  從 Windows XP 起，此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="868aa-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-530">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-531">0</span><span class="sxs-lookup"><span data-stu-id="868aa-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-532">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-533">整數</span><span class="sxs-lookup"><span data-stu-id="868aa-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-534">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-535">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="868aa-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-536">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-537">實例或會話</span><span class="sxs-lookup"><span data-stu-id="868aa-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-538">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-539">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-540">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-541">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-542">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-543">No</span><span class="sxs-lookup"><span data-stu-id="868aa-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-544">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-545">No</span><span class="sxs-lookup"><span data-stu-id="868aa-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-546">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-547">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-548">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-549">No</span><span class="sxs-lookup"><span data-stu-id="868aa-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-550">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-551">全部</span><span class="sxs-lookup"><span data-stu-id="868aa-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="868aa-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="868aa-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="868aa-553">136</span><span class="sxs-lookup"><span data-stu-id="868aa-553">136</span></span>  

<span data-ttu-id="868aa-554">這個參數是用來指定要使用 Windows Server 2003 和先前的檔案命名配置來維護的檔案命名相容性功能。</span><span class="sxs-lookup"><span data-stu-id="868aa-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="868aa-555">如需不同檔案及其命名的詳細資訊，請參閱 [可擴充儲存引擎](./extensible-storage-engine-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="868aa-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="868aa-556">JET_bitESE98FileNames 可確保用於交易記錄檔和檢查點檔案的副檔名，與 Windows Server 2003 中使用的副檔名相同。</span><span class="sxs-lookup"><span data-stu-id="868aa-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="868aa-557">注意：如果從 Windows Server 2003 升級，則仍不需要指定此項，因為當 JET_paramCircularLog 設定為 **true** 時，引擎會自動升級副檔名，如果 JET_paramCircularLog 為 **false**，則保留較舊的記錄檔延伸模組。</span><span class="sxs-lookup"><span data-stu-id="868aa-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="868aa-558">**注意**  若要設定位，應先取出值，然後在所需的相容性位中取出 "or"。</span><span class="sxs-lookup"><span data-stu-id="868aa-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-559">預設值：3</span><span class="sxs-lookup"><span data-stu-id="868aa-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="868aa-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="868aa-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-561">輸入：</span><span class="sxs-lookup"><span data-stu-id="868aa-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="868aa-562">JET_GRBIT (整數) </span><span class="sxs-lookup"><span data-stu-id="868aa-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-563">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="868aa-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="868aa-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-565">範圍：</span><span class="sxs-lookup"><span data-stu-id="868aa-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="868aa-566">執行個體</span><span class="sxs-lookup"><span data-stu-id="868aa-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-567">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-568">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-569">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="868aa-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="868aa-570">No</span><span class="sxs-lookup"><span data-stu-id="868aa-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-571">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="868aa-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="868aa-572">Yes</span><span class="sxs-lookup"><span data-stu-id="868aa-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-573">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="868aa-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-574">No</span><span class="sxs-lookup"><span data-stu-id="868aa-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-575">影響效能：</span><span class="sxs-lookup"><span data-stu-id="868aa-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="868aa-576">No</span><span class="sxs-lookup"><span data-stu-id="868aa-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-577">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="868aa-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="868aa-578">No</span><span class="sxs-lookup"><span data-stu-id="868aa-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-579">可用性：</span><span class="sxs-lookup"><span data-stu-id="868aa-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="868aa-580">從 Windows Server 2008 和 Windows Vista 開始</span><span class="sxs-lookup"><span data-stu-id="868aa-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="868aa-581">規格需求</span><span class="sxs-lookup"><span data-stu-id="868aa-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="868aa-582"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="868aa-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="868aa-583">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="868aa-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="868aa-584"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="868aa-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="868aa-585">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="868aa-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="868aa-586"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="868aa-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="868aa-587">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="868aa-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="868aa-588">另請參閱</span><span class="sxs-lookup"><span data-stu-id="868aa-588">See Also</span></span>

[<span data-ttu-id="868aa-589">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="868aa-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="868aa-590">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="868aa-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="868aa-591">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="868aa-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="868aa-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="868aa-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="868aa-593">JetTerm</span><span class="sxs-lookup"><span data-stu-id="868aa-593">JetTerm</span></span>](./jetterm-function.md)
