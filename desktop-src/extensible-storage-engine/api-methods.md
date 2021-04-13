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
# <a name="api-methods"></a><span data-ttu-id="a5caa-103">Api 方法</span><span class="sxs-lookup"><span data-stu-id="a5caa-103">Api methods</span></span>

<span data-ttu-id="a5caa-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="a5caa-104">Include protected members</span></span>  
<span data-ttu-id="a5caa-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="a5caa-105">Include inherited members</span></span>  

<span data-ttu-id="a5caa-106">[Api](./api-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="a5caa-106">The [Api](./api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="a5caa-107">方法</span><span class="sxs-lookup"><span data-stu-id="a5caa-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5caa-108">名稱</span><span class="sxs-lookup"><span data-stu-id="a5caa-108">Name</span></span></th>
<th><span data-ttu-id="a5caa-109">描述</span><span class="sxs-lookup"><span data-stu-id="a5caa-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-112"><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-112"><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-113">從資料行還原序列化物件。</span><span class="sxs-lookup"><span data-stu-id="a5caa-113">Deserialize an object from a column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-116"><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-116"><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-117">從資料行還原序列化物件。</span><span class="sxs-lookup"><span data-stu-id="a5caa-117">Deserialize an object from a column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-120"><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-120"><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></span></span></td>
<td><span data-ttu-id="a5caa-121">在一個資料行上執行不可部分完成的加法。</span><span class="sxs-lookup"><span data-stu-id="a5caa-121">Perform atomic addition on one column.</span></span> <span data-ttu-id="a5caa-122">資料行的類型必須為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-122">The column must be of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span> <span data-ttu-id="a5caa-123">此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="a5caa-123">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-126"><a href="dn292099(v=exchg.10).md">GetBookmark</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-126"><a href="dn292099(v=exchg.10).md">GetBookmark</a></span></span></td>
<td><span data-ttu-id="a5caa-127">抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-127">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="a5caa-128">然後，您可以使用這個書簽，將該資料指標重新放置到使用 JetGotoBookmark 的相同記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-128">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-131"><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-131"><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></span></span></td>
<td><span data-ttu-id="a5caa-132">建立將資料行名稱對應至其資料行識別碼的字典。</span><span class="sxs-lookup"><span data-stu-id="a5caa-132">Creates a dictionary which maps column names to their column IDs.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-135"><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-135"><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></span></span></td>
<td><span data-ttu-id="a5caa-136">取得指定之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="a5caa-136">Get the columnid of the specified column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-139"><a href="dn292090(v=exchg.10).md">GetTableColumns (JET_SESID JET_TABLEID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-139"><a href="dn292090(v=exchg.10).md">GetTableColumns(JET_SESID, JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="a5caa-140">逐一查看資料表中的所有資料行，並傳回每個資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-140">Iterates over all the columns in the table, returning information about each one.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-143"><a href="dn292089(v=exchg.10).md">GetTableColumns (JET_SESID、JET_DBID、字串) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-143"><a href="dn292089(v=exchg.10).md">GetTableColumns(JET_SESID, JET_DBID, String)</a></span></span></td>
<td><span data-ttu-id="a5caa-144">逐一查看資料表中的所有資料行，並傳回每個資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-144">Iterates over all the columns in the table, returning information about each one.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-147"><a href="dn292093(v=exchg.10).md">GetTableIndexes (JET_SESID JET_TABLEID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-147"><a href="dn292093(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="a5caa-148">逐一查看資料表中的所有索引，傳回每個索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-148">Iterates over all the indexes in the table, returning information about each one.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-151"><a href="dn292092(v=exchg.10).md">GetTableIndexes (JET_SESID、JET_DBID、字串) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-151"><a href="dn292092(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_DBID, String)</a></span></span></td>
<td><span data-ttu-id="a5caa-152">逐一查看資料表中的所有索引，傳回每個資料表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-152">Iterates over all the indexs in the table, returning information about each one.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-155"><a href="dn292095(v=exchg.10).md">GetTableNames</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-155"><a href="dn292095(v=exchg.10).md">GetTableNames</a></span></span></td>
<td><span data-ttu-id="a5caa-156">傳回資料庫中的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-156">Returns the names of the tables in the database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-159"><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-159"><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></span></span></td>
<td><span data-ttu-id="a5caa-160">交集一組索引範圍，並傳回在所有索引範圍中找到之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-160">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="a5caa-161">另請參閱 <a href="dn292212(v=exchg.10).md">JetIntersectIndexes (JET_SESID、[]、Int32、JET_RECORDLIST、IntersectIndexesGrbit) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-161">Also see <a href="dn292212(v=exchg.10).md">JetIntersectIndexes(JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-164"><a href="dn292097(v=exchg.10).md">JetAddColumn</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-164"><a href="dn292097(v=exchg.10).md">JetAddColumn</a></span></span></td>
<td><span data-ttu-id="a5caa-165">將新的資料行加入至現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-165">Add a new column to an existing table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-168"><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-168"><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-169">附加資料庫檔案以與資料庫實例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-169">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="a5caa-170">若要使用資料庫，就必須使用 <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) </a>來開啟它。</span><span class="sxs-lookup"><span data-stu-id="a5caa-170">In order to use the database, it will need to be subsequently opened with <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-173"><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-173"><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></span></span></td>
<td><span data-ttu-id="a5caa-174">附加資料庫檔案以與資料庫實例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-174">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="a5caa-175">若要使用資料庫，就必須使用 <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) </a>來開啟它。</span><span class="sxs-lookup"><span data-stu-id="a5caa-175">In order to use the database, it will need to be subsequently opened with <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-178"><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-178"><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-179">執行實例的串流備份，包括所有附加的資料庫，到目錄中。</span><span class="sxs-lookup"><span data-stu-id="a5caa-179">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="a5caa-180">如果引擎支援多個備份方法，這是最簡單且最簡單的封裝函數。</span><span class="sxs-lookup"><span data-stu-id="a5caa-180">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-183"><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-183"><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-184">當引擎和資料庫在線上且作用中時，起始外部備份。</span><span class="sxs-lookup"><span data-stu-id="a5caa-184">Initiates an external backup while the engine and database are online and active.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-187"><a href="dn292103(v=exchg.10).md">JetBeginSession</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-187"><a href="dn292103(v=exchg.10).md">JetBeginSession</a></span></span></td>
<td><span data-ttu-id="a5caa-188">初始化新的 ESENT 會話。</span><span class="sxs-lookup"><span data-stu-id="a5caa-188">Initialize a new ESENT session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-191"><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-191"><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></span></span></td>
<td><span data-ttu-id="a5caa-192">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="a5caa-192">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-195"><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-195"><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></span></span></td>
<td><span data-ttu-id="a5caa-196">導致會話進入交易，或在現有的交易中建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="a5caa-196">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-199"><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-199"><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-200">關閉先前以 JetOpenDatabase 開啟的資料庫檔案 <a href="dn292219(v=exchg.10).md"> (JET_SESID、字串、字串、JET_DBID、OpenDatabaseGrbit) </a> 或使用 <a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID、字串、字串、JET_DBID、CreateDatabaseGrbit) </a>建立。</span><span class="sxs-lookup"><span data-stu-id="a5caa-200">Closes a database file that was previously opened with <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a> or created with <a href="dn292118(v=exchg.10).md">JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-203"><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-203"><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-204">當使用 JetReadFileInstance 解壓縮該檔案中的資料之後，關閉以 JetOpenFileInstance 開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="a5caa-204">Closes a file that was opened with JetOpenFileInstance after the data from that file has been extracted using JetReadFileInstance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-207"><a href="dn292109(v=exchg.10).md">JetCloseTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-207"><a href="dn292109(v=exchg.10).md">JetCloseTable</a></span></span></td>
<td><span data-ttu-id="a5caa-208">關閉開啟的資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-208">Close an open table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-211"><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-211"><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></span></span></td>
<td><span data-ttu-id="a5caa-212">認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="a5caa-212">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="a5caa-213">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="a5caa-213">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-216"><a href="dn292112(v=exchg.10).md">JetCompact</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-216"><a href="dn292112(v=exchg.10).md">JetCompact</a></span></span></td>
<td><span data-ttu-id="a5caa-217">建立現有資料庫的複本。</span><span class="sxs-lookup"><span data-stu-id="a5caa-217">Makes a copy of an existing database.</span></span> <span data-ttu-id="a5caa-218">複本會壓縮為使用狀態的最佳狀態。</span><span class="sxs-lookup"><span data-stu-id="a5caa-218">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="a5caa-219">複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="a5caa-219">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="a5caa-220">如此一來，壓縮的資料可能會盡可能儲存為密集。</span><span class="sxs-lookup"><span data-stu-id="a5caa-220">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="a5caa-221">或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-221">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-224"><a href="dn292113(v=exchg.10).md">JetComputeStats</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-224"><a href="dn292113(v=exchg.10).md">JetComputeStats</a></span></span></td>
<td><span data-ttu-id="a5caa-225">逐步解說資料表的每個索引，以精確計算索引中的專案數，以及索引中的相異索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="a5caa-225">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="a5caa-226">這項資訊，以及配置給索引的資料庫頁面數目和目前的計算時間，都會儲存在資料庫的索引中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="a5caa-226">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="a5caa-227">之後可以使用資訊作業來抓取此資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-227">This data can be subsequently retrieved with information operations.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-230"><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-230"><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-231">建立和附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="a5caa-231">Creates and attaches a database file.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-234"><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-234"><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></span></span></td>
<td><span data-ttu-id="a5caa-235">建立並附加資料庫檔案，並指定最大資料庫大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-235">Creates and attaches a database file with a maximum database size specified.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-238"><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-238"><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></span></span></td>
<td><span data-ttu-id="a5caa-239">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-239">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="a5caa-240">索引可以用來快速找出特定資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-240">An index can be used to locate specific data quickly.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-243"><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-243"><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></span></span></td>
<td><span data-ttu-id="a5caa-244">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-244">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-247"><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-247"><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-248">配置 database engine 的新實例。</span><span class="sxs-lookup"><span data-stu-id="a5caa-248">Allocates a new instance of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-251"><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-251"><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></span></span></td>
<td><span data-ttu-id="a5caa-252">配置 database engine 的新實例，以在單一進程中使用，並指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-252">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-255"><a href="dn292127(v=exchg.10).md">JetCreateTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-255"><a href="dn292127(v=exchg.10).md">JetCreateTable</a></span></span></td>
<td><span data-ttu-id="a5caa-256">建立空的資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-256">Create an empty table.</span></span> <span data-ttu-id="a5caa-257">新建立的資料表會以獨佔方式開啟。</span><span class="sxs-lookup"><span data-stu-id="a5caa-257">The newly created table is opened exclusively.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-260"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-260"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></span></span></td>
<td><span data-ttu-id="a5caa-261">建立資料表，並在該資料表上加入資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-261">Creates a table, adds columns, and indices on that table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-264"><a href="dn292130(v=exchg.10).md">JetDefragment</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-264"><a href="dn292130(v=exchg.10).md">JetDefragment</a></span></span></td>
<td><span data-ttu-id="a5caa-265">啟動和停止資料庫重組工作，以改善資料庫中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="a5caa-265">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-268"><a href="dn292145(v=exchg.10).md">JetDefragment2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-268"><a href="dn292145(v=exchg.10).md">JetDefragment2</a></span></span></td>
<td><span data-ttu-id="a5caa-269">啟動和停止資料庫重組工作，以改善資料庫中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="a5caa-269">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-272"><a href="dn292131(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-272"><a href="dn292131(v=exchg.10).md">JetDelete</a></span></span></td>
<td><span data-ttu-id="a5caa-273">刪除資料庫資料表中的目前記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-273">Deletes the current record in a database table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-276"><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-276"><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></span></span></td>
<td><span data-ttu-id="a5caa-277">從資料庫資料表中刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-277">Deletes a column from a database table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-280"><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-280"><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></span></span></td>
<td><span data-ttu-id="a5caa-281">從資料庫資料表中刪除資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-281">Deletes a column from a database table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-284"><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-284"><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></span></span></td>
<td><span data-ttu-id="a5caa-285">從資料庫資料表中刪除索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-285">Deletes an index from a database table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-288"><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-288"><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></span></span></td>
<td><span data-ttu-id="a5caa-289">從資料庫刪除資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-289">Deletes a table from a database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-292"><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-292"><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-293">釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="a5caa-293">Releases a database file that was previously attached to a database session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-296"><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-296"><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></span></span></td>
<td><span data-ttu-id="a5caa-297">釋放先前附加至資料庫會話的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="a5caa-297">Releases a database file that was previously attached to a database session.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-300"><a href="dn292137(v=exchg.10).md">JetDupCursor</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-300"><a href="dn292137(v=exchg.10).md">JetDupCursor</a></span></span></td>
<td><span data-ttu-id="a5caa-301">複製開啟的資料指標，並傳回重復資料指標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5caa-301">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="a5caa-302">如果複製的資料指標是唯讀資料指標，則重復資料指標也是唯讀資料指標。</span><span class="sxs-lookup"><span data-stu-id="a5caa-302">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="a5caa-303">任何與建立搜尋索引鍵或更新記錄相關的狀態都不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="a5caa-303">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="a5caa-304">此外，原始資料指標的位置不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="a5caa-304">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="a5caa-305">重複的資料指標一律會在叢集索引上開啟，而且其位置一律會在資料表的第一個資料列上。</span><span class="sxs-lookup"><span data-stu-id="a5caa-305">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-308"><a href="dn292140(v=exchg.10).md">JetDupSession</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-308"><a href="dn292140(v=exchg.10).md">JetDupSession</a></span></span></td>
<td><span data-ttu-id="a5caa-309">在與指定 sesid 相同的實例中，初始化新的 ESE 會話。</span><span class="sxs-lookup"><span data-stu-id="a5caa-309">Initialize a new ESE session in the same instance as the given sesid.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-312"><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-312"><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-313">結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="a5caa-313">Ends an external backup session.</span></span> <span data-ttu-id="a5caa-314">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="a5caa-314">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-317"><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-317"><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></span></span></td>
<td><span data-ttu-id="a5caa-318">結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="a5caa-318">Ends an external backup session.</span></span> <span data-ttu-id="a5caa-319">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="a5caa-319">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-322"><a href="dn292144(v=exchg.10).md">JetEndSession</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-322"><a href="dn292144(v=exchg.10).md">JetEndSession</a></span></span></td>
<td><span data-ttu-id="a5caa-323">結束會話。</span><span class="sxs-lookup"><span data-stu-id="a5caa-323">Ends a session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-326"><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-326"><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></span></span></td>
<td><span data-ttu-id="a5caa-327">有效率地從資料指標的目前記錄或該資料指標的複製緩衝區，抓取一組資料行和其值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-327">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="a5caa-328">您可以使用資料行識別碼、itagSequence 數位和其他特性的清單來限制抓取的資料行和值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-328">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="a5caa-329">此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 realloc 相容回呼所取得。</span><span class="sxs-lookup"><span data-stu-id="a5caa-329">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="a5caa-330">這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。</span><span class="sxs-lookup"><span data-stu-id="a5caa-330">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="a5caa-331">如此一來，就不需要使用 JetRetrieveColumn 的探索模式來判斷這些特性，以便設定 JetRetrieveColumn 的最後一個呼叫，以成功取得所需的資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-331">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-334"><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-334"><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></span></span></td>
<td><span data-ttu-id="a5caa-335">在一個資料行上執行不可部分完成的加法運算。</span><span class="sxs-lookup"><span data-stu-id="a5caa-335">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="a5caa-336">此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="a5caa-336">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="a5caa-337">另請參閱 <a href="dn292114(v=exchg.10).md">EscrowUpdate (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-337">Also see <a href="dn292114(v=exchg.10).md">EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-340"><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-340"><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></span></span></td>
<td><span data-ttu-id="a5caa-341">釋出由 database engine 呼叫所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a5caa-341">Frees memory that was allocated by a database engine call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-344"><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-344"><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-345">在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="a5caa-345">Used during a backup initiated by <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="a5caa-346">系統只會考慮目前使用 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a> 連接到實例的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a5caa-346">Only databases that are currently attached to the instance using <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> will be considered.</span></span> <span data-ttu-id="a5caa-347">之後，這些檔案可能會使用 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a> 和 Read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE，JET_HANDLE，[]，int32，int32) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-347">These files may subsequently be opened using <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> and read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-350"><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-350"><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></span></span></td>
<td><span data-ttu-id="a5caa-351">抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-351">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="a5caa-352">然後，您可以使用 <a href="dn292200(v=exchg.10).md">JetGotoBookmark (JET_SESID、JET_TABLEID、[]、Int32) </a>，利用這個書簽將該資料指標重新置放回相同記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-352">This bookmark can then be used to reposition that cursor back to the same record using <a href="dn292200(v=exchg.10).md">JetGotoBookmark(JET_SESID, JET_TABLEID, [], Int32)</a>.</span></span> <span data-ttu-id="a5caa-353">書簽將不再超過 <a href="dn351215(v=exchg.10).md">BookmarkMost</a> 個位元組。</span><span class="sxs-lookup"><span data-stu-id="a5caa-353">The bookmark will be no longer than <a href="dn351215(v=exchg.10).md">BookmarkMost</a> bytes.</span></span> <span data-ttu-id="a5caa-354">另請參閱 <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID JET_TABLEID) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-354">Also see <a href="dn292099(v=exchg.10).md">GetBookmark(JET_SESID, JET_TABLEID)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-357"><a href="dn292158(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNBASE) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-357"><a href="dn292158(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</a></span></span></td>
<td><span data-ttu-id="a5caa-358">抓取資料表中資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-358">Retrieves information about a column in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-361"><a href="dn292151(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNDEF) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-361"><a href="dn292151(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</a></span></span></td>
<td><span data-ttu-id="a5caa-362">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-362">Retrieves information about a table column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-365"><a href="dn292152(v=exchg.10).md">JetGetColumnInfo (JET_SESID、JET_DBID、字串、字串、JET_COLUMNLIST) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-365"><a href="dn292152(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</a></span></span></td>
<td><span data-ttu-id="a5caa-366">抓取資料表中所有資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-366">Retrieves information about all columns in a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-369"><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-369"><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></span></span></td>
<td><span data-ttu-id="a5caa-370">Ddetermines 指定資料指標目前索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-370">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="a5caa-371">這個名稱也用來在稍後使用 <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex (JET_SESID、JET_TABLEID、String) </a>，重新選取該索引做為目前的索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-371">This name is also used to later re-select that index as the current index using <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)</a>.</span></span> <span data-ttu-id="a5caa-372">它也可以用來使用 JetGetTableIndexInfo 探索該索引的屬性。</span><span class="sxs-lookup"><span data-stu-id="a5caa-372">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-375"><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-375"><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></span></span></td>
<td><span data-ttu-id="a5caa-376">根據記錄目前的更新狀態，判斷資料指標的目前記錄更新是否會導致寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="a5caa-376">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="a5caa-377">即使 JetGetCursorInfo 成功傳回，還是可能會傳回寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="a5caa-377">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="a5caa-378">因為另一個會話可能會在目前的會話可以更新相同記錄之前更新記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-378">because another session may update the record before the current session is able to update the same record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-381"><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo (字串、JET_DBINFOMISC JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-381"><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo(String, JET_DBINFOMISC, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-382">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-382">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-385"><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo (String、Int32、JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-385"><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int32, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-386">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-386">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-389"><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo (String、Int64、JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-389"><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int64, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-390">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-390">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-393"><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、JET_DBINFOMISC JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-393"><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-394">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-394">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-397"><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、Int32、JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-397"><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-398">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-398">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-401"><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID、JET_DBID、字串、JET_DbInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-401"><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, String, JET_DbInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-402">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-402">Retrieves certain information about the given database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-405"><a href="dn292168(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-405"><a href="dn292168(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</a></span></span></td>
<td><span data-ttu-id="a5caa-406"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="a5caa-406"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a5caa-407">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-407">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-410"><a href="dn292172(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXID JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-410"><a href="dn292172(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-411">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-411">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-414"><a href="dn292166(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-414"><a href="dn292166(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-415">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-415">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-418"><a href="dn292171(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、Int32、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-418"><a href="dn292171(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-419">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-419">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-422"><a href="dn292169(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、字串、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-422"><a href="dn292169(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-423">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-423">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-426"><a href="dn292173(v=exchg.10).md">JetGetIndexInfo (JET_SESID、JET_DBID、字串、字串、UInt16、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-426"><a href="dn292173(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-427">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-427">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-430"><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-430"><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></span></span></td>
<td><span data-ttu-id="a5caa-431">抓取正在執行之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-431">Retrieves information about the instances that are running.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-434"><a href="dn292175(v=exchg.10).md">JetGetLock</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-434"><a href="dn292175(v=exchg.10).md">JetGetLock</a></span></span></td>
<td><span data-ttu-id="a5caa-435">明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。</span><span class="sxs-lookup"><span data-stu-id="a5caa-435">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="a5caa-436">一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。</span><span class="sxs-lookup"><span data-stu-id="a5caa-436">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="a5caa-437">由於記錄版本控制，通常不需要讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="a5caa-437">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="a5caa-438">不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</span><span class="sxs-lookup"><span data-stu-id="a5caa-438">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-441"><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-441"><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-442">在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以取得資料庫修補檔和記錄檔的名稱，該檔案會成為備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="a5caa-442">Used during a backup initiated by <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="a5caa-443">之後，這些檔案可能會使用 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a> 和 Read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE，JET_HANDLE，[]，int32，int32) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-443">These files may subsequently be opened using <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> and read using <a href="dn332987(v=exchg.10).md">JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-446"><a href="dn292177(v=exchg.10).md">JetGetLS</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-446"><a href="dn292177(v=exchg.10).md">JetGetLS</a></span></span></td>
<td><span data-ttu-id="a5caa-447">讓應用程式取出與資料指標相關聯的內容控制碼，或與該資料指標相關聯的資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-447">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="a5caa-448">先前必須使用 <a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) </a>設定此內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5caa-448">This context handle must have been previously set using <a href="dn334015(v=exchg.10).md">JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>.</span></span> <span data-ttu-id="a5caa-449">JetGetLS 也可以用來同時提取資料指標或資料表的目前內容控制碼，並重設該內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a5caa-449">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-452"><a href="dn292179(v=exchg.10).md">JetGetObjectInfo (JET_SESID、JET_DBID、JET_OBJECTLIST) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-452"><a href="dn292179(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_OBJECTLIST)</a></span></span></td>
<td><span data-ttu-id="a5caa-453">抓取資料庫物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-453">Retrieves information about database objects.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-456"><a href="dn292178(v=exchg.10).md">JetGetObjectInfo (JET_SESID、JET_DBID、JET_objtyp、String JET_OBJECTINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-456"><a href="dn292178(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-457">抓取資料庫物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-457">Retrieves information about database objects.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-460"><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-460"><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></span></span></td>
<td><span data-ttu-id="a5caa-461">以 <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> 結構的形式，傳回目前索引中目前記錄的小數位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-461">Returns the fractional position of the current record in the current index in the form of a <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> structure.</span></span> <span data-ttu-id="a5caa-462">另請參閱 <a href="dn292207(v=exchg.10).md">JetGotoPosition (JET_SESID、JET_TABLEID JET_RECPOS) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-462">Also see <a href="dn292207(v=exchg.10).md">JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-465"><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-465"><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></span></span></td>
<td><span data-ttu-id="a5caa-466">在資料指標的目前位置，抓取次要索引項目的特殊書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-466">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="a5caa-467">然後，您可以使用這個書簽，利用 JetGotoSecondaryIndexBookmark 將該資料指標有效率地重新放置到相同的索引項目。</span><span class="sxs-lookup"><span data-stu-id="a5caa-467">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="a5caa-468">當在包含重複索引鍵或包含相同記錄之多個索引項目的次要索引上重新置放時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-468">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-471"><a href="dn292182(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、Int32、String、Int32) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-471"><a href="dn292182(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></span></span></td>
<td><span data-ttu-id="a5caa-472">取得資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="a5caa-472">Gets database configuration options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-475"><a href="dn292185(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-475"><a href="dn292185(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></span></span></td>
<td><span data-ttu-id="a5caa-476">取得資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="a5caa-476">Gets database configuration options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-479"><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、JET_COLUMNID JET_COLUMNDEF) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-479"><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></span></span></td>
<td><span data-ttu-id="a5caa-480">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-480">Retrieves information about a table column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-483"><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、字串、JET_COLUMNDEF) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-483"><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</a></span></span></td>
<td><span data-ttu-id="a5caa-484">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-484">Retrieves information about a table column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-487"><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-487"><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</a></span></span></td>
<td><span data-ttu-id="a5caa-488">抓取資料表中所有資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-488">Retrieves information about all columns in the table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-491"><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-491"><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</a></span></span></td>
<td><span data-ttu-id="a5caa-492"><strong>已淘汰。</strong></span><span class="sxs-lookup"><span data-stu-id="a5caa-492"><strong>Obsolete.</strong></span></span> <span data-ttu-id="a5caa-493">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-493">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-496"><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXID JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-496"><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-497">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-497">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-500"><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-500"><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-501">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-501">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-504"><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、Int32、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-504"><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-505">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-505">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-508"><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、字串、字串、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-508"><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-509">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-509">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-512"><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID、JET_TABLEID、String、UInt16、JET_IdxInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-512"><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-513">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-513">Retrieves information about indexes on a table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-516"><a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_DBID JET_TblInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-516"><a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-517">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-517">Retrieves various pieces of information about a table in a database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-520"><a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_OBJECTINFO JET_TblInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-520"><a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-521">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-521">Retrieves various pieces of information about a table in a database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-524"><a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-524"><a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-525">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-525">Retrieves various pieces of information about a table in a database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-528"><a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-528"><a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-529">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-529">Retrieves various pieces of information about a table in a database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-532"><a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-532"><a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a></span></span></td>
<td><span data-ttu-id="a5caa-533">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="a5caa-533">Retrieves various pieces of information about a table in a database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-536"><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-536"><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-537">在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 <a href="dn292104(v=exchg.10).md">，BeginExternalBackupGrbit) </a> 來查詢實例，以找出備份順利完成之後可安全刪除的交易記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-537">Used during a backup initiated by <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-540"><a href="dn292203(v=exchg.10).md">JetGetVersion</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-540"><a href="dn292203(v=exchg.10).md">JetGetVersion</a></span></span></td>
<td><span data-ttu-id="a5caa-541">抓取資料庫引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="a5caa-541">Retrieves the version of the database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-544"><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-544"><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></span></span></td>
<td><span data-ttu-id="a5caa-545">將游標放置在與指定書簽相關聯之記錄的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="a5caa-545">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="a5caa-546">書簽可以搭配資料表上定義的任何索引使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-546">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="a5caa-547">您可以使用 <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID、JET_TABLEID、[]、int32、int32) </a>來取出記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-547">The bookmark for a record can be retrieved using <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-550"><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-550"><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></span></span></td>
<td><span data-ttu-id="a5caa-551">將游標移至新的位置，這是透過目前索引的一小部分。</span><span class="sxs-lookup"><span data-stu-id="a5caa-551">Moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="a5caa-552">另請參閱 <a href="dn292181(v=exchg.10).md">JetGetRecordPosition (JET_SESID、JET_TABLEID JET_RECPOS) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-552">Also see <a href="dn292181(v=exchg.10).md">JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-555"><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-555"><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></span></span></td>
<td><span data-ttu-id="a5caa-556">將游標放置在與指定次要索引書簽相關聯的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="a5caa-556">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="a5caa-557">次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-557">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="a5caa-558">您可以使用 <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、[]、int32、[]、int32、GotoSecondaryIndexBookmarkGrbit) </a>，來抓取索引項目的次要索引書簽。</span><span class="sxs-lookup"><span data-stu-id="a5caa-558">The secondary index bookmark for an index entry can be retrieved using <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-561"><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-561"><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-562">擴充目前開啟之資料庫的大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-562">Extends the size of a database that is currently open.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-565"><a href="dn292208(v=exchg.10).md">JetIdle</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-565"><a href="dn292208(v=exchg.10).md">JetIdle</a></span></span></td>
<td><span data-ttu-id="a5caa-566">執行閒置清除工作或檢查 ESE 中的版本存放區狀態。</span><span class="sxs-lookup"><span data-stu-id="a5caa-566">Performs idle cleanup tasks or checks the version store status in ESE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-569"><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-569"><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></span></span></td>
<td><span data-ttu-id="a5caa-570">計算目前索引中的專案數，從目前的位置向前算。</span><span class="sxs-lookup"><span data-stu-id="a5caa-570">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="a5caa-571">目前的位置會包含在計數中。</span><span class="sxs-lookup"><span data-stu-id="a5caa-571">The current position is included in the count.</span></span> <span data-ttu-id="a5caa-572">如果目前索引超過多重值資料行，而且資料行的實例具有多個值，則計數可以大於資料表中的記錄總數。</span><span class="sxs-lookup"><span data-stu-id="a5caa-572">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="a5caa-573">如果資料表是空的，則會傳回計數的0。</span><span class="sxs-lookup"><span data-stu-id="a5caa-573">If the table is empty, then 0 will be returned for the count.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-576"><a href="dn292210(v=exchg.10).md">JetInit</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-576"><a href="dn292210(v=exchg.10).md">JetInit</a></span></span></td>
<td><span data-ttu-id="a5caa-577">初始化 ESENT 資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="a5caa-577">Initialize the ESENT database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-580"><a href="dn292214(v=exchg.10).md">JetInit2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-580"><a href="dn292214(v=exchg.10).md">JetInit2</a></span></span></td>
<td><span data-ttu-id="a5caa-581">初始化 ESENT 資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="a5caa-581">Initialize the ESENT database engine.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-584"><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-584"><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></span></span></td>
<td><span data-ttu-id="a5caa-585">計算相同資料表上不同次要索引的多個索引項目目集合之間的交集。</span><span class="sxs-lookup"><span data-stu-id="a5caa-585">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="a5caa-586">這項作業適用于在資料表中尋找符合可使用索引範圍表示之兩個或多個準則的一組記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-586">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="a5caa-587">另請參閱 <a href="dn292094(v=exchg.10).md">IntersectIndexes (JET_SESID，[] ) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-587">Also see <a href="dn292094(v=exchg.10).md">IntersectIndexes(JET_SESID, [])</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-590"><a href="dn292216(v=exchg.10).md">JetMakeKey</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-590"><a href="dn292216(v=exchg.10).md">JetMakeKey</a></span></span></td>
<td><span data-ttu-id="a5caa-591">會建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-591">Constructs search keys that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-594"><a href="dn292218(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-594"><a href="dn292218(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-595">流覽索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-595">Navigate through an index.</span></span> <span data-ttu-id="a5caa-596">資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-596">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="a5caa-597">另請參閱 <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID、JET_TABLEID) </a>、 <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID、JET_TABLEID) </a>、 <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID、JET_TABLEID) </a>、 <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID JET_TABLEID) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-597">Also see <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-600"><a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-600"><a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-601">流覽索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-601">Navigate through an index.</span></span> <span data-ttu-id="a5caa-602">資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-602">The cursor can be positioned at the start or end of the index and moved backwards and forwards by a specified number of index entries.</span></span> <span data-ttu-id="a5caa-603">另請參閱 <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID、JET_TABLEID) </a>、 <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID、JET_TABLEID) </a>、 <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID、JET_TABLEID) </a>、 <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID JET_TABLEID) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-603">Also see <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-606"><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-606"><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></span></span></td>
<td><span data-ttu-id="a5caa-607">開啟先前附加了 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a>的資料庫，以搭配資料庫會話使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-607">Opens a database previously attached with <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a>, for use with a database session.</span></span> <span data-ttu-id="a5caa-608">您可以針對相同的資料庫多次呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="a5caa-608">This function can be called multiple times for the same database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-611"><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-611"><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-612">開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。</span><span class="sxs-lookup"><span data-stu-id="a5caa-612">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="a5caa-613">之後可以使用 JetReadFileInstance，透過傳回的控制碼讀取這些檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-613">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="a5caa-614">傳回的控制碼必須使用 JetCloseFileInstance 來關閉。</span><span class="sxs-lookup"><span data-stu-id="a5caa-614">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="a5caa-615">實例的外部備份必須先前已使用 JetBeginExternalBackupInstance 起始。</span><span class="sxs-lookup"><span data-stu-id="a5caa-615">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-618"><a href="dn292234(v=exchg.10).md">JetOpenTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-618"><a href="dn292234(v=exchg.10).md">JetOpenTable</a></span></span></td>
<td><span data-ttu-id="a5caa-619">在先前建立的資料表上開啟資料指標。</span><span class="sxs-lookup"><span data-stu-id="a5caa-619">Opens a cursor on a previously created table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-622"><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-622"><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></span></span></td>
<td><span data-ttu-id="a5caa-623">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-623">Creates a temporary table with a single index.</span></span> <span data-ttu-id="a5caa-624">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="a5caa-624">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="a5caa-625">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="a5caa-625">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a5caa-626">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="a5caa-626">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="a5caa-627">另請參閱 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-627">Also see <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="a5caa-628"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-628"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-631"><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-631"><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></span></span></td>
<td><span data-ttu-id="a5caa-632">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-632">Creates a temporary table with a single index.</span></span> <span data-ttu-id="a5caa-633">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="a5caa-633">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="a5caa-634">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="a5caa-634">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a5caa-635">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="a5caa-635">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="a5caa-636">另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID、[]、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、[] ) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-636">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="a5caa-637"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-637"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-640"><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-640"><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></span></span></td>
<td><span data-ttu-id="a5caa-641">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-641">Creates a temporary table with a single index.</span></span> <span data-ttu-id="a5caa-642">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="a5caa-642">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="a5caa-643">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="a5caa-643">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a5caa-644">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="a5caa-644">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="a5caa-645">另請參閱 <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID、[]、Int32、TempTableGrbit、JET_TABLEID、[] ) </a>、 <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-645">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-648"><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-648"><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></span></span></td>
<td><span data-ttu-id="a5caa-649">啟動快照集。</span><span class="sxs-lookup"><span data-stu-id="a5caa-649">Starts a snapshot.</span></span> <span data-ttu-id="a5caa-650">當快照集進行中時，引擎無法進行寫入磁片的活動。</span><span class="sxs-lookup"><span data-stu-id="a5caa-650">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-653"><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-653"><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></span></span></td>
<td><span data-ttu-id="a5caa-654">開始快照集會話的準備工作。</span><span class="sxs-lookup"><span data-stu-id="a5caa-654">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="a5caa-655">快照集會話是一個短暫的時間間隔，在此時間間隔中，引擎不會將任何寫入 Io 發出至磁片，因此引擎可以在由快照寫入器驅動) 時，參與磁片區快照集會話 (。</span><span class="sxs-lookup"><span data-stu-id="a5caa-655">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-658"><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-658"><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></span></span></td>
<td><span data-ttu-id="a5caa-659">通知引擎可在凍結期間之後繼續正常 IO 作業，以及成功的快照集。</span><span class="sxs-lookup"><span data-stu-id="a5caa-659">Notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-662"><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-662"><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></span></span></td>
<td><span data-ttu-id="a5caa-663">準備資料指標進行更新。</span><span class="sxs-lookup"><span data-stu-id="a5caa-663">Prepare a cursor for update.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-666"><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-666"><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-667">抓取以 <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) </a>開啟的檔案內容。</span><span class="sxs-lookup"><span data-stu-id="a5caa-667">Retrieves the contents of a file opened with <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-670"><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-670"><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></span></span></td>
<td><span data-ttu-id="a5caa-671">允許應用程式將資料庫引擎設定為對應用程式發出特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="a5caa-671">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="a5caa-672">這些通知會與特定的資料表相關聯，而且只有在包含該資料表的實例使用 <a href="dn334020(v=exchg.10).md">JetTerm (JET_INSTANCE) </a>關閉時，才會維持有效狀態。</span><span class="sxs-lookup"><span data-stu-id="a5caa-672">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using <a href="dn334020(v=exchg.10).md">JetTerm(JET_INSTANCE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-675"><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-675"><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></span></span></td>
<td><span data-ttu-id="a5caa-676">變更現有資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-676">Changes the name of an existing column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-679"><a href="dn332993(v=exchg.10).md">JetRenameTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-679"><a href="dn332993(v=exchg.10).md">JetRenameTable</a></span></span></td>
<td><span data-ttu-id="a5caa-680">變更現有資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5caa-680">Changes the name of an existing table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-683"><a href="dn332991(v=exchg.10).md">JetResetSessionCoNtext</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-683"><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></span></span></td>
<td><span data-ttu-id="a5caa-684">解除會話與目前線程之間的之間的解除。</span><span class="sxs-lookup"><span data-stu-id="a5caa-684">Disassociates a session from the current thread.</span></span> <span data-ttu-id="a5caa-685">這應該與 <a href="dn334027(v=exchg.10).md">JetSetSessionCoNtext (JET_SESID、IntPtr) </a>一起使用。</span><span class="sxs-lookup"><span data-stu-id="a5caa-685">This should be used in conjunction with <a href="dn334027(v=exchg.10).md">JetSetSessionContext(JET_SESID, IntPtr)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-688"><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-688"><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></span></span></td>
<td><span data-ttu-id="a5caa-689">通知資料庫引擎應用程式不再掃描游標所在的整個索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-689">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="a5caa-690">此呼叫會反轉 <a href="dn334018(v=exchg.10).md">JetSetTableSequential (JET_SESID、JET_TABLEID、SetTableSequentialGrbit) </a>所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="a5caa-690">This call reverses a notification sent by <a href="dn334018(v=exchg.10).md">JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-693"><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-693"><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-694">還原和復原實例（包括所有附加的資料庫）的資料流程備份。</span><span class="sxs-lookup"><span data-stu-id="a5caa-694">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="a5caa-695">它是設計來搭配使用 <a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) </a> 函數所建立的備份。</span><span class="sxs-lookup"><span data-stu-id="a5caa-695">It is designed to work with a backup created with the <a href="dn292102(v=exchg.10).md">JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)</a> function.</span></span> <span data-ttu-id="a5caa-696">這是最簡單且最具封裝的還原功能。</span><span class="sxs-lookup"><span data-stu-id="a5caa-696">This is the simplest and most encapsulated restore function.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-699"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-699"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-700">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-700">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-701">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-701">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-702">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-702">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a5caa-703">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-703">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a5caa-704">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-704">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-707"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID，JET_TABLEID，JET_COLUMNID，[]，Int32，Int32，Int32，RetrieveColumnGrbit，JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-707"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-708">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-708">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-709">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-709">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-710">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-710">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a5caa-711">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-711">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a5caa-712">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-712">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-715"><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-715"><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></span></span></td>
<td><span data-ttu-id="a5caa-716">從單一作業中的目前記錄抓取多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-716">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="a5caa-717">JET_RETRIEVECOLUMN 結構的陣列用來描述要抓取的資料行值集合，以及描述要抓取之每個資料行值的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a5caa-717">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-720"><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-720"><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></span></span></td>
<td><span data-ttu-id="a5caa-721">在資料指標的目前位置，抓取索引項目的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-721">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="a5caa-722">另請參閱 <a href="dn334085(v=exchg.10).md">RetrieveKey (JET_SESID、JET_TABLEID、RetrieveKeyGrbit) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-722">Also see <a href="dn334085(v=exchg.10).md">RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-725"><a href="dn334001(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-725"><a href="dn334001(v=exchg.10).md">JetRollback</a></span></span></td>
<td><span data-ttu-id="a5caa-726">復原對資料庫狀態所做的變更，並返回到最後一個儲存點。</span><span class="sxs-lookup"><span data-stu-id="a5caa-726">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="a5caa-727">JetRollback 也會關閉儲存點期間開啟的任何資料指標。</span><span class="sxs-lookup"><span data-stu-id="a5caa-727">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="a5caa-728">如果最外層的儲存點復原，會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="a5caa-728">If the outermost save point is undone, the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-731"><a href="dn334003(v=exchg.10).md">JetSeek</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-731"><a href="dn334003(v=exchg.10).md">JetSeek</a></span></span></td>
<td><span data-ttu-id="a5caa-732">有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="a5caa-732">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="a5caa-733">您先前必須使用 <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID、JET_TABLEID、[]、Int32、MakeKeyGrbit) </a>來建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-733">A search key must have been previously constructed using <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>.</span></span> <span data-ttu-id="a5caa-734">另請參閱 <a href="dn334145(v=exchg.10).md">TrySeek (JET_SESID、JET_TABLEID、SeekGrbit) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-734">Also see <a href="dn334145(v=exchg.10).md">TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-737"><a href="dn334009(v=exchg.10).md">JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、SetColumnGrbit、JET_SETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-737"><a href="dn334009(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-738">JetSetColumn 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-738">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="a5caa-739">它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a>) 類型資料行的完整或部分 long (值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-739">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-742"><a href="dn334008(v=exchg.10).md">JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、Int32、SetColumnGrbit、JET_SETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-742"><a href="dn334008(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-743">JetSetColumn 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-743">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="a5caa-744">它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新 <a href="hh577895(v=exchg.10).md">LongText</a> 或 <a href="hh577895(v=exchg.10).md">LongBinary</a>) 類型資料行的完整或部分 long (值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-744">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a>).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-747"><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-747"><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></span></span></td>
<td><span data-ttu-id="a5caa-748">變更現有資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-748">Changes the default value of an existing column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-751"><a href="dn334006(v=exchg.10).md">JetSetColumns</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-751"><a href="dn334006(v=exchg.10).md">JetSetColumns</a></span></span></td>
<td><span data-ttu-id="a5caa-752">允許應用程式在單一作業中設定多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-752">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="a5caa-753"><a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a>結構的陣列用來描述要設定的資料行值集合，以及描述要設定之每個資料行值的輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a5caa-753">An array of <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-756"><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-756"><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></span></span></td>
<td><span data-ttu-id="a5caa-757">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-757">Set the current index of a cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-760"><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-760"><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></span></span></td>
<td><span data-ttu-id="a5caa-761">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-761">Set the current index of a cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-764"><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-764"><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></span></span></td>
<td><span data-ttu-id="a5caa-765">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-765">Set the current index of a cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-768"><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-768"><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></span></span></td>
<td><span data-ttu-id="a5caa-769">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-769">Set the current index of a cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-772"><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-772"><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></span></span></td>
<td><span data-ttu-id="a5caa-773">設定未開啟之資料庫檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-773">Sets the size of an unopened database file.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-776"><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-776"><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></span></span></td>
<td><span data-ttu-id="a5caa-777">暫時限制資料指標可以使用 <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID、JET_TABLEID、Int32、MoveGrbit) </a> 的索引項目集合，以從目前索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定的搜尋準則和指定的系結準則的索引項目目結束。</span><span class="sxs-lookup"><span data-stu-id="a5caa-777">Temporarily limits the set of index entries that the cursor can walk using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="a5caa-778">您先前必須使用 <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID、JET_TABLEID、[]、Int32、MakeKeyGrbit) </a>來建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-778">A search key must have been previously constructed using <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>.</span></span> <span data-ttu-id="a5caa-779">另請參閱 <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-779">Also see <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-782"><a href="dn334015(v=exchg.10).md">JetSetLS</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-782"><a href="dn334015(v=exchg.10).md">JetSetLS</a></span></span></td>
<td><span data-ttu-id="a5caa-783">讓應用程式將稱為本機儲存的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a5caa-783">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="a5caa-784">應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-784">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="a5caa-785">當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。</span><span class="sxs-lookup"><span data-stu-id="a5caa-785">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="a5caa-786">這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a5caa-786">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-789"><a href="dn334027(v=exchg.10).md">JetSetSessionCoNtext</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-789"><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></span></span></td>
<td><span data-ttu-id="a5caa-790">使用指定的內容控制碼，將會話與目前的執行緒產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a5caa-790">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="a5caa-791">此關聯會覆寫指定會話的交易必須完全在相同執行緒上執行的預設引擎需求。</span><span class="sxs-lookup"><span data-stu-id="a5caa-791">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="a5caa-792">使用 <a href="dn332991(v=exchg.10).md">JetResetSessionCoNtext (JET_SESID) </a> 來移除關聯。</span><span class="sxs-lookup"><span data-stu-id="a5caa-792">Use <a href="dn332991(v=exchg.10).md">JetResetSessionContext(JET_SESID)</a> to remove the association.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-795"><a href="dn334028(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、JET_CALLBACK、字串) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-795"><a href="dn334028(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</a></span></span></td>
<td><span data-ttu-id="a5caa-796">設定資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="a5caa-796">Sets database configuration options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-799"><a href="dn334017(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、Int32、String) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-799"><a href="dn334017(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></span></span></td>
<td><span data-ttu-id="a5caa-800">設定資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="a5caa-800">Sets database configuration options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-803"><a href="dn334029(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-803"><a href="dn334029(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></span></span></td>
<td><span data-ttu-id="a5caa-804">設定資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="a5caa-804">Sets database configuration options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-807"><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-807"><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></span></span></td>
<td><span data-ttu-id="a5caa-808">通知資料庫引擎應用程式正在掃描資料指標所在的整個索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-808">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="a5caa-809">因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。</span><span class="sxs-lookup"><span data-stu-id="a5caa-809">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="a5caa-810">另請參閱 <a href="dn332994(v=exchg.10).md">JetResetTableSequential (JET_SESID、JET_TABLEID、ResetTableSequentialGrbit) </a>。</span><span class="sxs-lookup"><span data-stu-id="a5caa-810">Also see <a href="dn332994(v=exchg.10).md">JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-813"><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-813"><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-814">防止串流備份相關的活動在特定執行中的實例上繼續執行，因此以可預測的方式結束資料流程備份。</span><span class="sxs-lookup"><span data-stu-id="a5caa-814">Prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-817"><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-817"><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-818">準備實例以進行終止。</span><span class="sxs-lookup"><span data-stu-id="a5caa-818">Prepares an instance for termination.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-821"><a href="dn334020(v=exchg.10).md">JetTerm</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-821"><a href="dn334020(v=exchg.10).md">JetTerm</a></span></span></td>
<td><span data-ttu-id="a5caa-822">終止以 <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 或 <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE、String) </a>建立的實例。</span><span class="sxs-lookup"><span data-stu-id="a5caa-822">Terminate an instance that was created with <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> or <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-825"><a href="dn334037(v=exchg.10).md">JetTerm2</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-825"><a href="dn334037(v=exchg.10).md">JetTerm2</a></span></span></td>
<td><span data-ttu-id="a5caa-826">終止以 <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 或 <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE、String) </a>建立的實例。</span><span class="sxs-lookup"><span data-stu-id="a5caa-826">Terminate an instance that was created with <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> or <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-829"><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-829"><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></span></span></td>
<td><span data-ttu-id="a5caa-830">在 JetBeginExternalBackup 所起始的備份期間，用來刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a5caa-830">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-833"><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-833"><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></span></span></td>
<td><span data-ttu-id="a5caa-834">設定 database engine，以停止在先前透過 <a href="dn332989(v=exchg.10).md">JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE) </a>要求的情況下發出通知至應用程式。</span><span class="sxs-lookup"><span data-stu-id="a5caa-834">Configures the database engine to stop issuing notifications to the application as previously requested through <a href="dn332989(v=exchg.10).md">JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-837"><a href="dn334036(v=exchg.10).md">JetUpdate (JET_SESID JET_TABLEID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-837"><a href="dn334036(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="a5caa-838">JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="a5caa-838">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="a5caa-839">藉由呼叫 <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID JET_TABLEID) </a>來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="a5caa-839">Deleting a table row is performed by calling <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-842"><a href="dn334023(v=exchg.10).md">JetUpdate (JET_SESID、JET_TABLEID、[]、Int32、Int32) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-842"><a href="dn334023(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID, [], Int32, Int32)</a></span></span></td>
<td><span data-ttu-id="a5caa-843">JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="a5caa-843">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="a5caa-844">藉由呼叫 <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID JET_TABLEID) </a>來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="a5caa-844">Deleting a table row is performed by calling <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-847"><a href="dn334042(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、布林值、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-847"><a href="dn334042(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-848">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-848">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-851"><a href="dn334026(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Byte、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-851"><a href="dn334026(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-852">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-852">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-855"><a href="dn334044(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、[]、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-855"><a href="dn334044(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-856">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-856">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-859"><a href="dn334025(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、DateTime、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-859"><a href="dn334025(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-860">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-860">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-863"><a href="dn334046(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Double、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-863"><a href="dn334046(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-864">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-864">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-867"><a href="dn334030(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Guid、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-867"><a href="dn334030(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-868">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-868">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-871"><a href="dn334048(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int16、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-871"><a href="dn334048(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-872">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-872">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-875"><a href="dn334031(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int32、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-875"><a href="dn334031(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-876">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-876">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-879"><a href="dn334050(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Int64、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-879"><a href="dn334050(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-880">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-880">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-883"><a href="dn334033(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、Single、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-883"><a href="dn334033(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-884">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-884">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-887"><a href="dn334052(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt16、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-887"><a href="dn334052(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-888">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-888">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-891"><a href="dn334054(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt32、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-891"><a href="dn334054(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-892">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-892">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-895"><a href="dn334034(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、UInt64、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-895"><a href="dn334034(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-896">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-896">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-899"><a href="dn334038(v=exchg.10).md">MakeKey (JET_SESID、JET_TABLEID、字串、編碼、MakeKeyGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-899"><a href="dn334038(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-900">建立可供 <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID、JET_TABLEID、SeekGrbit) </a> 和 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>使用的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-900">Constructs a search key that may then be used by <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> and <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-903"><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-903"><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></span></span></td>
<td><span data-ttu-id="a5caa-904">將游標放在資料表中的最後一筆記錄之後。</span><span class="sxs-lookup"><span data-stu-id="a5caa-904">Position the cursor after the last record in the table.</span></span> <span data-ttu-id="a5caa-905">接下來的移動會將游標放在最後一筆記錄上。</span><span class="sxs-lookup"><span data-stu-id="a5caa-905">A subsequent move previous will position the cursor on the last record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-908"><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-908"><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></span></span></td>
<td><span data-ttu-id="a5caa-909">將游標放在資料表的第一筆記錄之前。</span><span class="sxs-lookup"><span data-stu-id="a5caa-909">Position the cursor before the first record in the table.</span></span> <span data-ttu-id="a5caa-910">接下來的移動會將游標放在第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-910">A subsequent move next will position the cursor on the first record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-913"><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-913"><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></span></span></td>
<td><span data-ttu-id="a5caa-914">移除以 <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a> 或 <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) </a>建立的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="a5caa-914">Removes an index range created with <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> or <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</span></span> <span data-ttu-id="a5caa-915">如果沒有索引範圍存在，這個方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a5caa-915">If no index range is present this method does nothing.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-918"><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-918"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-919">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-919">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-920">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-920">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-923"><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-923"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="a5caa-924">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-924">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-925">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-925">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-926">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-926">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a5caa-927">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-927">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="a5caa-928">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-928">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-931"><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-931"><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-932">從目前的記錄抓取布林資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-932">Retrieves a boolean column value from the current record.</span></span> <span data-ttu-id="a5caa-933">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-933">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-936"><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-936"><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-937">從目前的記錄抓取布林資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-937">Retrieves a boolean column value from the current record.</span></span> <span data-ttu-id="a5caa-938">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-938">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-941"><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-941"><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-942">從目前的記錄抓取位元組資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-942">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="a5caa-943">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-943">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-946"><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-946"><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-947">從目前的記錄抓取位元組資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-947">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="a5caa-948">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-948">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-951"><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-951"><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-952">從目前的記錄抓取 datetime 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-952">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="a5caa-953">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-953">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-956"><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-956"><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-957">從目前的記錄抓取 datetime 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-957">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="a5caa-958">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-958">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-961"><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-961"><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-962">從目前的記錄抓取雙資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-962">Retrieves a double column value from the current record.</span></span> <span data-ttu-id="a5caa-963">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-963">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-966"><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-966"><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-967">從目前的記錄抓取雙資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-967">Retrieves a double column value from the current record.</span></span> <span data-ttu-id="a5caa-968">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-968">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-971"><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-971"><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-972">從目前的記錄抓取 float 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-972">Retrieves a float column value from the current record.</span></span> <span data-ttu-id="a5caa-973">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-973">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-976"><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-976"><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-977">從目前的記錄抓取 float 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-977">Retrieves a float column value from the current record.</span></span> <span data-ttu-id="a5caa-978">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-978">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-981"><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-981"><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-982">從目前的記錄抓取 guid 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-982">Retrieves a guid column value from the current record.</span></span> <span data-ttu-id="a5caa-983">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-983">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-986"><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-986"><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-987">從目前的記錄抓取 guid 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-987">Retrieves a guid column value from the current record.</span></span> <span data-ttu-id="a5caa-988">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-988">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-991"><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-991"><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-992">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-992">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-993">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-993">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-996"><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-996"><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-997">從目前的記錄抓取 int16 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-997">Retrieves an int16 column value from the current record.</span></span> <span data-ttu-id="a5caa-998">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-998">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1001"><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1001"><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1002">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1002">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1003">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1003">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1006"><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1006"><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1007">從目前的記錄抓取 int32 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1007">Retrieves an int32 column value from the current record.</span></span> <span data-ttu-id="a5caa-1008">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1008">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1011"><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1011"><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1012">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1012">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1013">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1013">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1016"><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1016"><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1017">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1017">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1018">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1018">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1021"><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1021"><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1022">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1022">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1023">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1023">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-1024">使用 Unicode 編碼。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1024">The Unicode encoding is used.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1027"><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1027"><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</a></span></span></td>
<td><span data-ttu-id="a5caa-1028">從目前的記錄抓取字串資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1028">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="a5caa-1029">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1029">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1032"><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1032"><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1033">從目前的記錄抓取字串資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1033">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="a5caa-1034">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1034">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1037"><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1037"><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1038">從目前的記錄抓取 uint16 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1038">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="a5caa-1039">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1039">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1042"><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1042"><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1043">從目前的記錄抓取 uint16 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1043">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="a5caa-1044">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1044">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1047"><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1047"><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1048">從目前的記錄抓取 uint32 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1048">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="a5caa-1049">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1049">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1052"><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1052"><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1053">從目前的記錄抓取 uint32 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1053">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="a5caa-1054">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1054">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1057"><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1057"><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1058">從目前的記錄抓取 uint64 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1058">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="a5caa-1059">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1059">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1062"><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1062"><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1063">從目前的記錄抓取 uint64 資料行值。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1063">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="a5caa-1064">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1064">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1067"><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1067"><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></span></span></td>
<td><span data-ttu-id="a5caa-1068">將資料行抓取 ColumnValue 物件。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1068">Retrieves columns into ColumnValue objects.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1071"><a href="dn334076(v=exchg.10).md">RetrieveColumnSize (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1071"><a href="dn334076(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="a5caa-1072">從目前的記錄抓取單一資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1072">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1073">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1073">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-1074">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1074">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a5caa-1075">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1075">This function can also retrieve column data from an index entry that references the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1078"><a href="dn334117(v=exchg.10).md">RetrieveColumnSize (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32、RetrieveColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1078"><a href="dn334117(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1079">從目前的記錄抓取單一資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1079">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="a5caa-1080">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1080">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="a5caa-1081">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1081">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="a5caa-1082">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1082">This function can also retrieve column data from an index entry that references the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1085"><a href="dn334085(v=exchg.10).md">RetrieveKey</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1085"><a href="dn334085(v=exchg.10).md">RetrieveKey</a></span></span></td>
<td><span data-ttu-id="a5caa-1086">在資料指標的目前位置，抓取索引項目的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1086">Retrieves the key for the index entry at the current position of a cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1089"><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1089"><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></span></span></td>
<td><span data-ttu-id="a5caa-1090">將物件的序列化形式寫入資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1090">Write a serialized form of an object to a column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1093"><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Boolean) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1093"><a href="dn334123(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)</a></span></span></td>
<td><span data-ttu-id="a5caa-1094">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1094">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1097"><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1097"><a href="dn334080(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></span></span></td>
<td><span data-ttu-id="a5caa-1098">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1098">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1101"><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[] ) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1101"><a href="dn334121(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></span></span></td>
<td><span data-ttu-id="a5caa-1102">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1102">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1105"><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、DateTime) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1105"><a href="dn334082(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></span></span></td>
<td><span data-ttu-id="a5caa-1106">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1106">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1109"><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Double) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1109"><a href="dn334125(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></span></span></td>
<td><span data-ttu-id="a5caa-1110">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1110">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1113"><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Guid) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1113"><a href="dn334081(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</a></span></span></td>
<td><span data-ttu-id="a5caa-1114">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1114">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1117"><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int16) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1117"><a href="dn334127(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></span></span></td>
<td><span data-ttu-id="a5caa-1118">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1118">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1121"><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1121"><a href="dn334083(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></span></span></td>
<td><span data-ttu-id="a5caa-1122">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1122">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1125"><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、Int64) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1125"><a href="dn334130(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></span></span></td>
<td><span data-ttu-id="a5caa-1126">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1126">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1129"><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、單一) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1129"><a href="dn334087(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</a></span></span></td>
<td><span data-ttu-id="a5caa-1130">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1130">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1133"><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt16) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1133"><a href="dn334132(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></span></span></td>
<td><span data-ttu-id="a5caa-1134">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1134">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1137"><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt32) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1137"><a href="dn334086(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></span></span></td>
<td><span data-ttu-id="a5caa-1138">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1138">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1141"><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt64) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1141"><a href="dn334135(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></span></span></td>
<td><span data-ttu-id="a5caa-1142">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1142">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1145"><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、SetColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1145"><a href="dn334089(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1146">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1146">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1149"><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1149"><a href="dn334136(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</a></span></span></td>
<td><span data-ttu-id="a5caa-1150">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1150">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1153"><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、字串、編碼、SetColumnGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1153"><a href="dn334090(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)</a></span></span></td>
<td><span data-ttu-id="a5caa-1154">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1154">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1157"><a href="dn334138(v=exchg.10).md">SetColumns</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1157"><a href="dn334138(v=exchg.10).md">SetColumns</a></span></span></td>
<td><span data-ttu-id="a5caa-1158">設定 ColumnValue 物件中的資料行。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1158">Sets columns from ColumnValue objects.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1161"><a href="dn334139(v=exchg.10).md">TryGetLock</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1161"><a href="dn334139(v=exchg.10).md">TryGetLock</a></span></span></td>
<td><span data-ttu-id="a5caa-1162">明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1162">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="a5caa-1163">一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1163">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="a5caa-1164">由於記錄版本控制，通常不需要讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1164">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="a5caa-1165">不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1165">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1168"><a href="dn334094(v=exchg.10).md">TryMove</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1168"><a href="dn334094(v=exchg.10).md">TryMove</a></span></span></td>
<td><span data-ttu-id="a5caa-1169">嘗試流覽索引。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1169">Try to navigate through an index.</span></span> <span data-ttu-id="a5caa-1170">如果流覽成功，這個方法會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1170">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="a5caa-1171">如果沒有任何記錄可流覽此方法，則會傳回 false;將會擲回例外狀況，以找出其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1171">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1174"><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1174"><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></span></span></td>
<td><span data-ttu-id="a5caa-1175">請嘗試移至資料表中的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1175">Try to move to the first record in the table.</span></span> <span data-ttu-id="a5caa-1176">如果資料表是空的，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1176">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1179"><a href="dn334140(v=exchg.10).md">TryMoveLast</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1179"><a href="dn334140(v=exchg.10).md">TryMoveLast</a></span></span></td>
<td><span data-ttu-id="a5caa-1180">請嘗試移至資料表中的最後一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1180">Try to move to the last record in the table.</span></span> <span data-ttu-id="a5caa-1181">如果資料表是空的，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1181">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1184"><a href="dn334095(v=exchg.10).md">TryMoveNext</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1184"><a href="dn334095(v=exchg.10).md">TryMoveNext</a></span></span></td>
<td><span data-ttu-id="a5caa-1185">請嘗試移至資料表中的下一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1185">Try to move to the next record in the table.</span></span> <span data-ttu-id="a5caa-1186">如果沒有下一個記錄，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1186">If there is not a next record this returns false, if a different error is encountered an exception is thrown.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1189"><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1189"><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></span></span></td>
<td><span data-ttu-id="a5caa-1190">請嘗試移至資料表中的上一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1190">Try to move to the previous record in the table.</span></span> <span data-ttu-id="a5caa-1191">如果沒有先前的記錄，則會傳回 false，如果發生不同的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1191">If there is not a previous record this returns false, if a different error is encountered an exception is thrown.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1194"><a href="dn334096(v=exchg.10).md">TryOpenTable</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1194"><a href="dn334096(v=exchg.10).md">TryOpenTable</a></span></span></td>
<td><span data-ttu-id="a5caa-1195">嘗試開啟資料表。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1195">Try to open a table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1198"><a href="dn334145(v=exchg.10).md">TrySeek</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1198"><a href="dn334145(v=exchg.10).md">TrySeek</a></span></span></td>
<td><span data-ttu-id="a5caa-1199">有效率地將游標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1199">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="a5caa-1200">搜尋金鑰必須先前已使用 JetMakeKey 來建立。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1200">A search key must have been previously constructed using JetMakeKey.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5caa-1203"><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></span><span class="sxs-lookup"><span data-stu-id="a5caa-1203"><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></span></span></td>
<td><span data-ttu-id="a5caa-1204">暫時限制索引項目的索引項目集合，其可使用 JetMove 從目前的索引項目目開始，然後在符合該資料指標中搜尋索引鍵所指定之搜尋準則的索引項目目和指定的系結準則中結束。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1204">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="a5caa-1205">搜尋金鑰必須先前已使用 JetMakeKey 來建立。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1205">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="a5caa-1206">如果索引範圍不是空的，則傳回 true，否則傳回 false。</span><span class="sxs-lookup"><span data-stu-id="a5caa-1206">Returns true if the index range is non-empty, false otherwise.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5caa-1207">頁首</span><span class="sxs-lookup"><span data-stu-id="a5caa-1207">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a5caa-1208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5caa-1208">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5caa-1209">參考</span><span class="sxs-lookup"><span data-stu-id="a5caa-1209">Reference</span></span>

[<span data-ttu-id="a5caa-1210">Api 類別</span><span class="sxs-lookup"><span data-stu-id="a5caa-1210">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a5caa-1211">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a5caa-1211">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
