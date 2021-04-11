---
description: 深入瞭解： JetSetDatabaseSize 函數
title: JetSetDatabaseSize 函式
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112036"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="f1dc0-103">JetSetDatabaseSize 函式</span><span class="sxs-lookup"><span data-stu-id="f1dc0-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="f1dc0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1dc0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="f1dc0-105">JetSetDatabaseSize 函式</span><span class="sxs-lookup"><span data-stu-id="f1dc0-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="f1dc0-106">**JetSetDatabaseSize** 函式會設定未開啟之資料庫檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="f1dc0-107">參數</span><span class="sxs-lookup"><span data-stu-id="f1dc0-107">Parameters</span></span>

<span data-ttu-id="f1dc0-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f1dc0-108">*sesid*</span></span>

<span data-ttu-id="f1dc0-109">識別要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="f1dc0-110">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="f1dc0-110">*szDatabaseName*</span></span>

<span data-ttu-id="f1dc0-111">識別要改變其大小的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="f1dc0-112">*Cpg*</span><span class="sxs-lookup"><span data-stu-id="f1dc0-112">*cpg*</span></span>

<span data-ttu-id="f1dc0-113">在頁面中指定所需的資料庫大小。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="f1dc0-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="f1dc0-114">*pcpgReal*</span></span>

<span data-ttu-id="f1dc0-115">在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="f1dc0-116">如果 API 呼叫失敗， *pcpgReal* 的內容會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="f1dc0-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1dc0-117">Return Value</span></span>

<span data-ttu-id="f1dc0-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f1dc0-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1dc0-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1dc0-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f1dc0-121">Description</span><span class="sxs-lookup"><span data-stu-id="f1dc0-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f1dc0-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="f1dc0-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="f1dc0-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="f1dc0-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-126">JET_errDatabaseInconsistent 和 JET_errDatabaseDirtyShutdown 是相同的數值。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="f1dc0-127">要調整其大小的資料庫必須處於正常關機狀態，也就是所謂的一致狀態。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="f1dc0-128">不一致的資料庫並未損毀，但需要重新執行記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="f1dc0-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-130"><em>szDatabaseName</em> 不得為空的非 Null 字串。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="f1dc0-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-132">磁片區上的可用空間不足，無法執行成長作業。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="f1dc0-133"><strong>JetSetDatabaseSize</strong> 可能也會傳回許多與檔案相關的錯誤，包括但不限於：</span><span class="sxs-lookup"><span data-stu-id="f1dc0-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="f1dc0-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="f1dc0-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="f1dc0-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="f1dc0-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="f1dc0-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="f1dc0-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="f1dc0-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="f1dc0-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="f1dc0-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="f1dc0-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f1dc0-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-140">可能會傳回此錯誤的其中一個原因是 <em>cpg</em> 符合資料庫大小下限。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="f1dc0-141">目前的最小資料庫大小為256頁。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f1dc0-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f1dc0-143">系統的記憶體資源不足。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f1dc0-144">備註</span><span class="sxs-lookup"><span data-stu-id="f1dc0-144">Remarks</span></span>

<span data-ttu-id="f1dc0-145">如果在插入大量資料之前呼叫 **JetSetDatabaseSize** ，資料庫檔案將會在一項作業中成長。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="f1dc0-146">這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="f1dc0-147">成長資料庫檔案一次可能會比將其成長數次快。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="f1dc0-148">目前只支援成長盤案。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="f1dc0-149">若要壓縮檔案，請使用 esentutl.exe 公用程式的磁碟重組功能。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="f1dc0-150">如果 *cpg* 小於資料庫的目前大小，則會忽略此作業。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="f1dc0-151">如果 *cpg* 小於最小資料庫大小 (目前256頁) ，它將會傳回 JET_errInvalidParameter。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="f1dc0-152">若要設定開啟的資料庫大小，請參閱 [JetGrowDatabase](./jetgrowdatabase-function.md)。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="f1dc0-153">檔案大小可能不符合 *pcpgReal* 中傳回的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="f1dc0-154">有兩個額外的保留頁面可能不會在 *pcpgReal* 中計算。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f1dc0-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1dc0-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-156"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-157">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-158"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-159">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-160"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-161">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-162"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-163">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1dc0-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-165">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1dc0-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f1dc0-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f1dc0-167">實作為 <strong>JetSetDatabaseSizeW</strong> (Unicode) 和 <strong>JetSetDatabaseSizeA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="f1dc0-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f1dc0-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1dc0-168">See Also</span></span>

[<span data-ttu-id="f1dc0-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f1dc0-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f1dc0-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f1dc0-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f1dc0-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f1dc0-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f1dc0-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f1dc0-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f1dc0-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="f1dc0-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="f1dc0-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="f1dc0-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="f1dc0-175">JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="f1dc0-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
