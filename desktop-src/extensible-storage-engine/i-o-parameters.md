---
description: 深入瞭解： i/o 參數
title: I/o 參數
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691671"
---
# <a name="io-parameters"></a><span data-ttu-id="e3952-103">I/o 參數</span><span class="sxs-lookup"><span data-stu-id="e3952-103">I/O Parameters</span></span>


<span data-ttu-id="e3952-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e3952-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="e3952-105">I/o 參數</span><span class="sxs-lookup"><span data-stu-id="e3952-105">I/O Parameters</span></span>

<span data-ttu-id="e3952-106">本主題包含用於輸入和輸出 (i/o) 的參數。</span><span class="sxs-lookup"><span data-stu-id="e3952-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="e3952-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="e3952-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="e3952-108">53</span><span class="sxs-lookup"><span data-stu-id="e3952-108">53</span></span>  

<span data-ttu-id="e3952-109">**WINDOWS XP 和更新版本：**  此參數會設定時間長度 () （以毫秒為單位），資料庫引擎會使用此時間來存取已鎖定的檔案，然後 JET_errFileAccessDenied 失敗。</span><span class="sxs-lookup"><span data-stu-id="e3952-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="e3952-110">這段時間延遲的設計目的，是為了解決防毒軟體的問題，這些軟體可能會在關閉後短暫開啟一些資料庫引擎的檔案。</span><span class="sxs-lookup"><span data-stu-id="e3952-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="e3952-111">**注意**  由於上述重試邏輯的結果，任何附加至資料庫或使用資料庫引擎所使用之記錄檔的嘗試，都會導致此大小的延遲，然後 API 呼叫才會傳回 (合法) 失敗。</span><span class="sxs-lookup"><span data-stu-id="e3952-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="e3952-112">如果這是常見的案例，則可以使用這個參數來關閉該延遲。</span><span class="sxs-lookup"><span data-stu-id="e3952-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-113">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-114">10000</span><span class="sxs-lookup"><span data-stu-id="e3952-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-115">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-116">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-117">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-118">0-4294967295</span><span class="sxs-lookup"><span data-stu-id="e3952-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-119">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-120">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-121">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-122">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-123">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-124">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-125">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-126">No</span><span class="sxs-lookup"><span data-stu-id="e3952-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-127">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-128">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-129">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-130">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-131">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-132">No</span><span class="sxs-lookup"><span data-stu-id="e3952-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-133">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-134">Windows XP 及更新版本</span><span class="sxs-lookup"><span data-stu-id="e3952-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="e3952-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="e3952-136">100</span><span class="sxs-lookup"><span data-stu-id="e3952-136">100</span></span>  

<span data-ttu-id="e3952-137">當這個參數設定為 true 時，資料庫引擎所使用之檔案系統路徑中遺失的任何資料夾都會以無訊息模式建立。</span><span class="sxs-lookup"><span data-stu-id="e3952-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="e3952-138">否則，使用遺失檔案系統路徑的作業將會失敗，並 JET_errInvalidPath。</span><span class="sxs-lookup"><span data-stu-id="e3952-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-139">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-140">否</span><span class="sxs-lookup"><span data-stu-id="e3952-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-141">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="e3952-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-143">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-144">False, True</span><span class="sxs-lookup"><span data-stu-id="e3952-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-145">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-146">執行個體</span><span class="sxs-lookup"><span data-stu-id="e3952-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-147">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-148">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-149">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-150">No</span><span class="sxs-lookup"><span data-stu-id="e3952-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-151">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-152">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-153">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-154">No</span><span class="sxs-lookup"><span data-stu-id="e3952-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-155">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-156">No</span><span class="sxs-lookup"><span data-stu-id="e3952-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-157">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-158">No</span><span class="sxs-lookup"><span data-stu-id="e3952-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-159">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-160">全部</span><span class="sxs-lookup"><span data-stu-id="e3952-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="e3952-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="e3952-162">126</span><span class="sxs-lookup"><span data-stu-id="e3952-162">126</span></span>  

