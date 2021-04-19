---
description: 深入瞭解： JetOpenTemporaryTable 函數
title: JetOpenTemporaryTable 函式
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975813"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="fa90e-103">JetOpenTemporaryTable 函式</span><span class="sxs-lookup"><span data-stu-id="fa90e-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="fa90e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fa90e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="fa90e-105">JetOpenTemporaryTable 函式</span><span class="sxs-lookup"><span data-stu-id="fa90e-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="fa90e-106">**JetOpenTemporaryTable** 函式會建立一個具有單一索引的 volatile 資料表，可用來儲存和取出記錄，就像透過 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="fa90e-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="fa90e-107">**Windows vista：**  **JetOpenTemporaryTable** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="fa90e-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="fa90e-108">臨時表比一般資料表快很多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="fa90e-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="fa90e-109">當記錄集以純粹順序的方式存取時，它們可以快速排序並執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="fa90e-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="fa90e-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa90e-110">Parameters</span></span>

<span data-ttu-id="fa90e-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="fa90e-111">*sesid*</span></span>

<span data-ttu-id="fa90e-112">此呼叫將使用的會話。</span><span class="sxs-lookup"><span data-stu-id="fa90e-112">The session that will be used for this call.</span></span>

<span data-ttu-id="fa90e-113">*popentemporarytable*</span><span class="sxs-lookup"><span data-stu-id="fa90e-113">*popentemporarytable*</span></span>

<span data-ttu-id="fa90e-114">[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)結構的指標，其中包含要在輸入上建立之臨時表的描述。</span><span class="sxs-lookup"><span data-stu-id="fa90e-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="fa90e-115">在成功呼叫之後，結構會包含臨時表和資料行標識的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa90e-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="fa90e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa90e-116">Return Value</span></span>

