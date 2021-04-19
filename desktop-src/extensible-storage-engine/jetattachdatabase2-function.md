---
description: 深入瞭解： JetAttachDatabase2 函數
title: JetAttachDatabase2 函式
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987370"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="90650-103">JetAttachDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="90650-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="90650-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="90650-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="90650-105">JetAttachDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="90650-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="90650-106">**JetAttachDatabase2** 函式會附加資料庫檔案，以便與資料庫實例搭配使用，並指定該資料庫的大小上限。</span><span class="sxs-lookup"><span data-stu-id="90650-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="90650-107">若要使用資料庫，就必須使用 [JetOpenDatabase](./jetopendatabase-function.md)來開啟它。</span><span class="sxs-lookup"><span data-stu-id="90650-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="90650-108">參數</span><span class="sxs-lookup"><span data-stu-id="90650-108">Parameters</span></span>

<span data-ttu-id="90650-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="90650-109">*sesid*</span></span>

<span data-ttu-id="90650-110">將用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="90650-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="90650-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="90650-111">*szFilename*</span></span>

<span data-ttu-id="90650-112">要附加的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="90650-112">The name of the database to attach.</span></span>

<span data-ttu-id="90650-113">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="90650-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="90650-114">資料庫的大小上限（資料庫頁面）。</span><span class="sxs-lookup"><span data-stu-id="90650-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="90650-115">預設資料庫頁面大小為 4 kb，在建立資料庫之前，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數來變更。</span><span class="sxs-lookup"><span data-stu-id="90650-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="90650-116">傳遞零表示資料庫引擎沒有強制執行的最大值。</span><span class="sxs-lookup"><span data-stu-id="90650-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="90650-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="90650-117">*grbit*</span></span>

<span data-ttu-id="90650-118">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="90650-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90650-119">值</span><span class="sxs-lookup"><span data-stu-id="90650-119">Value</span></span></p></th>
<th><p><span data-ttu-id="90650-120">意義</span><span class="sxs-lookup"><span data-stu-id="90650-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90650-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="90650-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="90650-122">如果已設定 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> ，將會刪除 Unicode 資料上的所有索引。</span><span class="sxs-lookup"><span data-stu-id="90650-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="90650-123">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="90650-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="90650-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="90650-125">無論 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>的設定為何，都將刪除所有 Unicode 資料的索引。</span><span class="sxs-lookup"><span data-stu-id="90650-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="90650-126">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="90650-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="90650-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="90650-128">防止修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="90650-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="90650-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="90650-130">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="90650-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="90650-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="90650-131">Return Value</span></span>

<span data-ttu-id="90650-132">函數會傳回其中一個 [JET_ERR](./jet-err.md) 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="90650-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="90650-133">以下是最常傳回的。</span><span class="sxs-lookup"><span data-stu-id="90650-133">The following are the most commonly returned.</span></span> <span data-ttu-id="90650-134"> (如需此 API 的完整錯誤清單，請參閱可延伸的 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="90650-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90650-135">傳回碼</span><span class="sxs-lookup"><span data-stu-id="90650-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="90650-136">Description</span><span class="sxs-lookup"><span data-stu-id="90650-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90650-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="90650-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="90650-138">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="90650-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="90650-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="90650-140">在備份期間，不允許附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="90650-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="90650-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="90650-142"><em>SzFilename</em>所指定的資料庫檔案必須是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="90650-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="90650-143">不能設定 Read-Only 屬性，而且執行中的進程必須有足夠的許可權可寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="90650-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="90650-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="90650-145">資料庫檔案已經由另一個進程開啟。</span><span class="sxs-lookup"><span data-stu-id="90650-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="90650-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="90650-147"><em>SzFilename</em>中提供了不正確路徑。</span><span class="sxs-lookup"><span data-stu-id="90650-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="90650-148"><em>szFilename</em> 必須為非 Null，並參考有效的路徑。</span><span class="sxs-lookup"><span data-stu-id="90650-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="90650-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="90650-150">已由不同的會話附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="90650-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="90650-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="90650-152"><em>SzFilename</em>中提供的檔案不存在。</span><span class="sxs-lookup"><span data-stu-id="90650-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="90650-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="90650-154">主要索引發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="90650-154">There is an error with the primary index.</span></span> <span data-ttu-id="90650-155">這可能是因為物理損毀 (例如磁片或記憶體損毀) 。</span><span class="sxs-lookup"><span data-stu-id="90650-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="90650-156">當附加資料庫上次修改較舊的作業系統，而且主要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="90650-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="90650-157">如需 Unicode 資料之索引的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="90650-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="90650-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="90650-159">次要索引發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="90650-159">There is an error with a secondary index.</span></span> <span data-ttu-id="90650-160">這可能是因為物理損毀 (例如磁片或記憶體損毀) 。</span><span class="sxs-lookup"><span data-stu-id="90650-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="90650-161">當附加資料庫上次修改于較舊的作業系統上，而且次要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="90650-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="90650-162">如需 Unicode 資料之索引的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="90650-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="90650-163">使用下列命令，以離線公用程式重新整理資料庫時，會完整重建次要索引： <strong>esentutl-d</strong>。</span><span class="sxs-lookup"><span data-stu-id="90650-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="90650-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="90650-165">每個實例只能附加有限數量的資料庫。</span><span class="sxs-lookup"><span data-stu-id="90650-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="90650-166">限制目前為每個實例七個資料庫。</span><span class="sxs-lookup"><span data-stu-id="90650-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="90650-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="90650-168">非嚴重警告，指出此會話已附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="90650-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="90650-169">備註</span><span class="sxs-lookup"><span data-stu-id="90650-169">Remarks</span></span>

<span data-ttu-id="90650-170">使用 [JetDetachDatabase](./jetdetachdatabase-function.md) 或 [JetDetachDatabase2](./jetdetachdatabase2-function.md)卸離資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="90650-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="90650-171">如需備註，請參閱 [JetAttachDatabase](./jetattachdatabase-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="90650-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="90650-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="90650-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90650-173"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="90650-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-174">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="90650-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-175"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="90650-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-176">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="90650-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-177"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="90650-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-178">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="90650-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-179"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="90650-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-180">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="90650-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90650-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="90650-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-182">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="90650-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90650-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="90650-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="90650-184">實作為 <strong>JetAttachDatabase2W</strong> (Unicode) 和 <strong>JetAttachDatabase2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="90650-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="90650-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90650-185">See Also</span></span>

[<span data-ttu-id="90650-186">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="90650-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="90650-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="90650-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="90650-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="90650-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="90650-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="90650-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="90650-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="90650-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="90650-191">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="90650-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="90650-192">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="90650-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="90650-193">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="90650-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="90650-194">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="90650-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
