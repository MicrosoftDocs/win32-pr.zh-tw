---
description: 深入瞭解： JetCloseFileInstance 函數
title: JetCloseFileInstance 函式
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510918"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="1b9c6-103">JetCloseFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="1b9c6-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="1b9c6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1b9c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="1b9c6-105">JetCloseFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="1b9c6-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="1b9c6-106">**JetCloseFileInstance** 函式會在使用 [JetReadFileInstance](./jetreadfileinstance-function.md)解壓縮該檔案中的資料之後，關閉使用 [JetOpenFileInstance](./jetopenfileinstance-function.md)開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="1b9c6-107">**Windows xp： JetCloseFileInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="1b9c6-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b9c6-108">Parameters</span></span>

<span data-ttu-id="1b9c6-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="1b9c6-109">*instance*</span></span>

<span data-ttu-id="1b9c6-110">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-110">The instance to use for this call.</span></span>

<span data-ttu-id="1b9c6-111">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="1b9c6-112">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="1b9c6-113">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="1b9c6-114">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="1b9c6-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="1b9c6-115">*hfFile*</span></span>

<span data-ttu-id="1b9c6-116">要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="1b9c6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b9c6-117">Return Value</span></span>

<span data-ttu-id="1b9c6-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1b9c6-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b9c6-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1b9c6-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="1b9c6-121">Description</span><span class="sxs-lookup"><span data-stu-id="1b9c6-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1b9c6-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1b9c6-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-125">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1b9c6-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-127">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="1b9c6-128">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1b9c6-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-130">提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="1b9c6-131">在下列情況下， <strong>JetCloseFileInstance</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="1b9c6-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="1b9c6-132"> (Windows XP 和更新版本時，指定的實例控制碼無效) </span><span class="sxs-lookup"><span data-stu-id="1b9c6-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="1b9c6-133">指定的檔案控制代碼無效</span><span class="sxs-lookup"><span data-stu-id="1b9c6-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="1b9c6-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-135">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1b9c6-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-137">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1b9c6-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-139">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="1b9c6-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-141">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1b9c6-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1b9c6-143">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1b9c6-144">成功時，會關閉檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-144">On success, the file handle is closed.</span></span> <span data-ttu-id="1b9c6-145">如果資料庫檔案已關閉，則相關聯的資料庫修補檔 (（如果有任何) 損毀）。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="1b9c6-146">失敗時，不會發生任何變更。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1b9c6-147">備註</span><span class="sxs-lookup"><span data-stu-id="1b9c6-147">Remarks</span></span>

<span data-ttu-id="1b9c6-148">資料庫引擎目前僅支援透過 [JetOpenFileInstance](./jetopenfileinstance-function.md) 一次開啟一個開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="1b9c6-149">如果使用 [JetOpenFileInstance](./jetopenfileinstance-function.md) 來開啟檔案控制代碼，則必須先使用 **JetCloseFileInstance** 關閉，才能開啟另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1b9c6-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b9c6-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-151"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1b9c6-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9c6-152">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-153"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1b9c6-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9c6-154">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-155"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1b9c6-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9c6-156">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b9c6-157"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="1b9c6-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9c6-158">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b9c6-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1b9c6-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1b9c6-160">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="1b9c6-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1b9c6-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b9c6-161">See Also</span></span>

[<span data-ttu-id="1b9c6-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1b9c6-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1b9c6-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="1b9c6-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="1b9c6-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1b9c6-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="1b9c6-165">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="1b9c6-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="1b9c6-166">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="1b9c6-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="1b9c6-167">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="1b9c6-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
