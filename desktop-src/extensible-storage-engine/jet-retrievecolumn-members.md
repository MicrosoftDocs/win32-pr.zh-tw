---
description: 深入瞭解： JET_RETRIEVECOLUMN 成員
title: JET_RETRIEVECOLUMN 成員
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553942"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="dedc7-103">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="dedc7-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="dedc7-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="dedc7-104">Include protected members</span></span>  
<span data-ttu-id="dedc7-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="dedc7-105">Include inherited members</span></span>  

<span data-ttu-id="dedc7-106">包含[JetRetrieveColumns (JET_SESID、JET_TABLEID、 \[ \] 、Int32) ](./api.jetretrievecolumns-method.md)的輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="dedc7-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="dedc7-107">結構中的欄位描述要取出的資料行值、如何取出它，以及要儲存結果的位置。</span><span class="sxs-lookup"><span data-stu-id="dedc7-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="dedc7-108">[JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="dedc7-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="dedc7-109">建構函式</span><span class="sxs-lookup"><span data-stu-id="dedc7-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dedc7-110">名稱</span><span class="sxs-lookup"><span data-stu-id="dedc7-110">Name</span></span></th>
<th><span data-ttu-id="dedc7-111">描述</span><span class="sxs-lookup"><span data-stu-id="dedc7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="dedc7-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dedc7-114">頁首</span><span class="sxs-lookup"><span data-stu-id="dedc7-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="dedc7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="dedc7-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dedc7-116">名稱</span><span class="sxs-lookup"><span data-stu-id="dedc7-116">Name</span></span></th>
<th><span data-ttu-id="dedc7-117">描述</span><span class="sxs-lookup"><span data-stu-id="dedc7-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="dedc7-120">取得抓取資料行作業抓取之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dedc7-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="dedc7-123">取得或設定 <a href="dn351040(v=exchg.10).md">pvData</a> 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dedc7-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="dedc7-124">抓取資料行作業將不會在 pvData 中儲存比 cbData 更多的資料。</span><span class="sxs-lookup"><span data-stu-id="dedc7-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-126"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="dedc7-127">取得或設定要取得之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="dedc7-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="dedc7-130">藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="dedc7-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-132"><a href="dn335231(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="dedc7-133">取得從資料行抓取傳回的警告。</span><span class="sxs-lookup"><span data-stu-id="dedc7-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-135"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="dedc7-136">取得或設定資料行抓取的選項。</span><span class="sxs-lookup"><span data-stu-id="dedc7-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-138"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="dedc7-139">取得或設定資料將儲存在緩衝區中的位移。</span><span class="sxs-lookup"><span data-stu-id="dedc7-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="dedc7-142">取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="dedc7-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="dedc7-145">取得或設定包含在多值資料行中之值的序號。</span><span class="sxs-lookup"><span data-stu-id="dedc7-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="dedc7-146">如果 itagSequence 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="dedc7-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="dedc7-148"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="dedc7-149">取得或設定將儲存從資料行取出之資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dedc7-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dedc7-150">頁首</span><span class="sxs-lookup"><span data-stu-id="dedc7-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="dedc7-151">方法</span><span class="sxs-lookup"><span data-stu-id="dedc7-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="dedc7-152">名稱</span><span class="sxs-lookup"><span data-stu-id="dedc7-152">Name</span></span></th>
<th><span data-ttu-id="dedc7-153">描述</span><span class="sxs-lookup"><span data-stu-id="dedc7-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="dedc7-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="dedc7-156"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="dedc7-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="dedc7-159"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="dedc7-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="dedc7-162"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="dedc7-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="dedc7-165"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="dedc7-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="dedc7-168"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="dedc7-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="dedc7-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="dedc7-171">傳回表示目前<a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="dedc7-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="dedc7-172"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="dedc7-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dedc7-173">頁首</span><span class="sxs-lookup"><span data-stu-id="dedc7-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="dedc7-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dedc7-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dedc7-175">參考</span><span class="sxs-lookup"><span data-stu-id="dedc7-175">Reference</span></span>

[<span data-ttu-id="dedc7-176">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="dedc7-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="dedc7-177">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="dedc7-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
