---
description: 深入瞭解：暫存資料庫參數
title: 暫存資料庫參數
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194592"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="e9c6c-103">暫存資料庫參數</span><span class="sxs-lookup"><span data-stu-id="e9c6c-103">Temporary Database Parameters</span></span>


<span data-ttu-id="e9c6c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e9c6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="e9c6c-105">暫存資料庫參數</span><span class="sxs-lookup"><span data-stu-id="e9c6c-105">Temporary Database Parameters</span></span>

<span data-ttu-id="e9c6c-106">本主題包含用於暫存資料庫的參數。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="e9c6c-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="e9c6c-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="e9c6c-108">46</span><span class="sxs-lookup"><span data-stu-id="e9c6c-108">46</span></span>  

<span data-ttu-id="e9c6c-109">此參數控制臨時表中交易的使用。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="e9c6c-110">當此參數為 false 時，臨時表會更快，但無法回復在交易中所做的任何更新。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-111">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e9c6c-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-112">對</span><span class="sxs-lookup"><span data-stu-id="e9c6c-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="e9c6c-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-115">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-116">False, True</span><span class="sxs-lookup"><span data-stu-id="e9c6c-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-117">範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-118">執行個體</span><span class="sxs-lookup"><span data-stu-id="e9c6c-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-119">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-120">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-121">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-122">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-123">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-124">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-125">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-126">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-127">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-128">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-129">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-130">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-131">可用性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-132">全部</span><span class="sxs-lookup"><span data-stu-id="e9c6c-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9c6c-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="e9c6c-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="e9c6c-134">19</span><span class="sxs-lookup"><span data-stu-id="e9c6c-134">19</span></span>  

<span data-ttu-id="e9c6c-135">此參數會控制暫存資料庫的初始大小。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="e9c6c-136">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-136">The size is in database pages.</span></span> <span data-ttu-id="e9c6c-137">大小為零表示應該使用一般資料庫的預設大小。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="e9c6c-138">小型應用程式通常需要將暫存資料庫設定為盡可能小。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="e9c6c-139">將此參數設定為14將可以達到最小的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="e9c6c-140">請注意，將 **JET_paramMaxTemporaryTables** 設定為零，也可以完全消除暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-141">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e9c6c-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-142">0</span><span class="sxs-lookup"><span data-stu-id="e9c6c-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-143">輸入：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-144">整數</span><span class="sxs-lookup"><span data-stu-id="e9c6c-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-145">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-146">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="e9c6c-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-147">範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-148">執行個體</span><span class="sxs-lookup"><span data-stu-id="e9c6c-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-149">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-150">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-151">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-152">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-153">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-154">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-155">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-156">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-157">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-158">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-159">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-160">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-161">可用性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-162">全部</span><span class="sxs-lookup"><span data-stu-id="e9c6c-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e9c6c-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="e9c6c-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="e9c6c-164">1</span><span class="sxs-lookup"><span data-stu-id="e9c6c-164">1</span></span>  

<span data-ttu-id="e9c6c-165">此參數表示將包含實例之暫存資料庫之資料夾或檔案的相對或絕對檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="e9c6c-166">如果路徑是要包含暫存資料庫的資料夾，則必須以反斜線字元作為結尾。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="e9c6c-167">暫存資料庫是用來保存在處理 ESE API 資訊呼叫、建立索引或儲存臨時表內容的過程中所產生的暫時性資料。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="e9c6c-168">**注意**  如果指定相對路徑，則會相對於裝載使用資料庫引擎的應用程式之進程的目前工作目錄。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-169">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e9c6c-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-170">&quot;.tmp&quot;</span><span class="sxs-lookup"><span data-stu-id="e9c6c-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-171">輸入：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-172">路徑 (字串) </span><span class="sxs-lookup"><span data-stu-id="e9c6c-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-173">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-174">0–247個字元</span><span class="sxs-lookup"><span data-stu-id="e9c6c-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-175">範圍：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-176">執行個體</span><span class="sxs-lookup"><span data-stu-id="e9c6c-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-177">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-178">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-179">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-180">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-181">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-182">Yes</span><span class="sxs-lookup"><span data-stu-id="e9c6c-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-183">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-184">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-185">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-186">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-187">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-188">No</span><span class="sxs-lookup"><span data-stu-id="e9c6c-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-189">可用性：</span><span class="sxs-lookup"><span data-stu-id="e9c6c-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e9c6c-190">全部</span><span class="sxs-lookup"><span data-stu-id="e9c6c-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e9c6c-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9c6c-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e9c6c-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e9c6c-193">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9c6c-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e9c6c-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e9c6c-195">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9c6c-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e9c6c-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e9c6c-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e9c6c-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e9c6c-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9c6c-198">See Also</span></span>

[<span data-ttu-id="e9c6c-199">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="e9c6c-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="e9c6c-200">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="e9c6c-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e9c6c-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="e9c6c-201">JetInit</span></span>](./jetinit-function.md)
