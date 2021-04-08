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
# <a name="vistagrbits-fields"></a>VistaGrbits 欄位

包含受保護的成員  
包含繼承的成員  

[VistaGrbits](./vistagrbits-class.md)類型會公開下列成員。

## <a name="fields"></a>欄位

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>快照會話會在 JetOSSnapshotThaw 之後繼續進行，而且需要 JetOSSnapshotEnd 函式呼叫。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。 否則，索引在最重要的索引鍵資料行中的每個多重值都只會有一個專案，這是多重值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值（多重值資料行）。 例如，如果您對資料行 A 的索引指定此旗標，而資料行 A 的值為 &quot; 紅色 &quot; 和 &quot; 藍色， &quot; 而資料行 B 的值為 &quot; 1 &quot; 和2，則 &quot; &quot; 會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;紅色 &quot; 、 &quot; 2 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 2 &quot; 。 否則，將會建立下列索引項目： &quot; 紅色 &quot; 、 &quot; 1 &quot; ; &quot;藍色 &quot; 、 &quot; 1 &quot; 。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>指定此旗標將會導致索引的任何更新會導致截斷的金鑰因 <a href="hh564840(v=exchg.10).md">KeyTruncated</a>而失敗。 否則，將會以無訊息方式截斷金鑰。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>多個多重值資料行的索引，但只含相同 itagSequence 的值。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>交易記錄檔必須存在於記錄檔目錄中 (亦即無法自動啟動新的資料流程) 。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>執行復原，但在恢復階段停止。 允許重新執行任何記錄檔，然後可以複製並重新執行稍後的其他記錄檔。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>遺漏資料庫對應專案預設為相同的位置。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>引擎可以在適當的情況下標記資料庫標頭 (例如，完整備份已完成) ，即使未完成截斷的呼叫也是一樣。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>在成功的軟修復上，截斷記錄檔。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaGrbits 類別](./vistagrbits-class.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
