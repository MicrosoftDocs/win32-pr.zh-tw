---
description: 深入瞭解： JetStopBackup 函數
title: JetStopBackup 函式
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106983935"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="f2f71-103">JetStopBackup 函式</span><span class="sxs-lookup"><span data-stu-id="f2f71-103">JetStopBackup Function</span></span>


<span data-ttu-id="f2f71-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2f71-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="f2f71-105">JetStopBackup 函式</span><span class="sxs-lookup"><span data-stu-id="f2f71-105">JetStopBackup Function</span></span>

<span data-ttu-id="f2f71-106">**JetStopBackup** 函式會防止任何串流備份相關的活動繼續執行特定執行中的實例，進而以可預測的方式結束串流備份。</span><span class="sxs-lookup"><span data-stu-id="f2f71-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="f2f71-107">**WINDOWS XP：**  這項功能是在 Windows XP 中引進。</span><span class="sxs-lookup"><span data-stu-id="f2f71-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="f2f71-108">[JetStopService](./jetstopservice-function.md) 是僅允許一個實例時的舊版呼叫。</span><span class="sxs-lookup"><span data-stu-id="f2f71-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="f2f71-109">在此情況下，唯一的作用中實例是準備進行終止的實例。</span><span class="sxs-lookup"><span data-stu-id="f2f71-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="f2f71-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2f71-110">Parameters</span></span>

<span data-ttu-id="f2f71-111">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f2f71-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="f2f71-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2f71-112">Return Value</span></span>

<span data-ttu-id="f2f71-113">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f2f71-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2f71-114">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f2f71-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2f71-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f2f71-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2f71-116">Description</span><span class="sxs-lookup"><span data-stu-id="f2f71-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f71-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f2f71-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f2f71-118">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f2f71-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f71-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f2f71-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f2f71-120">使用具有多個實例模式的 <a href="gg269240(v=exchg.10).md">JetStopService</a> 時，不會清除要準備終止的實例。</span><span class="sxs-lookup"><span data-stu-id="f2f71-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="f2f71-121"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f2f71-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2f71-122">如果此函式成功，實例將開始失敗任何新的串流備份 Api。</span><span class="sxs-lookup"><span data-stu-id="f2f71-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="f2f71-123">如果此函式失敗，就不會執行在實例上進行備份終止的任何步驟，也不會發生實例狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="f2f71-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f2f71-124">備註</span><span class="sxs-lookup"><span data-stu-id="f2f71-124">Remarks</span></span>

<span data-ttu-id="f2f71-125">備份通常是由進程機制之外的事件所觸發，而使用此 API 時，ESENT 應用程式本身會對串流備份 Api 進行任何進一步的呼叫，以使其失敗。</span><span class="sxs-lookup"><span data-stu-id="f2f71-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="f2f71-126">大部分的串流備份 Api 都會隨著 JET_errBackupAbortByServer 開始失敗。</span><span class="sxs-lookup"><span data-stu-id="f2f71-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="f2f71-127">因此，任何串流備份進度 (如 [JetReadFileInstance](./jetreadfileinstance-function.md)) 都會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2f71-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="f2f71-128">備份終止 (的備份作業（例如 [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ）仍會被允許。</span><span class="sxs-lookup"><span data-stu-id="f2f71-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f2f71-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2f71-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f71-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f2f71-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f71-131">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f2f71-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f71-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f2f71-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f71-133">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f2f71-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f71-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f2f71-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f71-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f2f71-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f71-136"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f2f71-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f71-137">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f2f71-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f71-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f2f71-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f71-139">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f2f71-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2f71-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2f71-140">See Also</span></span>

[<span data-ttu-id="f2f71-141">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="f2f71-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="f2f71-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2f71-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2f71-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f2f71-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f2f71-144">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="f2f71-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="f2f71-145">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f2f71-145">JetStopService</span></span>](./jetstopservice-function.md)
