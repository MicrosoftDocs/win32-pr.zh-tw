---
description: 深入瞭解： JetOpenDatabase 函數
title: JetOpenDatabase 函式
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695667"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="048e0-103">JetOpenDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="048e0-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="048e0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="048e0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="048e0-105">JetOpenDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="048e0-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="048e0-106">**JetOpenDatabase** 函式會使用 [JetAttachDatabase](./jetattachdatabase-function.md)或 [JetAttachDatabase2](./jetattachdatabase2-function.md)函數來開啟先前附加的資料庫，以搭配資料庫會話使用。</span><span class="sxs-lookup"><span data-stu-id="048e0-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="048e0-107">您可以針對相同的資料庫多次呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="048e0-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="048e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="048e0-108">Parameters</span></span>

<span data-ttu-id="048e0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="048e0-109">*sesid*</span></span>

<span data-ttu-id="048e0-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="048e0-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="048e0-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="048e0-111">*szFilename*</span></span>

<span data-ttu-id="048e0-112">要開啟之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="048e0-112">The name of the database to open.</span></span>

<span data-ttu-id="048e0-113">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="048e0-113">*szConnect*</span></span>

<span data-ttu-id="048e0-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="048e0-114">Reserved.</span></span> <span data-ttu-id="048e0-115">設定為 NULL。</span><span class="sxs-lookup"><span data-stu-id="048e0-115">Set to NULL.</span></span>

<span data-ttu-id="048e0-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="048e0-116">*pdbid*</span></span>

<span data-ttu-id="048e0-117">在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="048e0-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="048e0-118">如果呼叫失敗，則值為未定義。</span><span class="sxs-lookup"><span data-stu-id="048e0-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="048e0-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="048e0-119">*grbit*</span></span>

<span data-ttu-id="048e0-120">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="048e0-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="048e0-121">值</span><span class="sxs-lookup"><span data-stu-id="048e0-121">Value</span></span></p></th>
<th><p><span data-ttu-id="048e0-122">意義</span><span class="sxs-lookup"><span data-stu-id="048e0-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048e0-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="048e0-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="048e0-124">只允許單一會話附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="048e0-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="048e0-125">一般來說，數個會話可以開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="048e0-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="048e0-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="048e0-127">防止修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="048e0-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="048e0-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="048e0-128">Return Value</span></span>

<span data-ttu-id="048e0-129">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="048e0-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="048e0-130">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="048e0-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="048e0-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="048e0-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="048e0-132">Description</span><span class="sxs-lookup"><span data-stu-id="048e0-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048e0-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="048e0-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="048e0-134">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="048e0-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="048e0-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="048e0-136">已要求獨佔存取權，但無法授與。</span><span class="sxs-lookup"><span data-stu-id="048e0-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048e0-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="048e0-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="048e0-138"><em>SzFilename</em>中提供了不正確路徑。</span><span class="sxs-lookup"><span data-stu-id="048e0-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="048e0-139"><em>szFilename</em> 必須為非 Null，並參考有效的檔案。</span><span class="sxs-lookup"><span data-stu-id="048e0-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="048e0-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="048e0-141">另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="048e0-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048e0-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="048e0-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="048e0-143">先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</span><span class="sxs-lookup"><span data-stu-id="048e0-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="048e0-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="048e0-145">嘗試開啟的檔案不是有效的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="048e0-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048e0-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="048e0-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="048e0-147">嘗試開啟一個以上的資料庫，並已設定 <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> 。</span><span class="sxs-lookup"><span data-stu-id="048e0-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="048e0-148">如需詳細資訊，請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a>。</span><span class="sxs-lookup"><span data-stu-id="048e0-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="048e0-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="048e0-150">檔案已附加為唯讀，但 <strong>JetOpenDatabase</strong> 未通過 JET_bitDbReadOnly。</span><span class="sxs-lookup"><span data-stu-id="048e0-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="048e0-151">資料庫仍會以唯讀存取權開啟。</span><span class="sxs-lookup"><span data-stu-id="048e0-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="048e0-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="048e0-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="048e0-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-154">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="048e0-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-156">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="048e0-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048e0-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="048e0-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-159"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-160">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="048e0-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="048e0-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-162">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="048e0-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="048e0-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="048e0-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="048e0-164">實作為 <strong>JetOpenDatabaseW</strong> (Unicode) 和 <strong>JetOpenDatabaseA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="048e0-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="048e0-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="048e0-165">See Also</span></span>

[<span data-ttu-id="048e0-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="048e0-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="048e0-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="048e0-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="048e0-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="048e0-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="048e0-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="048e0-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="048e0-170">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="048e0-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="048e0-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="048e0-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="048e0-172">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="048e0-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="048e0-173">系統參數</span><span class="sxs-lookup"><span data-stu-id="048e0-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
