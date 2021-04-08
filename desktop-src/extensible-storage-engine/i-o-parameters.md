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
# <a name="io-parameters"></a><span data-ttu-id="4db8e-103">I/o 參數</span><span class="sxs-lookup"><span data-stu-id="4db8e-103">I/O Parameters</span></span>


<span data-ttu-id="4db8e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4db8e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="4db8e-105">I/o 參數</span><span class="sxs-lookup"><span data-stu-id="4db8e-105">I/O Parameters</span></span>

<span data-ttu-id="4db8e-106">本主題包含用於輸入和輸出 (i/o) 的參數。</span><span class="sxs-lookup"><span data-stu-id="4db8e-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="4db8e-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="4db8e-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="4db8e-108">53</span><span class="sxs-lookup"><span data-stu-id="4db8e-108">53</span></span>  

<span data-ttu-id="4db8e-109">**WINDOWS XP 和更新版本：**  此參數會設定時間長度 () （以毫秒為單位），資料庫引擎會使用此時間來存取已鎖定的檔案，然後 JET_errFileAccessDenied 失敗。</span><span class="sxs-lookup"><span data-stu-id="4db8e-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="4db8e-110">這段時間延遲的設計目的，是為了解決防毒軟體的問題，這些軟體可能會在關閉後短暫開啟一些資料庫引擎的檔案。</span><span class="sxs-lookup"><span data-stu-id="4db8e-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="4db8e-111">**注意**  由於上述重試邏輯的結果，任何附加至資料庫或使用資料庫引擎所使用之記錄檔的嘗試，都會導致此大小的延遲，然後 API 呼叫才會傳回 (合法) 失敗。</span><span class="sxs-lookup"><span data-stu-id="4db8e-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="4db8e-112">如果這是常見的案例，則可以使用這個參數來關閉該延遲。</span><span class="sxs-lookup"><span data-stu-id="4db8e-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-113">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-114">10000</span><span class="sxs-lookup"><span data-stu-id="4db8e-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-115">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-116">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-117">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-118">0-4294967295</span><span class="sxs-lookup"><span data-stu-id="4db8e-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-119">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-120">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-121">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-122">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-123">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-124">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-125">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-126">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-127">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-128">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-129">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-130">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-131">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-132">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-133">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-134">Windows XP 及更新版本</span><span class="sxs-lookup"><span data-stu-id="4db8e-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="4db8e-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="4db8e-136">100</span><span class="sxs-lookup"><span data-stu-id="4db8e-136">100</span></span>  

<span data-ttu-id="4db8e-137">當這個參數設定為 true 時，資料庫引擎所使用之檔案系統路徑中遺失的任何資料夾都會以無訊息模式建立。</span><span class="sxs-lookup"><span data-stu-id="4db8e-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="4db8e-138">否則，使用遺失檔案系統路徑的作業將會失敗，並 JET_errInvalidPath。</span><span class="sxs-lookup"><span data-stu-id="4db8e-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-139">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-140">否</span><span class="sxs-lookup"><span data-stu-id="4db8e-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-141">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="4db8e-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-143">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-144">False, True</span><span class="sxs-lookup"><span data-stu-id="4db8e-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-145">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-146">執行個體</span><span class="sxs-lookup"><span data-stu-id="4db8e-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-147">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-148">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-149">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-150">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-151">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-152">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-153">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-154">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-155">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-156">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-157">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-158">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-159">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-160">全部</span><span class="sxs-lookup"><span data-stu-id="4db8e-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="4db8e-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="4db8e-162">126</span><span class="sxs-lookup"><span data-stu-id="4db8e-162">126</span></span>  

<span data-ttu-id="4db8e-163">當此參數為 **True** 時，資料庫引擎會使用 Windows 檔案快取做為其所有不同檔案的讀取快取。</span><span class="sxs-lookup"><span data-stu-id="4db8e-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="4db8e-164">它也會使用它做為暫存資料庫的寫入快取，或使用已停用復原開啟的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4db8e-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="4db8e-165">資料庫引擎必須停用一般資料庫、交易記錄檔和檢查點檔案的寫入快取，以保護資料庫的交易完整性。</span><span class="sxs-lookup"><span data-stu-id="4db8e-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="4db8e-166">請務必注意，使用 Windows 檔案快取會為資料庫檔案新增第二個快取的分層。</span><span class="sxs-lookup"><span data-stu-id="4db8e-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="4db8e-167">資料庫快取仍會使用自己的記憶體來快取資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4db8e-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="4db8e-168">這種模式的目的是讓應用程式使用小型專用快取來設定 database engine，並允許 Windows 捐贈備用記憶體，以進一步改善資料庫資料的快取。</span><span class="sxs-lookup"><span data-stu-id="4db8e-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-169">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-170">否</span><span class="sxs-lookup"><span data-stu-id="4db8e-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-171">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="4db8e-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-173">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-174">False, True</span><span class="sxs-lookup"><span data-stu-id="4db8e-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-175">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-176">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-177">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-178">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-179">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-180">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-181">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-182">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-183">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-184">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-185">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-186">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-187">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-188">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-189">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-190">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="4db8e-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="4db8e-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="4db8e-192">152</span><span class="sxs-lookup"><span data-stu-id="4db8e-192">152</span></span>  

