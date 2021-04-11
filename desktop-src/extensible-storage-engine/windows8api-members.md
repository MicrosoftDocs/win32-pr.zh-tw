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
# <a name="windows8api-members"></a><span data-ttu-id="defd5-103">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="defd5-103">Windows8Api members</span></span>

<span data-ttu-id="defd5-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="defd5-104">Include protected members</span></span>  
<span data-ttu-id="defd5-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="defd5-105">Include inherited members</span></span>  

<span data-ttu-id="defd5-106">Windows 8 中引進的 Api 呼叫。</span><span class="sxs-lookup"><span data-stu-id="defd5-106">Api calls introduced in Windows 8.</span></span>

<span data-ttu-id="defd5-107">[Windows8Api](./windows8api-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="defd5-107">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="defd5-108">方法</span><span class="sxs-lookup"><span data-stu-id="defd5-108">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="defd5-109">名稱</span><span class="sxs-lookup"><span data-stu-id="defd5-109">Name</span></span></th>
<th><span data-ttu-id="defd5-110">描述</span><span class="sxs-lookup"><span data-stu-id="defd5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="defd5-113"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="defd5-114">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="defd5-114">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="defd5-117"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="defd5-118">認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="defd5-118">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="defd5-119">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="defd5-119">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="defd5-122"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="defd5-123">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="defd5-123">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="defd5-126"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="defd5-127">建立資料表，並在該資料表上加入資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="defd5-127">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="defd5-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID、JET_DBID、JET_TABLECREATE) </a></span><span class="sxs-lookup"><span data-stu-id="defd5-128"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-131"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span><span class="sxs-lookup"><span data-stu-id="defd5-131"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="defd5-132">取得有關錯誤的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="defd5-132">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="defd5-135"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="defd5-136">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="defd5-136">Creates a temporary table with a single index.</span></span> <span data-ttu-id="defd5-137">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="defd5-137">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="defd5-138">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="defd5-138">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="defd5-139">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="defd5-139">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="defd5-140">另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、Int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 &quot; JetOpenTempTable2 &quot; 、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。</span><span class="sxs-lookup"><span data-stu-id="defd5-140">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="defd5-141"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</span><span class="sxs-lookup"><span data-stu-id="defd5-141"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-144"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="defd5-144"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="defd5-145">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="defd5-145">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-148"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span><span class="sxs-lookup"><span data-stu-id="defd5-148"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="defd5-149">調整目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="defd5-149">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-152"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span><span class="sxs-lookup"><span data-stu-id="defd5-152"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="defd5-153">為 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a>設定簡單篩選的陣列。</span><span class="sxs-lookup"><span data-stu-id="defd5-153">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-156"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span><span class="sxs-lookup"><span data-stu-id="defd5-156"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="defd5-157">在提供的會話狀態上設定參數，用於此會話的存留期，或在重設之前使用。</span><span class="sxs-lookup"><span data-stu-id="defd5-157">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="defd5-160"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="defd5-161">準備實例以進行終止。</span><span class="sxs-lookup"><span data-stu-id="defd5-161">Prepares an instance for termination.</span></span> <span data-ttu-id="defd5-162">也可以用來繼續先前的靜止。</span><span class="sxs-lookup"><span data-stu-id="defd5-162">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-165"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="defd5-165"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="defd5-166">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="defd5-166">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="defd5-169"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span><span class="sxs-lookup"><span data-stu-id="defd5-169"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="defd5-170">如果具有指定索引鍵範圍的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。</span><span class="sxs-lookup"><span data-stu-id="defd5-170">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="defd5-171">頁首</span><span class="sxs-lookup"><span data-stu-id="defd5-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="defd5-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="defd5-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="defd5-173">參考</span><span class="sxs-lookup"><span data-stu-id="defd5-173">Reference</span></span>

[<span data-ttu-id="defd5-174">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="defd5-174">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="defd5-175">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="defd5-175">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
