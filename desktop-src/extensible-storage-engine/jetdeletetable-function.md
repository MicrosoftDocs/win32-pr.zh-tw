---
description: 深入瞭解： JetDeleteTable 函數
title: JetDeleteTable 函式
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975555"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="1d7a8-103">JetDeleteTable 函式</span><span class="sxs-lookup"><span data-stu-id="1d7a8-103">JetDeleteTable Function</span></span>


<span data-ttu-id="1d7a8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1d7a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="1d7a8-105">JetDeleteTable 函式</span><span class="sxs-lookup"><span data-stu-id="1d7a8-105">JetDeleteTable Function</span></span>

<span data-ttu-id="1d7a8-106">**JetDeleteTable** 函數會刪除 ESE 資料庫中的資料表。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="1d7a8-107">參數</span><span class="sxs-lookup"><span data-stu-id="1d7a8-107">Parameters</span></span>

<span data-ttu-id="1d7a8-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1d7a8-108">*sesid*</span></span>

<span data-ttu-id="1d7a8-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="1d7a8-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="1d7a8-110">*dbid*</span></span>

<span data-ttu-id="1d7a8-111">用於 API 呼叫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="1d7a8-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="1d7a8-112">*szTableName*</span></span>

<span data-ttu-id="1d7a8-113">要刪除的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="1d7a8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d7a8-114">Return Value</span></span>

<span data-ttu-id="1d7a8-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1d7a8-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d7a8-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1d7a8-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="1d7a8-118">Description</span><span class="sxs-lookup"><span data-stu-id="1d7a8-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d7a8-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1d7a8-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1d7a8-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7a8-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="1d7a8-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="1d7a8-122">嘗試刪除資料表，而另一個會話具有開啟的資料表識別碼 (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) 具有 <a href="gg294118(v=exchg.10).md">JetOpenTable</a> 或 <a href="gg269193(v=exchg.10).md">JetDupCursor</a>。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d7a8-123">JET_errCannotDeletetemporary 資料表</span><span class="sxs-lookup"><span data-stu-id="1d7a8-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="1d7a8-124">嘗試刪除臨時表。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="1d7a8-125">當臨時表以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉時，就會自動刪除。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7a8-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="1d7a8-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="1d7a8-127">嘗試刪除範本資料表，也就是可以繼承 DDL 的資料表。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="1d7a8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d7a8-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d7a8-129"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-130">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7a8-131"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-132">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d7a8-133"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-134">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7a8-135"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-136">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d7a8-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-138">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d7a8-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="1d7a8-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="1d7a8-140">實作為 <strong>JetDeleteTableW</strong> (Unicode) 和 <strong>JetDeleteTableA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="1d7a8-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1d7a8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d7a8-141">See Also</span></span>

[<span data-ttu-id="1d7a8-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="1d7a8-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="1d7a8-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1d7a8-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1d7a8-144">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="1d7a8-144">JetCloseTable</span></span>](./jetclosetable-function.md)
