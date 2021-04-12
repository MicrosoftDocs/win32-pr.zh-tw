---
description: 深入瞭解： JetResetSessionCoNtext 函數
title: JetResetSessionCoNtext 函式
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193038"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="9bdb4-103">JetResetSessionCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="9bdb4-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="9bdb4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9bdb4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="9bdb4-105">JetResetSessionCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="9bdb4-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="9bdb4-106">**JetResetSessionCoNtext** 函式會解除會話與目前線程的與之間的之間的解除。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="9bdb4-107">參數</span><span class="sxs-lookup"><span data-stu-id="9bdb4-107">Parameters</span></span>

<span data-ttu-id="9bdb4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9bdb4-108">*sesid*</span></span>

<span data-ttu-id="9bdb4-109">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="9bdb4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9bdb4-110">Return Value</span></span>

<span data-ttu-id="9bdb4-111">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9bdb4-112">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bdb4-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9bdb4-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="9bdb4-114">Description</span><span class="sxs-lookup"><span data-stu-id="9bdb4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9bdb4-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-116">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdb4-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9bdb4-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-118">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9bdb4-119">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9bdb4-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-121">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdb4-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9bdb4-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-123">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-124">JET_errSessionCoNtextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="9bdb4-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-125">因為會話與不同的執行緒相關聯，所以無法從目前的執行緒解除關聯。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdb4-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9bdb4-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9bdb4-127">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bdb4-128">成功時，會話將會與目前的執行緒解除關聯。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="9bdb4-129">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-129">No change to the database state will occur.</span></span>

<span data-ttu-id="9bdb4-130">失敗時，會話狀態會維持不變。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="9bdb4-131">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9bdb4-132">備註</span><span class="sxs-lookup"><span data-stu-id="9bdb4-132">Remarks</span></span>

<span data-ttu-id="9bdb4-133">**JetResetSessionCoNtext** 必須在呼叫 [JetSetSessionCoNtext](./jetsetsessioncontext-function.md) 的相同執行緒上呼叫指定的會話。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9bdb4-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bdb4-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-135"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9bdb4-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdb4-136">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdb4-137"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9bdb4-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdb4-138">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-139"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9bdb4-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdb4-140">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdb4-141"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="9bdb4-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdb4-142">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdb4-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9bdb4-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdb4-144">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="9bdb4-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9bdb4-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bdb4-145">See Also</span></span>

[<span data-ttu-id="9bdb4-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="9bdb4-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="9bdb4-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9bdb4-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9bdb4-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9bdb4-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9bdb4-149">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="9bdb4-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
