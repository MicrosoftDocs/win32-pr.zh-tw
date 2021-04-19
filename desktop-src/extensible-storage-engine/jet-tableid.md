---
description: 深入瞭解： JET_TABLEID
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975388"
---
# <a name="jet_tableid"></a><span data-ttu-id="3d846-103">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d846-103">JET_TABLEID</span></span>


<span data-ttu-id="3d846-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3d846-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tableid"></a><span data-ttu-id="3d846-105">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d846-105">JET_TABLEID</span></span>

<span data-ttu-id="3d846-106">JET_TABLEID 資料類型包含資料庫資料指標的控制碼，可用於呼叫 JET API。</span><span class="sxs-lookup"><span data-stu-id="3d846-106">The JET_TABLEID data type contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="3d846-107">資料指標只能搭配用來開啟該資料指標的會話使用。</span><span class="sxs-lookup"><span data-stu-id="3d846-107">A cursor can only be used with the session that was used to open that cursor.</span></span>

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a><span data-ttu-id="3d846-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="3d846-108">Data Types</span></span>

<span data-ttu-id="3d846-109">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d846-109">JET_TABLEID</span></span>

<span data-ttu-id="3d846-110">**Null** 或 [JET_tableidNil](./invalid-handle-constants.md)可以用來表示不正確資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="3d846-110">Either **NULL** or [JET_tableidNil](./invalid-handle-constants.md) can be used to indicate an invalid cursor handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="3d846-111">備註</span><span class="sxs-lookup"><span data-stu-id="3d846-111">Remarks</span></span>

<span data-ttu-id="3d846-112">資料指標會管理資料庫引擎的資料表使用。</span><span class="sxs-lookup"><span data-stu-id="3d846-112">A cursor manages the use of a table for the database engine.</span></span> <span data-ttu-id="3d846-113">資料指標可以執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="3d846-113">A cursor can do the following tasks:</span></span>

  - <span data-ttu-id="3d846-114">掃描記錄</span><span class="sxs-lookup"><span data-stu-id="3d846-114">Scan records</span></span>

  - <span data-ttu-id="3d846-115">搜尋記錄</span><span class="sxs-lookup"><span data-stu-id="3d846-115">Search for records</span></span>

  - <span data-ttu-id="3d846-116">選擇有效的排序次序以及這些記錄的可見度</span><span class="sxs-lookup"><span data-stu-id="3d846-116">Choose the effective sort order and visibility of those records</span></span>

  - <span data-ttu-id="3d846-117">建立、更新或刪除記錄</span><span class="sxs-lookup"><span data-stu-id="3d846-117">Create, update, or delete records</span></span>

  - <span data-ttu-id="3d846-118">修改資料表的架構</span><span class="sxs-lookup"><span data-stu-id="3d846-118">Modify the schema of the table</span></span>

<span data-ttu-id="3d846-119">當基礎資料表的狀態或類型變更時，資料指標支援的功能可能會變更。</span><span class="sxs-lookup"><span data-stu-id="3d846-119">The supported functionality of the cursor might change as the status or type of the underlying table changes.</span></span> <span data-ttu-id="3d846-120">例如，臨時表可能不允許在使用某些選項開啟資料時進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="3d846-120">For example, a temporary table might disallow searching for data when it is opened with certain options.</span></span> <span data-ttu-id="3d846-121">資料指標一律會完全連接到基礎資料表，並直接與該資料互動，而不需要任何快取。</span><span class="sxs-lookup"><span data-stu-id="3d846-121">The cursor is always fully connected to the underlying table and interacts with that data directly without any caching.</span></span> <span data-ttu-id="3d846-122">此資料庫引擎公開的所有核心 ISAM 功能幾乎都可透過資料指標運作。</span><span class="sxs-lookup"><span data-stu-id="3d846-122">Almost all of the core ISAM functionality that is exposed by this database engine is works through the cursor.</span></span>

<span data-ttu-id="3d846-123">您可以使用 [JetOpenTable](./jetopentable-function.md) 或 [JetOpenTempTable](./jetopentemptable-function.md)來建立資料指標。</span><span class="sxs-lookup"><span data-stu-id="3d846-123">A cursor can be created using [JetOpenTable](./jetopentable-function.md) or [JetOpenTempTable](./jetopentemptable-function.md).</span></span> <span data-ttu-id="3d846-124">您可以使用 [JetDupCursor](./jetdupcursor-function.md)來重復資料指標。</span><span class="sxs-lookup"><span data-stu-id="3d846-124">A cursor can be duplicated using [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="3d846-125">您可以使用 [JetCloseTable](./jetclosetable-function.md) 明確地關閉資料指標，或使用 [JetEndSession](./jetendsession-function.md) 或 [JetTerm](./jetterm-function.md)以隱含方式關閉資料指標。</span><span class="sxs-lookup"><span data-stu-id="3d846-125">A cursor can be explicitly closed using [JetCloseTable](./jetclosetable-function.md) or implicitly closed using [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span> <span data-ttu-id="3d846-126">如果資料指標是在中止的交易中開啟，則 [JetRollback](./jetrollback-function.md) 也可以隱含地將它關閉。</span><span class="sxs-lookup"><span data-stu-id="3d846-126">A cursor can also be implicitly closed by [JetRollback](./jetrollback-function.md) if it was opened in the transaction that was aborted.</span></span> <span data-ttu-id="3d846-127">可以在任何時間建立的最大資料指標數目是由 [JET_paramMaxCursors](./resource-parameters.md)所控制，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行設定。</span><span class="sxs-lookup"><span data-stu-id="3d846-127">The maximum number of cursors that can be created at any one time is controlled by [JET_paramMaxCursors](./resource-parameters.md), which can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="3d846-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d846-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d846-129"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3d846-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3d846-130">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="3d846-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d846-131"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3d846-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3d846-132">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="3d846-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d846-133"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3d846-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3d846-134">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3d846-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3d846-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d846-135">See Also</span></span>

[<span data-ttu-id="3d846-136">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="3d846-136">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="3d846-137">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="3d846-137">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="3d846-138">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="3d846-138">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="3d846-139">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="3d846-139">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="3d846-140">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="3d846-140">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="3d846-141">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="3d846-141">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="3d846-142">JetRollback</span><span class="sxs-lookup"><span data-stu-id="3d846-142">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="3d846-143">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3d846-143">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3d846-144">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3d846-144">JetTerm</span></span>](./jetterm-function.md)
