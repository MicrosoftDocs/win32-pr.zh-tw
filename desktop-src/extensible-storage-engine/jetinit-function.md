---
description: 深入瞭解： JetInit 函數
title: JetInit 函式
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323463"
---
# <a name="jetinit-function"></a><span data-ttu-id="4a4a5-103">JetInit 函式</span><span class="sxs-lookup"><span data-stu-id="4a4a5-103">JetInit Function</span></span>


<span data-ttu-id="4a4a5-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a4a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="4a4a5-105">JetInit 函式</span><span class="sxs-lookup"><span data-stu-id="4a4a5-105">JetInit Function</span></span>

<span data-ttu-id="4a4a5-106">**JetInit** 函式會將資料庫引擎置於可支援資料庫檔案之應用程式使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="4a4a5-107">引擎必須已正確設定，才能使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行初始化。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="4a4a5-108">資料庫損毀復原會在初始化過程中自動執行。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="4a4a5-109">參數</span><span class="sxs-lookup"><span data-stu-id="4a4a5-109">Parameters</span></span>

<span data-ttu-id="4a4a5-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="4a4a5-110">*pinstance*</span></span>

<span data-ttu-id="4a4a5-111">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-111">The instance to use for this call.</span></span>

<span data-ttu-id="4a4a5-112">若為 Windows 2000，則會忽略此參數，且應一律為 Null。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="4a4a5-113">若為 Windows XP 和更新版本，則使用這個參數取決於引擎的操作模式。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="4a4a5-114">如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可以是 Null，也可以設定為有效的輸出緩衝區，它會傳回做為初始化的副作用而建立的全域實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="4a4a5-115">此輸出緩衝區必須設定為 Null 或 JET_instanceNil。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="4a4a5-116">然後，這個實例控制碼可以傳遞給任何其他使用實例的函數。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="4a4a5-117">如果引擎是在多重實例模式中作業，則這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 函式實例所傳回的實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="4a4a5-118">備註</span><span class="sxs-lookup"><span data-stu-id="4a4a5-118">Remarks</span></span>

