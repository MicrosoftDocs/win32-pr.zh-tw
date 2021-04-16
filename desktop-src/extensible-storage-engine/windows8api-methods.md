---
description: 深入瞭解： Windows8Api 方法
title: Windows8) 的 Windows8Api 方法 (
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550726"
---
# <a name="windows8api-methods"></a><span data-ttu-id="6c04a-103">Windows8Api 方法</span><span class="sxs-lookup"><span data-stu-id="6c04a-103">Windows8Api methods</span></span>

<span data-ttu-id="6c04a-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="6c04a-104">Include protected members</span></span>  
<span data-ttu-id="6c04a-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="6c04a-105">Include inherited members</span></span>  

<span data-ttu-id="6c04a-106">[Windows8Api](./windows8api-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="6c04a-106">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="6c04a-107">方法</span><span class="sxs-lookup"><span data-stu-id="6c04a-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6c04a-108">名稱</span><span class="sxs-lookup"><span data-stu-id="6c04a-108">Name</span></span></th>
<th><span data-ttu-id="6c04a-109">描述</span><span class="sxs-lookup"><span data-stu-id="6c04a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="6c04a-113">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="6c04a-113">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="6c04a-117">認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="6c04a-117">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="6c04a-118">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="6c04a-118">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="6c04a-122">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="6c04a-122">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="6c04a-126">建立資料表，並在該資料表上加入資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="6c04a-126">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="6c04a-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID、JET_DBID、JET_TABLECREATE) </a></span><span class="sxs-lookup"><span data-stu-id="6c04a-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="6c04a-131">取得有關錯誤的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="6c04a-131">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="6c04a-135">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="6c04a-135">Creates a temporary table with a single index.</span></span> <span data-ttu-id="6c04a-136">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="6c04a-136">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="6c04a-137">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="6c04a-137">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="6c04a-138">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="6c04a-138">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="6c04a-139">另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、Int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 &quot; JetOpenTempTable2 &quot; 、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。</span><span class="sxs-lookup"><span data-stu-id="6c04a-139">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="6c04a-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</span><span class="sxs-lookup"><span data-stu-id="6c04a-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="6c04a-144">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="6c04a-144">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="6c04a-148">調整目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="6c04a-148">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="6c04a-152">為 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a>設定簡單篩選的陣列。</span><span class="sxs-lookup"><span data-stu-id="6c04a-152">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="6c04a-156">在提供的會話狀態上設定參數，用於此會話的存留期，或在重設之前使用。</span><span class="sxs-lookup"><span data-stu-id="6c04a-156">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="6c04a-160">準備實例以進行終止。</span><span class="sxs-lookup"><span data-stu-id="6c04a-160">Prepares an instance for termination.</span></span> <span data-ttu-id="6c04a-161">也可以用來繼續先前的靜止。</span><span class="sxs-lookup"><span data-stu-id="6c04a-161">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="6c04a-165">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="6c04a-165">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="6c04a-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span><span class="sxs-lookup"><span data-stu-id="6c04a-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="6c04a-169">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="6c04a-169">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c04a-170">頁首</span><span class="sxs-lookup"><span data-stu-id="6c04a-170">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6c04a-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c04a-171">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c04a-172">參考</span><span class="sxs-lookup"><span data-stu-id="6c04a-172">Reference</span></span>

[<span data-ttu-id="6c04a-173">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="6c04a-173">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="6c04a-174">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6c04a-174">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
