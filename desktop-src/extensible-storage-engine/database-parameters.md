---
description: 深入瞭解：資料庫參數
title: 資料庫參數
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114084"
---
# <a name="database-parameters"></a><span data-ttu-id="c78bc-103">資料庫參數</span><span class="sxs-lookup"><span data-stu-id="c78bc-103">Database Parameters</span></span>


<span data-ttu-id="c78bc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c78bc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="c78bc-105">資料庫參數</span><span class="sxs-lookup"><span data-stu-id="c78bc-105">Database Parameters</span></span>

<span data-ttu-id="c78bc-106">本主題包含用於資料庫的參數。</span><span class="sxs-lookup"><span data-stu-id="c78bc-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="c78bc-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="c78bc-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="c78bc-108">44</span><span class="sxs-lookup"><span data-stu-id="c78bc-108">44</span></span>  

<span data-ttu-id="c78bc-109">設定時，此參數會在開啟資料庫引擎的資料庫或交易記錄檔時，導致 [JetInit](./jetinit-function.md) 傳回特殊錯誤。</span><span class="sxs-lookup"><span data-stu-id="c78bc-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="c78bc-110">這些錯誤包括：</span><span class="sxs-lookup"><span data-stu-id="c78bc-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c78bc-111">錯誤</span><span class="sxs-lookup"><span data-stu-id="c78bc-111">Error</span></span></p></th>
<th><p><span data-ttu-id="c78bc-112">描述</span><span class="sxs-lookup"><span data-stu-id="c78bc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="c78bc-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="c78bc-114">資料庫和/或交易記錄檔是使用 database engine 在 Windows NT 3.51 中建立的。</span><span class="sxs-lookup"><span data-stu-id="c78bc-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="c78bc-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="c78bc-116">資料庫和/或交易記錄檔是使用 database engine 在 Windows NT Server 4.0 之前的測試版本中建立的。</span><span class="sxs-lookup"><span data-stu-id="c78bc-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="c78bc-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="c78bc-118">資料庫和/或交易記錄檔是使用 Windows NT Server 4.0 中的 database engine 所建立。</span><span class="sxs-lookup"><span data-stu-id="c78bc-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-119">**Windows Vista：**  若為 Windows Vista 和更新版本，此參數已過時，而且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="c78bc-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-120">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-121">對</span><span class="sxs-lookup"><span data-stu-id="c78bc-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-122">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="c78bc-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-124">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-125">False, True</span><span class="sxs-lookup"><span data-stu-id="c78bc-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-126">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-127">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-128">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-129">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-130">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-131">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-132">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-133">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-134">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-135">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-136">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-137">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-138">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-139">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-140">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-141">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="c78bc-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="c78bc-143">64</span><span class="sxs-lookup"><span data-stu-id="c78bc-143">64</span></span>  

<span data-ttu-id="c78bc-144">此參數會設定資料庫的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="c78bc-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="c78bc-145">頁面大小是資料庫檔案可能的最小空間配置單位。</span><span class="sxs-lookup"><span data-stu-id="c78bc-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="c78bc-146">資料庫頁面大小也非常重要，因為它會在資料庫中設定個別記錄大小的上限。</span><span class="sxs-lookup"><span data-stu-id="c78bc-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="c78bc-147">**注意** 目前每個進程只支援一個資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="c78bc-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="c78bc-148">這表示，如果您在包含使用資料庫引擎之不同應用程式的單一進程中，則它們都必須同意資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="c78bc-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-149">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-150">4096</span><span class="sxs-lookup"><span data-stu-id="c78bc-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-151">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-152">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-153">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-154">2048、4096、8192</span><span class="sxs-lookup"><span data-stu-id="c78bc-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-155">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-156">全球</span><span class="sxs-lookup"><span data-stu-id="c78bc-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-157">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-158">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-159">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-160">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-161">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-162">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-163">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-164">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-165">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-166">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-167">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-168">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-169">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-170">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="c78bc-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="c78bc-172">18</span><span class="sxs-lookup"><span data-stu-id="c78bc-172">18</span></span>  