<span data-ttu-id="fa90e-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="fa90e-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fa90e-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="fa90e-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa90e-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fa90e-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="fa90e-120">Description</span><span class="sxs-lookup"><span data-stu-id="fa90e-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fa90e-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fa90e-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="fa90e-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="fa90e-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="fa90e-124">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="fa90e-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="fa90e-125">如果主機進程的位址空間變得太分散， <strong>JetOpenTemporaryTable</strong>可能會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="fa90e-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="fa90e-126">無論儲存的資料量為何，臨時表管理員都會為每個建立的臨時表配置 1 MB 的位址空間區塊。</span><span class="sxs-lookup"><span data-stu-id="fa90e-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fa90e-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fa90e-128">其中一個提供的參數包含未預期的值，或數個參數值的組合導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="fa90e-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="fa90e-129">在下列情況下， <strong>JetOpenTemporaryTable</strong> 會傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="fa90e-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa90e-130"><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbStruct</strong>成員未對應到該版本的 database engine 所支援的這個結構版本</span><span class="sxs-lookup"><span data-stu-id="fa90e-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="fa90e-131"><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbKeyMost</strong>成員小於 JET_cbKeyMostMin。</span><span class="sxs-lookup"><span data-stu-id="fa90e-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="fa90e-132"><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbKeyMost</strong>成員大於實例 (JET_paramDatabasePageSize) 之資料庫頁面大小的最大支援值。</span><span class="sxs-lookup"><span data-stu-id="fa90e-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="fa90e-133">如需詳細資訊，請參閱 <a href="gg269241(v=exchg.10).md">資訊參數</a> 清單中的 JET_paramKeyMost 參數。</span><span class="sxs-lookup"><span data-stu-id="fa90e-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="fa90e-134"><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的 cbVarSegMac 成員大於<strong>cbKeyMost</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="fa90e-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fa90e-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fa90e-136">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="fa90e-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fa90e-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fa90e-138">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="fa90e-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fa90e-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fa90e-140">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="fa90e-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="fa90e-141"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa90e-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fa90e-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa90e-143">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="fa90e-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fa90e-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa90e-145">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="fa90e-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fa90e-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fa90e-147">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa90e-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="fa90e-148"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa90e-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="fa90e-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="fa90e-150">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="fa90e-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="fa90e-151"><strong>注意</strong>  在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa90e-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="fa90e-152">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="fa90e-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="fa90e-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="fa90e-154">作業失敗，因為引擎無法配置開啟新資料指標所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fa90e-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="fa90e-155">資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa90e-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="fa90e-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="fa90e-157">作業失敗，因為引擎無法配置建立臨時表所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fa90e-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="fa90e-158">臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa90e-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="fa90e-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="fa90e-160"><strong>JetOpenTemporaryTable</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="fa90e-161"><strong>Windows Server 2003：</strong>  只有 Windows Server 2003 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa90e-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="fa90e-163">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="fa90e-164">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="fa90e-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="fa90e-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="fa90e-166">作業失敗，因為引擎無法配置快取資料表架構所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fa90e-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="fa90e-167">若要設定具有可快取之架構的資料表數目，請使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>。</span><span class="sxs-lookup"><span data-stu-id="fa90e-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="fa90e-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="fa90e-169"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="fa90e-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="fa90e-170">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="fa90e-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="fa90e-171">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="fa90e-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="fa90e-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="fa90e-173"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的<strong>coltyp</strong>成員未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="fa90e-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="fa90e-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="fa90e-175">無法建立索引，因為嘗試使用不正確地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa90e-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="fa90e-176">地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</span><span class="sxs-lookup"><span data-stu-id="fa90e-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="fa90e-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="fa90e-178">無法建立索引，因為嘗試使用一組不正確正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="fa90e-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="fa90e-179"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa90e-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="fa90e-180"><strong>Windows 2000：</strong>  在 Windows 2000 上，不正確正規化旗標會導致 JET_errIndexInvalidDef。</span><span class="sxs-lookup"><span data-stu-id="fa90e-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="fa90e-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="fa90e-182">無法建立索引，因為指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="fa90e-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="fa90e-183"><strong>JetOpenTemporaryTable</strong> 會在下列情況下傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="fa90e-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa90e-184">指定了中性語言的地區設定。</span><span class="sxs-lookup"><span data-stu-id="fa90e-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="fa90e-185">指定了不正確正規化旗標集合。</span><span class="sxs-lookup"><span data-stu-id="fa90e-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="fa90e-186"><strong>Windows 2000：</strong>  此錯誤只會由 Windows 2000 傳回。</span><span class="sxs-lookup"><span data-stu-id="fa90e-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="fa90e-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="fa90e-188">作業失敗，因為引擎無法配置快取資料表索引所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fa90e-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="fa90e-189">若要設定具有可快取之架構的索引數目，請使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>。</span><span class="sxs-lookup"><span data-stu-id="fa90e-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa90e-190">成功時，會傳回在新建立的臨時表上開啟的資料指標。</span><span class="sxs-lookup"><span data-stu-id="fa90e-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="fa90e-191">暫存資料庫的狀態將準備好包含新的臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="fa90e-192">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="fa90e-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="fa90e-193">失敗時，將不會建立臨時表，也不會傳回資料指標。</span><span class="sxs-lookup"><span data-stu-id="fa90e-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="fa90e-194">暫存資料庫的狀態可以變更。</span><span class="sxs-lookup"><span data-stu-id="fa90e-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="fa90e-195">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="fa90e-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fa90e-196">備註</span><span class="sxs-lookup"><span data-stu-id="fa90e-196">Remarks</span></span>

