---
description: 深入瞭解： JetCompact 函數
title: JetCompact 函式
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988844"
---
# <a name="jetcompact-function"></a><span data-ttu-id="6fc5b-103">JetCompact 函式</span><span class="sxs-lookup"><span data-stu-id="6fc5b-103">JetCompact Function</span></span>


<span data-ttu-id="6fc5b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6fc5b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcompact-function"></a><span data-ttu-id="6fc5b-105">JetCompact 函式</span><span class="sxs-lookup"><span data-stu-id="6fc5b-105">JetCompact Function</span></span>

<span data-ttu-id="6fc5b-106">**JetCompact** 函數會建立現有資料庫的複本。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-106">The **JetCompact** function makes a copy of an existing database.</span></span> <span data-ttu-id="6fc5b-107">複本會壓縮為使用狀態的最佳狀態。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-107">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="6fc5b-108">複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-108">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="6fc5b-109">如此一來，壓縮的資料可能會盡可能儲存為密集。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-109">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="6fc5b-110">或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-110">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6fc5b-111">參數</span><span class="sxs-lookup"><span data-stu-id="6fc5b-111">Parameters</span></span>

<span data-ttu-id="6fc5b-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-112">*sesid*</span></span>

<span data-ttu-id="6fc5b-113">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-113">The session to use for this call.</span></span>

<span data-ttu-id="6fc5b-114">*szDatabaseSrc*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-114">*szDatabaseSrc*</span></span>

<span data-ttu-id="6fc5b-115">將壓縮的源資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-115">The source database that will be compacted.</span></span>

<span data-ttu-id="6fc5b-116">*szDatabaseDest*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-116">*szDatabaseDest*</span></span>

<span data-ttu-id="6fc5b-117">要用於壓縮資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-117">The name to use for the compacted database.</span></span>

<span data-ttu-id="6fc5b-118">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-118">*pfnStatus*</span></span>

<span data-ttu-id="6fc5b-119">可透過資料庫 compact 作業定期呼叫以報告進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-119">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<span data-ttu-id="6fc5b-120">*pconvert*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-120">*pconvert*</span></span>

<span data-ttu-id="6fc5b-121">用來指定替代 ESE DLL 的指標，這個 DLL 可用來讀取源資料庫，並提供 **JetCompact** 作業的選擇性參數，將資料庫從較早的版本格式轉換為較新的版本。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-121">A pointer used to designate an alternative ESE DLL that can be used to read the source database, and to provide optional parameters for a **JetCompact** operation that is converting a database from an earlier to a later version format.</span></span> <span data-ttu-id="6fc5b-122">這項功能已在 Windows Server 2003 中停用。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-122">This feature was discontinued in Windows Server 2003.</span></span>

<span data-ttu-id="6fc5b-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6fc5b-123">*grbit*</span></span>

<span data-ttu-id="6fc5b-124">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-124">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fc5b-125">值</span><span class="sxs-lookup"><span data-stu-id="6fc5b-125">Value</span></span></p></th>
<th><p><span data-ttu-id="6fc5b-126">意義</span><span class="sxs-lookup"><span data-stu-id="6fc5b-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-127">JET_bitCompactRepair</span><span class="sxs-lookup"><span data-stu-id="6fc5b-127">JET_bitCompactRepair</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-128">當源資料庫已知已損毀時使用。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-128">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="6fc5b-129">它會啟用一組完整的新行為，以盡可能從源資料庫中回收最多的資料。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-129">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="6fc5b-130">使用這個選項組的<strong>JetCompact</strong>可能會傳回 JET_errSuccess 但不會複製在源資料庫中建立的所有資料。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-130"><strong>JetCompact</strong> with this option set may return JET_errSuccess but not copy all of the data created in the source database.</span></span> <span data-ttu-id="6fc5b-131">將略過源資料庫中損毀部分的資料。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-131">Data that was in damaged portions of the source database will be skipped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-132">JET_bitCompactStats</span><span class="sxs-lookup"><span data-stu-id="6fc5b-132">JET_bitCompactStats</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-133">讓 <strong>JetCompact</strong> 將源資料庫的統計資料傾印到名為 DFRGINFO.TXT 的檔案。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-133">Causes <strong>JetCompact</strong> to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="6fc5b-134">統計資料包括源資料庫中每個資料表的名稱、每個資料表中的資料列數目、每個資料表中所有資料列的總大小（以位元組為單位）、所有資料行<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>類型的總大小（以位元組為單位），而這些資料行的大小總計與記錄、叢集索引分葉頁面的數目，以及 long 值分葉頁面的數目相同</span><span class="sxs-lookup"><span data-stu-id="6fc5b-134">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="6fc5b-135">此外，摘要統計資料，包括源資料庫的大小、目的地資料庫、資料庫壓縮所需的時間，也會全部傾印暫存資料庫空間。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-135">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6fc5b-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fc5b-136">Return Value</span></span>