<span data-ttu-id="4a4a5-119">必須先使用 **JetInit** 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="4a4a5-120">實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 **JetInit** 初始化也是一樣。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="4a4a5-121">實例是 database engine 的復原單位。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="4a4a5-122">它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="4a4a5-123">這些檔案包括檢查點檔案和交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="4a4a5-124">可以在任何時間建立的實例數目上限是由 [JET_paramMaxInstances](./resource-parameters.md)所控制，可以透過呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="4a4a5-125">當資料庫引擎第一次初始化時， **JetInit** 會建立一組初始的檔案，以支援該實例。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="4a4a5-126">這些檔案包含名為 (的檢查點檔案 \<[JET_paramBaseName](./transaction-log-parameters.md)\> 。.CHK) 是一組名為 RES1 (的保留交易記錄檔。記錄檔和 RES2。記錄) ， (名為的初始交易記錄檔 \<[JET_paramBaseName](./transaction-log-parameters.md)\> 。記錄) 和暫存資料庫檔案 (根據 [JET_paramTempPath](./temporary-database-parameters.md)) 進行命名。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="4a4a5-127">如果 [JET_paramRecovery](./transaction-log-parameters.md) 設定為 [關閉]，則不會建立檢查點檔案和記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="4a4a5-128">如果 [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) 設定為零，則不會建立暫存資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="4a4a5-129">這些檔案代表實例的磁片使用量，且必須小心管理。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="4a4a5-130">如果這些檔案是個別損毀或彼此相關，則與實例相關聯之資料庫中儲存的資料可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="4a4a5-131">使用一組現有的交易記錄檔初始化資料庫引擎時，系統會檢查這些檔案，以查看先前的具現化身是否遇到損毀。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="4a4a5-132">如果偵測到損毀，則會自動執行損毀復原。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="4a4a5-133">此程式會在先前化身引擎期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="4a4a5-134">結果會是交易一致的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="4a4a5-135">如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要很長的時間。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="4a4a5-136">由於 **JetInit** 會執行損毀復原，因此在發生失敗的情況下，幾乎可能會傳回任何資料庫引擎錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="4a4a5-137">在實務上，部署中的大部分錯誤都分為兩種類別：資料損毀和檔案 mismanagement。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="4a4a5-138">資料損毀的資訊清單本身通常會出現在下列或類似的錯誤中：</span><span class="sxs-lookup"><span data-stu-id="4a4a5-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="4a4a5-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="4a4a5-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="4a4a5-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="4a4a5-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="4a4a5-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="4a4a5-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="4a4a5-142">這些錯誤幾乎都是由硬體問題所造成，因此無法避免。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="4a4a5-143">檔案 mismanagement 會在下列或類似的錯誤中最常出現的資訊清單：</span><span class="sxs-lookup"><span data-stu-id="4a4a5-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="4a4a5-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="4a4a5-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="4a4a5-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="4a4a5-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="4a4a5-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4a4a5-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="4a4a5-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="4a4a5-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="4a4a5-148">如果復原是在一組記錄檔上執行，而且並非所有資料庫都存在 (這會在正常) 情況下傳回錯誤 JET_errAttachedDatabaseMismatch，而且用戶端想要復原以 JET_ 繼續進行可用的資料庫的復原。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="4a4a5-149">這些錯誤是由應用程式所 preventable。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-149">These errors are preventable by the application.</span></span> <span data-ttu-id="4a4a5-150">應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="4a4a5-151">如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="4a4a5-152">這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="4a4a5-153">在 Windows 2000 和更新版本之間， **JetInit** 函式的行為與附加至實例的資料庫檔案有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="4a4a5-154">**Windows 2000：**  在 Windows 2000 中，在先前化身實例期間附加至實例的任何資料庫，在 **JetInit** 順利完成之後仍會附加至實例。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="4a4a5-155">在 **JetInit** 之後不需要呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) ，以確保日後的資料庫存取。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="4a4a5-156">如果在 **JetInit** 函數之後呼叫 [JetAttachDatabase](./jetattachdatabase-function.md)函數，則會傳回 JET_wrnDatabaseAttached 警告。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="4a4a5-157">此警告表示已保留資料庫附件，而且可以忽略。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="4a4a5-158">**WINDOWS XP：**  在 Windows XP 和更新版本中， **JetInit** 會自動將所有資料庫從實例卸離。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="4a4a5-159">這表示在這種情況下，必須一律在 **JetInit** 之後呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="4a4a5-160">任何撰寫為在 Windows 2000 和更新版本上執行的應用程式，在 **JetInit** 之後都必須一律呼叫 [JetAttachDatabase](./jetattachdatabase-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="4a4a5-161">如果應用程式在 Windows 2000 上執行，則在某些情況下，它必須預期會有 JET_wrnDatabaseAttached。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="4a4a5-162">如需詳細資訊，請參閱 [JetAttachDatabase](./jetattachdatabase-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4a4a5-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a4a5-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a4a5-164"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4a4a5-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a4a5-165">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a4a5-166"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4a4a5-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a4a5-167">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a4a5-168"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4a4a5-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a4a5-169">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a4a5-170"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4a4a5-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4a4a5-171">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a4a5-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4a4a5-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4a4a5-173">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4a4a5-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4a4a5-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a4a5-174">See Also</span></span>

[<span data-ttu-id="4a4a5-175">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="4a4a5-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="4a4a5-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4a4a5-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4a4a5-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4a4a5-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4a4a5-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a4a5-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4a4a5-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="4a4a5-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="4a4a5-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="4a4a5-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="4a4a5-181">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="4a4a5-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="4a4a5-182">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4a4a5-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4a4a5-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="4a4a5-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="4a4a5-184">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4a4a5-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
