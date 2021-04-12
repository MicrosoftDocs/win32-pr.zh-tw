---
description: 深入瞭解： JetDetachDatabase 函數
title: JetDetachDatabase 函式
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320947"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="ab365-103">JetDetachDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="ab365-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="ab365-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ab365-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="ab365-105">JetDetachDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="ab365-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="ab365-106">**JetDetachDatabase** 函式會釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="ab365-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="ab365-107">參數</span><span class="sxs-lookup"><span data-stu-id="ab365-107">Parameters</span></span>

<span data-ttu-id="ab365-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ab365-108">*sesid*</span></span>

<span data-ttu-id="ab365-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="ab365-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="ab365-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="ab365-110">*szFilename*</span></span>

<span data-ttu-id="ab365-111">要卸離的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ab365-111">The name of the database to detach.</span></span> <span data-ttu-id="ab365-112">如果 *szFilename* 為 **Null** 或空字串，則會卸離附加至 *sesid* 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="ab365-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="ab365-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab365-113">Return Value</span></span>

<span data-ttu-id="ab365-114">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ab365-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ab365-115">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ab365-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab365-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ab365-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="ab365-117">Description</span><span class="sxs-lookup"><span data-stu-id="ab365-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab365-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ab365-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ab365-119">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ab365-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab365-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="ab365-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="ab365-121">正在備份資料庫，且無法中斷連結。</span><span class="sxs-lookup"><span data-stu-id="ab365-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab365-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="ab365-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="ab365-123">資料庫已由 <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>開啟。</span><span class="sxs-lookup"><span data-stu-id="ab365-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="ab365-124">必須先關閉資料庫，然後再卸離。</span><span class="sxs-lookup"><span data-stu-id="ab365-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab365-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="ab365-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="ab365-126">先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> 或 <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>) 。</span><span class="sxs-lookup"><span data-stu-id="ab365-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab365-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ab365-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ab365-128">嘗試在交易中卸離資料庫。</span><span class="sxs-lookup"><span data-stu-id="ab365-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ab365-129">備註</span><span class="sxs-lookup"><span data-stu-id="ab365-129">Remarks</span></span>

<span data-ttu-id="ab365-130">如果已使用 [JetAttachDatabase](./jetattachdatabase-function.md)) 開啟附加的資料庫 (，則必須先將它關閉， [然後再卸](./jetclosedatabase-function.md) 離。</span><span class="sxs-lookup"><span data-stu-id="ab365-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="ab365-131">僅限 Windows 2000：下次呼叫[JetInit](./jetinit-function.md)時，未在呼叫[JetTerm](./jetterm-function.md)之前卸離的資料庫將會自動重新連接。</span><span class="sxs-lookup"><span data-stu-id="ab365-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ab365-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab365-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab365-133"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-134">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ab365-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab365-135"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-136">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ab365-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab365-137"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-138">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ab365-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab365-139"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-140">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ab365-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab365-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-142">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ab365-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab365-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ab365-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ab365-144">實作為 <strong>JetDetachDatabaseW</strong> (Unicode) 和 <strong>JetDetachDatabaseA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="ab365-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ab365-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab365-145">See Also</span></span>

[<span data-ttu-id="ab365-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ab365-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ab365-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ab365-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ab365-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ab365-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ab365-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ab365-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ab365-150">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="ab365-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="ab365-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab365-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="ab365-152">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="ab365-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="ab365-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="ab365-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="ab365-154">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="ab365-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="ab365-155">JetTerm</span><span class="sxs-lookup"><span data-stu-id="ab365-155">JetTerm</span></span>](./jetterm-function.md)