<span data-ttu-id="4db8e-193">此參數可控制 ESE 處理 i/o 作業的方式。</span><span class="sxs-lookup"><span data-stu-id="4db8e-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="4db8e-194">這些值可以設定為 0 (一般作業 JET_IOPriorityNormal) ，或針對低優先順序作業的 1 (JET_IOPriorityLow) 。</span><span class="sxs-lookup"><span data-stu-id="4db8e-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="4db8e-195">當優先權設定為 JET_IOPriorityLow 時，ESE 會使用 Windows Vista 中提供的新執行緒 i/o 優先權功能來減少執行緒的 i/o 優先順序，以便在新的低優先順序發行後續的 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="4db8e-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="4db8e-196">**Windows Vista：**  JET_paramIOPriority 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="4db8e-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-197">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-198">0</span><span class="sxs-lookup"><span data-stu-id="4db8e-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-199">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-200">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-201">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="4db8e-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-203">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-204">執行個體</span><span class="sxs-lookup"><span data-stu-id="4db8e-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-205">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-206">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-207">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-208">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-209">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-210">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-211">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-212">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-213">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-214">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-215">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-216">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-217">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4db8e-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="4db8e-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="4db8e-220">30</span><span class="sxs-lookup"><span data-stu-id="4db8e-220">30</span></span> 

<span data-ttu-id="4db8e-221">此參數控制一次可在主機作業系統中佇列的資料庫檔案 i/o 數量。</span><span class="sxs-lookup"><span data-stu-id="4db8e-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="4db8e-222">較大的參數值可大幅協助大型資料庫應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="4db8e-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="4db8e-223">**WINDOWS XP 和 Windows Server 2003：**  Windows XP 和 Windows Server 2003 會忽略此參數，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="4db8e-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-224">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-225"><strong>Windows 2000： </strong>  64</span><span class="sxs-lookup"><span data-stu-id="4db8e-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="4db8e-226"><strong>Windows Vista：</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="4db8e-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-227">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-228">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-229">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-230"><strong>Windows 2000：</strong>  8 –2147483647</span><span class="sxs-lookup"><span data-stu-id="4db8e-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="4db8e-231"><strong>Windows Vista：</strong>  0-65536</span><span class="sxs-lookup"><span data-stu-id="4db8e-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-232">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-233">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-234">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-235">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-236">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-237">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-238">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-239">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-240">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-241">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-242">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-243">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-244">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-245">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-246">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-247">全部</span><span class="sxs-lookup"><span data-stu-id="4db8e-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="4db8e-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="4db8e-249">164</span><span class="sxs-lookup"><span data-stu-id="4db8e-249">164</span></span>  

<span data-ttu-id="4db8e-250">合併的讀取作業可分組的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4db8e-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-251">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-252">262144</span><span class="sxs-lookup"><span data-stu-id="4db8e-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-253">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-254">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-255">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="4db8e-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-257">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-258">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-259">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-260">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-261">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-262">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-263">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-264">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-265">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-266">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-267">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-268">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-269">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-270">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-271">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4db8e-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="4db8e-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="4db8e-274">165</span><span class="sxs-lookup"><span data-stu-id="4db8e-274">165</span></span>  

<span data-ttu-id="4db8e-275">合併寫入作業可分組的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4db8e-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-276">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-277">393216</span><span class="sxs-lookup"><span data-stu-id="4db8e-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-278">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-279">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-280">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="4db8e-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-282">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-283">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-284">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-285">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-286">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-287">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-288">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-289">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-290">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-291">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-292">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-293">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-294">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-295">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-296">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4db8e-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="4db8e-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="4db8e-299">166</span><span class="sxs-lookup"><span data-stu-id="4db8e-299">166</span></span>  

<span data-ttu-id="4db8e-300">結合的寫入 i/o 作業可能會有空隙的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4db8e-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-301">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-302">262144</span><span class="sxs-lookup"><span data-stu-id="4db8e-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-303">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-304">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-305">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="4db8e-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-307">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-308">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-309">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-310">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-311">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-312">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-313">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-314">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-315">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-316">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-317">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-318">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-319">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-320">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-321">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4db8e-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4db8e-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="4db8e-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="4db8e-324">167</span><span class="sxs-lookup"><span data-stu-id="4db8e-324">167</span></span>  

<span data-ttu-id="4db8e-325">結合的讀取 i/o 作業可能會有空隙的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4db8e-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-326">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4db8e-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-327">393216</span><span class="sxs-lookup"><span data-stu-id="4db8e-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-328">輸入：</span><span class="sxs-lookup"><span data-stu-id="4db8e-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-329">整數</span><span class="sxs-lookup"><span data-stu-id="4db8e-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-330">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="4db8e-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-332">範圍：</span><span class="sxs-lookup"><span data-stu-id="4db8e-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-333">全球</span><span class="sxs-lookup"><span data-stu-id="4db8e-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-334">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-335">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-336">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4db8e-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-337">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-338">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4db8e-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-339">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-340">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-341">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-342">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4db8e-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-343">Yes</span><span class="sxs-lookup"><span data-stu-id="4db8e-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-344">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4db8e-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-345">No</span><span class="sxs-lookup"><span data-stu-id="4db8e-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-346">可用性：</span><span class="sxs-lookup"><span data-stu-id="4db8e-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4db8e-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4db8e-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="4db8e-348">規格需求</span><span class="sxs-lookup"><span data-stu-id="4db8e-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-349"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4db8e-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4db8e-350">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4db8e-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4db8e-351"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4db8e-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4db8e-352">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4db8e-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4db8e-353"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4db8e-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4db8e-354">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4db8e-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4db8e-355">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4db8e-355">See Also</span></span>

[<span data-ttu-id="4db8e-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4db8e-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4db8e-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="4db8e-357">JetInit</span></span>](./jetinit-function.md)
