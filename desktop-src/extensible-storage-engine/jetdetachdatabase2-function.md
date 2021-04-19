---
description: 深入瞭解： JetDetachDatabase2 函數
title: JetDetachDatabase2 函式
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998139"
---
# <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ff6c4-103">JetDetachDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="ff6c4-103">JetDetachDatabase2 Function</span></span>


<span data-ttu-id="ff6c4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ff6c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase2-function"></a><span data-ttu-id="ff6c4-105">JetDetachDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="ff6c4-105">JetDetachDatabase2 Function</span></span>

<span data-ttu-id="ff6c4-106">**JetDetachDatabase2** 函式會釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-106">The **JetDetachDatabase2** function releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="ff6c4-107">**Windows xp：**  **JetDetachDatabase2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-107">**Windows XP:**  **JetDetachDatabase2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ff6c4-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff6c4-108">Parameters</span></span>

<span data-ttu-id="ff6c4-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ff6c4-109">*sesid*</span></span>

<span data-ttu-id="ff6c4-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="ff6c4-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="ff6c4-111">*szFilename*</span></span>

<span data-ttu-id="ff6c4-112">要卸離的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-112">The name of the database to detach.</span></span> <span data-ttu-id="ff6c4-113">如果 *szFilename* 為 **Null** 或空字串，則會卸離附加至 *sesid* 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-113">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

<span data-ttu-id="ff6c4-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ff6c4-114">*grbit*</span></span>

<span data-ttu-id="ff6c4-115">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-115">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff6c4-116">值</span><span class="sxs-lookup"><span data-stu-id="ff6c4-116">Value</span></span></p></th>
<th><p><span data-ttu-id="ff6c4-117">意義</span><span class="sxs-lookup"><span data-stu-id="ff6c4-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-118">JET_bitForceCloseAndDetach</span><span class="sxs-lookup"><span data-stu-id="ff6c4-118">JET_bitForceCloseAndDetach</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-119">強制關閉和卸離資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-119">Forces the database to be closed and detached.</span></span> <span data-ttu-id="ff6c4-120">如果不支援 JET_bitForceCloseAndDetach，將會傳回 JET_errForceDetachNotAllowed。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-120">If JET_bitForceCloseAndDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-121">JET_bitForceDetach</span><span class="sxs-lookup"><span data-stu-id="ff6c4-121">JET_bitForceDetach</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-122">強制卸離資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-122">Forces the database to be detached.</span></span> <span data-ttu-id="ff6c4-123">如果不支援 JET_bitForceDetach，將會傳回 JET_errForceDetachNotAllowed。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-123">If JET_bitForceDetach is not supported, JET_errForceDetachNotAllowed will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ff6c4-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff6c4-124">Return Value</span></span>

<span data-ttu-id="ff6c4-125">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ff6c4-126">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff6c4-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ff6c4-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="ff6c4-128">Description</span><span class="sxs-lookup"><span data-stu-id="ff6c4-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ff6c4-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-130">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="ff6c4-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-132">正在備份資料庫，且無法中斷連結。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-132">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-133">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="ff6c4-133">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-134">資料庫已由 <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>開啟。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-134">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="ff6c4-135">必須先關閉資料庫，然後再卸離。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-135">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-136">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="ff6c4-136">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-137">先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> 或 <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>) 。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-137">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-138">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ff6c4-138">JET_errForceDetachNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-139">不支援 JET_bitForceDetach。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-139">JET_bitForceDetach is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-140">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ff6c4-140">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ff6c4-141">嘗試在交易中卸離資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-141">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ff6c4-142">備註</span><span class="sxs-lookup"><span data-stu-id="ff6c4-142">Remarks</span></span>

<span data-ttu-id="ff6c4-143">如果已使用 [JetAttachDatabase](./jetattachdatabase-function.md)) 開啟附加的資料庫 (，則必須先將它關閉， [然後再卸](./jetclosedatabase-function.md) 離。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-143">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="ff6c4-144">僅限 Windows 2000：下次呼叫[JetInit](./jetinit-function.md)時，未在呼叫[JetTerm](./jetterm-function.md)之前卸離的資料庫將會自動重新連接。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-144">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ff6c4-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff6c4-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-146"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-147">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-148"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-149">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-150"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-151">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-152"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-153">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff6c4-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-155">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff6c4-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ff6c4-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ff6c4-157">實作為 <strong>JetDetachDatabase2W</strong> (Unicode) 和 <strong>JetDetachDatabase2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="ff6c4-157">Implemented as <strong>JetDetachDatabase2W</strong> (Unicode) and <strong>JetDetachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ff6c4-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff6c4-158">See Also</span></span>

[<span data-ttu-id="ff6c4-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ff6c4-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ff6c4-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ff6c4-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ff6c4-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ff6c4-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ff6c4-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff6c4-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ff6c4-163">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="ff6c4-163">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="ff6c4-164">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ff6c4-164">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="ff6c4-165">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="ff6c4-165">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="ff6c4-166">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="ff6c4-166">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="ff6c4-167">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="ff6c4-167">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="ff6c4-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="ff6c4-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="ff6c4-169">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="ff6c4-169">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="ff6c4-170">JetTerm</span><span class="sxs-lookup"><span data-stu-id="ff6c4-170">JetTerm</span></span>](./jetterm-function.md)
