---
description: 深入瞭解： JetCloseTable 函數
title: JetCloseTable 函式
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b38ba9b14c34d20b01b6530f2ed3406e55b3bc3f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514725"
---
# <a name="jetclosetable-function"></a><span data-ttu-id="aa078-103">JetCloseTable 函式</span><span class="sxs-lookup"><span data-stu-id="aa078-103">JetCloseTable Function</span></span>


<span data-ttu-id="aa078-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aa078-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosetable-function"></a><span data-ttu-id="aa078-105">JetCloseTable 函式</span><span class="sxs-lookup"><span data-stu-id="aa078-105">JetCloseTable Function</span></span>

<span data-ttu-id="aa078-106">**JetCloseTable** 函式會在資料庫中關閉開啟的資料表。</span><span class="sxs-lookup"><span data-stu-id="aa078-106">The **JetCloseTable** function closes an open table in a database.</span></span> <span data-ttu-id="aa078-107">資料表可以是臨時表或一般資料表。</span><span class="sxs-lookup"><span data-stu-id="aa078-107">The table may be a temporary table or a normal table.</span></span>

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a><span data-ttu-id="aa078-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa078-108">Parameters</span></span>

<span data-ttu-id="aa078-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="aa078-109">*sesid*</span></span>

<span data-ttu-id="aa078-110">識別將用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="aa078-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="aa078-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="aa078-111">*tableid*</span></span>

<span data-ttu-id="aa078-112">識別要關閉的資料表。</span><span class="sxs-lookup"><span data-stu-id="aa078-112">Identifies the table to be closed.</span></span>

<span data-ttu-id="aa078-113">將 *tableid* 設定為 JET_tableidNil 釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa078-113">Set *tableid* to JET_tableidNil to release memory.</span></span>

### <a name="return-value"></a><span data-ttu-id="aa078-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa078-114">Return Value</span></span>

<span data-ttu-id="aa078-115">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="aa078-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aa078-116">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="aa078-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa078-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aa078-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="aa078-118">Description</span><span class="sxs-lookup"><span data-stu-id="aa078-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa078-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aa078-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aa078-120">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="aa078-120">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="aa078-121">備註</span><span class="sxs-lookup"><span data-stu-id="aa078-121">Remarks</span></span>

<span data-ttu-id="aa078-122">您必須在以 [JetOpenTable](./jetopentable-function.md)開啟的所有資料表上呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="aa078-122">This function must be called on all tables opened with [JetOpenTable](./jetopentable-function.md).</span></span>

<span data-ttu-id="aa078-123">在交易中呼叫 [JetOpenTable](./jetopentable-function.md) 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。</span><span class="sxs-lookup"><span data-stu-id="aa078-123">The exception to this rule happens when [JetOpenTable](./jetopentable-function.md) is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="aa078-124">回復交易時，資料表會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="aa078-124">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="aa078-125">在此情況下，使用 **JetCloseTable** 關閉資料表是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="aa078-125">In this case, it is an error to close the table with **JetCloseTable**.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aa078-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa078-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa078-127"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="aa078-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aa078-128">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="aa078-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa078-129"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="aa078-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aa078-130">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="aa078-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa078-131"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="aa078-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aa078-132">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="aa078-132">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa078-133"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="aa078-133"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aa078-134">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="aa078-134">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa078-135"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aa078-135"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aa078-136">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="aa078-136">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aa078-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa078-137">See Also</span></span>

[<span data-ttu-id="aa078-138">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aa078-138">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aa078-139">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="aa078-139">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="aa078-140">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="aa078-140">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="aa078-141">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="aa078-141">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="aa078-142">JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="aa078-142">JetOpenTable</span></span>](./jetopentable-function.md)  
[<span data-ttu-id="aa078-143">JetRollback</span><span class="sxs-lookup"><span data-stu-id="aa078-143">JetRollback</span></span>](./jetrollback-function.md)
