---
description: 深入瞭解： VistaApi 成員
title: " (的 VistaApi 成員) 的成員"
TOCTitle: VistaApi members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaApi
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi_members(v=EXCHG.10)
ms:contentKeyID: 55104282
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1ada48839d05f1eaeec5eae5fe541ea89c5e0b641bba35441b3f189bf2973ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106836"
---
# <a name="vistaapi-members"></a>VistaApi 成員

包含受保護的成員  
包含繼承的成員  

Windows Vista 中第一次支援的 ESENT api。

[VistaApi](./vistaapi-class.md)類型會公開下列成員。

## <a name="methods"></a>方法

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335319(v=exchg.10).md">JetGetColumnInfo</a></td>
<td>抓取資料表中資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351258(v=exchg.10).md">JetGetInstanceMiscInfo</a></td>
<td>抓取實例的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335320(v=exchg.10).md">JetGetRecordSize</a></td>
<td>從所需的位置抓取記錄大小資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351264(v=exchg.10).md">JetGetThreadStats</a></td>
<td>從資料庫引擎抓取目前線程的效能資訊。 您可以使用多個呼叫來收集統計資料，以反映這些呼叫之間的資料庫引擎在此執行緒上的活動。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351265(v=exchg.10).md">JetInit3</a></td>
<td>初始化 ESENT 資料庫引擎。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable</a></td>
<td>使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351267(v=exchg.10).md">JetOSSnapshotEnd</a></td>
<td>通知引擎快照會話已完成。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351269(v=exchg.10).md">JetOSSnapshotGetFreezeInfo</a></td>
<td>在任何指定的時間，取得屬於快照會話一部分的實例和資料庫清單。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335341(v=exchg.10).md">JetOSSnapshotPrepareInstance</a></td>
<td>選取要成為快照會話一部分的特定實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335343(v=exchg.10).md">JetOSSnapshotTruncateLog</a></td>
<td>針對屬於快照會話一部分的所有實例啟用記錄截斷。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351271(v=exchg.10).md">JetOSSnapshotTruncateLogInstance</a></td>
<td>在快照會話期間截斷指定之實例的記錄檔。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaApi 類別](./vistaapi-class.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