<span data-ttu-id="e3952-163">當此參數為 **True** 時，資料庫引擎會使用 Windows 檔案快取做為其所有不同檔案的讀取快取。</span><span class="sxs-lookup"><span data-stu-id="e3952-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="e3952-164">它也會使用它做為暫存資料庫的寫入快取，或使用已停用復原開啟的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e3952-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="e3952-165">資料庫引擎必須停用一般資料庫、交易記錄檔和檢查點檔案的寫入快取，以保護資料庫的交易完整性。</span><span class="sxs-lookup"><span data-stu-id="e3952-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="e3952-166">請務必注意，使用 Windows 檔案快取會為資料庫檔案新增第二個快取的分層。</span><span class="sxs-lookup"><span data-stu-id="e3952-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="e3952-167">資料庫快取仍會使用自己的記憶體來快取資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="e3952-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="e3952-168">這種模式的目的是讓應用程式使用小型專用快取來設定 database engine，並允許 Windows 捐贈備用記憶體，以進一步改善資料庫資料的快取。</span><span class="sxs-lookup"><span data-stu-id="e3952-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-169">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-170">否</span><span class="sxs-lookup"><span data-stu-id="e3952-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-171">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="e3952-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-173">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-174">False, True</span><span class="sxs-lookup"><span data-stu-id="e3952-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-175">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-176">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-177">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-178">No</span><span class="sxs-lookup"><span data-stu-id="e3952-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-179">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-180">No</span><span class="sxs-lookup"><span data-stu-id="e3952-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-181">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-182">No</span><span class="sxs-lookup"><span data-stu-id="e3952-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-183">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-184">No</span><span class="sxs-lookup"><span data-stu-id="e3952-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-185">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-186">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-187">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-188">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-189">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-190">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="e3952-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="e3952-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="e3952-192">152</span><span class="sxs-lookup"><span data-stu-id="e3952-192">152</span></span>  

<span data-ttu-id="e3952-193">此參數可控制 ESE 處理 i/o 作業的方式。</span><span class="sxs-lookup"><span data-stu-id="e3952-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="e3952-194">這些值可以設定為 0 (一般作業 JET_IOPriorityNormal) ，或針對低優先順序作業的 1 (JET_IOPriorityLow) 。</span><span class="sxs-lookup"><span data-stu-id="e3952-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="e3952-195">當優先權設定為 JET_IOPriorityLow 時，ESE 會使用 Windows Vista 中提供的新執行緒 i/o 優先權功能來減少執行緒的 i/o 優先順序，以便在新的低優先順序發行後續的 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="e3952-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="e3952-196">**Windows Vista：**  JET_paramIOPriority 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="e3952-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-197">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-198">0</span><span class="sxs-lookup"><span data-stu-id="e3952-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-199">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-200">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-201">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="e3952-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-203">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-204">執行個體</span><span class="sxs-lookup"><span data-stu-id="e3952-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-205">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-206">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-207">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-208">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-209">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-210">No</span><span class="sxs-lookup"><span data-stu-id="e3952-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-211">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-212">No</span><span class="sxs-lookup"><span data-stu-id="e3952-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-213">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-214">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-215">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-216">No</span><span class="sxs-lookup"><span data-stu-id="e3952-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-217">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3952-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="e3952-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="e3952-220">30</span><span class="sxs-lookup"><span data-stu-id="e3952-220">30</span></span> 

<span data-ttu-id="e3952-221">此參數控制一次可在主機作業系統中佇列的資料庫檔案 i/o 數量。</span><span class="sxs-lookup"><span data-stu-id="e3952-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="e3952-222">較大的參數值可大幅協助大型資料庫應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="e3952-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="e3952-223">**WINDOWS XP 和 Windows Server 2003：**  Windows XP 和 Windows Server 2003 會忽略此參數，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="e3952-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-224">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-225"><strong>Windows 2000： </strong>  64</span><span class="sxs-lookup"><span data-stu-id="e3952-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="e3952-226"><strong>Windows Vista：</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="e3952-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-227">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-228">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-229">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-230"><strong>Windows 2000：</strong>  8 –2147483647</span><span class="sxs-lookup"><span data-stu-id="e3952-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="e3952-231"><strong>Windows Vista：</strong>  0-65536</span><span class="sxs-lookup"><span data-stu-id="e3952-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-232">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-233">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-234">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-235">No</span><span class="sxs-lookup"><span data-stu-id="e3952-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-236">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-237">No</span><span class="sxs-lookup"><span data-stu-id="e3952-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-238">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-239">No</span><span class="sxs-lookup"><span data-stu-id="e3952-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-240">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-241">No</span><span class="sxs-lookup"><span data-stu-id="e3952-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-242">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-243">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-244">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-245">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-246">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-247">全部</span><span class="sxs-lookup"><span data-stu-id="e3952-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="e3952-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="e3952-249">164</span><span class="sxs-lookup"><span data-stu-id="e3952-249">164</span></span>  

