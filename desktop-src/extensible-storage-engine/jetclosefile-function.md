---
description: 深入瞭解： JetCloseFile 函數
title: JetCloseFile 函式
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386085"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="73390-103">JetCloseFile 函式</span><span class="sxs-lookup"><span data-stu-id="73390-103">JetCloseFile Function</span></span>


<span data-ttu-id="73390-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="73390-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="73390-105">JetCloseFile 函式</span><span class="sxs-lookup"><span data-stu-id="73390-105">JetCloseFile Function</span></span>

<span data-ttu-id="73390-106">**JetCloseFile** 函式會在使用 [JetReadFile](./jetreadfile-function.md)解壓縮該檔案中的資料之後，關閉使用 [JetOpenFile](./jetopenfile-function.md)開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="73390-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="73390-107">參數</span><span class="sxs-lookup"><span data-stu-id="73390-107">Parameters</span></span>

<span data-ttu-id="73390-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="73390-108">*hfFile*</span></span>

<span data-ttu-id="73390-109">要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="73390-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="73390-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="73390-110">Return Value</span></span>

<span data-ttu-id="73390-111">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="73390-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="73390-112">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="73390-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73390-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="73390-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="73390-114">Description</span><span class="sxs-lookup"><span data-stu-id="73390-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73390-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="73390-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="73390-116">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="73390-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="73390-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="73390-118">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="73390-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="73390-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="73390-120">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="73390-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="73390-121">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="73390-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="73390-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="73390-123">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="73390-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="73390-124">在下列情況下， <strong>JetCloseFile</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="73390-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="73390-125"> (Windows XP 和更新版本) ，指定的實例控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="73390-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="73390-126">指定的檔案控制代碼無效。</span><span class="sxs-lookup"><span data-stu-id="73390-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="73390-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="73390-128">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="73390-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="73390-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="73390-130">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="73390-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="73390-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="73390-132">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="73390-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="73390-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="73390-134">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="73390-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="73390-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="73390-136">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="73390-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73390-137">成功時，會關閉檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="73390-137">On success, the file handle is closed.</span></span> <span data-ttu-id="73390-138">如果資料庫檔案已關閉，則相關聯的資料庫修補檔 (（如果有任何) 損毀）。</span><span class="sxs-lookup"><span data-stu-id="73390-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="73390-139">失敗時，不會發生任何變更。</span><span class="sxs-lookup"><span data-stu-id="73390-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="73390-140">備註</span><span class="sxs-lookup"><span data-stu-id="73390-140">Remarks</span></span>

<span data-ttu-id="73390-141">資料庫引擎目前僅支援透過 [JetOpenFile](./jetopenfile-function.md) 一次開啟一個開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="73390-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="73390-142">如果使用 [JetOpenFile](./jetopenfile-function.md) 來開啟檔案控制代碼，則必須先使用 **JetCloseFile** 關閉，才能開啟另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="73390-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="73390-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="73390-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73390-144"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="73390-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73390-145">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="73390-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-146"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="73390-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73390-147">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="73390-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-148"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="73390-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73390-149">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="73390-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73390-150"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="73390-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="73390-151">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="73390-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73390-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="73390-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="73390-153">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="73390-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="73390-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73390-154">See Also</span></span>

[<span data-ttu-id="73390-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="73390-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="73390-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="73390-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="73390-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="73390-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="73390-158">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="73390-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="73390-159">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="73390-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="73390-160">JetStopService</span><span class="sxs-lookup"><span data-stu-id="73390-160">JetStopService</span></span>](./jetstopservice-function.md)
