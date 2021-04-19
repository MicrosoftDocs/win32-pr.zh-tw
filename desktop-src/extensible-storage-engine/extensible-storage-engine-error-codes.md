---
description: 深入瞭解：可擴充儲存引擎錯誤碼
title: 可擴充儲存引擎錯誤碼
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984691"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="c6bc0-103">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c6bc0-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="c6bc0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c6bc0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="c6bc0-105">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c6bc0-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="c6bc0-106">下列錯誤碼 (旗標) 可延伸儲存引擎 API 中的函式使用。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="c6bc0-107">[JET_ERR](./jet-err.md)值為零應該會被視為成功。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6bc0-108">Success</span><span class="sxs-lookup"><span data-stu-id="c6bc0-108">Success</span></span></p></th>
<th><p><span data-ttu-id="c6bc0-109">Description</span><span class="sxs-lookup"><span data-stu-id="c6bc0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="c6bc0-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-111">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6bc0-112">大於零的 [JET_ERR](./jet-err.md) 值應解釋為警告。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6bc0-113">警告</span><span class="sxs-lookup"><span data-stu-id="c6bc0-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="c6bc0-114">Description</span><span class="sxs-lookup"><span data-stu-id="c6bc0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="c6bc0-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="c6bc0-116">321</span><span class="sxs-lookup"><span data-stu-id="c6bc0-116">321</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-117">版本存放區仍處於使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-117">The version store is still active.</span></span> <span data-ttu-id="c6bc0-118">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="c6bc0-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="c6bc0-120">345</span><span class="sxs-lookup"><span data-stu-id="c6bc0-120">345</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-121">非唯一索引的搜尋產生了唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="c6bc0-122">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="c6bc0-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="c6bc0-124">406</span><span class="sxs-lookup"><span data-stu-id="c6bc0-124">406</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-125">資料庫資料行是分隔的 long 值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-125">A database column is a separated long value.</span></span> <span data-ttu-id="c6bc0-126">記錄管理員會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="c6bc0-128">558</span><span class="sxs-lookup"><span data-stu-id="c6bc0-128">558</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-129">現有的記錄檔有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="c6bc0-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="c6bc0-131">559</span><span class="sxs-lookup"><span data-stu-id="c6bc0-131">559</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-132">現有的記錄檔不是連續的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="c6bc0-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="c6bc0-134">564</span><span class="sxs-lookup"><span data-stu-id="c6bc0-134">564</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-135">此錯誤僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="c6bc0-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="c6bc0-137">578</span><span class="sxs-lookup"><span data-stu-id="c6bc0-137">578</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-138">為還原指定的 TargetInstance 正在執行中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="c6bc0-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="c6bc0-140">595</span><span class="sxs-lookup"><span data-stu-id="c6bc0-140">595</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-141">資料庫損毀已修復。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="c6bc0-143">1004</span><span class="sxs-lookup"><span data-stu-id="c6bc0-143">1004</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-144">資料行具有 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="c6bc0-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="c6bc0-146">1006</span><span class="sxs-lookup"><span data-stu-id="c6bc0-146">1006</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-147">緩衝區對資料而言太小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="c6bc0-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="c6bc0-149">1007</span><span class="sxs-lookup"><span data-stu-id="c6bc0-149">1007</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-150">資料庫已附加。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="c6bc0-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="c6bc0-152">1009</span><span class="sxs-lookup"><span data-stu-id="c6bc0-152">1009</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-153">所嘗試的排序沒有足夠的記憶體可完成。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="c6bc0-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="c6bc0-155">1039</span><span class="sxs-lookup"><span data-stu-id="c6bc0-155">1039</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-156">搜尋期間找不到完全相符的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="c6bc0-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="c6bc0-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="c6bc0-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-159">搜尋期間找不到完全相符的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="c6bc0-160">記錄管理員會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="c6bc0-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="c6bc0-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="c6bc0-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-163">搜尋期間找不到完全相符的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="c6bc0-164">記錄管理員會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="c6bc0-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="c6bc0-166">1055</span><span class="sxs-lookup"><span data-stu-id="c6bc0-166">1055</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-167">沒有任何延伸的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="c6bc0-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="c6bc0-169">1058</span><span class="sxs-lookup"><span data-stu-id="c6bc0-169">1058</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-170">未發生任何閒置活動。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="c6bc0-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="c6bc0-172">1067</span><span class="sxs-lookup"><span data-stu-id="c6bc0-172">1067</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-173">交易層級0沒有寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="c6bc0-175">1068</span><span class="sxs-lookup"><span data-stu-id="c6bc0-175">1068</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-176">此資料行設定為 <strong>Null</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="c6bc0-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="c6bc0-178">1301</span><span class="sxs-lookup"><span data-stu-id="c6bc0-178">1301</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-179">已開啟空白資料表。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="c6bc0-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="c6bc0-181">1327</span><span class="sxs-lookup"><span data-stu-id="c6bc0-181">1327</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-182">系統清除會在資料表上開啟資料指標。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="c6bc0-184">1415</span><span class="sxs-lookup"><span data-stu-id="c6bc0-184">1415</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-185">必須移除過期的索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="c6bc0-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="c6bc0-187">1512</span><span class="sxs-lookup"><span data-stu-id="c6bc0-187">1512</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-188">最大長度太大且已被截斷。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="c6bc0-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="c6bc0-190">1520</span><span class="sxs-lookup"><span data-stu-id="c6bc0-190">1520</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-191">BLOB 值已從記錄移至不同的大型 Blob 儲存體。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="c6bc0-192"><strong>注意</strong> 此錯誤僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="c6bc0-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="c6bc0-194">1531</span><span class="sxs-lookup"><span data-stu-id="c6bc0-194">1531</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-195">因為對應的資料行識別碼或 <em>itagSequence</em> 成員來自要求列舉的 <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> 結構，所以不會傳回資料行值為 null。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="c6bc0-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="c6bc0-197">1532</span><span class="sxs-lookup"><span data-stu-id="c6bc0-197">1532</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-198">因為無法從現有的資料重建資料行值，所以不會傳回這些值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="c6bc0-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="c6bc0-200">1533</span><span class="sxs-lookup"><span data-stu-id="c6bc0-200">1533</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-201">未要求列舉的現有資料行值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="c6bc0-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="c6bc0-203">1534</span><span class="sxs-lookup"><span data-stu-id="c6bc0-203">1534</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-204">在列舉期間，資料行值已被截斷為要求的大小限制。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="c6bc0-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="c6bc0-206">1535</span><span class="sxs-lookup"><span data-stu-id="c6bc0-206">1535</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-207">資料行值存在但未由要求傳回。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="c6bc0-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="c6bc0-209">1536</span><span class="sxs-lookup"><span data-stu-id="c6bc0-209">1536</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-210">因為設定 JET_bitEnumerateCompressOutput，所以 JET_COLUMNENUM 中傳回資料行值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="c6bc0-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="c6bc0-212">1537</span><span class="sxs-lookup"><span data-stu-id="c6bc0-212">1537</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-213">資料行值會設定為數據行的預設值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="c6bc0-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="c6bc0-215">1610</span><span class="sxs-lookup"><span data-stu-id="c6bc0-215">1610</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-216">資料已經變更。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="c6bc0-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="c6bc0-218">1618</span><span class="sxs-lookup"><span data-stu-id="c6bc0-218">1618</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-219">正在使用新的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="c6bc0-221">1813</span><span class="sxs-lookup"><span data-stu-id="c6bc0-221">1813</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-222">資料庫檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="c6bc0-224">1908</span><span class="sxs-lookup"><span data-stu-id="c6bc0-224">1908</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-225">閒置登錄已滿。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="c6bc0-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="c6bc0-227">2000</span><span class="sxs-lookup"><span data-stu-id="c6bc0-227">2000</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-228">已在指定的資料庫上執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="c6bc0-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="c6bc0-230">2001</span><span class="sxs-lookup"><span data-stu-id="c6bc0-230">2001</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-231">未在指定的資料庫上執行線上磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="c6bc0-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="c6bc0-233">2100</span><span class="sxs-lookup"><span data-stu-id="c6bc0-233">2100</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-234">不存在的回呼函數已取消註冊。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c6bc0-235">小於零的 [JET_ERR](./jet-err.md) 值應視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6bc0-236">Errors</span><span class="sxs-lookup"><span data-stu-id="c6bc0-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="c6bc0-237">Description</span><span class="sxs-lookup"><span data-stu-id="c6bc0-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="c6bc0-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="c6bc0-239">-1</span><span class="sxs-lookup"><span data-stu-id="c6bc0-239">-1</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-240">函數尚未執行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="c6bc0-242">-100</span><span class="sxs-lookup"><span data-stu-id="c6bc0-242">-100</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-243">資源失敗模擬器失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="c6bc0-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="c6bc0-245">-101</span><span class="sxs-lookup"><span data-stu-id="c6bc0-245">-101</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-246">資源失敗模擬器尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="c6bc0-247">JET_errFileClose</span></span><br />
<span data-ttu-id="c6bc0-248">-102</span><span class="sxs-lookup"><span data-stu-id="c6bc0-248">-102</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-249">無法關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="c6bc0-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="c6bc0-251">-103</span><span class="sxs-lookup"><span data-stu-id="c6bc0-251">-103</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-252">無法啟動執行緒。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="c6bc0-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="c6bc0-254">-105</span><span class="sxs-lookup"><span data-stu-id="c6bc0-254">-105</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-255">因為 IOs 太多，所以系統正在忙碌中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="c6bc0-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="c6bc0-257">-106</span><span class="sxs-lookup"><span data-stu-id="c6bc0-257">-106</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-258">無法執行要求的非同步工作。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="c6bc0-259">JET_errInternalError</span></span><br />
<span data-ttu-id="c6bc0-260">-107</span><span class="sxs-lookup"><span data-stu-id="c6bc0-260">-107</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-261">發生嚴重的內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="c6bc0-263">-255</span><span class="sxs-lookup"><span data-stu-id="c6bc0-263">-255</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-264">緩衝區相依性設定不正確，且發生復原失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="c6bc0-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="c6bc0-266">-322</span><span class="sxs-lookup"><span data-stu-id="c6bc0-266">-322</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-267">版本已經存在，而且發生復原失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="c6bc0-268">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="c6bc0-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="c6bc0-270">-323</span><span class="sxs-lookup"><span data-stu-id="c6bc0-270">-323</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-271">已達到頁面界限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-271">The page boundary has been reached.</span></span> <span data-ttu-id="c6bc0-272">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="c6bc0-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="c6bc0-274">-324</span><span class="sxs-lookup"><span data-stu-id="c6bc0-274">-324</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-275">已達到金鑰界限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-275">The key boundary has been reached.</span></span> <span data-ttu-id="c6bc0-276">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="c6bc0-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="c6bc0-278">-327</span><span class="sxs-lookup"><span data-stu-id="c6bc0-278">-327</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-279">資料庫已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-279">The database is corrupt.</span></span> <span data-ttu-id="c6bc0-280">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="c6bc0-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="c6bc0-282">-328</span><span class="sxs-lookup"><span data-stu-id="c6bc0-282">-328</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-283">書簽在資料庫中沒有對應的位址。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="c6bc0-284">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="c6bc0-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="c6bc0-286">-334</span><span class="sxs-lookup"><span data-stu-id="c6bc0-286">-334</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-287">作業系統的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-287">The call to the operating system failed.</span></span> <span data-ttu-id="c6bc0-288">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="c6bc0-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="c6bc0-290">-338</span><span class="sxs-lookup"><span data-stu-id="c6bc0-290">-338</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-291">父資料庫已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-291">A parent database is corrupt.</span></span> <span data-ttu-id="c6bc0-292">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="c6bc0-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="c6bc0-294">-340</span><span class="sxs-lookup"><span data-stu-id="c6bc0-294">-340</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-295">AvailExt 快取不符合 B + 樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="c6bc0-296">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="c6bc0-298">-341</span><span class="sxs-lookup"><span data-stu-id="c6bc0-298">-341</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-299">AllAvailExt 空間樹狀結構已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="c6bc0-300">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c6bc0-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="c6bc0-302">-342</span><span class="sxs-lookup"><span data-stu-id="c6bc0-302">-342</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-303">配置 AvailExt 快取節點時發生記憶體不足的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="c6bc0-304">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="c6bc0-306">-343</span><span class="sxs-lookup"><span data-stu-id="c6bc0-306">-343</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-307">OwnExt 空間樹狀結構已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="c6bc0-308">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="c6bc0-310">-344</span><span class="sxs-lookup"><span data-stu-id="c6bc0-310">-344</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-311">目前頁面上的 Dbtime 大於全域資料庫 Dbtime。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="c6bc0-312">目錄管理員會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="c6bc0-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="c6bc0-314">-346</span><span class="sxs-lookup"><span data-stu-id="c6bc0-314">-346</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-315">嘗試建立索引項目的索引鍵失敗，因為索引鍵會被截斷，而且索引定義不允許索引鍵截斷。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="c6bc0-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="c6bc0-317">-408</span><span class="sxs-lookup"><span data-stu-id="c6bc0-317">-408</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-318">金鑰太大。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-318">The key is too large.</span></span> <span data-ttu-id="c6bc0-319">記錄管理員會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="c6bc0-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="c6bc0-321">-500</span><span class="sxs-lookup"><span data-stu-id="c6bc0-321">-500</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-322">無法重做記錄的作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="c6bc0-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="c6bc0-324">-501</span><span class="sxs-lookup"><span data-stu-id="c6bc0-324">-501</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-325">記錄檔已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="c6bc0-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="c6bc0-327">-503</span><span class="sxs-lookup"><span data-stu-id="c6bc0-327">-503</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-328">未提供備份目錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="c6bc0-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="c6bc0-330">-504</span><span class="sxs-lookup"><span data-stu-id="c6bc0-330">-504</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-331">備份目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="c6bc0-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="c6bc0-333">-505</span><span class="sxs-lookup"><span data-stu-id="c6bc0-333">-505</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-334">備份已在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c6bc0-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="c6bc0-336">-506</span><span class="sxs-lookup"><span data-stu-id="c6bc0-336">-506</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-337">還原進行中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="c6bc0-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="c6bc0-339">-509</span><span class="sxs-lookup"><span data-stu-id="c6bc0-339">-509</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-340">檢查點缺少記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="c6bc0-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="c6bc0-342">-510</span><span class="sxs-lookup"><span data-stu-id="c6bc0-342">-510</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-343">寫入記錄檔時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="c6bc0-345">-511</span><span class="sxs-lookup"><span data-stu-id="c6bc0-345">-511</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-346">復原失敗後，嘗試寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="c6bc0-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="c6bc0-348">-512</span><span class="sxs-lookup"><span data-stu-id="c6bc0-348">-512</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-349">復原重做失敗時，嘗試寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="c6bc0-351">-513</span><span class="sxs-lookup"><span data-stu-id="c6bc0-351">-513</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-352">記錄檔的名稱與內部世代編號不相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="c6bc0-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="c6bc0-354">-514</span><span class="sxs-lookup"><span data-stu-id="c6bc0-354">-514</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-355">記錄檔的版本與 ESE 版本不相容。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="c6bc0-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="c6bc0-357">-515</span><span class="sxs-lookup"><span data-stu-id="c6bc0-357">-515</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-358">下一個記錄檔中的時間戳記不符合預期的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="c6bc0-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="c6bc0-360">-516</span><span class="sxs-lookup"><span data-stu-id="c6bc0-360">-516</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-361">記錄檔並非使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c6bc0-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="c6bc0-363">-517</span><span class="sxs-lookup"><span data-stu-id="c6bc0-363">-517</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-364">記錄緩衝區太小，無法進行復原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="c6bc0-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="c6bc0-366">-519</span><span class="sxs-lookup"><span data-stu-id="c6bc0-366">-519</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-367">已超過記錄檔的最大數目。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="c6bc0-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="c6bc0-369">-520</span><span class="sxs-lookup"><span data-stu-id="c6bc0-369">-520</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-370">沒有進行中的備份。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="c6bc0-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="c6bc0-372">-521</span><span class="sxs-lookup"><span data-stu-id="c6bc0-372">-521</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-373">備份呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="c6bc0-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="c6bc0-375">-523</span><span class="sxs-lookup"><span data-stu-id="c6bc0-375">-523</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-376">目前無法執行備份。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="c6bc0-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="c6bc0-378">-524</span><span class="sxs-lookup"><span data-stu-id="c6bc0-378">-524</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-379">無法刪除備份檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="c6bc0-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="c6bc0-381">-525</span><span class="sxs-lookup"><span data-stu-id="c6bc0-381">-525</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-382">無法建立備份臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="c6bc0-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="c6bc0-384">-526</span><span class="sxs-lookup"><span data-stu-id="c6bc0-384">-526</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-385">已啟用迴圈記錄;無法執行增量備份。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="c6bc0-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="c6bc0-387">-527</span><span class="sxs-lookup"><span data-stu-id="c6bc0-387">-527</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-388">資料已還原，但發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="c6bc0-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="c6bc0-390">-528</span><span class="sxs-lookup"><span data-stu-id="c6bc0-390">-528</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-391">遺失目前的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="c6bc0-393">-529</span><span class="sxs-lookup"><span data-stu-id="c6bc0-393">-529</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-394">記錄磁碟已滿。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="c6bc0-396">-530</span><span class="sxs-lookup"><span data-stu-id="c6bc0-396">-530</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-397">記錄檔有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="c6bc0-399">-531</span><span class="sxs-lookup"><span data-stu-id="c6bc0-399">-531</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-400">資料庫檔案有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="c6bc0-402">-532</span><span class="sxs-lookup"><span data-stu-id="c6bc0-402">-532</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-403">檢查點檔案有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="c6bc0-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="c6bc0-405">-533</span><span class="sxs-lookup"><span data-stu-id="c6bc0-405">-533</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-406">找不到檢查點檔案或已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="c6bc0-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="c6bc0-408">-534</span><span class="sxs-lookup"><span data-stu-id="c6bc0-408">-534</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-409">復原期間找不到 [資料庫修補檔案] 頁面。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="c6bc0-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="c6bc0-411">-535</span><span class="sxs-lookup"><span data-stu-id="c6bc0-411">-535</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-412">資料庫修補檔案頁面無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="c6bc0-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="c6bc0-414">-536</span><span class="sxs-lookup"><span data-stu-id="c6bc0-414">-536</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-415">因為從記錄檔讀取記錄檔突然失敗，所以重做突然終止。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="c6bc0-417">-537</span><span class="sxs-lookup"><span data-stu-id="c6bc0-417">-537</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-418">此旗標為保留。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="c6bc0-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="c6bc0-420">-538</span><span class="sxs-lookup"><span data-stu-id="c6bc0-420">-538</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-421">硬還原偵測到備份組遺失資料庫修補檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="c6bc0-423">-539</span><span class="sxs-lookup"><span data-stu-id="c6bc0-423">-539</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-424">資料庫不屬於目前的記錄檔集。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="c6bc0-426">-540</span><span class="sxs-lookup"><span data-stu-id="c6bc0-426">-540</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-427">此旗標為保留。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="c6bc0-429">-541</span><span class="sxs-lookup"><span data-stu-id="c6bc0-429">-541</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-430">實際的記錄檔大小與 <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>不相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="c6bc0-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="c6bc0-432">-542</span><span class="sxs-lookup"><span data-stu-id="c6bc0-432">-542</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-433">找不到檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="c6bc0-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="c6bc0-435">-543</span><span class="sxs-lookup"><span data-stu-id="c6bc0-435">-543</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-436">遺漏修復所需的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="c6bc0-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="c6bc0-438">-544</span><span class="sxs-lookup"><span data-stu-id="c6bc0-438">-544</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-439">當您應該改為使用還原時，就必須在備份資料庫上使用軟復原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="c6bc0-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="c6bc0-441">-545</span><span class="sxs-lookup"><span data-stu-id="c6bc0-441">-545</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-442">已復原資料庫，但復原期間使用的記錄檔大小與 <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>不相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="c6bc0-444">-546</span><span class="sxs-lookup"><span data-stu-id="c6bc0-444">-546</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-445">記錄檔磁區大小不符合目前磁片區的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="c6bc0-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="c6bc0-447">-547</span><span class="sxs-lookup"><span data-stu-id="c6bc0-447">-547</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-448">已復原資料庫，但在復原期間使用的記錄檔磁區大小 () 不符合目前磁片區的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="c6bc0-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="c6bc0-450">-548</span><span class="sxs-lookup"><span data-stu-id="c6bc0-450">-548</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-451">已復原資料庫，但目前的順序中所有可能的記錄層代都已使用。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="c6bc0-452">必須刪除所有記錄檔和檢查點檔案，而且必須備份資料庫，才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="c6bc0-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="c6bc0-454">-549</span><span class="sxs-lookup"><span data-stu-id="c6bc0-454">-549</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-455">重新執行未記錄資料的串流檔案作業時發生不合法的嘗試。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="c6bc0-456">這可能是因為嘗試向前復原已啟用迴圈記錄所致。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="c6bc0-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="c6bc0-458">-550</span><span class="sxs-lookup"><span data-stu-id="c6bc0-458">-550</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-459">資料庫未完全關閉。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="c6bc0-460">必須先執行復原，才能適當完成先前關機的資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="c6bc0-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="c6bc0-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="c6bc0-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-463">此錯誤已淘汰，且已由 JET_errDatabaseDirtyShutdown 取代。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="c6bc0-465">-551</span><span class="sxs-lookup"><span data-stu-id="c6bc0-465">-551</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-466">資料庫的上次一致時間尚未相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="c6bc0-468">-552</span><span class="sxs-lookup"><span data-stu-id="c6bc0-468">-552</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-469">此備份不會產生資料庫修補檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="c6bc0-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="c6bc0-471">-553</span><span class="sxs-lookup"><span data-stu-id="c6bc0-471">-553</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-472">開始記錄檔編號太低，無法進行還原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="c6bc0-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="c6bc0-474">-554</span><span class="sxs-lookup"><span data-stu-id="c6bc0-474">-554</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-475">還原的起始記錄檔編號過高。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="c6bc0-477">-555</span><span class="sxs-lookup"><span data-stu-id="c6bc0-477">-555</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-478">還原記錄檔有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="c6bc0-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="c6bc0-480">-556</span><span class="sxs-lookup"><span data-stu-id="c6bc0-480">-556</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-481">還原記錄檔不是連續的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="c6bc0-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="c6bc0-483">-557</span><span class="sxs-lookup"><span data-stu-id="c6bc0-483">-557</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-484">有些還原記錄檔遺失。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="c6bc0-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="c6bc0-486">-560</span><span class="sxs-lookup"><span data-stu-id="c6bc0-486">-560</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-487">資料庫在嘗試執行增量備份之前，遺漏了先前的完整備份。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="c6bc0-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="c6bc0-489">-561</span><span class="sxs-lookup"><span data-stu-id="c6bc0-489">-561</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-490">備份資料庫大小不是資料庫頁面大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="c6bc0-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="c6bc0-492">-562</span><span class="sxs-lookup"><span data-stu-id="c6bc0-492">-562</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-493">目前嘗試升級資料庫已停止，因為資料庫已經是最新的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="c6bc0-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="c6bc0-495">-563</span><span class="sxs-lookup"><span data-stu-id="c6bc0-495">-563</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-496">資料庫只會部分轉換為目前的格式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="c6bc0-497">您必須從備份還原資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="c6bc0-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="c6bc0-499">-565</span><span class="sxs-lookup"><span data-stu-id="c6bc0-499">-565</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-500">部分目前的記錄檔遺漏了連續還原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="c6bc0-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="c6bc0-502">-566</span><span class="sxs-lookup"><span data-stu-id="c6bc0-502">-566</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-503">頁面上的 dbtime 小於記錄中的 dbtimeBefore。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="c6bc0-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="c6bc0-505">-567</span><span class="sxs-lookup"><span data-stu-id="c6bc0-505">-567</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-506">頁面上的 dbtime 會在記錄中的 dbtimeBefore 之前。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="c6bc0-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="c6bc0-508">-569</span><span class="sxs-lookup"><span data-stu-id="c6bc0-508">-569</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-509">備份期間缺少某些記錄檔或資料庫修補檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="c6bc0-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="c6bc0-511">-570</span><span class="sxs-lookup"><span data-stu-id="c6bc0-511">-570</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-512">在硬還原期間設定的備份中偵測到寫入損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="c6bc0-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="c6bc0-514">-571</span><span class="sxs-lookup"><span data-stu-id="c6bc0-514">-571</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-515">在硬復原期間偵測到寫入損毀 (記錄檔不是備份組) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="c6bc0-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="c6bc0-517">-573</span><span class="sxs-lookup"><span data-stu-id="c6bc0-517">-573</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-518">在硬還原期間于備份組中偵測到損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="c6bc0-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="c6bc0-520">-574</span><span class="sxs-lookup"><span data-stu-id="c6bc0-520">-574</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-521">硬碟上偵測到損毀 (記錄檔不是備份組) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="c6bc0-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="c6bc0-523">-575</span><span class="sxs-lookup"><span data-stu-id="c6bc0-523">-575</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-524">嘗試升級資料庫時，無法啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="c6bc0-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="c6bc0-526">-577</span><span class="sxs-lookup"><span data-stu-id="c6bc0-526">-577</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-527">找不到為還原指定的 TargetInstance 或記錄檔不相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="c6bc0-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="c6bc0-529">-579</span><span class="sxs-lookup"><span data-stu-id="c6bc0-529">-579</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-530">資料庫引擎已成功重新執行交易記錄中的所有作業，以執行損毀復原，但呼叫端選擇停止復原而不回復未認可的更新。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="c6bc0-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="c6bc0-532">-580</span><span class="sxs-lookup"><span data-stu-id="c6bc0-532">-580</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-533">要還原的資料庫不是來自相同的陰影複本備份。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="c6bc0-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="c6bc0-535">-581</span><span class="sxs-lookup"><span data-stu-id="c6bc0-535">-581</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-536">您可以從陰影複本備份集的資料庫進行軟復原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c6bc0-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="c6bc0-538">-601</span><span class="sxs-lookup"><span data-stu-id="c6bc0-538">-601</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-539">Unicode 轉譯緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="c6bc0-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="c6bc0-541">-602</span><span class="sxs-lookup"><span data-stu-id="c6bc0-541">-602</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-542">Unicode 正規化失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="c6bc0-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="c6bc0-544">-603</span><span class="sxs-lookup"><span data-stu-id="c6bc0-544">-603</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-545">作業系統未提供 Unicode 正規化的支援，且未指定正規化回呼。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="c6bc0-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="c6bc0-547">-610</span><span class="sxs-lookup"><span data-stu-id="c6bc0-547">-610</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-548">現有的記錄檔有錯誤的簽章。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="c6bc0-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="c6bc0-550">-611</span><span class="sxs-lookup"><span data-stu-id="c6bc0-550">-611</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-551">現有的記錄檔不是連續的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="c6bc0-553">-612</span><span class="sxs-lookup"><span data-stu-id="c6bc0-553">-612</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-554">備份期間在記錄檔中發現總和檢查碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="c6bc0-556">-613</span><span class="sxs-lookup"><span data-stu-id="c6bc0-556">-613</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-557">此旗標為保留。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="c6bc0-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="c6bc0-559">-614</span><span class="sxs-lookup"><span data-stu-id="c6bc0-559">-614</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-560">檢查點和目前世代之間有太多未完成的層代。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="c6bc0-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="c6bc0-562">-615</span><span class="sxs-lookup"><span data-stu-id="c6bc0-562">-615</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-563">在非備份資料庫的資料庫上嘗試進行硬復原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="c6bc0-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="c6bc0-565">-900</span><span class="sxs-lookup"><span data-stu-id="c6bc0-565">-900</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-566">有不正確 grbit 參數。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c6bc0-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="c6bc0-568">-1000</span><span class="sxs-lookup"><span data-stu-id="c6bc0-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-569">終止正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="c6bc0-571">-1001</span><span class="sxs-lookup"><span data-stu-id="c6bc0-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-572">不支援此 API 元素。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="c6bc0-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="c6bc0-574">-1002</span><span class="sxs-lookup"><span data-stu-id="c6bc0-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-575">使用了不正確名稱。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c6bc0-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="c6bc0-577">-1003</span><span class="sxs-lookup"><span data-stu-id="c6bc0-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-578">使用了不正確 API 參數。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="c6bc0-580">-1008</span><span class="sxs-lookup"><span data-stu-id="c6bc0-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-581">嘗試附加至唯讀資料庫檔案以進行讀取/寫入作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="c6bc0-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="c6bc0-583">-1010</span><span class="sxs-lookup"><span data-stu-id="c6bc0-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-584">有不正確資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c6bc0-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="c6bc0-586">-1011</span><span class="sxs-lookup"><span data-stu-id="c6bc0-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-587">系統記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="c6bc0-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="c6bc0-589">-1012</span><span class="sxs-lookup"><span data-stu-id="c6bc0-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-590">已達到資料庫大小上限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="c6bc0-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="c6bc0-592">-1013</span><span class="sxs-lookup"><span data-stu-id="c6bc0-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-593">資料表已超出資料指標。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="c6bc0-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="c6bc0-595">-1014</span><span class="sxs-lookup"><span data-stu-id="c6bc0-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-596">資料庫超出頁面緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="c6bc0-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="c6bc0-598">-1015</span><span class="sxs-lookup"><span data-stu-id="c6bc0-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-599">有太多索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="c6bc0-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="c6bc0-601">-1016</span><span class="sxs-lookup"><span data-stu-id="c6bc0-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-602">索引中有太多資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="c6bc0-604">-1017</span><span class="sxs-lookup"><span data-stu-id="c6bc0-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-605">記錄已刪除。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="c6bc0-607">-1018</span><span class="sxs-lookup"><span data-stu-id="c6bc0-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-608">資料庫頁面上發生總和檢查碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c6bc0-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="c6bc0-610">-1019</span><span class="sxs-lookup"><span data-stu-id="c6bc0-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-611">有空白的資料庫頁面。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="c6bc0-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="c6bc0-613">-1020</span><span class="sxs-lookup"><span data-stu-id="c6bc0-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-614">沒有檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="c6bc0-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="c6bc0-616">-1022</span><span class="sxs-lookup"><span data-stu-id="c6bc0-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-617">發生磁片 IO 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="c6bc0-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="c6bc0-619">-1023</span><span class="sxs-lookup"><span data-stu-id="c6bc0-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-620">檔案路徑無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="c6bc0-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="c6bc0-622">-1024</span><span class="sxs-lookup"><span data-stu-id="c6bc0-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-623">有不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="c6bc0-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="c6bc0-625">-1025</span><span class="sxs-lookup"><span data-stu-id="c6bc0-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-626">有不正確記錄檔目錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="c6bc0-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="c6bc0-628">-1026</span><span class="sxs-lookup"><span data-stu-id="c6bc0-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-629">記錄大於大小上限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="c6bc0-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="c6bc0-631">-1027</span><span class="sxs-lookup"><span data-stu-id="c6bc0-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-632">開啟的資料庫太多。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="c6bc0-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="c6bc0-634">-1028</span><span class="sxs-lookup"><span data-stu-id="c6bc0-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-635">這不是資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c6bc0-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="c6bc0-637">-1029</span><span class="sxs-lookup"><span data-stu-id="c6bc0-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-638">資料庫引擎尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="c6bc0-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="c6bc0-640">-1030</span><span class="sxs-lookup"><span data-stu-id="c6bc0-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-641">資料庫引擎已初始化。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="c6bc0-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="c6bc0-643">-1031</span><span class="sxs-lookup"><span data-stu-id="c6bc0-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-644">資料庫引擎正在初始化。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="c6bc0-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="c6bc0-646">-1032</span><span class="sxs-lookup"><span data-stu-id="c6bc0-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-647">無法存取檔案，因為檔案已鎖定或正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c6bc0-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="c6bc0-649">-1038</span><span class="sxs-lookup"><span data-stu-id="c6bc0-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-650">緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="c6bc0-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="c6bc0-652">-1040</span><span class="sxs-lookup"><span data-stu-id="c6bc0-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-653">定義的資料行太多。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="c6bc0-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="c6bc0-655">-1043</span><span class="sxs-lookup"><span data-stu-id="c6bc0-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-656">容器不是空的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="c6bc0-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="c6bc0-658">-1044</span><span class="sxs-lookup"><span data-stu-id="c6bc0-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-659">檔案名無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="c6bc0-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="c6bc0-661">-1045</span><span class="sxs-lookup"><span data-stu-id="c6bc0-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-662">有不正確書簽。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="c6bc0-664">-1046</span><span class="sxs-lookup"><span data-stu-id="c6bc0-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-665">使用的資料行位於索引中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="c6bc0-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="c6bc0-667">-1047</span><span class="sxs-lookup"><span data-stu-id="c6bc0-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-668">資料緩衝區不符合資料行大小。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="c6bc0-670">-1048</span><span class="sxs-lookup"><span data-stu-id="c6bc0-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-671">無法設定資料行值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="c6bc0-673">-1051</span><span class="sxs-lookup"><span data-stu-id="c6bc0-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-674">索引正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="c6bc0-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="c6bc0-676">-1052</span><span class="sxs-lookup"><span data-stu-id="c6bc0-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-677">連結支援無法使用。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="c6bc0-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="c6bc0-679">-1053</span><span class="sxs-lookup"><span data-stu-id="c6bc0-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-680">索引上不允許 Null 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="c6bc0-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="c6bc0-682">-1054</span><span class="sxs-lookup"><span data-stu-id="c6bc0-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-683">作業必須在交易內發生。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="c6bc0-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="c6bc0-685">-1059</span><span class="sxs-lookup"><span data-stu-id="c6bc0-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-686">有太多活動資料庫使用者</span><span class="sxs-lookup"><span data-stu-id="c6bc0-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="c6bc0-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="c6bc0-688">-1061</span><span class="sxs-lookup"><span data-stu-id="c6bc0-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-689">有無效或未知的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="c6bc0-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="c6bc0-691">-1062</span><span class="sxs-lookup"><span data-stu-id="c6bc0-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-692">有無效或未知的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="c6bc0-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="c6bc0-694">-1063</span><span class="sxs-lookup"><span data-stu-id="c6bc0-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-695">有無效或未知的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="c6bc0-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="c6bc0-697">-1064</span><span class="sxs-lookup"><span data-stu-id="c6bc0-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-698"><a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>使用了不正確旗標。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="c6bc0-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="c6bc0-700">-1065</span><span class="sxs-lookup"><span data-stu-id="c6bc0-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-701">嘗試建立的版本存放區專案 (大於版本值區的 RCE) 。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="c6bc0-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="c6bc0-703">-1066</span><span class="sxs-lookup"><span data-stu-id="c6bc0-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-704">版本存放區的記憶體不足，因此清理嘗試無法完成。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c6bc0-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="c6bc0-706">-1069</span><span class="sxs-lookup"><span data-stu-id="c6bc0-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-707">版本存放區記憶體不足，已嘗試清除) 。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="c6bc0-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="c6bc0-709">-1071</span><span class="sxs-lookup"><span data-stu-id="c6bc0-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-710">無法編制 [保管] 和 [SLV] 資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="c6bc0-712">-1072</span><span class="sxs-lookup"><span data-stu-id="c6bc0-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-713">尚未刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="c6bc0-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="c6bc0-715">-1073</span><span class="sxs-lookup"><span data-stu-id="c6bc0-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-716">已要求太多 mempool 專案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="c6bc0-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="c6bc0-718">-1074</span><span class="sxs-lookup"><span data-stu-id="c6bc0-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-719">資料庫超出 B + 樹狀 Objectid，因此必須執行離線磁碟重組，才能回收釋放或未使用的 Objectid。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="c6bc0-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="c6bc0-721">-1075</span><span class="sxs-lookup"><span data-stu-id="c6bc0-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-722">長值識別碼計數器已達最大值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="c6bc0-723">您必須執行離線磁碟重組，才能回收免費或未使用的 LongValueIDs。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="c6bc0-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="c6bc0-725">-1076</span><span class="sxs-lookup"><span data-stu-id="c6bc0-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-726">自動遞增計數器已達最大值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="c6bc0-727">離線磁碟重組將無法) 回收免費或未使用的自動遞增值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="c6bc0-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="c6bc0-729">-1077</span><span class="sxs-lookup"><span data-stu-id="c6bc0-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-730">Dbtime 計數器已達到最大值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="c6bc0-731">您必須執行離線磁碟重組，才能回收免費或未使用的 Dbtime 值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="c6bc0-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="c6bc0-733">-1078</span><span class="sxs-lookup"><span data-stu-id="c6bc0-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-734">連續索引計數器已達到最大值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="c6bc0-735">您必須執行離線磁碟重組，才能回收免費或未使用的 SequentialIndex 值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c6bc0-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="c6bc0-737">-1080</span><span class="sxs-lookup"><span data-stu-id="c6bc0-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-738">這個多重實例呼叫已啟用單一實例模式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c6bc0-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="c6bc0-740">-1081</span><span class="sxs-lookup"><span data-stu-id="c6bc0-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-741">此單一實例呼叫已啟用多重實例模式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="c6bc0-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="c6bc0-743">-1082</span><span class="sxs-lookup"><span data-stu-id="c6bc0-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-744">全域系統參數已設定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="c6bc0-746">-1083</span><span class="sxs-lookup"><span data-stu-id="c6bc0-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-747">系統路徑已被另一個資料庫實例使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="c6bc0-749">-1084</span><span class="sxs-lookup"><span data-stu-id="c6bc0-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-750">記錄檔路徑已被另一個資料庫實例使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="c6bc0-752">-1085</span><span class="sxs-lookup"><span data-stu-id="c6bc0-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-753">已有另一個資料庫實例正在使用暫存資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="c6bc0-755">-1086</span><span class="sxs-lookup"><span data-stu-id="c6bc0-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-756">實例名稱已在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="c6bc0-758">-1090</span><span class="sxs-lookup"><span data-stu-id="c6bc0-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-759">因為發生嚴重錯誤，所以無法使用這個實例。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="c6bc0-761">-1091</span><span class="sxs-lookup"><span data-stu-id="c6bc0-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-762">無法使用此資料庫，因為發生嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="c6bc0-764">-1092</span><span class="sxs-lookup"><span data-stu-id="c6bc0-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-765">無法使用這個實例，因為它在執行作業時遇到了記錄磁片-full 錯誤 (例如無法容忍失敗的交易回復) 。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="c6bc0-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="c6bc0-767">-1101</span><span class="sxs-lookup"><span data-stu-id="c6bc0-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-768">資料庫不在會話中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="c6bc0-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="c6bc0-770">-1102</span><span class="sxs-lookup"><span data-stu-id="c6bc0-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-771">因為有未處理的寫入鎖定，所以寫入鎖定失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="c6bc0-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="c6bc0-773">-1103</span><span class="sxs-lookup"><span data-stu-id="c6bc0-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-774">交易的嵌套太深。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="c6bc0-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="c6bc0-776">-1104</span><span class="sxs-lookup"><span data-stu-id="c6bc0-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-777">有不正確會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="c6bc0-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="c6bc0-779">-1105</span><span class="sxs-lookup"><span data-stu-id="c6bc0-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-780">嘗試在未認可的主要索引上進行更新。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="c6bc0-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="c6bc0-782">-1108</span><span class="sxs-lookup"><span data-stu-id="c6bc0-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-783">交易內不允許此作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="c6bc0-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="c6bc0-785">-1109</span><span class="sxs-lookup"><span data-stu-id="c6bc0-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-786">目前的交易必須回復。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="c6bc0-787">無法認可，且無法啟動新的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="c6bc0-789">-1110</span><span class="sxs-lookup"><span data-stu-id="c6bc0-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-790">唯讀交易嘗試修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="c6bc0-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="c6bc0-792">-1111</span><span class="sxs-lookup"><span data-stu-id="c6bc0-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-793">在相同的會話中，嘗試以兩個不同的資料指標取代相同的記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="c6bc0-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="c6bc0-795">-1112</span><span class="sxs-lookup"><span data-stu-id="c6bc0-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-796">如果以舊版 Jet 的資料庫格式表示，記錄會太大。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="c6bc0-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="c6bc0-798">-1113</span><span class="sxs-lookup"><span data-stu-id="c6bc0-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-799">因為與 JET_bitTTForwardOnly 衝突的參數，所以無法建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="c6bc0-801">-1114</span><span class="sxs-lookup"><span data-stu-id="c6bc0-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-802">會話控制碼無法與資料表識別碼搭配使用，因為它不是用來建立它。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="c6bc0-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="c6bc0-804">-1115</span><span class="sxs-lookup"><span data-stu-id="c6bc0-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-805">實例控制碼無效，或參考已關閉的實例。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="c6bc0-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="c6bc0-807">-1119</span><span class="sxs-lookup"><span data-stu-id="c6bc0-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-808">從磁片讀取的資料庫頁面上有先前的寫入未在頁面上表示。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="c6bc0-809">適用于用戶端的 Windows 8 和更新版本，以及適用于伺服器的 Windows Server 2012 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="c6bc0-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="c6bc0-811">-1201</span><span class="sxs-lookup"><span data-stu-id="c6bc0-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-812">資料庫已經存在。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="c6bc0-814">-1202</span><span class="sxs-lookup"><span data-stu-id="c6bc0-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-815">使用中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="c6bc0-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="c6bc0-817">-1203</span><span class="sxs-lookup"><span data-stu-id="c6bc0-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-818">沒有這類資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="c6bc0-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="c6bc0-820">-1204</span><span class="sxs-lookup"><span data-stu-id="c6bc0-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-821">資料庫名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="c6bc0-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="c6bc0-823">-1205</span><span class="sxs-lookup"><span data-stu-id="c6bc0-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-824">有不正確頁面數目。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="c6bc0-826">-1206</span><span class="sxs-lookup"><span data-stu-id="c6bc0-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-827">有非資料庫檔案或損毀的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="c6bc0-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="c6bc0-829">-1207</span><span class="sxs-lookup"><span data-stu-id="c6bc0-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-830">以獨佔方式鎖定資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="c6bc0-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="c6bc0-832">-1208</span><span class="sxs-lookup"><span data-stu-id="c6bc0-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-833">無法停用此資料庫的版本控制。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="c6bc0-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="c6bc0-835">-1209</span><span class="sxs-lookup"><span data-stu-id="c6bc0-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-836">資料庫引擎與資料庫不相容。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="c6bc0-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="c6bc0-838">-1210</span><span class="sxs-lookup"><span data-stu-id="c6bc0-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-839">資料庫是舊版 (200) 格式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-839">The database is in an older (200) format.</span></span> <span data-ttu-id="c6bc0-840">如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="c6bc0-841">僅 Windows NT 用戶端。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="c6bc0-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="c6bc0-843">-1211</span><span class="sxs-lookup"><span data-stu-id="c6bc0-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-844">資料庫是舊版 (400) 格式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-844">The database is in an older (400) format.</span></span> <span data-ttu-id="c6bc0-845">如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="c6bc0-846">僅 Windows NT 用戶端。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="c6bc0-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="c6bc0-848">-1212</span><span class="sxs-lookup"><span data-stu-id="c6bc0-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-849">資料庫是舊版 (500) 格式。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-849">The database is in an older (500) format.</span></span> <span data-ttu-id="c6bc0-850">如果設定<a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> ， <a href="gg294068(v=exchg.10).md">JetInit</a>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="c6bc0-851">僅 Windows NT 用戶端。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="c6bc0-853">-1213</span><span class="sxs-lookup"><span data-stu-id="c6bc0-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-854">資料庫頁面大小與引擎不相符。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="c6bc0-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="c6bc0-856">-1214</span><span class="sxs-lookup"><span data-stu-id="c6bc0-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-857">沒有其他資料庫實例可以啟動。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c6bc0-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="c6bc0-859">-1215</span><span class="sxs-lookup"><span data-stu-id="c6bc0-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-860">不同的資料庫實例正在使用這個資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="c6bc0-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="c6bc0-862">-1216</span><span class="sxs-lookup"><span data-stu-id="c6bc0-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-863">在復原的開頭或結尾偵測到未處理的資料庫附件，但資料庫遺失或不符合附件資訊。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="c6bc0-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="c6bc0-865">-1217</span><span class="sxs-lookup"><span data-stu-id="c6bc0-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-866">指定的資料庫檔案路徑不合法。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="c6bc0-868">-1218</span><span class="sxs-lookup"><span data-stu-id="c6bc0-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-869">正在將已在使用中的識別碼指派給資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="c6bc0-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="c6bc0-871">-1219</span><span class="sxs-lookup"><span data-stu-id="c6bc0-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-872">只有在因為發生錯誤而停止一般卸離時，才允許強制卸離。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="c6bc0-874">-1220</span><span class="sxs-lookup"><span data-stu-id="c6bc0-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-875">在目錄中偵測到損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="c6bc0-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="c6bc0-877">-1221</span><span class="sxs-lookup"><span data-stu-id="c6bc0-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-878">資料庫只會部分附加，且無法完成附加作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="c6bc0-880">-1222</span><span class="sxs-lookup"><span data-stu-id="c6bc0-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-881">使用相同簽章的資料庫已在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="c6bc0-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="c6bc0-883">-1224</span><span class="sxs-lookup"><span data-stu-id="c6bc0-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-884">資料庫已損毀，但不允許修復。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="c6bc0-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="c6bc0-886">-1225</span><span class="sxs-lookup"><span data-stu-id="c6bc0-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-887">資料庫引擎嘗試從交易記錄重新執行建立資料庫作業，但因為該作業的版本不相容而失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="c6bc0-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="c6bc0-889">-1302</span><span class="sxs-lookup"><span data-stu-id="c6bc0-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-890">資料表會被獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="c6bc0-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="c6bc0-892">-1303</span><span class="sxs-lookup"><span data-stu-id="c6bc0-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-893">資料表已經存在。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="c6bc0-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="c6bc0-895">-1304</span><span class="sxs-lookup"><span data-stu-id="c6bc0-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-896">資料表正在使用中，因此無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="c6bc0-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="c6bc0-898">-1305</span><span class="sxs-lookup"><span data-stu-id="c6bc0-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-899">沒有這類資料表或物件。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="c6bc0-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="c6bc0-901">-1307</span><span class="sxs-lookup"><span data-stu-id="c6bc0-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-902">檔案或索引密度不正確。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="c6bc0-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="c6bc0-904">-1308</span><span class="sxs-lookup"><span data-stu-id="c6bc0-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-905">資料表不是空的。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="c6bc0-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="c6bc0-907">-1310</span><span class="sxs-lookup"><span data-stu-id="c6bc0-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-908">資料表識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="c6bc0-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="c6bc0-910">-1311</span><span class="sxs-lookup"><span data-stu-id="c6bc0-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-911">即使在執行內部清除工作之後，也無法開啟其他資料表。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="c6bc0-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="c6bc0-913">-1312</span><span class="sxs-lookup"><span data-stu-id="c6bc0-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-914">資料表不支援此作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="c6bc0-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="c6bc0-916">-1313</span><span class="sxs-lookup"><span data-stu-id="c6bc0-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-917">因為清除嘗試無法完成，所以無法開啟其他資料表。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="c6bc0-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="c6bc0-919">-1314</span><span class="sxs-lookup"><span data-stu-id="c6bc0-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-920">資料表或物件名稱正在使用中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="c6bc0-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="c6bc0-922">-1316</span><span class="sxs-lookup"><span data-stu-id="c6bc0-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-923">物件對作業無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="c6bc0-925">-1317</span><span class="sxs-lookup"><span data-stu-id="c6bc0-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-926">您必須使用<a href="gg294087(v=exchg.10).md">JetCloseTable</a>而非<a href="gg294128(v=exchg.10).md">JetDeleteTable</a>來刪除臨時表。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="c6bc0-928">-1318</span><span class="sxs-lookup"><span data-stu-id="c6bc0-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-929">刪除系統資料表時發生不合法的嘗試。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="c6bc0-931">-1319</span><span class="sxs-lookup"><span data-stu-id="c6bc0-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-932">刪除範本資料表時發生不合法的嘗試。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="c6bc0-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="c6bc0-934">-1322</span><span class="sxs-lookup"><span data-stu-id="c6bc0-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-935">資料表上必須有獨佔鎖定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="c6bc0-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="c6bc0-937">-1323</span><span class="sxs-lookup"><span data-stu-id="c6bc0-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-938">此資料表禁止 DDL 作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="c6bc0-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="c6bc0-940">-1324</span><span class="sxs-lookup"><span data-stu-id="c6bc0-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-941">在衍生的資料表上，ddl 的繼承部分禁止 DDL 作業。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="c6bc0-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="c6bc0-943">-1325</span><span class="sxs-lookup"><span data-stu-id="c6bc0-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-944">目前不支援階層式 DDL 的嵌套。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="c6bc0-946">-1326</span><span class="sxs-lookup"><span data-stu-id="c6bc0-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-947">嘗試從未標示為範本資料表的資料表繼承 DDL。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="c6bc0-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="c6bc0-949">-1328</span><span class="sxs-lookup"><span data-stu-id="c6bc0-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-950">系統參數設定不正確。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c6bc0-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="c6bc0-952">-1329</span><span class="sxs-lookup"><span data-stu-id="c6bc0-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-953">用戶端已要求停止服務。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="c6bc0-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="c6bc0-955">-1330</span><span class="sxs-lookup"><span data-stu-id="c6bc0-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-956">範本資料表是使用 NoFixedVarColumnsInDerivedTables 旗標集所建立。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="c6bc0-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="c6bc0-958">-1401</span><span class="sxs-lookup"><span data-stu-id="c6bc0-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-959">索引建立失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="c6bc0-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="c6bc0-961">-1402</span><span class="sxs-lookup"><span data-stu-id="c6bc0-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-962">已定義主要索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="c6bc0-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="c6bc0-964">-1403</span><span class="sxs-lookup"><span data-stu-id="c6bc0-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-965">已定義索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="c6bc0-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="c6bc0-967">-1404</span><span class="sxs-lookup"><span data-stu-id="c6bc0-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-968">沒有這類索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="c6bc0-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="c6bc0-970">-1405</span><span class="sxs-lookup"><span data-stu-id="c6bc0-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-971">無法刪除叢集索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="c6bc0-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="c6bc0-973">-1406</span><span class="sxs-lookup"><span data-stu-id="c6bc0-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-974">索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="c6bc0-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="c6bc0-976">-1409</span><span class="sxs-lookup"><span data-stu-id="c6bc0-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-977">索引描述的建立無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="c6bc0-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="c6bc0-979">-1410</span><span class="sxs-lookup"><span data-stu-id="c6bc0-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-980">資料庫超出索引描述區塊。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="c6bc0-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="c6bc0-982">-1411</span><span class="sxs-lookup"><span data-stu-id="c6bc0-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-983">針對多重值索引產生了非唯一的內部記錄索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="c6bc0-985">-1412</span><span class="sxs-lookup"><span data-stu-id="c6bc0-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-986">正確反映主要索引的次要索引無法建立。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="c6bc0-988">-1413</span><span class="sxs-lookup"><span data-stu-id="c6bc0-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-989">主要索引已損毀，且資料庫必須經過磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="c6bc0-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="c6bc0-991">-1414</span><span class="sxs-lookup"><span data-stu-id="c6bc0-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-992">次要索引已損毀，且資料庫必須經過磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="c6bc0-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="c6bc0-994">-1416</span><span class="sxs-lookup"><span data-stu-id="c6bc0-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-995">索引識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="c6bc0-997">-1430</span><span class="sxs-lookup"><span data-stu-id="c6bc0-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-998">元組索引只能針對次要索引進行設定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="c6bc0-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="c6bc0-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1001">元組索引的索引定義包含更多資料庫引擎可支援的索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="c6bc0-1002"><strong>注意  </strong>JET_errIndexTuplesOneColumnOnly 錯誤已淘汰，且已由 JET_errIndexTuplesTooManyColumns 取代。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="c6bc0-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1005">元組索引必須是非唯一的索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="c6bc0-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1008">元組索引定義只能包含具有文字或二進位資料行類型的索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="c6bc0-1009"><strong>注意  </strong>JET_errIndexTuplesTextColumnsOnly 錯誤已淘汰，且已由 JET_errIndexTuplesTextBinaryColumnsOnly 取代。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="c6bc0-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1012">元組索引不允許設定 cbVarSegMac。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="c6bc0-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1015">最小/最大元組長度或為索引指定的最大字元數無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="c6bc0-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1018">在元組索引上抓取資料行時，無法使用 JET_bitRetrieveFromIndex 旗標來呼叫<a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="c6bc0-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1021">指定的索引鍵不符合最小元組長度。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="c6bc0-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1024">資料行值為 long。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="c6bc0-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1027">長值沒有這類區塊。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="c6bc0-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1030">欄位將無法放入記錄中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="c6bc0-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1033">Null 無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="c6bc0-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1036">Null 無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1036">Null is not valid.</span></span> <span data-ttu-id="c6bc0-1037">記錄管理員會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1039">資料行已編制索引，無法刪除。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1041">欄位長度大於允許的長度上限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1043">沒有這類資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1045">這個欄位已經定義過了。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1047">嘗試建立多重值資料行，但資料行未標記。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1049">有第二個自動遞增或版本資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1051">資料行資料類型無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1052">JET_errTaggedNotNull-1514</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1053">沒有非 Null 的標記資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1055">資料庫無效，因為它不包含目前的索引。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1057">金鑰完全由您決定。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1059">資料行識別碼不正確。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1061">標記的資料行有不正確的 itagSequence。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1063">無法刪除資料行，因為它是關聯性的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1065">自動遞增和版本無法標記。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1067">預設值超過大小上限。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1069">在唯一多重值資料行上偵測到重複的值。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1071">在長值樹狀結構中發生損毀。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1073">在資料正規化之後，在唯一多重值資料行上偵測到重複的值，並且在比較之前正規化資料截斷。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1075">衍生資料表中有不正確資料行。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1077">嘗試將資料行轉換為主要索引預留位置，但資料行不符合必要的準則。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1079">找不到索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1081">沒有可運作的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1083">目前沒有記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1085">主鍵可能不會變更。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1087">有不合法的重複索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1089">已嘗試在記錄更新進行時更新記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1091">未對 <a href="gg269329(v=exchg.10).md">JetMakeKey</a>進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1093">未對 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1095">資料已變更，且作業已中止。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1097">此 Windows 安裝不支援選取的語言。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1099">排序處理常式太多。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1101">排序期間發生不正確操作。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1103">無法開啟暫存檔。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1105">開啟太多資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1107">磁片上沒有剩餘的空間。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1109">許可權遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1111">找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1113">檔案類型無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1115">無法在初始化之後啟動還原。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1117">無法解讀記錄。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1119">作業無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1121">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1123">無限分割。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1125">多個執行緒使用相同的會話。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1127">找不到必要 DLL 中的進入點。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1128">JET_errSessionCoNtextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1129">指定的會話已經有會話內容集。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1130">JET_errSessionCoNtextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1131">嘗試重設會話內容，但目前的執行緒不是設定會話內容的原始執行緒。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1133">嘗試終止目前使用中的會話。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1135">動態記錄格式轉換期間發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1137"> (，您可以在建立資料庫) 期間設定 <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> 旗標，藉以指定每個會話只會有一個開啟的使用者資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1139">復原期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1141">回呼函數調用失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1143">找不到回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1145">作業系統陰影複製 API 使用了不正確順序。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1147">作業系統陰影複製以超時時間結束。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1149">不允許作業系統陰影複製，因為中的備份或復原正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1151">操作失敗，因為指定的作業系統陰影複製控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1153">嘗試在未指定回呼函數的情況下使用本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1155">嘗試為已設定的物件設定本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1157">嘗試從沒有設定它的物件中取出本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1159">I/o 作業失敗，因為它是針對檔案未配置的區域嘗試。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1161">讀取已發出至 EOF 以外的位置 (寫入將會展開檔案) 。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1163">此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端中止指定的 i/o。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1165">此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端重試指定的 i/o。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1167">此旗標會指示 JET_ABORTRETRYFAILCALLBACK 呼叫端使指定的 i/o 失敗。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1169">壓縮檔案不支援讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="c6bc0-1170">備註</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1170">Remarks</span></span>

<span data-ttu-id="c6bc0-1171">一般情況下，大於零的值應解釋為警告、值為零應解讀為成功，而小於零的值則應視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="c6bc0-1172">這些值中的其他模式（例如值的範圍）應該是由應用程式所依賴。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="c6bc0-1173">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1174"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c6bc0-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1175">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6bc0-1176"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c6bc0-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1177">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c6bc0-1178"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c6bc0-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c6bc0-1179">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c6bc0-1180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1180">See Also</span></span>

[<span data-ttu-id="c6bc0-1181">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c6bc0-1182">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c6bc0-1183">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="c6bc0-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