<span data-ttu-id="fa90e-197">臨時表不支援資料庫引擎通常支援之資料行定義選項的完整補充。</span><span class="sxs-lookup"><span data-stu-id="fa90e-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="fa90e-198">事實上，只支援 JET_bitColumnFixed 和 JET_bitColumnTagged。</span><span class="sxs-lookup"><span data-stu-id="fa90e-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="fa90e-199">這表示不可能在臨時表中建立自動遞增、版本或多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="fa90e-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="fa90e-200">最後，不支援保管更新資料行，因為一次只能由一個會話使用。</span><span class="sxs-lookup"><span data-stu-id="fa90e-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="fa90e-201">如果要求這些選項中的任何一項，則會忽略這些選項。</span><span class="sxs-lookup"><span data-stu-id="fa90e-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="fa90e-202">臨時表不支援預設值。</span><span class="sxs-lookup"><span data-stu-id="fa90e-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="fa90e-203">如果提供的資料行定義包含預設值規格，則會忽略該規格。</span><span class="sxs-lookup"><span data-stu-id="fa90e-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="fa90e-204">由於許多不同的 ESE 函數，臨時表會傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="fa90e-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="fa90e-205">例如，JET_IdxInfo 選項組的 [JetGetIndexInfo](./jetgetindexinfo-function.md) 會傳回臨時表，其中包含給定索引中所有索引鍵資料行的清單。</span><span class="sxs-lookup"><span data-stu-id="fa90e-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="fa90e-206">臨時表會遵循與一般臨時表相同的生命週期規則，如下所述。</span><span class="sxs-lookup"><span data-stu-id="fa90e-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="fa90e-207">資料庫引擎也會在內部使用臨時表來進行許多工。</span><span class="sxs-lookup"><span data-stu-id="fa90e-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="fa90e-208">這些工作中最重要的就是在現有的資料表上建立索引。</span><span class="sxs-lookup"><span data-stu-id="fa90e-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="fa90e-209">臨時表將用來排序用來建立索引的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fa90e-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="fa90e-210">所有臨時表都會儲存在暫存資料庫中。</span><span class="sxs-lookup"><span data-stu-id="fa90e-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="fa90e-211">暫存資料庫是一個特殊的資料庫檔案，會在 ESE 實例的存留期內進行維護，當該實例關閉或重新開機時，就會將其刪除。</span><span class="sxs-lookup"><span data-stu-id="fa90e-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="fa90e-212">您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramTempPath](./temporary-database-parameters.md)來設定暫存資料庫的位置。</span><span class="sxs-lookup"><span data-stu-id="fa90e-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="fa90e-213">如果您的應用程式大量使用臨時表或經常建立索引，則相對於交易記錄檔和資料庫檔案的暫存資料庫放置在磁片上可能很重要。</span><span class="sxs-lookup"><span data-stu-id="fa90e-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="fa90e-214">臨時表的生命週期會系結至參考它的資料指標。</span><span class="sxs-lookup"><span data-stu-id="fa90e-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="fa90e-215">如果參考臨時表的所有資料指標都是以隱含或明確的方式關閉，則會刪除臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="fa90e-216">如果在交易內建立臨時表，而且之後復原該交易，則會刪除該臨時表，因為此時參考該資料表的任何資料指標都會以隱含方式關閉。</span><span class="sxs-lookup"><span data-stu-id="fa90e-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="fa90e-217">新的資料指標只能透過使用 [JetDupCursor](./jetdupcursor-function.md)來參考臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="fa90e-218">在此情況下，新的資料指標將定位於臨時表的第一個索引項目目。</span><span class="sxs-lookup"><span data-stu-id="fa90e-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="fa90e-219">[JetDupCursor](./jetdupcursor-function.md) 僅適用于臨時表的特定使用階段。</span><span class="sxs-lookup"><span data-stu-id="fa90e-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="fa90e-220">如需詳細資訊，請參閱關於臨時表資料指標功能的備註。</span><span class="sxs-lookup"><span data-stu-id="fa90e-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="fa90e-221">一次只能從一個以上的會話參考臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="fa90e-222">**注意** [JetDupCursor](./jetdupcursor-function.md) 中有一個會影響臨時表的重要問題。</span><span class="sxs-lookup"><span data-stu-id="fa90e-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="fa90e-223">如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。</span><span class="sxs-lookup"><span data-stu-id="fa90e-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="fa90e-224">在具體化的臨時表上重復資料指標仍然是安全的。</span><span class="sxs-lookup"><span data-stu-id="fa90e-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="fa90e-225">臨時表管理員可以用三種方式來執行臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="fa90e-226">第一個方法是維護記憶體中的資料表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="fa90e-227">這是最快的策略，但只能用於小型、簡單的臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="fa90e-228">第二種方法是建立以磁片為基礎的排序，該排序可使用順向反覆運算器驅動。</span><span class="sxs-lookup"><span data-stu-id="fa90e-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="fa90e-229">這項策略只能在特定情況下使用，而且是從非常大的資料集排序和移除重複專案的最快速方式。</span><span class="sxs-lookup"><span data-stu-id="fa90e-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="fa90e-230">第三種方法是在暫存資料庫中建立 B + 樹狀結構，以保存臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="fa90e-231">這個策略是最慢的，但最多用途，而且稱為具體化臨時表。</span><span class="sxs-lookup"><span data-stu-id="fa90e-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="fa90e-232">這些策略可以組合使用，以最終達成臨時表所要求的功能。</span><span class="sxs-lookup"><span data-stu-id="fa90e-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="fa90e-233">當臨時表未具體化時，主要是在兩個主要階段中使用。</span><span class="sxs-lookup"><span data-stu-id="fa90e-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="fa90e-234">第一個階段是插入階段，其中資料表會填入其初始資料集。</span><span class="sxs-lookup"><span data-stu-id="fa90e-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="fa90e-235">在這個階段中，只允許插入資料。</span><span class="sxs-lookup"><span data-stu-id="fa90e-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="fa90e-236">當嘗試使用 [JetMove](./jetmove-function.md) 或 [JetSeek](./jetseek-function.md)移動資料指標時，就會結束這個階段。</span><span class="sxs-lookup"><span data-stu-id="fa90e-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="fa90e-237">第二個階段是資料解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="fa90e-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="fa90e-238">在這個階段中，您可以根據建立臨時表時所要求的功能，來解壓縮儲存在臨時表中的資料。</span><span class="sxs-lookup"><span data-stu-id="fa90e-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="fa90e-239">**臨時表資料指標功能**</span><span class="sxs-lookup"><span data-stu-id="fa90e-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="fa90e-240">當臨時表具體化時，資料指標有下列功能，但可能會進一步受要求的選項限制：</span><span class="sxs-lookup"><span data-stu-id="fa90e-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="fa90e-241">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fa90e-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="fa90e-242">JetDelete</span><span class="sxs-lookup"><span data-stu-id="fa90e-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="fa90e-243">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="fa90e-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="fa90e-244">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="fa90e-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="fa90e-246">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="fa90e-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="fa90e-247">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="fa90e-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="fa90e-248">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="fa90e-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="fa90e-249">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="fa90e-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="fa90e-250">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="fa90e-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="fa90e-251">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="fa90e-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="fa90e-252">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="fa90e-253">JetMove</span><span class="sxs-lookup"><span data-stu-id="fa90e-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="fa90e-254">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="fa90e-255">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="fa90e-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="fa90e-256">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="fa90e-257">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="fa90e-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="fa90e-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="fa90e-259">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="fa90e-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="fa90e-260">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="fa90e-261">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="fa90e-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="fa90e-262">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="fa90e-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="fa90e-263">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="fa90e-264">當臨時表未具體化且在插入階段時，資料指標有下列功能，但可能會進一步受要求的選項限制：</span><span class="sxs-lookup"><span data-stu-id="fa90e-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="fa90e-265">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fa90e-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="fa90e-266">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="fa90e-267">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="fa90e-268">JetMove</span><span class="sxs-lookup"><span data-stu-id="fa90e-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="fa90e-269">**注意**  導致轉換成解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="fa90e-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="fa90e-270">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="fa90e-271">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="fa90e-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="fa90e-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="fa90e-273">**注意**  導致轉換成解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="fa90e-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="fa90e-274">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="fa90e-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="fa90e-275">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="fa90e-276">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="fa90e-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="fa90e-277">當臨時表未具體化而且在解壓縮階段時，資料指標有下列功能，但可能會進一步受要求的選項限制：</span><span class="sxs-lookup"><span data-stu-id="fa90e-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="fa90e-278">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fa90e-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="fa90e-279">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="fa90e-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="fa90e-280">**注意**  如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。</span><span class="sxs-lookup"><span data-stu-id="fa90e-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="fa90e-281">在具體化的臨時表上重復資料指標仍然是安全的。</span><span class="sxs-lookup"><span data-stu-id="fa90e-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="fa90e-282">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="fa90e-283">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="fa90e-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="fa90e-284">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="fa90e-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="fa90e-285">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="fa90e-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="fa90e-286">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="fa90e-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="fa90e-287">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="fa90e-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="fa90e-288">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="fa90e-289">JetMove</span><span class="sxs-lookup"><span data-stu-id="fa90e-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="fa90e-290">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="fa90e-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="fa90e-291">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="fa90e-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="fa90e-292">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="fa90e-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="fa90e-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="fa90e-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="fa90e-294">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="fa90e-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="fa90e-295">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="fa90e-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="fa90e-296">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa90e-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-297"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="fa90e-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fa90e-298">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="fa90e-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-299"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="fa90e-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fa90e-300">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="fa90e-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-301"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="fa90e-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fa90e-302">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="fa90e-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa90e-303"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="fa90e-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fa90e-304">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="fa90e-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa90e-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fa90e-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fa90e-306">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="fa90e-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fa90e-307">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa90e-307">See Also</span></span>

[<span data-ttu-id="fa90e-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fa90e-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fa90e-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fa90e-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fa90e-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="fa90e-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="fa90e-311">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="fa90e-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="fa90e-312">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="fa90e-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="fa90e-313">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="fa90e-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="fa90e-314">JetMove</span><span class="sxs-lookup"><span data-stu-id="fa90e-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="fa90e-315">JetRollback</span><span class="sxs-lookup"><span data-stu-id="fa90e-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="fa90e-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="fa90e-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="fa90e-317">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fa90e-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="fa90e-318">資訊參數</span><span class="sxs-lookup"><span data-stu-id="fa90e-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="fa90e-319">暫存資料庫參數</span><span class="sxs-lookup"><span data-stu-id="fa90e-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
