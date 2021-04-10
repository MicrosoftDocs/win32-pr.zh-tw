---
description: 深入瞭解： JET_ENUMCOLUMNID 成員
title: JET_ENUMCOLUMNID 成員
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026088"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="799bd-103">JET_ENUMCOLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="799bd-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="799bd-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="799bd-104">Include protected members</span></span>  
<span data-ttu-id="799bd-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="799bd-105">Include inherited members</span></span>  

<span data-ttu-id="799bd-106">當使用 JetEnumerateColumns 函式時，列舉一組特定的資料行，並選擇性地列舉這些資料行的一組特定的多重值。</span><span class="sxs-lookup"><span data-stu-id="799bd-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="799bd-107">JetEnumerateColumns 會選擇性地採用 JET_ENUMCOLUMNID 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="799bd-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="799bd-108">[JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="799bd-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="799bd-109">建構函式</span><span class="sxs-lookup"><span data-stu-id="799bd-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="799bd-110">名稱</span><span class="sxs-lookup"><span data-stu-id="799bd-110">Name</span></span></th>
<th><span data-ttu-id="799bd-111">描述</span><span class="sxs-lookup"><span data-stu-id="799bd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="799bd-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="799bd-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="799bd-114">頁首</span><span class="sxs-lookup"><span data-stu-id="799bd-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="799bd-115">屬性</span><span class="sxs-lookup"><span data-stu-id="799bd-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="799bd-116">名稱</span><span class="sxs-lookup"><span data-stu-id="799bd-116">Name</span></span></th>
<th><span data-ttu-id="799bd-117">描述</span><span class="sxs-lookup"><span data-stu-id="799bd-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="799bd-119"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="799bd-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="799bd-120">取得或設定要列舉的 columnid 識別碼。</span><span class="sxs-lookup"><span data-stu-id="799bd-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="799bd-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="799bd-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="799bd-123">取得或設定以一為基礎的索引) 所 (的資料行值計數，以列舉指定的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="799bd-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="799bd-124">如果 ctagSequence 為 0 (零) 則會忽略 rgtagSequence，並且會列舉指定之資料行識別碼的所有資料行值。</span><span class="sxs-lookup"><span data-stu-id="799bd-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="799bd-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="799bd-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="799bd-127">取得或設定指定資料行的資料行值陣列中，以一個為基底的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="799bd-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="799bd-128">單一元素是 JET_RETRIEVECOLUMN 中定義的 itagSequence。</span><span class="sxs-lookup"><span data-stu-id="799bd-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="799bd-129">ItagSequence 0 (零) 表示 &quot; skip &quot; 。</span><span class="sxs-lookup"><span data-stu-id="799bd-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="799bd-130">1的 itagSequence 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="799bd-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="799bd-131">頁首</span><span class="sxs-lookup"><span data-stu-id="799bd-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="799bd-132">方法</span><span class="sxs-lookup"><span data-stu-id="799bd-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="799bd-133">名稱</span><span class="sxs-lookup"><span data-stu-id="799bd-133">Name</span></span></th>
<th><span data-ttu-id="799bd-134">描述</span><span class="sxs-lookup"><span data-stu-id="799bd-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="799bd-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="799bd-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="799bd-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="799bd-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="799bd-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="799bd-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="799bd-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="799bd-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="799bd-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="799bd-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="799bd-143"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="799bd-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="799bd-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="799bd-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="799bd-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="799bd-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="799bd-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="799bd-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="799bd-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="799bd-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="799bd-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="799bd-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="799bd-152">傳回表示目前<a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="799bd-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="799bd-153"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="799bd-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="799bd-154">頁首</span><span class="sxs-lookup"><span data-stu-id="799bd-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="799bd-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="799bd-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="799bd-156">參考</span><span class="sxs-lookup"><span data-stu-id="799bd-156">Reference</span></span>

[<span data-ttu-id="799bd-157">JET_ENUMCOLUMNID 類別</span><span class="sxs-lookup"><span data-stu-id="799bd-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="799bd-158">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="799bd-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
