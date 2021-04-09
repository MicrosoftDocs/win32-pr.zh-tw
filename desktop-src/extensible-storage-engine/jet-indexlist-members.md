---
description: 深入瞭解： JET_INDEXLIST 成員
title: JET_INDEXLIST 成員
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027304"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="eca99-103">JET_INDEXLIST 成員</span><span class="sxs-lookup"><span data-stu-id="eca99-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="eca99-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="eca99-104">Include protected members</span></span>  
<span data-ttu-id="eca99-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="eca99-105">Include inherited members</span></span>  

<span data-ttu-id="eca99-106">臨時表的相關資訊，其中包含指定資料表之所有索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eca99-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="eca99-107">[JET_INDEXLIST](./jet-indexlist-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="eca99-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="eca99-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="eca99-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eca99-109">名稱</span><span class="sxs-lookup"><span data-stu-id="eca99-109">Name</span></span></th>
<th><span data-ttu-id="eca99-110">描述</span><span class="sxs-lookup"><span data-stu-id="eca99-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="eca99-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="eca99-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eca99-113">頁首</span><span class="sxs-lookup"><span data-stu-id="eca99-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="eca99-114">屬性</span><span class="sxs-lookup"><span data-stu-id="eca99-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eca99-115">名稱</span><span class="sxs-lookup"><span data-stu-id="eca99-115">Name</span></span></th>
<th><span data-ttu-id="eca99-116">描述</span><span class="sxs-lookup"><span data-stu-id="eca99-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="eca99-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="eca99-119">取得臨時表中的資料行 columnid，此資料表會儲存索引鍵中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="eca99-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="eca99-120">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="eca99-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="eca99-123">取得臨時表中的資料行 columnid，此資料表會儲存索引中的專案數。</span><span class="sxs-lookup"><span data-stu-id="eca99-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="eca99-124">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="eca99-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="eca99-125">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="eca99-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="eca99-128">取得臨時表中的資料行 columnid，此資料表會儲存索引中唯一索引鍵的數目。</span><span class="sxs-lookup"><span data-stu-id="eca99-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="eca99-129">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="eca99-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="eca99-130">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="eca99-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="eca99-133">取得臨時表中資料行的 columnid，該資料表會儲存正在編制索引之資料行的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="eca99-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="eca99-134">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="eca99-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="eca99-137">取得臨時表中的資料行 columnid，此資料表會儲存正在編制索引之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="eca99-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="eca99-138">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="eca99-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="eca99-141">取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。</span><span class="sxs-lookup"><span data-stu-id="eca99-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="eca99-142">請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="eca99-143">資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="eca99-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="eca99-146">取得臨時表中的資料行 columnid，此資料表會儲存已編制索引之資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="eca99-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="eca99-147">資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="eca99-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="eca99-150">取得臨時表中的資料行 columnid，此資料表會儲存索引中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="eca99-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="eca99-151">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="eca99-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="eca99-152">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="eca99-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="eca99-155">取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。</span><span class="sxs-lookup"><span data-stu-id="eca99-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="eca99-156">請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="eca99-157">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="eca99-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="eca99-160">取得臨時表中的資料行 columnid，此資料表會儲存用於索引的 grbits。</span><span class="sxs-lookup"><span data-stu-id="eca99-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="eca99-161">請參閱 <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="eca99-162">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="eca99-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="eca99-165">取得臨時表中的資料行 columnid，此資料表會將此資料行的索引儲存在索引鍵中。</span><span class="sxs-lookup"><span data-stu-id="eca99-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="eca99-166">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="eca99-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="eca99-169">取得臨時表中儲存索引名稱之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="eca99-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="eca99-170">資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="eca99-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="eca99-173">取得臨時表中的資料行 columnid，此資料表會儲存索引的語言識別項 (LCID) 。</span><span class="sxs-lookup"><span data-stu-id="eca99-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="eca99-174">資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="eca99-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="eca99-177">取得臨時表中的資料行 columnid，此資料表會儲存索引的 unicode 正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="eca99-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="eca99-178">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="eca99-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="eca99-181">取得臨時表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="eca99-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="eca99-183"><a href="dn335174(v=exchg.10).md">tableid</a></span><span class="sxs-lookup"><span data-stu-id="eca99-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="eca99-184">取得臨時表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="eca99-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="eca99-185">當不再需要資料表時，這應該會關閉。</span><span class="sxs-lookup"><span data-stu-id="eca99-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eca99-186">頁首</span><span class="sxs-lookup"><span data-stu-id="eca99-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="eca99-187">方法</span><span class="sxs-lookup"><span data-stu-id="eca99-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eca99-188">名稱</span><span class="sxs-lookup"><span data-stu-id="eca99-188">Name</span></span></th>
<th><span data-ttu-id="eca99-189">描述</span><span class="sxs-lookup"><span data-stu-id="eca99-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="eca99-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="eca99-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="eca99-192"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="eca99-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="eca99-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="eca99-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="eca99-195"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="eca99-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="eca99-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="eca99-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="eca99-198"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="eca99-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="eca99-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="eca99-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="eca99-201"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="eca99-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="eca99-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="eca99-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="eca99-204"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="eca99-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="eca99-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="eca99-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="eca99-207">傳回表示目前<a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="eca99-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="eca99-208"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="eca99-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eca99-209">頁首</span><span class="sxs-lookup"><span data-stu-id="eca99-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="eca99-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eca99-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eca99-211">參考</span><span class="sxs-lookup"><span data-stu-id="eca99-211">Reference</span></span>

[<span data-ttu-id="eca99-212">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="eca99-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="eca99-213">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="eca99-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
