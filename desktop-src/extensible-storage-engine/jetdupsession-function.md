---
description: 深入瞭解： JetDupSession 函數
title: JetDupSession 函式
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851436"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="1cbb9-103">JetDupSession 函式</span><span class="sxs-lookup"><span data-stu-id="1cbb9-103">JetDupSession Function</span></span>


<span data-ttu-id="1cbb9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1cbb9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="1cbb9-105">JetDupSession 函式</span><span class="sxs-lookup"><span data-stu-id="1cbb9-105">JetDupSession Function</span></span>

<span data-ttu-id="1cbb9-106">**JetDupSession** 函式會啟動會話，並初始化並傳回 ESE 會話控制碼 ([JET_SESID](./jet-sesid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="1cbb9-107">會話會控制資料庫的所有存取權，並且用來控制交易的範圍。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="1cbb9-108">會話可以用來開始、認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="1cbb9-109">會話也會用來附加、建立或開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="1cbb9-110">此會話會當做所有 DDL 和 DML 作業的內容使用。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="1cbb9-111">若要增加資料庫的平行存取和平行存取，可以開始多個會話。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="1cbb9-112">**注意** 此 API 會以所有方式運作，以在傳入的會話實例上呼叫 [JetBeginSession](./jetbeginsession-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="1cbb9-113">不建議使用此函數，建議使用 [JetBeginSession](./jetbeginsession-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="1cbb9-114">參數</span><span class="sxs-lookup"><span data-stu-id="1cbb9-114">Parameters</span></span>

<span data-ttu-id="1cbb9-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1cbb9-115">*sesid*</span></span>

<span data-ttu-id="1cbb9-116">要用來做為複製或開始會話之來源的會話。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="1cbb9-117">*psesid*</span><span class="sxs-lookup"><span data-stu-id="1cbb9-117">*psesid*</span></span>

<span data-ttu-id="1cbb9-118">在成功傳回時，會話控制碼初始化之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="1cbb9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cbb9-119">Return Value</span></span>

<span data-ttu-id="1cbb9-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1cbb9-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cbb9-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1cbb9-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="1cbb9-123">Description</span><span class="sxs-lookup"><span data-stu-id="1cbb9-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1cbb9-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1cbb9-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1cbb9-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-129">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1cbb9-130">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1cbb9-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-132">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1cbb9-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-134">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1cbb9-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-136">因為無法配置記憶體，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="1cbb9-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-138">引擎可讓用戶端啟動的會話數目有限。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="1cbb9-139">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <em>JET_paramMaxSessions</em> 常數來變更這個值。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="1cbb9-140">會話的預設數目為16。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-140">The default number of sessions is 16.</span></span> <span data-ttu-id="1cbb9-141">如需<em>JET_paramMaxSessions</em>的詳細資訊，請參閱<a href="gg294139(v=exchg.10).md">系統參數</a>。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1cbb9-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-143">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1cbb9-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1cbb9-145">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cbb9-146">成功時，會初始化會話控制碼，並可用於資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="1cbb9-147">失敗時，沒有可用的會話，或無法初始化新的會話。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1cbb9-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cbb9-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-149"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1cbb9-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1cbb9-150">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-151"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1cbb9-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1cbb9-152">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-153"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1cbb9-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1cbb9-154">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cbb9-155"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="1cbb9-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1cbb9-156">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cbb9-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1cbb9-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1cbb9-158">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1cbb9-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cbb9-159">See Also</span></span>

[<span data-ttu-id="1cbb9-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1cbb9-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1cbb9-161">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="1cbb9-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="1cbb9-162">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="1cbb9-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="1cbb9-163">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1cbb9-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="1cbb9-164">系統參數</span><span class="sxs-lookup"><span data-stu-id="1cbb9-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
