---
description: 深入瞭解： JetBeginSession 函數
title: JetBeginSession 函式
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983883"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="705b5-103">JetBeginSession 函式</span><span class="sxs-lookup"><span data-stu-id="705b5-103">JetBeginSession Function</span></span>


<span data-ttu-id="705b5-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="705b5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="705b5-105">JetBeginSession 函式</span><span class="sxs-lookup"><span data-stu-id="705b5-105">JetBeginSession Function</span></span>

<span data-ttu-id="705b5-106">**JetBeginSession** 函式會啟動會話，並初始化並傳回 ESE 會話控制碼 ([JET_SESID](./jet-sesid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="705b5-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="705b5-107">會話會控制資料庫的所有存取權，並且用來控制交易的範圍。</span><span class="sxs-lookup"><span data-stu-id="705b5-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="705b5-108">會話可以用來開始、認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="705b5-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="705b5-109">會話也會用來附加、建立或開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="705b5-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="705b5-110">此會話會當做所有 DDL 和 DML 作業的內容使用。</span><span class="sxs-lookup"><span data-stu-id="705b5-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="705b5-111">若要增加資料庫的平行存取和平行存取，可以開始多個會話。</span><span class="sxs-lookup"><span data-stu-id="705b5-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="705b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="705b5-112">Parameters</span></span>

<span data-ttu-id="705b5-113">*實例*</span><span class="sxs-lookup"><span data-stu-id="705b5-113">*instance*</span></span>

<span data-ttu-id="705b5-114">此呼叫所要使用的資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="705b5-114">The database instance to use for this call.</span></span>

<span data-ttu-id="705b5-115">*psesid*</span><span class="sxs-lookup"><span data-stu-id="705b5-115">*psesid*</span></span>

<span data-ttu-id="705b5-116">在成功傳回時，會話控制碼初始化之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="705b5-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="705b5-117">*szUserName*</span><span class="sxs-lookup"><span data-stu-id="705b5-117">*szUserName*</span></span>

<span data-ttu-id="705b5-118">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="705b5-118">This parameter is reserved.</span></span>

<span data-ttu-id="705b5-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="705b5-119">*szPassword*</span></span>

<span data-ttu-id="705b5-120">此參數已保留備用。</span><span class="sxs-lookup"><span data-stu-id="705b5-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="705b5-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="705b5-121">Return Value</span></span>

<span data-ttu-id="705b5-122">此函數可讓您傳回在此 API 中定義的任何 [JET_ERR](./jet-err.md)。</span><span class="sxs-lookup"><span data-stu-id="705b5-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="705b5-123">如需有關 Jet 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="705b5-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="705b5-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="705b5-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="705b5-125">Description</span><span class="sxs-lookup"><span data-stu-id="705b5-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705b5-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="705b5-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="705b5-127">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="705b5-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="705b5-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="705b5-129">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="705b5-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="705b5-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="705b5-131">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="705b5-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="705b5-132">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="705b5-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="705b5-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="705b5-134">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="705b5-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="705b5-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="705b5-136">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="705b5-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="705b5-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="705b5-138">因為無法配置記憶體，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="705b5-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="705b5-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="705b5-140">引擎可讓用戶端啟動的會話數目有限。</span><span class="sxs-lookup"><span data-stu-id="705b5-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="705b5-141">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 JET_paramMaxSessions 常數來變更這個值。</span><span class="sxs-lookup"><span data-stu-id="705b5-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="705b5-142">會話的預設數目為16。</span><span class="sxs-lookup"><span data-stu-id="705b5-142">The default number of sessions is 16.</span></span> <span data-ttu-id="705b5-143">如需 JET_paramMaxSessions 的詳細資訊，請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a> 。</span><span class="sxs-lookup"><span data-stu-id="705b5-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="705b5-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="705b5-145">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="705b5-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="705b5-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="705b5-147">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="705b5-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="705b5-148">成功時，會初始化會話控制碼，並可用於資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="705b5-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="705b5-149">失敗時，沒有可用的會話，或無法初始化新的會話。</span><span class="sxs-lookup"><span data-stu-id="705b5-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="705b5-150">備註</span><span class="sxs-lookup"><span data-stu-id="705b5-150">Remarks</span></span>

<span data-ttu-id="705b5-151">使用不同執行緒之間的會話時，必須小心使用。</span><span class="sxs-lookup"><span data-stu-id="705b5-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="705b5-152">會話會追蹤在 [JetBeginTransaction](./jetbegintransaction-function.md)、 [JetCommitTransaction](./jetcommittransaction-function.md)或 [JetRollback](./jetrollback-function.md)期間所使用的執行緒，如果在具有開啟交易的多個執行緒上使用，則會擲回錯誤。</span><span class="sxs-lookup"><span data-stu-id="705b5-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="705b5-153">[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)， [JetSetSessionCoNtext](./jetsetsessioncontext-function.md)可以變更此行為。</span><span class="sxs-lookup"><span data-stu-id="705b5-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="705b5-154">因為會話仍是序列化的內容，而且無法同時在單一會話上執行多個資料庫作業，所以只能以序列方式執行。</span><span class="sxs-lookup"><span data-stu-id="705b5-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="705b5-155">不過，您可以使用多個會話來達成並行資料庫存取。</span><span class="sxs-lookup"><span data-stu-id="705b5-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="705b5-156">您可以藉由設定和重設會話內容，在跨執行緒的交易內使用會話。</span><span class="sxs-lookup"><span data-stu-id="705b5-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="705b5-157">會話控制碼應該使用 [JetEndSession](./jetendsession-function.md)來關閉。</span><span class="sxs-lookup"><span data-stu-id="705b5-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="705b5-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="705b5-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705b5-159"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-160">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="705b5-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-161"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-162">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="705b5-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-163"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-164">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="705b5-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-165"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-166">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="705b5-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705b5-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-168">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="705b5-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705b5-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="705b5-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="705b5-170">實作為 <strong>JetBeginSessionW</strong> (Unicode) 和 <strong>JetBeginSessionA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="705b5-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="705b5-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="705b5-171">See Also</span></span>

[<span data-ttu-id="705b5-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="705b5-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="705b5-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="705b5-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="705b5-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="705b5-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="705b5-175">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="705b5-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="705b5-176">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="705b5-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="705b5-177">JetDupSession</span><span class="sxs-lookup"><span data-stu-id="705b5-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="705b5-178">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="705b5-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="705b5-179">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="705b5-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="705b5-180">JetRollback</span><span class="sxs-lookup"><span data-stu-id="705b5-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="705b5-181">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="705b5-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="705b5-182">JetStopService</span><span class="sxs-lookup"><span data-stu-id="705b5-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="705b5-183">系統參數</span><span class="sxs-lookup"><span data-stu-id="705b5-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
