---
description: 深入瞭解： Api 方法
title: Api 方法
TOCTitle: Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_methods(v=EXCHG.10)
ms:contentKeyID: 55100697
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3c6dbcee8fb33065169d0cfdfea3d8d557ef1d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560064"
---
# <a name="api-methods"></a>Api 方法

包含受保護的成員  
包含繼承的成員  

[Api](./api-class.md)類型會公開下列成員。

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
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從資料行還原序列化物件。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從資料行還原序列化物件。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>在一個資料行上執行不可部分完成的加法。 資料行的類型必須為 <a href="hh577895(v=exchg.10).md">Long</a>。 此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。 然後，您可以使用這個書簽，將該資料指標重新放置到使用 JetGotoBookmark 的相同記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>建立將資料行名稱對應至其資料行識別碼的字典。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>取得指定之資料行的 columnid。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns (JET_SESID JET_TABLEID) </a></td>
<td>逐一查看資料表中的所有資料行，並傳回每個資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns (JET_SESID、JET_DBID、字串) </a></td>
<td>逐一查看資料表中的所有資料行，並傳回每個資料行的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes (JET_SESID JET_TABLEID) </a></td>
<td>逐一查看資料表中的所有索引，傳回每個索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes (JET_SESID、JET_DBID、字串) </a></td>
<td>逐一查看資料表中的所有索引，傳回每個資料表的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">GetTableNames</a></td>
<td>傳回資料庫中的資料表名稱。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>交集一組索引範圍，並傳回在所有索引範圍中找到之記錄的書簽。 另請參閱 <a href="dn292212(v=exchg.10).md">JetIntersectIndexes (JET_SESID、[]、Int32、JET_RECORDLIST、IntersectIndexesGrbit) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>將新的資料行加入至現有的資料表。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>附加資料庫檔案以與資料庫實例搭配使用。 若要使用資料庫，就必須使用 <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) </a>來開啟它。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>附加資料庫檔案以與資料庫實例搭配使用。 若要使用資料庫，就必須使用 <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) </a>來開啟它。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>執行實例的串流備份，包括所有附加的資料庫，到目錄中。 如果引擎支援多個備份方法，這是最簡單且最簡單的封裝函數。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>當引擎和資料庫在線上且作用中時，起始外部備份。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>初始化新的 ESENT 會話。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>導致會話進入交易，或在現有的交易中建立新的儲存點。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>導致會話進入交易，或在現有的交易中建立新的儲存點。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>關閉先前以 JetOpenDatabase 開啟的資料庫檔案 <a href="dn292219(v=exchg.10).md"> (JET_SESID、字串、字串、JET_DBID、OpenDatabaseGrbit) </a> 或使用 <a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID、字串、字串、JET_DBID、CreateDatabaseGrbit) </a>建立。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>當使用 JetReadFileInstance 解壓縮該檔案中的資料之後，關閉以 JetOpenFileInstance 開啟的檔案。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>關閉開啟的資料表。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。 如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>建立現有資料庫的複本。 複本會壓縮為使用狀態的最佳狀態。 複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。 如此一來，壓縮的資料可能會盡可能儲存為密集。 或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>逐步解說資料表的每個索引，以精確計算索引中的專案數，以及索引中的相異索引鍵數目。 這項資訊，以及配置給索引的資料庫頁面數目和目前的計算時間，都會儲存在資料庫的索引中繼資料中。 之後可以使用資訊作業來抓取此資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>建立和附加資料庫檔案。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>建立並附加資料庫檔案，並指定最大資料庫大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>對 ESE 資料庫中的資料建立索引。 索引可以用來快速找出特定資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>對 ESE 資料庫中的資料建立索引。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>配置 database engine 的新實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>配置 database engine 的新實例，以在單一進程中使用，並指定顯示名稱。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>建立空的資料表。 新建立的資料表會以獨佔方式開啟。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>建立資料表，並在該資料表上加入資料行和索引。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>啟動和停止資料庫重組工作，以改善資料庫中的資料組織。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>啟動和停止資料庫重組工作，以改善資料庫中的資料組織。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>刪除資料庫資料表中的目前記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>從資料庫資料表中刪除資料行。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>從資料庫資料表中刪除資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>從資料庫資料表中刪除索引。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>從資料庫刪除資料表。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>釋放先前附加至資料庫會話的資料庫檔案。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>釋放先前附加至資料庫會話的資料庫檔案。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>複製開啟的資料指標，並傳回重復資料指標的控制碼。 如果複製的資料指標是唯讀資料指標，則重復資料指標也是唯讀資料指標。 任何與建立搜尋索引鍵或更新記錄相關的狀態都不會複製到重複的資料指標中。 此外，原始資料指標的位置不會複製到重複的資料指標中。 重複的資料指標一律會在叢集索引上開啟，而且其位置一律會在資料表的第一個資料列上。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">JetDupSession</a></td>
<td>在與指定 sesid 相同的實例中，初始化新的 ESE 會話。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>結束外部備份會話。 此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>結束會話。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>有效率地從資料指標的目前記錄或該資料指標的複製緩衝區，抓取一組資料行和其值。 您可以使用資料行識別碼、itagSequence 數位和其他特性的清單來限制抓取的資料行和值。 此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 realloc 相容回呼所取得。 這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。 如此一來，就不需要使用 JetRetrieveColumn 的探索模式來判斷這些特性，以便設定 JetRetrieveColumn 的最後一個呼叫，以成功取得所需的資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>在一個資料行上執行不可部分完成的加法運算。 此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。 另請參閱 <a href="dn292114(v=exchg.10).md">EscrowUpdate (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>釋出由 database engine 呼叫所配置的記憶體。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。 系統只會考慮目前使用 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a> 連接到實例的資料庫。 之後，這些檔案可能會使用 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a> 和 Read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE，JET_HANDLE，[]，int32，int32) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。 然後，您可以使用 <a href="dn292200(v=exchg.10).md">JetGotoBookmark (JET_SESID、JET_TABLEID、[]、Int32) </a>，利用這個書簽將該資料指標重新置放回相同記錄。 書簽將不再超過 <a href="dn351215(v=exchg.10).md">BookmarkMost</a> 個位元組。 另請參閱 <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID JET_TABLEID) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNBASE) </a></td>
<td>抓取資料表中資料行的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNDEF) </a></td>
<td>抓取資料表資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNLIST) </a></td>
<td>抓取資料表中所有資料行的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Ddetermines 指定資料指標目前索引的名稱。 這個名稱也用來在稍後使用 <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex (JET_SESID、JET_TABLEID、String) </a>，重新選取該索引做為目前的索引。 它也可以用來使用 JetGetTableIndexInfo 探索該索引的屬性。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>根據記錄目前的更新狀態，判斷資料指標的目前記錄更新是否會導致寫入衝突。 即使 JetGetCursorInfo 成功傳回，還是可能會傳回寫入衝突。 因為另一個會話可能會在目前的會話可以更新相同記錄之前更新記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo (字串、JET_DBINFOMISC JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo (String、Int32、JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo (String、Int64、JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、JET_DBINFOMISC JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、Int32、JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、字串、JET_DbInfo) </a></td>
<td>抓取特定資料庫的特定資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST) </a></td>
<td><strong>已淘汰。</strong> 抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXID JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、Int32、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、字串、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、UInt16、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>抓取正在執行之實例的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。 一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。 由於記錄版本控制，通常不需要讀取鎖定。 不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以取得資料庫修補檔和記錄檔的名稱，該檔案會成為備份檔案集的一部分。 之後，這些檔案可能會使用 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a> 和 Read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE，JET_HANDLE，[]，int32，int32) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>讓應用程式取出與資料指標相關聯的內容控制碼，或與該資料指標相關聯的資料表。 先前必須使用 <a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a>設定此內容控制碼。 JetGetLS 也可以用來同時提取資料指標或資料表的目前內容控制碼，並重設該內容控制碼。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo (JET_SESID、JET_DBID、JET_OBJECTLIST) </a></td>
<td>抓取資料庫物件的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo (JET_SESID、JET_DBID、JET_objtyp、String JET_OBJECTINFO) </a></td>
<td>抓取資料庫物件的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>以 <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> 結構的形式，傳回目前索引中目前記錄的小數位置。 另請參閱 <a href="dn292207(v=exchg.10).md">JetGotoPosition (JET_SESID、JET_TABLEID JET_RECPOS) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>在資料指標的目前位置，抓取次要索引項目的特殊書簽。 然後，您可以使用這個書簽，利用 JetGotoSecondaryIndexBookmark 將該資料指標有效率地重新放置到相同的索引項目。 當在包含重複索引鍵或包含相同記錄之多個索引項目的次要索引上重新置放時，這非常有用。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、Int32、String、Int32) </a></td>
<td>取得資料庫設定選項。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) </a></td>
<td>取得資料庫設定選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、JET_COLUMNID JET_COLUMNDEF) </a></td>
<td>抓取資料表資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、字串、JET_COLUMNDEF) </a></td>
<td>抓取資料表資料行的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) </a></td>
<td>抓取資料表中所有資料行的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST) </a></td>
<td><strong>已淘汰。</strong> 抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXID JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、Int32、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、字串、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、String、UInt16、JET_IdxInfo) </a></td>
<td>抓取資料表上索引的相關資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_DBID JET_TblInfo) </a></td>
<td>抓取資料庫中資料表的各種資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_OBJECTINFO JET_TblInfo) </a></td>
<td>抓取資料庫中資料表的各種資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a></td>
<td>抓取資料庫中資料表的各種資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a></td>
<td>抓取資料庫中資料表的各種資訊。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a></td>
<td>抓取資料庫中資料表的各種資訊。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以找出備份順利完成之後可安全刪除的交易記錄檔名稱。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>抓取資料庫引擎的版本。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>將游標放置在與指定書簽相關聯之記錄的索引項目目。 書簽可以搭配資料表上定義的任何索引使用。 您可以使用 <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID、JET_TABLEID、[]、int32、int32) </a>來取出記錄的書簽。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>將游標移至新的位置，這是透過目前索引的一小部分。 另請參閱 <a href="dn292181(v=exchg.10).md">JetGetRecordPosition (JET_SESID、JET_TABLEID JET_RECPOS) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>將游標放置在與指定次要索引書簽相關聯的索引項目目。 次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。 您可以使用 <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、[]、int32、[]、int32、GotoSecondaryIndexBookmarkGrbit) </a>，來抓取索引項目的次要索引書簽。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>擴充目前開啟之資料庫的大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>執行閒置清除工作或檢查 ESE 中的版本存放區狀態。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>計算目前索引中的專案數，從目前的位置向前算。 目前的位置會包含在計數中。 如果目前索引超過多重值資料行，而且資料行的實例具有多個值，則計數可以大於資料表中的記錄總數。 如果資料表是空的，則會傳回計數的0。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>初始化 ESENT 資料庫引擎。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>初始化 ESENT 資料庫引擎。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>計算相同資料表上不同次要索引的多個索引項目目集合之間的交集。 這項作業適用于在資料表中尋找符合可使用索引範圍表示之兩個或多個準則的一組記錄。 另請參閱 <a href="dn292094(v=exchg.10).md">IntersectIndexes (JET_SESID，[] ) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>會建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) </a></td>
<td>流覽索引。 資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。 另請參閱 <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID、JET_TABLEID) </a>、 <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID、JET_TABLEID) </a>、 <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID、JET_TABLEID) </a>、 <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID JET_TABLEID) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a></td>
<td>流覽索引。 資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。 另請參閱 <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID、JET_TABLEID) </a>、 <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID、JET_TABLEID) </a>、 <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID、JET_TABLEID) </a>、 <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID JET_TABLEID) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>開啟先前附加了 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a>的資料庫，以搭配資料庫會話使用。 您可以針對相同的資料庫多次呼叫這個函數。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。 之後可以使用 JetReadFileInstance，透過傳回的控制碼讀取這些檔案中的資料。 傳回的控制碼必須使用 JetCloseFileInstance 來關閉。 實例的外部備份必須先前已使用 JetBeginExternalBackupInstance 起始。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>在先前建立的資料表上開啟資料指標。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。 <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。 <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、Int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>啟動快照集。 當快照集進行中時，引擎無法進行寫入磁片的活動。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>開始快照集會話的準備工作。 快照集會話是一個短暫的時間間隔，在此時間間隔中，引擎不會將任何寫入 Io 發出至磁片，因此引擎可以在由快照寫入器驅動) 時，參與磁片區快照集會話 (。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>通知引擎可在凍結期間之後繼續正常 IO 作業，以及成功的快照集。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>準備資料指標進行更新。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>抓取以 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a>開啟的檔案內容。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>允許應用程式將資料庫引擎設定為對應用程式發出特定事件的通知。 這些通知會與特定的資料表相關聯，而且只有在包含該資料表的實例使用 <a href="dn334020(v=exchg.10).md">JetTerm (JET_INSTANCE) </a>關閉時，才會維持有效狀態。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>變更現有資料行的名稱。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>變更現有資料表的名稱。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionCoNtext</a></td>
<td>解除會話與目前線程之間的之間的解除。 這應該與 <a href="dn334027(v=exchg.10).md">JetSetSessionCoNtext (JET_SESID、IntPtr) </a>一起使用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>通知資料庫引擎應用程式不再掃描游標所在的整個索引。 此呼叫會反轉 <a href="dn334018(v=exchg.10).md">JetSetTableSequential (JET_SESID、JET_TABLEID、SetTableSequentialGrbit) </a>所傳送的通知。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>還原和復原實例（包括所有附加的資料庫）的資料流程備份。 它是設計來搭配使用 <a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) </a> 函數所建立的備份。 這是最簡單且最具封裝的還原功能。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。 除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID，JET_TABLEID，JET_COLUMNID，[]，Int32，Int32，Int32，RetrieveColumnGrbit，JET_RETINFO) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。 除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></td>
<td>從單一作業中的目前記錄抓取多個資料行值。 JET_RETRIEVECOLUMN 結構的陣列用來描述要抓取的資料行值集合，以及描述要抓取之每個資料行值的輸出緩衝區。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>在資料指標的目前位置，抓取索引項目的索引鍵。 另請參閱 <a href="dn334085(v=exchg.10).md">RetrieveKey (JET_SESID、JET_TABLEID、RetrieveKeyGrbit) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>復原對資料庫狀態所做的變更，並返回到最後一個儲存點。 JetRollback 也會關閉儲存點期間開啟的任何資料指標。 如果最外層的儲存點復原，會話將會結束交易。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。 您先前必須使用 <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID、JET_TABLEID、[]、Int32、MakeKeyGrbit) </a>來建立搜尋索引鍵。 另請參閱 <a href="dn334145(v=exchg.10).md">TrySeek (JET_SESID、JET_TABLEID、SeekGrbit) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、SetColumnGrbit、JET_SETINFO) </a></td>
<td>JetSetColumn 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。 它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a>) 類型資料行的完整或部分 long (值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、Int32、SetColumnGrbit、JET_SETINFO) </a></td>
<td>JetSetColumn 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。 它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a>) 類型資料行的完整或部分 long (值。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>變更現有資料行的預設值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">JetSetColumns</a></td>
<td>允許應用程式在單一作業中設定多個資料行值。 <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a>結構的陣列用來描述要設定的資料行值集合，以及描述要設定之每個資料行值的輸入緩衝區。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>設定資料指標的目前索引。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>設定資料指標的目前索引。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>設定資料指標的目前索引。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>設定資料指標的目前索引。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>設定未開啟之資料庫檔案的大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>暫時限制資料指標可以使用 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a> 的索引項目集合，以從目前索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定的搜尋準則和指定的系結準則的索引項目目結束。 您先前必須使用 <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID、JET_TABLEID、[]、Int32、MakeKeyGrbit) </a>來建立搜尋索引鍵。 另請參閱 <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>讓應用程式將稱為本機儲存的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。 應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。 當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。 這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionCoNtext</a></td>
<td>使用指定的內容控制碼，將會話與目前的執行緒產生關聯。 此關聯會覆寫指定會話的交易必須完全在相同執行緒上執行的預設引擎需求。 使用 <a href="dn332991(v=exchg.10).md">JetResetSessionCoNtext (JET_SESID) </a> 來移除關聯。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、JET_CALLBACK、字串) </a></td>
<td>設定資料庫設定選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、Int32、String) </a></td>
<td>設定資料庫設定選項。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String) </a></td>
<td>設定資料庫設定選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>通知資料庫引擎應用程式正在掃描資料指標所在的整個索引。 因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。 另請參閱 <a href="dn332994(v=exchg.10).md">JetResetTableSequential (JET_SESID、JET_TABLEID、ResetTableSequentialGrbit) </a>。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>防止串流備份相關的活動在特定執行中的實例上繼續執行，因此以可預測的方式結束資料流程備份。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>準備實例以進行終止。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>終止以 <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 或 <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE、String) </a>建立的實例。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>終止以 <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 或 <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE、String) </a>建立的實例。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>在 JetBeginExternalBackup 所起始的備份期間，用來刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>設定 database engine，以停止在先前透過 <a href="dn332989(v=exchg.10).md">JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE) </a>要求的情況下發出通知至應用程式。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate (JET_SESID JET_TABLEID) </a></td>
<td>JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。 藉由呼叫 <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID JET_TABLEID) </a>來執行刪除資料表資料列。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate (JET_SESID、JET_TABLEID、[]、Int32、Int32) </a></td>
<td>JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。 藉由呼叫 <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID JET_TABLEID) </a>來執行刪除資料表資料列。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、布林值、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Byte、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、[]、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、DateTime、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Double、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Guid、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int16、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int32、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int64、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Single、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt16、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt32、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt64、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、字串、編碼、MakeKeyGrbit) </a></td>
<td>建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>將游標放在資料表中的最後一筆記錄之後。 接下來的移動會將游標放在最後一筆記錄上。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>將游標放在資料表的第一筆記錄之前。 接下來的移動會將游標放在第一筆記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>移除以 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a> 或 <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>建立的索引範圍。 如果沒有索引範圍存在，這個方法不會執行任何動作。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。 除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取布林資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取布林資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取位元組資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取位元組資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 datetime 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 datetime 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取雙資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取雙資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 float 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 float 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 guid 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 guid 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 int16 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 int32 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 使用 Unicode 編碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼) </a></td>
<td>從目前的記錄抓取字串資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取字串資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 uint16 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 uint16 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 uint32 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 uint32 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取 uint64 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取 uint64 資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>將資料行抓取 ColumnValue 物件。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></td>
<td>從目前的記錄抓取單一資料行值的大小。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32、RetrieveColumnGrbit) </a></td>
<td>從目前的記錄抓取單一資料行值的大小。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>在資料指標的目前位置，抓取索引項目的索引鍵。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>將物件的序列化形式寫入資料行。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Boolean) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[] ) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、DateTime) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Double) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Guid) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int16) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int64) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、單一) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt16) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt32) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt64) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、SetColumnGrbit) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼、SetColumnGrbit) </a></td>
<td>修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>設定 ColumnValue 物件中的資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。 一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。 由於記錄版本控制，通常不需要讀取鎖定。 不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>嘗試流覽索引。 如果流覽成功，這個方法會傳回 true。 如果沒有任何記錄可流覽此方法，則會傳回 false;將會擲回例外狀況，以找出其他錯誤。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>請嘗試移至資料表中的第一筆記錄。 如果資料表是空的，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>請嘗試移至資料表中的最後一筆記錄。 如果資料表是空的，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>請嘗試移至資料表中的下一筆記錄。 如果沒有下一個記錄，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>請嘗試移至資料表中的上一筆記錄。 如果沒有先前的記錄，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>嘗試開啟資料表。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。 搜尋金鑰必須先前已使用 JetMakeKey 來建立。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>暫時限制索引項目的索引項目集合，其可使用 JetMove 從目前的索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定之搜尋準則的索引項目目和指定的系結準則中結束。 搜尋金鑰必須先前已使用 JetMakeKey 來建立。 如果索引範圍不是空的，則傳回 true，否則傳回 false。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
