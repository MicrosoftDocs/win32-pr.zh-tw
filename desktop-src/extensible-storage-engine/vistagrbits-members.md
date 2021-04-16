---
description: 深入瞭解： VistaGrbits 成員
title: " (的 VistaGrbits 成員) 的成員"
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557659"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="5bdee-103">VistaGrbits 成員</span><span class="sxs-lookup"><span data-stu-id="5bdee-103">VistaGrbits members</span></span>

<span data-ttu-id="5bdee-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="5bdee-104">Include protected members</span></span>  
<span data-ttu-id="5bdee-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="5bdee-105">Include inherited members</span></span>  

<span data-ttu-id="5bdee-106">已新增至 Vista 版本 ESENT 的 Grbits。</span><span class="sxs-lookup"><span data-stu-id="5bdee-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="5bdee-107">[VistaGrbits](./vistagrbits-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="5bdee-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="5bdee-108">欄位</span><span class="sxs-lookup"><span data-stu-id="5bdee-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5bdee-109">名稱</span><span class="sxs-lookup"><span data-stu-id="5bdee-109">Name</span></span></th>
<th><span data-ttu-id="5bdee-110">描述</span><span class="sxs-lookup"><span data-stu-id="5bdee-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="5bdee-114">快照會話會在 JetOSSnapshotThaw 之後繼續進行，而且需要 JetOSSnapshotEnd 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="5bdee-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="5bdee-118">針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="5bdee-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="5bdee-119">否則，索引在最重要的索引鍵資料行中的每個多重值都只會有一個專案，這是多重值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值（多重值資料行）。</span><span class="sxs-lookup"><span data-stu-id="5bdee-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="5bdee-120">例如，如果您對資料行 A 的索引指定此旗標，而資料行 A 的值為 &quot; 紅色 &quot; 和 &quot; 藍色， &quot; 而資料行 B 的值為 &quot; 1 &quot; 和2，則 &quot; &quot; 會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;紅色 &quot; 、 &quot; 2 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5bdee-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="5bdee-121">否則，將會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="5bdee-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="5bdee-125">指定此旗標將會導致索引的任何更新會導致截斷的金鑰因 <a href="hh564840(v=exchg.10).md">KeyTruncated</a>而失敗。</span><span class="sxs-lookup"><span data-stu-id="5bdee-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="5bdee-126">否則，將會以無訊息方式截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="5bdee-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="5bdee-130">多個多重值資料行的索引，但只含相同 itagSequence 的值。</span><span class="sxs-lookup"><span data-stu-id="5bdee-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="5bdee-134">交易記錄檔必須存在於記錄檔目錄中 (亦即無法自動啟動新的資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="5bdee-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="5bdee-138">執行復原，但在恢復階段停止。</span><span class="sxs-lookup"><span data-stu-id="5bdee-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="5bdee-139">允許重新執行任何記錄檔，然後可以複製並重新執行稍後的其他記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5bdee-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="5bdee-143">遺漏資料庫對應專案預設為相同的位置。</span><span class="sxs-lookup"><span data-stu-id="5bdee-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="5bdee-147">引擎可以在適當的情況下標記資料庫標頭 (例如，完整備份已完成) ，即使未完成截斷的呼叫也是一樣。</span><span class="sxs-lookup"><span data-stu-id="5bdee-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="5bdee-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="5bdee-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="5bdee-151">在成功的軟修復上，截斷記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5bdee-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5bdee-152">頁首</span><span class="sxs-lookup"><span data-stu-id="5bdee-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5bdee-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bdee-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bdee-154">參考</span><span class="sxs-lookup"><span data-stu-id="5bdee-154">Reference</span></span>

[<span data-ttu-id="5bdee-155">VistaGrbits 類別</span><span class="sxs-lookup"><span data-stu-id="5bdee-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="5bdee-156">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="5bdee-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
