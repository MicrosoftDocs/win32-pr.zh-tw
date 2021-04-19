---
description: 深入瞭解： JET_SPACEHINTS 結構
title: JET_SPACEHINTS 結構
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985397"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="95b0f-103">JET_SPACEHINTS 結構</span><span class="sxs-lookup"><span data-stu-id="95b0f-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="95b0f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95b0f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="95b0f-105">JET_SPACEHINTS 結構</span><span class="sxs-lookup"><span data-stu-id="95b0f-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="95b0f-106">當 b 型樹狀結構透過附加或 hotpoint 分割成長時， **JET_SPACEHINTS** 結構包含空間配置模式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="95b0f-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="95b0f-107">當將記錄加入 b 型樹狀目錄的結尾，並在多筆記錄新增至相同的虛擬插入點時，就會發生 hotpoint 分割 (例如，將 ' Marie '、' Mark '、' Martin'，' Mary ' 加入到依字母) 順序排序的 b 型樹狀目錄中間。</span><span class="sxs-lookup"><span data-stu-id="95b0f-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="95b0f-108">**Windows 7：** 在 Windows 7 中引進 **JET_SPACEHINTS** 結構。</span><span class="sxs-lookup"><span data-stu-id="95b0f-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="95b0f-109">成員</span><span class="sxs-lookup"><span data-stu-id="95b0f-109">Members</span></span>

<span data-ttu-id="95b0f-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="95b0f-110">**cbStruct**</span></span>

<span data-ttu-id="95b0f-111">此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95b0f-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="95b0f-112">將這個成員設定為 sizeof ( JET_SPACEHINTS ) 。</span><span class="sxs-lookup"><span data-stu-id="95b0f-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="95b0f-113">**ulInitialDensity**</span><span class="sxs-lookup"><span data-stu-id="95b0f-113">**ulInitialDensity**</span></span>

<span data-ttu-id="95b0f-114"> (的密度會附加) 版面配置。</span><span class="sxs-lookup"><span data-stu-id="95b0f-114">The density at (append) layout.</span></span>

<span data-ttu-id="95b0f-115">**cbInitial**</span><span class="sxs-lookup"><span data-stu-id="95b0f-115">**cbInitial**</span></span>

<span data-ttu-id="95b0f-116">所建立之物件的初始大小 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="95b0f-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="95b0f-117">這必須是資料庫頁面大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="95b0f-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="95b0f-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="95b0f-118">**grbit**</span></span>

