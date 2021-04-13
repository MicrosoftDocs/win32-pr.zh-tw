---
description: 深入瞭解： JET_INDEXLIST 屬性
title: JET_INDEXLIST 屬性
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568697"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="2f0cd-103">JET_INDEXLIST 屬性</span><span class="sxs-lookup"><span data-stu-id="2f0cd-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="2f0cd-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="2f0cd-104">Include protected members</span></span>  
<span data-ttu-id="2f0cd-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="2f0cd-105">Include inherited members</span></span>  

<span data-ttu-id="2f0cd-106">[JET_INDEXLIST](./jet-indexlist-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="2f0cd-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2f0cd-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2f0cd-108">名稱</span><span class="sxs-lookup"><span data-stu-id="2f0cd-108">Name</span></span></th>
<th><span data-ttu-id="2f0cd-109">描述</span><span class="sxs-lookup"><span data-stu-id="2f0cd-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="2f0cd-112">取得臨時表中的資料行 columnid，此資料表會儲存索引鍵中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="2f0cd-113">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="2f0cd-116">取得臨時表中的資料行 columnid，此資料表會儲存索引中的專案數。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="2f0cd-117">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="2f0cd-118">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="2f0cd-121">取得臨時表中的資料行 columnid，此資料表會儲存索引中唯一索引鍵的數目。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="2f0cd-122">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="2f0cd-123">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="2f0cd-126">取得臨時表中資料行的 columnid，該資料表會儲存正在編制索引之資料行的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="2f0cd-127">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="2f0cd-130">取得臨時表中的資料行 columnid，此資料表會儲存正在編制索引之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="2f0cd-131">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="2f0cd-134">取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="2f0cd-135">請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="2f0cd-136">資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="2f0cd-139">取得臨時表中的資料行 columnid，此資料表會儲存已編制索引之資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="2f0cd-140">資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="2f0cd-143">取得臨時表中的資料行 columnid，此資料表會儲存索引中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="2f0cd-144">此值不是最新值，而且只會由 &quot; JetComputeStats 更新 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="2f0cd-145">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="2f0cd-148">取得臨時表中的資料行 columnid，此資料表會儲存套用至索引資料行的 grbit。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="2f0cd-149">請參閱 <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="2f0cd-150">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="2f0cd-153">取得臨時表中的資料行 columnid，此資料表會儲存用於索引的 grbits。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="2f0cd-154">請參閱 <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="2f0cd-155">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="2f0cd-158">取得臨時表中的資料行 columnid，此資料表會將此資料行的索引儲存在索引鍵中。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="2f0cd-159">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="2f0cd-162">取得臨時表中儲存索引名稱之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="2f0cd-163">資料行的類型為 <a href="hh577895(v=exchg.10).md">Text</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="2f0cd-166">取得臨時表中的資料行 columnid，此資料表會儲存索引的語言識別項 (LCID) 。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="2f0cd-167">資料行的類型為 <a href="hh577895(v=exchg.10).md">Short</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="2f0cd-170">取得臨時表中的資料行 columnid，此資料表會儲存索引的 unicode 正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="2f0cd-171">資料行的類型為 <a href="hh577895(v=exchg.10).md">Long</a>。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="2f0cd-174">取得臨時表中的記錄數目。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2f0cd-176"><a href="dn335174(v=exchg.10).md">tableid</a></span><span class="sxs-lookup"><span data-stu-id="2f0cd-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="2f0cd-177">取得臨時表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="2f0cd-178">當不再需要資料表時，這應該會關閉。</span><span class="sxs-lookup"><span data-stu-id="2f0cd-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f0cd-179">頁首</span><span class="sxs-lookup"><span data-stu-id="2f0cd-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2f0cd-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f0cd-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2f0cd-181">參考</span><span class="sxs-lookup"><span data-stu-id="2f0cd-181">Reference</span></span>

[<span data-ttu-id="2f0cd-182">JET_INDEXLIST 類別</span><span class="sxs-lookup"><span data-stu-id="2f0cd-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="2f0cd-183">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2f0cd-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
