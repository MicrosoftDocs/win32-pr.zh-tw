---
description: 深入瞭解： JET_COLUMNBASE 成員
title: JET_COLUMNBASE 成員
TOCTitle: JET_COLUMNBASE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase_members(v=EXCHG.10)
ms:contentKeyID: 55103414
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 72f26e02963d1cc0617fb908ce325c0c0099f7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320291"
---
# <a name="jet_columnbase-members"></a><span data-ttu-id="835c1-103">JET_COLUMNBASE 成員</span><span class="sxs-lookup"><span data-stu-id="835c1-103">JET_COLUMNBASE members</span></span>

<span data-ttu-id="835c1-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="835c1-104">Include protected members</span></span>  
<span data-ttu-id="835c1-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="835c1-105">Include inherited members</span></span>  

<span data-ttu-id="835c1-106">描述 ESENT 資料庫之資料表中的資料行。</span><span class="sxs-lookup"><span data-stu-id="835c1-106">Describes a column in a table of an ESENT database.</span></span>

<span data-ttu-id="835c1-107">[JET_COLUMNBASE](./jet-columnbase-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="835c1-107">The [JET_COLUMNBASE](./jet-columnbase-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="835c1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="835c1-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="835c1-109">名稱</span><span class="sxs-lookup"><span data-stu-id="835c1-109">Name</span></span></th>
<th><span data-ttu-id="835c1-110">描述</span><span class="sxs-lookup"><span data-stu-id="835c1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-112"><a href="dn335065(v=exchg.10).md">cbMax</a></span><span class="sxs-lookup"><span data-stu-id="835c1-112"><a href="dn335065(v=exchg.10).md">cbMax</a></span></span></td>
<td><span data-ttu-id="835c1-113">取得資料行的最大長度。</span><span class="sxs-lookup"><span data-stu-id="835c1-113">Gets the maximum length of the column.</span></span> <span data-ttu-id="835c1-114">只有 <a href="hh577895(v=exchg.10).md">Text</a>、 <a href="hh577895(v=exchg.10).md">LongText</a>、 <a href="hh577895(v=exchg.10).md">Binary</a> 和 <a href="hh577895(v=exchg.10).md">LongBinary</a>類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="835c1-114">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LongText</a>, <a href="hh577895(v=exchg.10).md">Binary</a> and <a href="hh577895(v=exchg.10).md">LongBinary</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-116"><a href="dn351019(v=exchg.10).md">coltyp</a></span><span class="sxs-lookup"><span data-stu-id="835c1-116"><a href="dn351019(v=exchg.10).md">coltyp</a></span></span></td>
<td><span data-ttu-id="835c1-117">取得資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="835c1-117">Gets type of the column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-119"><a href="dn335024(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="835c1-119"><a href="dn335024(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="835c1-120">取得資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="835c1-120">Gets the columnid of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-122"><a href="dn335066(v=exchg.10).md">cp</a></span><span class="sxs-lookup"><span data-stu-id="835c1-122"><a href="dn335066(v=exchg.10).md">cp</a></span></span></td>
<td><span data-ttu-id="835c1-123">取得資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="835c1-123">Gets code page of the column.</span></span> <span data-ttu-id="835c1-124">只有 <a href="hh577895(v=exchg.10).md">Text</a> 和 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="835c1-124">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a> and <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-126"><a href="dn351020(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="835c1-126"><a href="dn351020(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="835c1-127">取得資料行選項。</span><span class="sxs-lookup"><span data-stu-id="835c1-127">Gets the column options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-129"><a href="dn335067(v=exchg.10).md">szBaseColumnName</a></span><span class="sxs-lookup"><span data-stu-id="835c1-129"><a href="dn335067(v=exchg.10).md">szBaseColumnName</a></span></span></td>
<td><span data-ttu-id="835c1-130">取得範本資料表中的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="835c1-130">Gets the name of the column in the template table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="835c1-132"><a href="dn335026(v=exchg.10).md">szBaseTableName</a></span><span class="sxs-lookup"><span data-stu-id="835c1-132"><a href="dn335026(v=exchg.10).md">szBaseTableName</a></span></span></td>
<td><span data-ttu-id="835c1-133">取得目前資料表繼承其 DDL 的資料表。</span><span class="sxs-lookup"><span data-stu-id="835c1-133">Gets the table from which the current table inherits its DDL.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="835c1-134">頁首</span><span class="sxs-lookup"><span data-stu-id="835c1-134">Top</span></span>

## <a name="methods"></a><span data-ttu-id="835c1-135">方法</span><span class="sxs-lookup"><span data-stu-id="835c1-135">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="835c1-136">名稱</span><span class="sxs-lookup"><span data-stu-id="835c1-136">Name</span></span></th>
<th><span data-ttu-id="835c1-137">描述</span><span class="sxs-lookup"><span data-stu-id="835c1-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="835c1-139"><a href="dn335062(v=exchg.10).md">等於 (物件) </a></span><span class="sxs-lookup"><span data-stu-id="835c1-139"><a href="dn335062(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="835c1-140">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="835c1-140">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="835c1-141"> (覆寫 <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_"> (物件) 的 Equals </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="835c1-141">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="835c1-143"><a href="dn351009(v=exchg.10).md">等於 (JET_COLUMNBASE) </a></span><span class="sxs-lookup"><span data-stu-id="835c1-143"><a href="dn351009(v=exchg.10).md">Equals(JET_COLUMNBASE)</a></span></span></td>
<td><span data-ttu-id="835c1-144">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="835c1-144">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="835c1-146"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="835c1-146"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="835c1-147"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="835c1-147">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="835c1-149"><a href="dn335023(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="835c1-149"><a href="dn335023(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="835c1-150">傳回這個執行個體的雜湊碼。</span><span class="sxs-lookup"><span data-stu-id="835c1-150">Returns the hash code for this instance.</span></span> <span data-ttu-id="835c1-151"> (覆寫 <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="835c1-151">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="835c1-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="835c1-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="835c1-154"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="835c1-154">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="835c1-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="835c1-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="835c1-157"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="835c1-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="835c1-159"><a href="dn335064(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="835c1-159"><a href="dn335064(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="835c1-160">傳回表示目前<a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="835c1-160">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>.</span></span> <span data-ttu-id="835c1-161"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="835c1-161">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="835c1-162">頁首</span><span class="sxs-lookup"><span data-stu-id="835c1-162">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="835c1-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="835c1-163">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="835c1-164">參考</span><span class="sxs-lookup"><span data-stu-id="835c1-164">Reference</span></span>

[<span data-ttu-id="835c1-165">JET_COLUMNBASE 類別</span><span class="sxs-lookup"><span data-stu-id="835c1-165">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="835c1-166">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="835c1-166">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
