---
description: 深入瞭解： JET_DBINFOMISC 結構
title: JET_DBINFOMISC 結構
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
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
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510946"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="77842-103">JET_DBINFOMISC 結構</span><span class="sxs-lookup"><span data-stu-id="77842-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="77842-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77842-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="77842-105">JET_DBINFOMISC 結構</span><span class="sxs-lookup"><span data-stu-id="77842-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="77842-106">**JET_DBINFOMISC** 結構會保存資料庫的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="77842-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="77842-107">這是包含在資料庫標頭中的資訊。</span><span class="sxs-lookup"><span data-stu-id="77842-107">This is the information that is contained in the database header.</span></span>

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
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="77842-108">成員</span><span class="sxs-lookup"><span data-stu-id="77842-108">Members</span></span>

<span data-ttu-id="77842-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="77842-109">**ulVersion**</span></span>

<span data-ttu-id="77842-110">建立資料庫之資料庫引擎的原生版本。</span><span class="sxs-lookup"><span data-stu-id="77842-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="77842-111">請參閱 [JetGetVersion](./jetgetversion-function.md) ，以取得目前資料庫引擎的原生版本。</span><span class="sxs-lookup"><span data-stu-id="77842-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="77842-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="77842-112">**ulUpdate**</span></span>

<span data-ttu-id="77842-113">追蹤可回溯相容的累加式資料庫格式更新。</span><span class="sxs-lookup"><span data-stu-id="77842-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77842-114">ulVersion、ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="77842-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="77842-115">意義</span><span class="sxs-lookup"><span data-stu-id="77842-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77842-116">0x620，0</span><span class="sxs-lookup"><span data-stu-id="77842-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="77842-117">原始作業系統 Beta 格式 (4/22/97) 。</span><span class="sxs-lookup"><span data-stu-id="77842-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-118">0x620，1</span><span class="sxs-lookup"><span data-stu-id="77842-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="77842-119">在目錄中新增條件式索引編制和舊的 (5/29/97) 的資料行。</span><span class="sxs-lookup"><span data-stu-id="77842-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-120">0x620，2</span><span class="sxs-lookup"><span data-stu-id="77842-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="77842-121">在 fLocalizedText 中新增旗標 (6/5/97) 。</span><span class="sxs-lookup"><span data-stu-id="77842-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-122">0x620、3</span><span class="sxs-lookup"><span data-stu-id="77842-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="77842-123">將 SPLIT_BUFFER 新增至空間樹狀結構的根頁面 (10/30/97) 。</span><span class="sxs-lookup"><span data-stu-id="77842-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-124">0x620，2</span><span class="sxs-lookup"><span data-stu-id="77842-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="77842-125">還原修訂以使 ESE97 維持 (1/28/98) 的向前相容性。</span><span class="sxs-lookup"><span data-stu-id="77842-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-126">0x620、3</span><span class="sxs-lookup"><span data-stu-id="77842-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="77842-127">將新的標記資料行新增至目錄， (&quot; CallbackData &quot; 和 &quot; CallbackDependencies &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="77842-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-128">0x620，4</span><span class="sxs-lookup"><span data-stu-id="77842-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="77842-129">SLV 支援： signSLV、db 標頭中的 fSLVExists (5/5/98) 。</span><span class="sxs-lookup"><span data-stu-id="77842-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-130">0x620，5</span><span class="sxs-lookup"><span data-stu-id="77842-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="77842-131">新的 SLV 空間樹狀結構 (5/29/98) 。</span><span class="sxs-lookup"><span data-stu-id="77842-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-132">0x620、6</span><span class="sxs-lookup"><span data-stu-id="77842-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="77842-133">SLV space map (10/12/98) 。</span><span class="sxs-lookup"><span data-stu-id="77842-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-134">0x620，7</span><span class="sxs-lookup"><span data-stu-id="77842-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="77842-135">4位元組 IDXSEG (12/10/98) 。</span><span class="sxs-lookup"><span data-stu-id="77842-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-136">0x620、8</span><span class="sxs-lookup"><span data-stu-id="77842-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="77842-137"> (1/25/99) 的新範本資料行格式。</span><span class="sxs-lookup"><span data-stu-id="77842-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-138">0x620、9</span><span class="sxs-lookup"><span data-stu-id="77842-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="77842-139">已排序的範本資料行 (6/24/99) 。</span><span class="sxs-lookup"><span data-stu-id="77842-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-140">0x623，0</span><span class="sxs-lookup"><span data-stu-id="77842-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="77842-141">新的空間管理員 (5/15/99) 。</span><span class="sxs-lookup"><span data-stu-id="77842-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77842-142">**signDb**</span><span class="sxs-lookup"><span data-stu-id="77842-142">**signDb**</span></span>

<span data-ttu-id="77842-143">資料庫 (的簽章，包括建立時間) 。</span><span class="sxs-lookup"><span data-stu-id="77842-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="77842-144">此結構是28個位元組。</span><span class="sxs-lookup"><span data-stu-id="77842-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="77842-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="77842-145">**dbstate**</span></span>

<span data-ttu-id="77842-146">這是資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="77842-146">This is the database state.</span></span>