<span data-ttu-id="e3952-250">合併的讀取作業可分組的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e3952-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-251">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-252">262144</span><span class="sxs-lookup"><span data-stu-id="e3952-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-253">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-254">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-255">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="e3952-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-257">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-258">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-259">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-260">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-261">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-262">No</span><span class="sxs-lookup"><span data-stu-id="e3952-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-263">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-264">No</span><span class="sxs-lookup"><span data-stu-id="e3952-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-265">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-266">No</span><span class="sxs-lookup"><span data-stu-id="e3952-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-267">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-268">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-269">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-270">No</span><span class="sxs-lookup"><span data-stu-id="e3952-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-271">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3952-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="e3952-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="e3952-274">165</span><span class="sxs-lookup"><span data-stu-id="e3952-274">165</span></span>  

<span data-ttu-id="e3952-275">合併寫入作業可分組的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e3952-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-276">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-277">393216</span><span class="sxs-lookup"><span data-stu-id="e3952-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-278">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-279">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-280">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="e3952-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-282">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-283">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-284">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-285">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-286">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-287">No</span><span class="sxs-lookup"><span data-stu-id="e3952-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-288">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-289">No</span><span class="sxs-lookup"><span data-stu-id="e3952-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-290">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-291">No</span><span class="sxs-lookup"><span data-stu-id="e3952-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-292">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-293">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-294">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-295">No</span><span class="sxs-lookup"><span data-stu-id="e3952-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-296">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3952-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="e3952-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="e3952-299">166</span><span class="sxs-lookup"><span data-stu-id="e3952-299">166</span></span>  

<span data-ttu-id="e3952-300">結合的寫入 i/o 作業可能會有空隙的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e3952-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-301">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-302">262144</span><span class="sxs-lookup"><span data-stu-id="e3952-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-303">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-304">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-305">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="e3952-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-307">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-308">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-309">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-310">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-311">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-312">No</span><span class="sxs-lookup"><span data-stu-id="e3952-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-313">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-314">No</span><span class="sxs-lookup"><span data-stu-id="e3952-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-315">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-316">No</span><span class="sxs-lookup"><span data-stu-id="e3952-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-317">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-318">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-319">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-320">No</span><span class="sxs-lookup"><span data-stu-id="e3952-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-321">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3952-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3952-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="e3952-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="e3952-324">167</span><span class="sxs-lookup"><span data-stu-id="e3952-324">167</span></span>  

<span data-ttu-id="e3952-325">結合的讀取 i/o 作業可能會有空隙的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e3952-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-326">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e3952-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e3952-327">393216</span><span class="sxs-lookup"><span data-stu-id="e3952-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-328">輸入：</span><span class="sxs-lookup"><span data-stu-id="e3952-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="e3952-329">整數</span><span class="sxs-lookup"><span data-stu-id="e3952-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-330">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e3952-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="e3952-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-332">範圍：</span><span class="sxs-lookup"><span data-stu-id="e3952-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e3952-333">全球</span><span class="sxs-lookup"><span data-stu-id="e3952-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-334">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-335">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-336">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e3952-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e3952-337">No</span><span class="sxs-lookup"><span data-stu-id="e3952-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-338">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e3952-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e3952-339">No</span><span class="sxs-lookup"><span data-stu-id="e3952-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-340">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e3952-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-341">No</span><span class="sxs-lookup"><span data-stu-id="e3952-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-342">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e3952-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e3952-343">Yes</span><span class="sxs-lookup"><span data-stu-id="e3952-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-344">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e3952-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e3952-345">No</span><span class="sxs-lookup"><span data-stu-id="e3952-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-346">可用性：</span><span class="sxs-lookup"><span data-stu-id="e3952-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e3952-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3952-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e3952-348">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3952-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3952-349"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e3952-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e3952-350">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="e3952-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3952-351"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e3952-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e3952-352">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="e3952-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3952-353"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e3952-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e3952-354">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e3952-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e3952-355">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3952-355">See Also</span></span>

[<span data-ttu-id="e3952-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="e3952-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e3952-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="e3952-357">JetInit</span></span>](./jetinit-function.md)
