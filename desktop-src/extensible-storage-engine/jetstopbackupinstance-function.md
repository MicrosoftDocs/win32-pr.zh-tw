---
description: 深入瞭解： JetStopBackupInstance 函數
title: JetStopBackupInstance 函式
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112516"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="a9a64-103">JetStopBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="a9a64-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="a9a64-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a9a64-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="a9a64-105">JetStopBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="a9a64-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="a9a64-106">**JetStopBackupInstance** 函式會防止串流備份相關的活動繼續執行特定執行中的實例，進而以可預測的方式結束串流備份。</span><span class="sxs-lookup"><span data-stu-id="a9a64-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="a9a64-107">**Windows xp：**  **JetStopBackupInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a9a64-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="a9a64-108">參數</span><span class="sxs-lookup"><span data-stu-id="a9a64-108">Parameters</span></span>

<span data-ttu-id="a9a64-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="a9a64-109">*instance*</span></span>

<span data-ttu-id="a9a64-110">識別要用於 API 呼叫的正在執行的實例。</span><span class="sxs-lookup"><span data-stu-id="a9a64-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="a9a64-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9a64-111">Return Value</span></span>

<span data-ttu-id="a9a64-112">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a9a64-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a9a64-113">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a9a64-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9a64-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a9a64-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="a9a64-115">Description</span><span class="sxs-lookup"><span data-stu-id="a9a64-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9a64-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a9a64-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a9a64-117">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a9a64-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9a64-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a9a64-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a9a64-119">指定的實例參數有不正確值 (不是目前正在執行) 的實例。</span><span class="sxs-lookup"><span data-stu-id="a9a64-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="a9a64-120"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a9a64-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9a64-121">如果此函式成功，則指定的實例將開始失敗任何新的串流備份 Api。</span><span class="sxs-lookup"><span data-stu-id="a9a64-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="a9a64-122">如果此函式失敗，就不會執行在實例上進行備份終止的任何步驟，也不會發生實例狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="a9a64-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a9a64-123">備註</span><span class="sxs-lookup"><span data-stu-id="a9a64-123">Remarks</span></span>

<span data-ttu-id="a9a64-124">備份通常是由進程機制之外的事件所觸發，而使用此 API 時，ESENT 應用程式本身會對串流備份 Api 進行任何進一步的呼叫，以使其失敗。</span><span class="sxs-lookup"><span data-stu-id="a9a64-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="a9a64-125">大部分的串流備份 Api 都會隨著 JET_errBackupAbortByServer 開始失敗。</span><span class="sxs-lookup"><span data-stu-id="a9a64-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="a9a64-126">因此，任何串流備份進度 (例如 [JetReadFileInstance](./jetreadfileinstance-function.md)) 都會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9a64-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="a9a64-127">備份終止 (的備份作業（例如 [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ）仍會被允許。</span><span class="sxs-lookup"><span data-stu-id="a9a64-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a9a64-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9a64-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9a64-129"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a9a64-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a9a64-130">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a9a64-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9a64-131"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a9a64-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a9a64-132">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a9a64-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9a64-133"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a9a64-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a9a64-134">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a9a64-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9a64-135"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a9a64-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a9a64-136">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a9a64-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9a64-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a9a64-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a9a64-138">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a9a64-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a9a64-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9a64-139">See Also</span></span>

[<span data-ttu-id="a9a64-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a9a64-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a9a64-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9a64-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a9a64-142">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="a9a64-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="a9a64-143">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="a9a64-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="a9a64-144">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a9a64-144">JetStopService</span></span>](./jetstopservice-function.md)