<span data-ttu-id="6fc5b-137">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-137">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6fc5b-138">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-138">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fc5b-139">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6fc5b-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="6fc5b-140">Description</span><span class="sxs-lookup"><span data-stu-id="6fc5b-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6fc5b-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-142">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-142">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6fc5b-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-144">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-145">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="6fc5b-145">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-146">已提供非 Null 的 <em>pconvert</em> 指標，但所使用的 ESE 版本不支援轉換功能。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-146">A non-NULL <em>pconvert</em> pointer has been supplied but the version of ESE being used does not support the convert feature.</span></span> <span data-ttu-id="6fc5b-147">這項功能已在 Windows Server 2003 版的 ESE 中移除。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-147">This feature was removed in the Windows Server 2003 version of ESE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6fc5b-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-149">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6fc5b-150">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-151">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6fc5b-151">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-152">呼叫會話是在交易內。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-152">The calling session is within a transaction.</span></span> <span data-ttu-id="6fc5b-153"><strong>JetCompact</strong> 必須由任何交易以外的會話呼叫。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-153"><strong>JetCompact</strong> must be called by a session outside of any transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-154">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6fc5b-154">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-155">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-155">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6fc5b-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-157">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6fc5b-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-159">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="6fc5b-160">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6fc5b-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6fc5b-162">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6fc5b-163">成功時，源資料庫會複製到目的地資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-163">On success, the source database is copied to the destination database.</span></span> <span data-ttu-id="6fc5b-164">目的地資料庫處於最佳狀態，例如，所有資料表索引都位於連續的邏輯磁碟空間中。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-164">The destination database is in an optimal state, for example, all table indexes are located in adjacent logical disk space.</span></span> <span data-ttu-id="6fc5b-165">每個索引頁面都會填補至最初在源資料庫中建立索引時所設定的數量。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-165">Each index page is padded to the amount configured when the indexes were originally created in the source database.</span></span> <span data-ttu-id="6fc5b-166">除非指定了 repair 選項，否則所有資料和中繼資料設定都會以完整的精確度複製。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-166">All data and metadata settings are copied with full fidelity, unless the repair option was specified.</span></span> <span data-ttu-id="6fc5b-167">如果指定了 repair 選項，源資料庫中的某些資料可能不會被覆制。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-167">If the repair option was specified, some data from the source database may not have been copied.</span></span>

<span data-ttu-id="6fc5b-168">失敗時，目的地資料庫可能存在，但不是源資料庫的完整複本。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-168">On failure, the destination database may exist but is not a full copy of the source database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6fc5b-169">備註</span><span class="sxs-lookup"><span data-stu-id="6fc5b-169">Remarks</span></span>