<span data-ttu-id="77842-147">此成員可以使用下列選項。</span><span class="sxs-lookup"><span data-stu-id="77842-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77842-148">值</span><span class="sxs-lookup"><span data-stu-id="77842-148">Value</span></span></p></th>
<th><p><span data-ttu-id="77842-149">意義</span><span class="sxs-lookup"><span data-stu-id="77842-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77842-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="77842-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="77842-151">1</span><span class="sxs-lookup"><span data-stu-id="77842-151">1</span></span></p></td>
<td><p><span data-ttu-id="77842-152">剛建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="77842-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="77842-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="77842-154">2</span><span class="sxs-lookup"><span data-stu-id="77842-154">2</span></span></p></td>
<td><p><span data-ttu-id="77842-155">資料庫需要執行硬或軟復原才能成為可用或可移動的。</span><span class="sxs-lookup"><span data-stu-id="77842-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="77842-156">其中一個不應嘗試移動處於此狀態的資料庫。</span><span class="sxs-lookup"><span data-stu-id="77842-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="77842-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="77842-158">3</span><span class="sxs-lookup"><span data-stu-id="77842-158">3</span></span></p></td>
<td><p><span data-ttu-id="77842-159">資料庫處於乾淨狀態。</span><span class="sxs-lookup"><span data-stu-id="77842-159">The database is in a clean state.</span></span> <span data-ttu-id="77842-160">您可以在沒有任何記錄檔的情況下附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="77842-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="77842-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="77842-162">4</span><span class="sxs-lookup"><span data-stu-id="77842-162">4</span></span></p></td>
<td><p><span data-ttu-id="77842-163">正在升級資料庫。</span><span class="sxs-lookup"><span data-stu-id="77842-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="77842-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="77842-165">5</span><span class="sxs-lookup"><span data-stu-id="77842-165">5</span></span></p></td>
<td><p><span data-ttu-id="77842-166">內部。</span><span class="sxs-lookup"><span data-stu-id="77842-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77842-167">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="77842-167">**lgposConsistent**</span></span>

<span data-ttu-id="77842-168">如果資料庫處於已變更狀態，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="77842-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="77842-169">這是資料庫最後一次進入正常關機狀態時所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="77842-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="77842-170">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="77842-170">**logtimeConsistent**</span></span>

<span data-ttu-id="77842-171">如果資料庫處於已變更狀態，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="77842-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="77842-172">這是資料庫上次進入正常關機狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="77842-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="77842-173">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="77842-173">**logtimeAttach**</span></span>

<span data-ttu-id="77842-174">上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)連接資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="77842-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="77842-175">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="77842-175">**lgposAttach**</span></span>

<span data-ttu-id="77842-176">上次使用 [JetAttachDatabase](./jetattachdatabase-function.md)附加資料庫時所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="77842-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="77842-177">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="77842-177">**logtimeDetach**</span></span>

<span data-ttu-id="77842-178">上次與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="77842-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="77842-179">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="77842-179">**lgposDetach**</span></span>

<span data-ttu-id="77842-180">上次資料庫與 [JetDetachDatabase](./jetdetachdatabase-function.md)卸離時，所使用的記錄檔位置。</span><span class="sxs-lookup"><span data-stu-id="77842-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="77842-181">**signLog**</span><span class="sxs-lookup"><span data-stu-id="77842-181">**signLog**</span></span>

<span data-ttu-id="77842-182">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-183">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="77842-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="77842-184">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-185">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="77842-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="77842-186">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-187">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="77842-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="77842-188">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-189">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="77842-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="77842-190">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-191">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="77842-191">**fUpgradeDb**</span></span>

<span data-ttu-id="77842-192">支援 ESE 基礎結構，而且無法在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="77842-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="77842-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="77842-193">**dwMajorVersion**</span></span>

<span data-ttu-id="77842-194">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="77842-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="77842-195">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="77842-195">Used for updating indexes.</span></span>

<span data-ttu-id="77842-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="77842-196">**dwMinorVersion**</span></span>

<span data-ttu-id="77842-197">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="77842-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="77842-198">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="77842-198">Used for updating indexes.</span></span>

<span data-ttu-id="77842-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="77842-199">**dwBuildNumber**</span></span>

<span data-ttu-id="77842-200">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="77842-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="77842-201">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="77842-201">Used for updating indexes.</span></span>

<span data-ttu-id="77842-202">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="77842-202">**lSPNumber**</span></span>

<span data-ttu-id="77842-203">表示更新資料庫索引時的 Windows NT 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="77842-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="77842-204">用來更新索引。</span><span class="sxs-lookup"><span data-stu-id="77842-204">Used for updating indexes.</span></span>

<span data-ttu-id="77842-205">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="77842-205">**cbPageSize**</span></span>

<span data-ttu-id="77842-206">資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="77842-206">Database page size.</span></span> <span data-ttu-id="77842-207">0表示頁面大小為 4 KB。</span><span class="sxs-lookup"><span data-stu-id="77842-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="77842-208">只有當 JET_DbInfoMisc 已傳遞至 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) 或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)時，才會抓取此值。</span><span class="sxs-lookup"><span data-stu-id="77842-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="77842-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="77842-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77842-210"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="77842-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77842-211">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="77842-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77842-212"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="77842-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77842-213">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="77842-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77842-214"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="77842-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77842-215">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="77842-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="77842-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77842-216">See Also</span></span>

[<span data-ttu-id="77842-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="77842-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="77842-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="77842-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="77842-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="77842-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="77842-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="77842-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="77842-221">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="77842-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="77842-222">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="77842-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
