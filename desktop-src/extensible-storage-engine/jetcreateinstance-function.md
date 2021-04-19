---
description: 深入瞭解： JetCreateInstance 函數
title: JetCreateInstance 函式
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989052"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="3f606-103">JetCreateInstance 函式</span><span class="sxs-lookup"><span data-stu-id="3f606-103">JetCreateInstance Function</span></span>


<span data-ttu-id="3f606-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3f606-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="3f606-105">JetCreateInstance 函式</span><span class="sxs-lookup"><span data-stu-id="3f606-105">JetCreateInstance Function</span></span>

<span data-ttu-id="3f606-106">**JetCreateInstance** 函式會配置新的 database engine 實例，以便在單一進程中使用。</span><span class="sxs-lookup"><span data-stu-id="3f606-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="3f606-107">**Windows xp： JetCreateInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="3f606-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="3f606-108">參數</span><span class="sxs-lookup"><span data-stu-id="3f606-108">Parameters</span></span>

<span data-ttu-id="3f606-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="3f606-109">*pinstance*</span></span>

<span data-ttu-id="3f606-110">接收新建立之實例的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3f606-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="3f606-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="3f606-111">*szInstanceName*</span></span>

<span data-ttu-id="3f606-112">要建立之實例的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f606-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="3f606-113">這個字串在主控資料庫引擎的指定進程內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3f606-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="3f606-114">**注意** Null 值會被視為實例的有效字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f606-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="3f606-115">只有一個實例可以有 Null 字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f606-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="3f606-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f606-116">Return Value</span></span>

<span data-ttu-id="3f606-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="3f606-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3f606-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3f606-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f606-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3f606-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="3f606-120">Description</span><span class="sxs-lookup"><span data-stu-id="3f606-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f606-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3f606-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3f606-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3f606-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f606-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="3f606-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="3f606-124">指定的實例名稱已用於此進程。</span><span class="sxs-lookup"><span data-stu-id="3f606-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f606-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3f606-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3f606-126">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="3f606-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="3f606-127">當<em>pinstance</em>為<strong>Null</strong>時， <strong>JetCreateInstance</strong>可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="3f606-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f606-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="3f606-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="3f606-129">作業失敗，因為當 database engine 在單一實例模式中運作時，無法使用此作業 (Windows 2000 相容性模式) 。</span><span class="sxs-lookup"><span data-stu-id="3f606-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f606-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="3f606-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="3f606-131">因為已達到實例的數目上限，所以無法建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="3f606-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="3f606-132">支援的實例數目上限是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> （使用 <em>JET_paramMaxInstances</em>）來設定。</span><span class="sxs-lookup"><span data-stu-id="3f606-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3f606-133">成功時，將會配置新的實例，並傳回它的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f606-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="3f606-134">此時，實例的所有系統參數都會有全域預設系統參數的值。</span><span class="sxs-lookup"><span data-stu-id="3f606-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="3f606-135">一旦配置實例之後，就必須稍後再將其終止及/或釋放。</span><span class="sxs-lookup"><span data-stu-id="3f606-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="3f606-136">失敗時，將會傳回代表失敗原因的錯誤，且不會配置任何實例。</span><span class="sxs-lookup"><span data-stu-id="3f606-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3f606-137">備註</span><span class="sxs-lookup"><span data-stu-id="3f606-137">Remarks</span></span>

<span data-ttu-id="3f606-138">必須先使用 [JetInit](./jetinit-function.md) 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。</span><span class="sxs-lookup"><span data-stu-id="3f606-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="3f606-139">實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md)初始化也是一樣。</span><span class="sxs-lookup"><span data-stu-id="3f606-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="3f606-140">可以在任何時間建立的實例數目上限是由 [JET_paramMaxInstances](./resource-parameters.md)所控制，可以透過呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。</span><span class="sxs-lookup"><span data-stu-id="3f606-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="3f606-141">實例是 database engine 的復原單位。</span><span class="sxs-lookup"><span data-stu-id="3f606-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="3f606-142">它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="3f606-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="3f606-143">這些檔案包括檢查點檔案和交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3f606-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="3f606-144">如果函式成功，資料庫引擎將會自動變更為多重實例模式，做為此呼叫的副作用。</span><span class="sxs-lookup"><span data-stu-id="3f606-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="3f606-145">如果應用程式想要在進程中只允許一個實例，則應該使用 [JetInit](./jetinit-function.md) 來啟動 Windows 2000 相容性模式中的 database engine。</span><span class="sxs-lookup"><span data-stu-id="3f606-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="3f606-146">如果有的話， *szDisplayName* 會用來識別事件記錄檔中的實例，或與其他呼叫端（例如，透過 [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) 或 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)) 等函式的備份應用 (程式）。</span><span class="sxs-lookup"><span data-stu-id="3f606-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="3f606-147">如果未提供顯示名稱，則會改用唯一的 *szInstanceName* （如果有的話），否則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="3f606-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="3f606-148">如果引擎沒有設定執行中的模式，則在呼叫之後，它會設定為多重實例模式。</span><span class="sxs-lookup"><span data-stu-id="3f606-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="3f606-149">可能執行多個 Jet 實例之進程的一般啟動順序為：</span><span class="sxs-lookup"><span data-stu-id="3f606-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="3f606-150">呼叫 [JetCreateInstance2](./jetcreateinstance2-function.md) ，它會配置並命名實例。</span><span class="sxs-lookup"><span data-stu-id="3f606-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="3f606-151">針對該實例的多個 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 呼叫，以便設定不同的系統參數。</span><span class="sxs-lookup"><span data-stu-id="3f606-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="3f606-152">請注意，某些系統參數在每個實例上都必須是唯一的 (例如 [JET_paramSystemPath](./transaction-log-parameters.md) 或 [JET_paramLogFilePath](./transaction-log-parameters.md)) 因此最有可能需要設定每一種。</span><span class="sxs-lookup"><span data-stu-id="3f606-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="3f606-153">使用 [JetInit](./jetinit-function.md) 或 [JetInit2](./jetinit2-function.md)來啟動實例。</span><span class="sxs-lookup"><span data-stu-id="3f606-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="3f606-154">為了終止及/或釋放實例，必須使用 [JetTerm](./jetterm-function.md)、 [JetTerm2](./jetterm2-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="3f606-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="3f606-155">如果這是第一個要啟動的實例，則在此呼叫期間會執行一些額外的步驟，以便進行基本系統初始化和設定。</span><span class="sxs-lookup"><span data-stu-id="3f606-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="3f606-156">其中一些步驟可能會導致從 JET_errOutOfMemory 開始的特定錯誤，但也 (看到上述錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="3f606-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3f606-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f606-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f606-158"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-159">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="3f606-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f606-160"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-161">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="3f606-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f606-162"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-163">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3f606-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f606-164"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-165">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="3f606-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f606-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-167">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="3f606-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f606-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3f606-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3f606-169">實作為 <strong>JetCreateInstanceW</strong> (Unicode) 和 <strong>JetCreateInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="3f606-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3f606-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f606-170">See Also</span></span>

[<span data-ttu-id="3f606-171">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="3f606-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="3f606-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3f606-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3f606-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3f606-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3f606-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="3f606-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="3f606-175">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="3f606-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="3f606-176">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="3f606-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="3f606-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="3f606-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="3f606-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="3f606-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="3f606-179">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="3f606-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="3f606-180">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3f606-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3f606-181">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3f606-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="3f606-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="3f606-182">JetTerm2</span></span>](./jetterm2-function.md)
