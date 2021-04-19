---
description: 深入瞭解： JET_DBINFOMISC4 結構
title: JET_DBINFOMISC4 結構
TOCTitle: JET_DBINFOMISC4 Structure
ms:assetid: 63f446bc-98b7-4a60-9575-d6b4757fb0fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269269(v=EXCHG.10)
ms:contentKeyID: 32765571
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e2242b1e419c4834a2a1843165e1c9a2ad1f2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973210"
---
# <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="7f79e-103">JET_DBINFOMISC4 結構</span><span class="sxs-lookup"><span data-stu-id="7f79e-103">JET_DBINFOMISC4 Structure</span></span>


<span data-ttu-id="7f79e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7f79e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc4-structure"></a><span data-ttu-id="7f79e-105">JET_DBINFOMISC4 結構</span><span class="sxs-lookup"><span data-stu-id="7f79e-105">JET_DBINFOMISC4 Structure</span></span>

<span data-ttu-id="7f79e-106">**JET_DBINFOMISC4** 結構會保存資料庫的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f79e-106">The **JET_DBINFOMISC4** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="7f79e-107">這是包含在資料庫標頭中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f79e-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
      JET_BKINFO bkinfoCopyPrev;
      JET_BKINFO bkinfoDiffPrev;
    } JET_DBINFOMISC4;