<span data-ttu-id="c78bc-173">此參數會控制每次需要成長以容納更多資料時，資料庫檔案所新增的空間量。</span><span class="sxs-lookup"><span data-stu-id="c78bc-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="c78bc-174">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="c78bc-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-175">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-176">256</span><span class="sxs-lookup"><span data-stu-id="c78bc-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-177">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-178">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-179">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-180">1–2147483647</span><span class="sxs-lookup"><span data-stu-id="c78bc-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-181">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-182">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-183">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-184">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-185">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-186">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-186">No</span></span></p>
<p><span data-ttu-id="c78bc-187"><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</span><span class="sxs-lookup"><span data-stu-id="c78bc-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-188">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-189">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-190">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-191">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-192">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-193">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-194">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-195">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-196">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-197">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="c78bc-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="c78bc-199">45</span><span class="sxs-lookup"><span data-stu-id="c78bc-199">45</span></span>  

<span data-ttu-id="c78bc-200">當此參數為 true 時，系統會在 [JetAttachDatabase](./jetattachdatabase-function.md) 階段檢查每個資料庫，以取得在作業系統中使用舊版 NLS 程式庫建立的 Unicode 索引鍵資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="c78bc-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="c78bc-201">這必須完成，因為資料庫引擎會保存 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 所產生的排序索引鍵，而這些排序索引鍵的值會從 release 變更為 release。</span><span class="sxs-lookup"><span data-stu-id="c78bc-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="c78bc-202">如果偵測到主要索引處於此狀態，則 [JetAttachDatabase](./jetattachdatabase-function.md) 一律會失敗，並 JET_errPrimaryIndexCorrupted。</span><span class="sxs-lookup"><span data-stu-id="c78bc-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="c78bc-203">如果偵測到任何次要索引處於此狀態，則有兩個可能的結果。</span><span class="sxs-lookup"><span data-stu-id="c78bc-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="c78bc-204">如果 JET_bitDbDeleteCorruptIndexes 已傳遞至 [JetAttachDatabase](./jetattachdatabase-function.md) ，則這些索引將會刪除，而且 JET_wrnCorruptIndexDeleted 將會從 [JetAttachDatabase](./jetattachdatabase-function.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="c78bc-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="c78bc-205">您的應用程式將需要重新建立這些索引。</span><span class="sxs-lookup"><span data-stu-id="c78bc-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="c78bc-206">如果 JET_bitDbDeleteCorruptIndexes 未傳遞至 [JetAttachDatabase](./jetattachdatabase-function.md) ，則呼叫會失敗併發生 JET_errSecondaryIndexCorrupted。</span><span class="sxs-lookup"><span data-stu-id="c78bc-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="c78bc-207">**注意** 強烈建議您的應用程式將此參數設定為 True。</span><span class="sxs-lookup"><span data-stu-id="c78bc-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="c78bc-208">**注意** 強烈建議應用程式避免在 (叢集) 索引的主鍵中使用 Unicode 索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="c78bc-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-209">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-210">否</span><span class="sxs-lookup"><span data-stu-id="c78bc-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-211">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="c78bc-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-213">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-214">False, True</span><span class="sxs-lookup"><span data-stu-id="c78bc-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-215">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-216">全球</span><span class="sxs-lookup"><span data-stu-id="c78bc-216">Global</span></span></p>
<p><span data-ttu-id="c78bc-217"><strong>Windows Vista：</strong>  Windows Vista 和更新版本：實例</span><span class="sxs-lookup"><span data-stu-id="c78bc-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-218">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-219">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-220">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-221">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-222">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-223">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-224">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-225">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-226">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-227">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-228">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-229">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-230">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-231">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="c78bc-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="c78bc-233">54</span><span class="sxs-lookup"><span data-stu-id="c78bc-233">54</span></span>  

<span data-ttu-id="c78bc-234">當這個參數設定為 true 時，資料庫引擎會視需要在 [JetInit](./jetinit-function.md) 時自動清除 Unicode 索引鍵資料行上的索引，以避免變更 WINDOWS 中 NLS 程式庫所造成的資料庫格式變更。</span><span class="sxs-lookup"><span data-stu-id="c78bc-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="c78bc-235">NLS 程式庫會定期進行這類變更，以新增對新語言的支援、將遺漏的字元新增至語言、將定序順序加入至語言，或是以語言的定序順序修正 bug。</span><span class="sxs-lookup"><span data-stu-id="c78bc-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="c78bc-236">這些變更會影響由資料庫引擎以索引鍵的元件的形式保存的 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 所產生的排序關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c78bc-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="c78bc-237">很重要的一點是，索引的變更可能很有可能無法進行累加式清除。</span><span class="sxs-lookup"><span data-stu-id="c78bc-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="c78bc-238">在此情況下，會依 **JET_paramEnableIndexChecking** 的規定來處理索引。</span><span class="sxs-lookup"><span data-stu-id="c78bc-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="c78bc-239">**注意** 強烈建議您的應用程式將此參數和 **JET_paramEnableIndexChecking** 設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="c78bc-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-240">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-241">對</span><span class="sxs-lookup"><span data-stu-id="c78bc-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-242">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="c78bc-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-244">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-245">False, True</span><span class="sxs-lookup"><span data-stu-id="c78bc-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-246">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-247">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-248">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-249">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-250">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-251">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-251">No</span></span></p>
<p><span data-ttu-id="c78bc-252"><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</span><span class="sxs-lookup"><span data-stu-id="c78bc-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-253">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-254">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-255">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-256">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-257">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-258">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-259">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-260">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-261">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-262">Windows Server 2003 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c78bc-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="c78bc-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="c78bc-264">102</span><span class="sxs-lookup"><span data-stu-id="c78bc-264">102</span></span>  

<span data-ttu-id="c78bc-265">當此參數為 true 時，指定會話一次只允許一個資料庫使用 [JetOpenDatabase](./jetopendatabase-function.md) 來開啟。</span><span class="sxs-lookup"><span data-stu-id="c78bc-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="c78bc-266">這項限制會排除暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="c78bc-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="c78bc-267">**WINDOWS XP 和 Windows Server 2003：**  此參數只會在 Windows XP 和 Windows Server 2003 上寫入。</span><span class="sxs-lookup"><span data-stu-id="c78bc-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="c78bc-268">**Windows Vista：**  此參數的行為通常是 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="c78bc-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="c78bc-269">**注意**  此參數只是寫入。</span><span class="sxs-lookup"><span data-stu-id="c78bc-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-270">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-271">否</span><span class="sxs-lookup"><span data-stu-id="c78bc-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-272">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="c78bc-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-274">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-275">False, True</span><span class="sxs-lookup"><span data-stu-id="c78bc-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-276">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-277">全球</span><span class="sxs-lookup"><span data-stu-id="c78bc-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-278">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-279">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-279">No</span></span></p>
<p><span data-ttu-id="c78bc-280"><strong>Windows Vista：</strong>  Windows Vista 和更新版本：是</span><span class="sxs-lookup"><span data-stu-id="c78bc-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-281">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-282">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-283">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-284">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-285">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-286">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-287">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-288">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-289">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-290">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-291">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-292">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c78bc-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="c78bc-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="c78bc-294">35</span><span class="sxs-lookup"><span data-stu-id="c78bc-294">35</span></span>  

<span data-ttu-id="c78bc-295">此參數會控制使用 [JetDefragment](./jetdefragment-function.md)起始時的線上磁碟重組行為。</span><span class="sxs-lookup"><span data-stu-id="c78bc-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="c78bc-296">如需詳細資訊，請參閱 [JetDefragment](./jetdefragment-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="c78bc-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="c78bc-297">Windows 2000：在 Windows 2000 上，此參數是簡單的布林值，會在 [JetDefragment](./jetdefragment-function.md)啟動時閘道進行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="c78bc-298">當設為 **TRUE** 時，會對資料庫中每個資料表的記錄執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="c78bc-299">**WINDOWS XP：**  在 Windows XP 和更新版本中，這個參數可以設定為下列其中一個或多個選項：</span><span class="sxs-lookup"><span data-stu-id="c78bc-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c78bc-300">選項</span><span class="sxs-lookup"><span data-stu-id="c78bc-300">Option</span></span></p></th>
<th><p><span data-ttu-id="c78bc-301">Description</span><span class="sxs-lookup"><span data-stu-id="c78bc-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="c78bc-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="c78bc-303">請勿執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="c78bc-304">這是與此參數的 Windows 2000 設定為 False 相等的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="c78bc-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="c78bc-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="c78bc-306">執行完整的線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-306">Perform full online defragmentation.</span></span> <span data-ttu-id="c78bc-307">這是對此參數而言，與 Windows 2000 設定為 True 的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="c78bc-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="c78bc-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="c78bc-309">針對資料庫中每個資料表的記錄執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="c78bc-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="c78bc-311">針對資料庫中每個資料表的空間樹狀目錄執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="c78bc-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="c78bc-313">這個參數是用來支援 Microsoft Exchange 基礎結構，而且不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="c78bc-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c78bc-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="c78bc-315">執行完整的線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-315">Perform full online defragmentation.</span></span> <span data-ttu-id="c78bc-316">這個參數的概念相當於 Windows 2000 設定 True。</span><span class="sxs-lookup"><span data-stu-id="c78bc-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-317">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-318"><strong>Windows 2000：</strong>  真</span><span class="sxs-lookup"><span data-stu-id="c78bc-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="c78bc-319"><strong>WINDOWS xp：適用于 WINDOWS xp 和更新版本：</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c78bc-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-320">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-321"><strong>Windows 2000：</strong>  布林</span><span class="sxs-lookup"><span data-stu-id="c78bc-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="c78bc-322"><strong>WINDOWS XP 和更新版本：</strong>  JET_GRBIT (整數) </span><span class="sxs-lookup"><span data-stu-id="c78bc-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-323">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-324"><strong>Windows 2000：</strong>  False、True</span><span class="sxs-lookup"><span data-stu-id="c78bc-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="c78bc-325"><strong>WINDOWS XP 及更新版本：</strong>  0 – JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="c78bc-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-326">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-327">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-328">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-329">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-330">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-331">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-332">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-333">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-334">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-335">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-336">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-337">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-338">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-339">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-340">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-341">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="c78bc-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="c78bc-343">20</span><span class="sxs-lookup"><span data-stu-id="c78bc-343">20</span></span>  

<span data-ttu-id="c78bc-344">此參數是資料庫引擎用來控制可用空間片段的臨界值。</span><span class="sxs-lookup"><span data-stu-id="c78bc-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="c78bc-345">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="c78bc-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-346">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-347">8</span><span class="sxs-lookup"><span data-stu-id="c78bc-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-348">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-349">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-350">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-351">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="c78bc-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-352">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-353">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-354">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-355">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-356">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-357">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-358">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-359">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-360">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-361">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-362">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-363">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-364">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-365">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-366">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-367">全部</span><span class="sxs-lookup"><span data-stu-id="c78bc-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="c78bc-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="c78bc-369">78</span><span class="sxs-lookup"><span data-stu-id="c78bc-369">78</span></span>

<span data-ttu-id="c78bc-370">此參數會控制資料庫頁面快取管理員撰寫資料庫頁面，而該頁面已經歷就地格式轉換的程度。</span><span class="sxs-lookup"><span data-stu-id="c78bc-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="c78bc-371">這些格式轉換會在頁面從使用 Windows 2000 資料庫引擎建立的資料庫載入，但是由 Windows XP 或更新版本的 database engine 所使用，而立即進行。</span><span class="sxs-lookup"><span data-stu-id="c78bc-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-372">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-373">1</span><span class="sxs-lookup"><span data-stu-id="c78bc-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-374">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-375">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-376">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-377">0-3</span><span class="sxs-lookup"><span data-stu-id="c78bc-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-378">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-379">全球</span><span class="sxs-lookup"><span data-stu-id="c78bc-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-380">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-381">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-382">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-383">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-384">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-385">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-386">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-387">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-388">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-389">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-390">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-391">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-392">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-393">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c78bc-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="c78bc-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="c78bc-395">153</span><span class="sxs-lookup"><span data-stu-id="c78bc-395">153</span></span>  

<span data-ttu-id="c78bc-396">) 記錄中的延遲 (于提示/最高認可記錄檔後方，以延遲資料庫頁面排清。</span><span class="sxs-lookup"><span data-stu-id="c78bc-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="c78bc-397">啟用此延遲可能會在最新的記錄檔發生嚴重遺失時，允許資料庫復原。</span><span class="sxs-lookup"><span data-stu-id="c78bc-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="c78bc-398">請參閱 JET_bitReplayIgnoreLostLogs。</span><span class="sxs-lookup"><span data-stu-id="c78bc-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-399">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-400">0</span><span class="sxs-lookup"><span data-stu-id="c78bc-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-401">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-402">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-403">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="c78bc-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-405">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-406">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-407">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-408">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-409">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-410">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-411">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-412">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-413">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-414">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-415">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-416">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-417">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-418">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-419">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c78bc-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="c78bc-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="c78bc-422">160</span><span class="sxs-lookup"><span data-stu-id="c78bc-422">160</span></span>  

<span data-ttu-id="c78bc-423">開啟/關閉自動連續的 B 型樹狀目錄磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c78bc-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-424">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-425">1</span><span class="sxs-lookup"><span data-stu-id="c78bc-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-426">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="c78bc-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-428">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-429">0-1</span><span class="sxs-lookup"><span data-stu-id="c78bc-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-430">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-431">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-432">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-433">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-434">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-435">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-436">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-437">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-438">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-439">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-440">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-441">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-442">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-443">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-444">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c78bc-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="c78bc-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="c78bc-447">161</span><span class="sxs-lookup"><span data-stu-id="c78bc-447">161</span></span>  

<span data-ttu-id="c78bc-448">決定選取 B 型樹狀結構密度的頻率。</span><span class="sxs-lookup"><span data-stu-id="c78bc-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-449">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-450">10</span><span class="sxs-lookup"><span data-stu-id="c78bc-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-451">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-452">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-453">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-454">0-最大整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-455">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-456">執行個體</span><span class="sxs-lookup"><span data-stu-id="c78bc-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-457">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-458">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-459">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-460">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-461">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-462">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-463">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-464">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-465">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-466">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-467">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-468">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-469">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c78bc-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c78bc-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="c78bc-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="c78bc-472">162</span><span class="sxs-lookup"><span data-stu-id="c78bc-472">162</span></span>  

<span data-ttu-id="c78bc-473">I/o 節流機制提供工作執行的最長時間（以毫秒為單位），以視為「已完成」。</span><span class="sxs-lookup"><span data-stu-id="c78bc-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-474">預設值：3</span><span class="sxs-lookup"><span data-stu-id="c78bc-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-475">125</span><span class="sxs-lookup"><span data-stu-id="c78bc-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-476">輸入：</span><span class="sxs-lookup"><span data-stu-id="c78bc-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-477">整數</span><span class="sxs-lookup"><span data-stu-id="c78bc-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-478">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="c78bc-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-480">範圍：</span><span class="sxs-lookup"><span data-stu-id="c78bc-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-481">全球</span><span class="sxs-lookup"><span data-stu-id="c78bc-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-482">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-483">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-484">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="c78bc-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-485">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-486">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="c78bc-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-487">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-488">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-489">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-490">影響效能：</span><span class="sxs-lookup"><span data-stu-id="c78bc-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-491">Yes</span><span class="sxs-lookup"><span data-stu-id="c78bc-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-492">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="c78bc-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-493">No</span><span class="sxs-lookup"><span data-stu-id="c78bc-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-494">可用性：</span><span class="sxs-lookup"><span data-stu-id="c78bc-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="c78bc-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c78bc-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c78bc-496">規格需求</span><span class="sxs-lookup"><span data-stu-id="c78bc-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-497"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c78bc-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c78bc-498">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c78bc-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c78bc-499"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c78bc-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c78bc-500">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c78bc-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c78bc-501"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c78bc-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c78bc-502">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c78bc-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c78bc-503">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c78bc-503">See Also</span></span>

[<span data-ttu-id="c78bc-504">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="c78bc-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="c78bc-505">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c78bc-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c78bc-506">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="c78bc-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="c78bc-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="c78bc-507">JetInit</span></span>](./jetinit-function.md)