<span data-ttu-id="6fc5b-170">壓縮資料庫也用來將資料庫從舊版格式升級為較新式的版本。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-170">Compacting a database is also used to upgrade a database from an earlier version format to a more modern version.</span></span> <span data-ttu-id="6fc5b-171">選擇性參數為 *pconvert*，其中包含的結構可以保存舊版 DLL 的描述，以用來讀取源資料庫格式。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-171">An optional parameter is *pconvert*, which contains a structure that can hold a description for an earlier version DLL to use for reading the source database format.</span></span> <span data-ttu-id="6fc5b-172">這項功能已在 Windows Server 2003 中停用。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-172">This feature was discontinued in Windows Server 2003.</span></span> <span data-ttu-id="6fc5b-173">在 Windows Server 2003 的後續版本中，新版本的 ESE 一律可以讀取舊版的資料庫格式，因此不需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-173">Subsequent to Windows Server 2003, new versions of ESE are always able to read older versions of the database format and hence this feature is not needed.</span></span>

<span data-ttu-id="6fc5b-174">當建立資料表和索引時，指定精簡作業之後所需的資料密度。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-174">The desired density of data after a compact operation is specified when tables and indexes are created.</span></span> <span data-ttu-id="6fc5b-175">密度必須介於20% 到100% 之間。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-175">The density must be between 20% and 100%.</span></span> <span data-ttu-id="6fc5b-176">如果資料庫主要是讀取和未更新，則應用程式會將密度設定為100%，以減少查詢處理期間的 i/o 作業數目。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-176">If a database is primarily read and not updated, applications will set the density to 100% to reduce the number of I/O operations during query processing.</span></span> <span data-ttu-id="6fc5b-177">但是，如果資料經常更新，且作業會增加與記錄一起儲存的資料大小，或經常插入新的資料，則應用程式會選擇較低的密度，讓更新更頻繁地找到所需的可用資源。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-177">However, if the data is updated frequently with operations that increase the size of data stored together with the record, or new data is frequently inserted, the application will choose a lower density so that updates will more often find needed resources available.</span></span> <span data-ttu-id="6fc5b-178">壓縮資料庫的作業會根據應用程式所選擇的填滿，在理想的情況下設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-178">The operation of compacting the database causes the database to be ideally laid out according to the fill chosen by the application.</span></span>

<span data-ttu-id="6fc5b-179">資料庫壓縮是離線作業。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-179">Database compaction is an off-line operation.</span></span> <span data-ttu-id="6fc5b-180">當資料庫正在使用中時，無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-180">It cannot be performed while the database is in use.</span></span> <span data-ttu-id="6fc5b-181">如此一來，通常會在開發應用程式的組建程式中完成，此應用程式會將資料集當作本身的一部分來傳遞。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-181">As a result, it is typically done as part of a build process of developing an application which delivers a data set as part of itself.</span></span>

<span data-ttu-id="6fc5b-182">離線資料庫壓縮會觸及資料庫中的每個資料，而且可用來做為檢查資料庫一致性的方法。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-182">Offline database compaction touches every bit of data in a database and can be used as a means of checking the consistency of a database.</span></span> <span data-ttu-id="6fc5b-183">如果資料庫有問題，則可以將它壓縮。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-183">If a database is suspect then it can be compacted.</span></span> <span data-ttu-id="6fc5b-184">如果從壓縮中找不到錯誤，則會知道資料庫處於 ESE 的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-184">If no error is found from compaction then it will be known that the database is in a valid state for ESE.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6fc5b-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fc5b-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-186"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-187">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-188"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-189">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-190"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-191">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-192"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-193">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc5b-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-195">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc5b-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6fc5b-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc5b-197">實作為 <strong>JetCompactW</strong> (Unicode) 和 <strong>JetCompactA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="6fc5b-197">Implemented as <strong>JetCompactW</strong> (Unicode) and <strong>JetCompactA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6fc5b-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fc5b-198">See Also</span></span>

[<span data-ttu-id="6fc5b-199">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6fc5b-199">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6fc5b-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6fc5b-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6fc5b-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6fc5b-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6fc5b-202">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="6fc5b-202">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="6fc5b-203">JetStopService</span><span class="sxs-lookup"><span data-stu-id="6fc5b-203">JetStopService</span></span>](./jetstopservice-function.md)
