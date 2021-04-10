---
description: 深入瞭解： Windows8Api 成員
title: Windows8Api 成員 (Windows8) 的成員
TOCTitle: Windows8Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_members(v=EXCHG.10)
ms:contentKeyID: 55104331
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21167b66736e5bc05ec14f32cb715226264d2757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943697"
---
# <a name="windows8api-members"></a>Windows8Api 成員

包含受保護的成員  
包含繼承的成員  

Windows 8 中引進的 Api 呼叫。

[Windows8Api](./windows8api-class.md)類型會公開下列成員。

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
<td><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></td>
<td>導致會話進入交易，或在現有的交易中建立新的儲存點。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></td>
<td>認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。 如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></td>
<td>對 ESE 資料庫中的資料建立索引。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></td>
<td>建立資料表，並在該資料表上加入資料行和索引。 <a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID、JET_DBID、JET_TABLECREATE) </a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></td>
<td>取得有關錯誤的延伸資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></td>
<td>使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、Int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 &quot; JetOpenTempTable2 &quot; 、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。 <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></td>
<td>如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></td>
<td>調整目前開啟之資料庫的大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></td>
<td>為 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a>設定簡單篩選的陣列。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></td>
<td>在提供的會話狀態上設定參數，用於此會話的存留期，或在重設之前使用。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></td>
<td>準備實例以進行終止。 也可以用來繼續先前的靜止。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></td>
<td>如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></td>
<td>如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8Api 類別](./windows8api-class.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