```

### <a name="members"></a><span data-ttu-id="7f79e-108">成員</span><span class="sxs-lookup"><span data-stu-id="7f79e-108">Members</span></span>

<span data-ttu-id="7f79e-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="7f79e-109">**ulVersion**</span></span>

<span data-ttu-id="7f79e-110">建立資料庫之資料庫引擎的原生版本。</span><span class="sxs-lookup"><span data-stu-id="7f79e-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="7f79e-111">請參閱 [JetGetVersion](./jetgetversion-function.md) ，以取得目前資料庫引擎的原生版本。</span><span class="sxs-lookup"><span data-stu-id="7f79e-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="7f79e-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="7f79e-112">**ulUpdate**</span></span>

<span data-ttu-id="7f79e-113">追蹤可回溯相容的累加式資料庫格式更新。</span><span class="sxs-lookup"><span data-stu-id="7f79e-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f79e-114">ulVersion、ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="7f79e-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="7f79e-115">意義</span><span class="sxs-lookup"><span data-stu-id="7f79e-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-116">0x620，0</span><span class="sxs-lookup"><span data-stu-id="7f79e-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="7f79e-117">原始作業系統 Beta 格式 (4/22/97) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-118">0x620，1</span><span class="sxs-lookup"><span data-stu-id="7f79e-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="7f79e-119">在目錄中新增條件式索引編制和舊的 (5/29/97) 的資料行。</span><span class="sxs-lookup"><span data-stu-id="7f79e-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-120">0x620，2</span><span class="sxs-lookup"><span data-stu-id="7f79e-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="7f79e-121">在 fLocalizedText 中新增旗標 (6/5/97) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-122">0x620、3</span><span class="sxs-lookup"><span data-stu-id="7f79e-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="7f79e-123">將 SPLIT_BUFFER 新增至空間樹狀結構的根頁面 (10/30/97) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-124">0x620，2</span><span class="sxs-lookup"><span data-stu-id="7f79e-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="7f79e-125">還原修訂以使 ESE97 維持 (1/28/98) 的向前相容性。</span><span class="sxs-lookup"><span data-stu-id="7f79e-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-126">0x620、3</span><span class="sxs-lookup"><span data-stu-id="7f79e-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="7f79e-127">將新的標記資料行新增至目錄， (&quot; CallbackData &quot; 和 &quot; CallbackDependencies &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-128">0x620，4</span><span class="sxs-lookup"><span data-stu-id="7f79e-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="7f79e-129">SLV 支援： signSLV、db 標頭中的 fSLVExists (5/5/98) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-130">0x620，5</span><span class="sxs-lookup"><span data-stu-id="7f79e-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="7f79e-131">新的 SLV 空間樹狀結構 (5/29/98) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-132">0x620、6</span><span class="sxs-lookup"><span data-stu-id="7f79e-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="7f79e-133">SLV space map (10/12/98) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-134">0x620，7</span><span class="sxs-lookup"><span data-stu-id="7f79e-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="7f79e-135">4位元組 IDXSEG (12/10/98) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-136">0x620、8</span><span class="sxs-lookup"><span data-stu-id="7f79e-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="7f79e-137"> (1/25/99) 的新範本資料行格式。</span><span class="sxs-lookup"><span data-stu-id="7f79e-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-138">0x620、9</span><span class="sxs-lookup"><span data-stu-id="7f79e-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="7f79e-139">已排序的範本資料行 (6/24/99) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-140">0x620，A</span><span class="sxs-lookup"><span data-stu-id="7f79e-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="7f79e-141">合併的程式碼基底 (3/26/2003) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-142">0x620，B</span><span class="sxs-lookup"><span data-stu-id="7f79e-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="7f79e-143">新的總和檢查碼格式 (1/08/2004) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-144">0x620、C</span><span class="sxs-lookup"><span data-stu-id="7f79e-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="7f79e-145">將 4/8kb 頁面的最大金鑰長度增加至1000/2000 個位元組， (1/15/2004) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-146">0x620，D</span><span class="sxs-lookup"><span data-stu-id="7f79e-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="7f79e-147">目錄空間提示，space_header v2 (7/15/2007) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-148">0x620，E</span><span class="sxs-lookup"><span data-stu-id="7f79e-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="7f79e-149">將新的節點/範圍格式新增至空間管理員，將其用於空間的保留集區 (8/9/2007) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-150">0x620、F</span><span class="sxs-lookup"><span data-stu-id="7f79e-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="7f79e-151">將內建的 long 值壓縮 (10/30/2007) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-152">0x620，10</span><span class="sxs-lookup"><span data-stu-id="7f79e-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="7f79e-153">壓縮 (12/05/2007) 的分隔 long 值。</span><span class="sxs-lookup"><span data-stu-id="7f79e-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-154">0x620，11</span><span class="sxs-lookup"><span data-stu-id="7f79e-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="7f79e-155"> (12/29/2007) 的大型頁面新的 LV 區塊大小。</span><span class="sxs-lookup"><span data-stu-id="7f79e-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f79e-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="7f79e-156">**signDb**</span></span>

<span data-ttu-id="7f79e-157">資料庫 (的簽章，包括建立時間) 。</span><span class="sxs-lookup"><span data-stu-id="7f79e-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="7f79e-158">此結構是28個位元組。</span><span class="sxs-lookup"><span data-stu-id="7f79e-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="7f79e-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="7f79e-159">**dbstate**</span></span>

<span data-ttu-id="7f79e-160">這是資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="7f79e-160">This is the database state.</span></span>

<span data-ttu-id="7f79e-161">此成員可以使用下列選項。</span><span class="sxs-lookup"><span data-stu-id="7f79e-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f79e-162">值</span><span class="sxs-lookup"><span data-stu-id="7f79e-162">Value</span></span></p></th>
<th><p><span data-ttu-id="7f79e-163">意義</span><span class="sxs-lookup"><span data-stu-id="7f79e-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="7f79e-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="7f79e-165">1</span><span class="sxs-lookup"><span data-stu-id="7f79e-165">1</span></span></p></td>
<td><p><span data-ttu-id="7f79e-166">剛建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f79e-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="7f79e-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="7f79e-168">2</span><span class="sxs-lookup"><span data-stu-id="7f79e-168">2</span></span></p></td>
<td><p><span data-ttu-id="7f79e-169">資料庫需要執行硬或軟復原才能成為可用或可移動的。</span><span class="sxs-lookup"><span data-stu-id="7f79e-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="7f79e-170">其中一個不應嘗試移動處於此狀態的資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f79e-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="7f79e-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="7f79e-172">3</span><span class="sxs-lookup"><span data-stu-id="7f79e-172">3</span></span></p></td>
<td><p><span data-ttu-id="7f79e-173">資料庫處於乾淨狀態。</span><span class="sxs-lookup"><span data-stu-id="7f79e-173">The database is in a clean state.</span></span> <span data-ttu-id="7f79e-174">您可以在沒有任何記錄檔的情況下附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f79e-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="7f79e-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="7f79e-176">4</span><span class="sxs-lookup"><span data-stu-id="7f79e-176">4</span></span></p></td>
<td><p><span data-ttu-id="7f79e-177">正在升級資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f79e-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="7f79e-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="7f79e-179">5</span><span class="sxs-lookup"><span data-stu-id="7f79e-179">5</span></span></p></td>
<td><p><span data-ttu-id="7f79e-180">內部。</span><span class="sxs-lookup"><span data-stu-id="7f79e-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f79e-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="7f79e-181">**lgposConsistent**</span></span>

<span data-ttu-id="7f79e-182">如果資料庫處於已變更狀態，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="7f79e-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="7f79e-183">這是資料庫最後一次進入正常關機狀態時所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="7f79e-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="7f79e-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="7f79e-184">**logtimeConsistent**</span></span>

<span data-ttu-id="7f79e-185">如果資料庫處於已變更狀態，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="7f79e-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="7f79e-186">這是資料庫上次進入正常關機狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="7f79e-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="7f79e-187">**logtimeAttach**</span></span>

<span data-ttu-id="7f79e-188">上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)連接資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="7f79e-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="7f79e-189">**lgposAttach**</span></span>

<span data-ttu-id="7f79e-190">上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)附加資料庫時所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="7f79e-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="7f79e-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="7f79e-191">**logtimeDetach**</span></span>

<span data-ttu-id="7f79e-192">上次與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="7f79e-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="7f79e-193">**lgposDetach**</span></span>

<span data-ttu-id="7f79e-194">上次資料庫與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離時，所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="7f79e-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="7f79e-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="7f79e-195">**signLog**</span></span>

<span data-ttu-id="7f79e-196">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="7f79e-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="7f79e-198">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="7f79e-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="7f79e-200">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="7f79e-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="7f79e-202">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="7f79e-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="7f79e-204">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="7f79e-205">**fUpgradeDb**</span></span>

<span data-ttu-id="7f79e-206">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7f79e-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="7f79e-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="7f79e-207">**dwMajorVersion**</span></span>

<span data-ttu-id="7f79e-208">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7f79e-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="7f79e-209">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="7f79e-209">Used for updating indexes.</span></span>

<span data-ttu-id="7f79e-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="7f79e-210">**dwMinorVersion**</span></span>

<span data-ttu-id="7f79e-211">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7f79e-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="7f79e-212">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="7f79e-212">Used for updating indexes.</span></span>

<span data-ttu-id="7f79e-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="7f79e-213">**dwBuildNumber**</span></span>

<span data-ttu-id="7f79e-214">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7f79e-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="7f79e-215">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="7f79e-215">Used for updating indexes.</span></span>

<span data-ttu-id="7f79e-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="7f79e-216">**lSPNumber**</span></span>

<span data-ttu-id="7f79e-217">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7f79e-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="7f79e-218">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="7f79e-218">Used for updating indexes.</span></span>

<span data-ttu-id="7f79e-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="7f79e-219">**cbPageSize**</span></span>

<span data-ttu-id="7f79e-220">資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="7f79e-220">Database page size.</span></span> <span data-ttu-id="7f79e-221">0表示頁面大小為 4 KB。</span><span class="sxs-lookup"><span data-stu-id="7f79e-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="7f79e-222">只有當 JET_DbInfoMisc 已傳遞至 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) 或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)時，才會抓取此值。</span><span class="sxs-lookup"><span data-stu-id="7f79e-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="7f79e-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="7f79e-223">**genMinRequired**</span></span>

<span data-ttu-id="7f79e-224">表示重新執行記錄所需的最小記錄檔產生。</span><span class="sxs-lookup"><span data-stu-id="7f79e-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="7f79e-225">這通常用來做為檢查點產生。</span><span class="sxs-lookup"><span data-stu-id="7f79e-225">This is typically used as the checkpoint generation.</span></span>

<span data-ttu-id="7f79e-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="7f79e-226">**genMaxRequired**</span></span>

<span data-ttu-id="7f79e-227">表示重新執行記錄所需的最大記錄檔產生。</span><span class="sxs-lookup"><span data-stu-id="7f79e-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="7f79e-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="7f79e-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="7f79e-229">代表 genMax 記錄檔的建立日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="7f79e-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="7f79e-230">**ulRepairCount**</span></span>

<span data-ttu-id="7f79e-231">在此資料庫上呼叫修復的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="7f79e-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="7f79e-232">**logtimeRepair**</span></span>

<span data-ttu-id="7f79e-233">代表上次執行修復的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="7f79e-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="7f79e-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="7f79e-235">上次磁碟重組之前，在此資料庫上執行修復的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="7f79e-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="7f79e-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="7f79e-237">修正一個位錯誤並產生良好頁面的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="7f79e-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="7f79e-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="7f79e-239">代表修正最後一個 bit 錯誤的日期和時間，並產生良好的頁面。</span><span class="sxs-lookup"><span data-stu-id="7f79e-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="7f79e-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="7f79e-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="7f79e-241">代表修正一個位錯誤的次數，並在最後一次修復前產生良好的頁面。</span><span class="sxs-lookup"><span data-stu-id="7f79e-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="7f79e-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="7f79e-242">**ulECCFixFail**</span></span>

<span data-ttu-id="7f79e-243">修正一個位錯誤並產生錯誤頁面的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="7f79e-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="7f79e-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="7f79e-245">代表修正最後一個 bit 錯誤的日期和時間，並導致錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="7f79e-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="7f79e-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="7f79e-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="7f79e-247">修正一個位錯誤的次數，並在最後一次修復前產生錯誤的頁面。</span><span class="sxs-lookup"><span data-stu-id="7f79e-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="7f79e-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="7f79e-248">**ulBadChecksum**</span></span>

<span data-ttu-id="7f79e-249">找到不可更正的 ECC/總和檢查碼錯誤的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="7f79e-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="7f79e-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="7f79e-251">表示找到最後一個不可更正的 ECC/總和檢查碼錯誤的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f79e-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="7f79e-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="7f79e-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="7f79e-253">在最後一次修復之前發現不可更正的 ECC/總和檢查碼錯誤的次數。</span><span class="sxs-lookup"><span data-stu-id="7f79e-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="7f79e-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="7f79e-254">**genCommitted**</span></span>

<span data-ttu-id="7f79e-255">認可至資料庫的最大記錄層代數目。</span><span class="sxs-lookup"><span data-stu-id="7f79e-255">The maximum number of log generations committed to the database.</span></span> <span data-ttu-id="7f79e-256">通常是目前的記錄產生。</span><span class="sxs-lookup"><span data-stu-id="7f79e-256">Typically the current log generation.</span></span>

<span data-ttu-id="7f79e-257">**bkinfoCopyPrev**</span><span class="sxs-lookup"><span data-stu-id="7f79e-257">**bkinfoCopyPrev**</span></span>

<span data-ttu-id="7f79e-258">上次成功的複本備份。</span><span class="sxs-lookup"><span data-stu-id="7f79e-258">The last successful Copy backup.</span></span>

<span data-ttu-id="7f79e-259">**bkinfoDiffPrev**</span><span class="sxs-lookup"><span data-stu-id="7f79e-259">**bkinfoDiffPrev**</span></span>

<span data-ttu-id="7f79e-260">上次成功的差異備份。</span><span class="sxs-lookup"><span data-stu-id="7f79e-260">The last successful Differential backup.</span></span> <span data-ttu-id="7f79e-261">設定 bkinfoFullPrev 時，會重設此值。</span><span class="sxs-lookup"><span data-stu-id="7f79e-261">This value is reset when bkinfoFullPrev is set.</span></span>

### <a name="requirements"></a><span data-ttu-id="7f79e-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f79e-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-263"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7f79e-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7f79e-264">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="7f79e-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f79e-265"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7f79e-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7f79e-266">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="7f79e-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f79e-267"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7f79e-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7f79e-268">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7f79e-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7f79e-269">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f79e-269">See Also</span></span>

[<span data-ttu-id="7f79e-270">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="7f79e-270">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="7f79e-271">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="7f79e-271">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="7f79e-272">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="7f79e-272">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="7f79e-273">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7f79e-273">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="7f79e-274">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="7f79e-274">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="7f79e-275">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="7f79e-275">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
