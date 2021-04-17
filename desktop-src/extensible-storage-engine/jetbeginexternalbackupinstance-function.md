---
description: 深入瞭解： JetBeginExternalBackupInstance 函數
title: JetBeginExternalBackupInstance 函式
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468708"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="4406e-103">JetBeginExternalBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4406e-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="4406e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4406e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="4406e-105">JetBeginExternalBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="4406e-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="4406e-106">**JetBeginExternalBackupInstance** 函式會在引擎和資料庫處於線上狀態且為使用中時，起始外部備份。</span><span class="sxs-lookup"><span data-stu-id="4406e-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="4406e-107">**Windows xp： JetBeginExternalBackupInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="4406e-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4406e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4406e-108">Parameters</span></span>

<span data-ttu-id="4406e-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="4406e-109">*instance*</span></span>

<span data-ttu-id="4406e-110">此呼叫所要使用的資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="4406e-110">The database instance to use for this call.</span></span>

<span data-ttu-id="4406e-111">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="4406e-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="4406e-112">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="4406e-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="4406e-113">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="4406e-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="4406e-114">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="4406e-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="4406e-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4406e-115">*grbit*</span></span>

<span data-ttu-id="4406e-116">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="4406e-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4406e-117">值</span><span class="sxs-lookup"><span data-stu-id="4406e-117">Value</span></span></p></th>
<th><p><span data-ttu-id="4406e-118">意義</span><span class="sxs-lookup"><span data-stu-id="4406e-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4406e-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="4406e-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="4406e-120">此旗標已被取代。</span><span class="sxs-lookup"><span data-stu-id="4406e-120">This flag is deprecated.</span></span> <span data-ttu-id="4406e-121">使用此位會導致傳回 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="4406e-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4406e-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="4406e-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="4406e-123">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="4406e-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="4406e-124">這表示只會備份自上次完整或增量備份之後的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4406e-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4406e-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="4406e-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="4406e-126">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="4406e-126">Reserved for future use.</span></span> <span data-ttu-id="4406e-127">針對 Windows XP 定義。</span><span class="sxs-lookup"><span data-stu-id="4406e-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4406e-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4406e-128">Return Value</span></span>

<span data-ttu-id="4406e-129">因為呼叫此函式，所以系統可能會產生成功或失敗的代碼。</span><span class="sxs-lookup"><span data-stu-id="4406e-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="4406e-130">如需此 API 的完整錯誤清單，請參閱 [可擴充儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="4406e-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="4406e-131">請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。</span><span class="sxs-lookup"><span data-stu-id="4406e-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="4406e-132">備註</span><span class="sxs-lookup"><span data-stu-id="4406e-132">Remarks</span></span>

<span data-ttu-id="4406e-133">**JetBeginExternalBackupInstance** 是一系列函式中的第一個函式，必須呼叫這些函式，以執行 (非 VSS 型) 備份的線上功能。</span><span class="sxs-lookup"><span data-stu-id="4406e-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="4406e-134">另請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) 和 [JetStopBackupInstance](./jetstopbackupinstance-function.md)。</span><span class="sxs-lookup"><span data-stu-id="4406e-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="4406e-135">外部備份可以用來執行完整、增量或差異備份。</span><span class="sxs-lookup"><span data-stu-id="4406e-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="4406e-136">備份將會是模糊的，在此情況下，備份將會與交易記錄中的單一時間點一致，但目前不可能控制確切的時間點。</span><span class="sxs-lookup"><span data-stu-id="4406e-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4406e-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="4406e-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4406e-138"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4406e-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4406e-139">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4406e-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4406e-140"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4406e-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4406e-141">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4406e-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4406e-142"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4406e-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4406e-143">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4406e-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4406e-144"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4406e-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4406e-145">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4406e-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4406e-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4406e-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4406e-147">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4406e-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4406e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4406e-148">See Also</span></span>

[<span data-ttu-id="4406e-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4406e-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4406e-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4406e-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4406e-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4406e-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4406e-152">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="4406e-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="4406e-153">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="4406e-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="4406e-154">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="4406e-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="4406e-155">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="4406e-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="4406e-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="4406e-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="4406e-157">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="4406e-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="4406e-158">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="4406e-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="4406e-159">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="4406e-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="4406e-160">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="4406e-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="4406e-161">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="4406e-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="4406e-162">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="4406e-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
