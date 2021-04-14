---
description: 深入瞭解： JET_ENUMCOLUMN 成員
title: JET_ENUMCOLUMN 成員
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552737"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="91da9-103">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="91da9-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="91da9-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="91da9-104">Include protected members</span></span>  
<span data-ttu-id="91da9-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="91da9-105">Include inherited members</span></span>  

<span data-ttu-id="91da9-106">使用 JetEnumerateColumns 函數來列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="91da9-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="91da9-107">JetEnumerateColumns 會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="91da9-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="91da9-108">陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</span><span class="sxs-lookup"><span data-stu-id="91da9-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="91da9-109">[JET_ENUMCOLUMN](./jet-enumcolumn-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="91da9-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="91da9-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="91da9-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="91da9-111">名稱</span><span class="sxs-lookup"><span data-stu-id="91da9-111">Name</span></span></th>
<th><span data-ttu-id="91da9-112">描述</span><span class="sxs-lookup"><span data-stu-id="91da9-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="91da9-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="91da9-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91da9-115">頁首</span><span class="sxs-lookup"><span data-stu-id="91da9-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="91da9-116">屬性</span><span class="sxs-lookup"><span data-stu-id="91da9-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="91da9-117">名稱</span><span class="sxs-lookup"><span data-stu-id="91da9-117">Name</span></span></th>
<th><span data-ttu-id="91da9-118">描述</span><span class="sxs-lookup"><span data-stu-id="91da9-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="91da9-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="91da9-121">取得為數據行列舉之值的大小。</span><span class="sxs-lookup"><span data-stu-id="91da9-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="91da9-122">只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="91da9-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="91da9-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="91da9-125">取得針對資料行列舉的資料行值數目。</span><span class="sxs-lookup"><span data-stu-id="91da9-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="91da9-126">只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="91da9-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-128"><a href="dn335135(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="91da9-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="91da9-129">取得已列舉的 columnid 識別碼。</span><span class="sxs-lookup"><span data-stu-id="91da9-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-131"><a href="dn335086(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="91da9-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="91da9-132">取得列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="91da9-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="91da9-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="91da9-135">取得為數據行列舉的值。</span><span class="sxs-lookup"><span data-stu-id="91da9-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="91da9-136">只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="91da9-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="91da9-137">這會指向傳遞給<a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a>的<a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a>配置器回呼所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="91da9-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="91da9-138">請記得在完成時釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="91da9-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="91da9-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="91da9-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="91da9-141">取得資料行的列舉資料行值。</span><span class="sxs-lookup"><span data-stu-id="91da9-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="91da9-142">只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="91da9-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91da9-143">頁首</span><span class="sxs-lookup"><span data-stu-id="91da9-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="91da9-144">方法</span><span class="sxs-lookup"><span data-stu-id="91da9-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="91da9-145">名稱</span><span class="sxs-lookup"><span data-stu-id="91da9-145">Name</span></span></th>
<th><span data-ttu-id="91da9-146">描述</span><span class="sxs-lookup"><span data-stu-id="91da9-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="91da9-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="91da9-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="91da9-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="91da9-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="91da9-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="91da9-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="91da9-152"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="91da9-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="91da9-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="91da9-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="91da9-155"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="91da9-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="91da9-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="91da9-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="91da9-158"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="91da9-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="91da9-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="91da9-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="91da9-161"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="91da9-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="91da9-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="91da9-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="91da9-164">傳回表示目前<a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="91da9-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="91da9-165"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="91da9-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91da9-166">頁首</span><span class="sxs-lookup"><span data-stu-id="91da9-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="91da9-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91da9-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91da9-168">參考</span><span class="sxs-lookup"><span data-stu-id="91da9-168">Reference</span></span>

[<span data-ttu-id="91da9-169">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="91da9-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="91da9-170">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="91da9-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
