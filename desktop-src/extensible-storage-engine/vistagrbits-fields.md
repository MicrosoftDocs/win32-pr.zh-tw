---
description: 深入瞭解： VistaGrbits 欄位
title: 'VistaGrbits fields (的欄位) '
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3694dae8c55a5da838b8fcc058b369d7f0a59ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853015"
---
# <a name="vistagrbits-fields"></a><span data-ttu-id="4752b-103">VistaGrbits 欄位</span><span class="sxs-lookup"><span data-stu-id="4752b-103">VistaGrbits fields</span></span>

<span data-ttu-id="4752b-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="4752b-104">Include protected members</span></span>  
<span data-ttu-id="4752b-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="4752b-105">Include inherited members</span></span>  

<span data-ttu-id="4752b-106">[VistaGrbits](./vistagrbits-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="4752b-106">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="4752b-107">欄位</span><span class="sxs-lookup"><span data-stu-id="4752b-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4752b-108">名稱</span><span class="sxs-lookup"><span data-stu-id="4752b-108">Name</span></span></th>
<th><span data-ttu-id="4752b-109">描述</span><span class="sxs-lookup"><span data-stu-id="4752b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="4752b-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="4752b-113">快照會話會在 JetOSSnapshotThaw 之後繼續進行，而且需要 JetOSSnapshotEnd 函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="4752b-113">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="4752b-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="4752b-117">針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="4752b-117">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="4752b-118">否則，索引在最重要的索引鍵資料行中的每個多重值都只會有一個專案，這是多重值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值（多重值資料行）。</span><span class="sxs-lookup"><span data-stu-id="4752b-118">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="4752b-119">例如，如果您對資料行 A 的索引指定此旗標，而資料行 A 的值為 &quot; 紅色 &quot; 和 &quot; 藍色， &quot; 而資料行 B 的值為 &quot; 1 &quot; 和2，則 &quot; &quot; 會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;紅色 &quot; 、 &quot; 2 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 2 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="4752b-119">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="4752b-120">否則，將會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="4752b-120">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="4752b-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="4752b-124">指定此旗標將會導致索引的任何更新會導致截斷的金鑰因 <a href="hh564840(v=exchg.10).md">KeyTruncated</a>而失敗。</span><span class="sxs-lookup"><span data-stu-id="4752b-124">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="4752b-125">否則，將會以無訊息方式截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="4752b-125">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="4752b-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="4752b-129">多個多重值資料行的索引，但只含相同 itagSequence 的值。</span><span class="sxs-lookup"><span data-stu-id="4752b-129">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="4752b-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="4752b-133">交易記錄檔必須存在於記錄檔目錄中 (亦即無法自動啟動新的資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="4752b-133">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="4752b-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="4752b-137">執行復原，但在恢復階段停止。</span><span class="sxs-lookup"><span data-stu-id="4752b-137">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="4752b-138">允許重新執行任何記錄檔，然後可以複製並重新執行稍後的其他記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4752b-138">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="4752b-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="4752b-142">遺漏資料庫對應專案預設為相同的位置。</span><span class="sxs-lookup"><span data-stu-id="4752b-142">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="4752b-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="4752b-146">引擎可以在適當的情況下標記資料庫標頭 (例如，完整備份已完成) ，即使未完成截斷的呼叫也是一樣。</span><span class="sxs-lookup"><span data-stu-id="4752b-146">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="4752b-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="4752b-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="4752b-150">在成功的軟修復上，截斷記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4752b-150">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4752b-151">頁首</span><span class="sxs-lookup"><span data-stu-id="4752b-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="4752b-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4752b-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4752b-153">參考</span><span class="sxs-lookup"><span data-stu-id="4752b-153">Reference</span></span>

[<span data-ttu-id="4752b-154">VistaGrbits 類別</span><span class="sxs-lookup"><span data-stu-id="4752b-154">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="4752b-155">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="4752b-155">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