<span data-ttu-id="95b0f-119">位群組，其中包含要用於此結構的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="95b0f-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95b0f-120">值</span><span class="sxs-lookup"><span data-stu-id="95b0f-120">Value</span></span></p></th>
<th><p><span data-ttu-id="95b0f-121">意義</span><span class="sxs-lookup"><span data-stu-id="95b0f-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b0f-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="95b0f-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="95b0f-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="95b0f-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="95b0f-124">變更內部配置原則，以從 b 型樹狀目錄的直屬父系取得空間 heirarchically。</span><span class="sxs-lookup"><span data-stu-id="95b0f-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b0f-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="95b0f-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="95b0f-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="95b0f-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="95b0f-127">根據 cbMinExtent、ulGrowth、cbMaxExtent) 所設定的 (資料表成長動態，讓附加分割行為成長。</span><span class="sxs-lookup"><span data-stu-id="95b0f-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b0f-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="95b0f-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="95b0f-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="95b0f-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="95b0f-130">根據 cbMinExtent、ulGrowth、cbMaxExtent) 所設定之資料表 (成長動態，讓 hotpoint 分割行為成長。</span><span class="sxs-lookup"><span data-stu-id="95b0f-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b0f-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="95b0f-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="95b0f-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="95b0f-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="95b0f-133">如果設定，用戶端會指出向前順序掃描是此資料表的主要使用模式。</span><span class="sxs-lookup"><span data-stu-id="95b0f-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b0f-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="95b0f-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="95b0f-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="95b0f-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="95b0f-136">如果設定，用戶端就會指出往後順序掃描是此資料表的主要使用模式。</span><span class="sxs-lookup"><span data-stu-id="95b0f-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b0f-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="95b0f-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="95b0f-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="95b0f-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="95b0f-139">如果設定，應用程式預期會依序從最小的索引鍵到最高的索引鍵來清除此資料表。</span><span class="sxs-lookup"><span data-stu-id="95b0f-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95b0f-140">**ulMaintDensity**</span><span class="sxs-lookup"><span data-stu-id="95b0f-140">**ulMaintDensity**</span></span>

<span data-ttu-id="95b0f-141">密度至 mulMaintDensity</span><span class="sxs-lookup"><span data-stu-id="95b0f-141">density to mulMaintDensity</span></span>

<span data-ttu-id="95b0f-142">要維護的密度。</span><span class="sxs-lookup"><span data-stu-id="95b0f-142">Density to maintain at.</span></span> <span data-ttu-id="95b0f-143">如果空間提示指定 JET_bitRetrieveHintTableScanForward 或 JET_bitRetrieveHintTableScanBackward，當資料表中的已使用空間低於此臨界值時，就會觸發資料表磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="95b0f-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="95b0f-144">您可以將此成員設定為零，以停用資料表磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="95b0f-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="95b0f-145">將這個成員設定為100，將會在釋放頁面時立即執行資料表磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="95b0f-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="95b0f-146">**ulGrowth**</span><span class="sxs-lookup"><span data-stu-id="95b0f-146">**ulGrowth**</span></span>

<span data-ttu-id="95b0f-147">從上一次成長或初始大小的成長百分比，舍入到最接近的原生 JET 配置大小。</span><span class="sxs-lookup"><span data-stu-id="95b0f-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="95b0f-148">**cbMinExtent 太小**</span><span class="sxs-lookup"><span data-stu-id="95b0f-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="95b0f-149">如果太小，則會覆寫 ulGrowth。</span><span class="sxs-lookup"><span data-stu-id="95b0f-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="95b0f-150">**cbMaxExtent**</span><span class="sxs-lookup"><span data-stu-id="95b0f-150">**cbMaxExtent**</span></span>

<span data-ttu-id="95b0f-151">成長的最大值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95b0f-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="95b0f-152">此 cap ulGrowth。</span><span class="sxs-lookup"><span data-stu-id="95b0f-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="95b0f-153">當 b 型樹狀結構透過附加或 hotpoint 分割 (而不是隨機記錄插入) 時，資料表將成長的空間量計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="95b0f-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="95b0f-154">在建立過程中，我們會為 b 型樹狀結構 cbInitial，一律為。</span><span class="sxs-lookup"><span data-stu-id="95b0f-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="95b0f-155">在指定區域的第一次配置期間，我們將配置： cbInitial \* ulGrowth/100 (四捨五入至 DB 的頁面大小) ，或 cbMinExtent （如果較大）。</span><span class="sxs-lookup"><span data-stu-id="95b0f-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="95b0f-156">在下一個配置期間，cbLastAlloc \* ulGrowth/100 (舍入至資料庫) 的頁面大小，如果較大則為 cbMinExtent。</span><span class="sxs-lookup"><span data-stu-id="95b0f-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="95b0f-157">在某些配置 (可能是第一次配置) 時，計算的大小會超過 cbMaxExtent，而這會是之後的成長大小。</span><span class="sxs-lookup"><span data-stu-id="95b0f-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="95b0f-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="95b0f-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b0f-159"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="95b0f-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95b0f-160">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="95b0f-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b0f-161"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="95b0f-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95b0f-162">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="95b0f-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b0f-163"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="95b0f-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95b0f-164">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="95b0f-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="95b0f-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95b0f-165">See Also</span></span>

[<span data-ttu-id="95b0f-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="95b0f-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="95b0f-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="95b0f-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
