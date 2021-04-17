---
description: 深入瞭解：資料表成員
title: 資料表成員
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557408"
---
# <a name="table-members"></a><span data-ttu-id="bc4dc-103">資料表成員</span><span class="sxs-lookup"><span data-stu-id="bc4dc-103">Table members</span></span>

<span data-ttu-id="bc4dc-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="bc4dc-104">Include protected members</span></span>  
<span data-ttu-id="bc4dc-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="bc4dc-105">Include inherited members</span></span>  

<span data-ttu-id="bc4dc-106">封裝可處置物件中之 JET_TABLEID 的類別。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-106">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="bc4dc-107">這會開啟現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-107">This opens an existing table.</span></span> <span data-ttu-id="bc4dc-108">若要建立資料表，請使用 JetCreateTable 方法。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-108">To create a table use the JetCreateTable method.</span></span>

<span data-ttu-id="bc4dc-109">[資料表](./table-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-109">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="bc4dc-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="bc4dc-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bc4dc-111">名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-111">Name</span></span></th>
<th><span data-ttu-id="bc4dc-112">描述</span><span class="sxs-lookup"><span data-stu-id="bc4dc-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-114"><a href="dn351234(v=exchg.10).md">資料表</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-114"><a href="dn351234(v=exchg.10).md">Table</a></span></span></td>
<td><span data-ttu-id="bc4dc-115">初始化 Table 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-115">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="bc4dc-116">資料表會從指定的資料庫開啟。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-116">The table is opened from the given database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc4dc-117">頁首</span><span class="sxs-lookup"><span data-stu-id="bc4dc-117">Top</span></span>

## <a name="properties"></a><span data-ttu-id="bc4dc-118">屬性</span><span class="sxs-lookup"><span data-stu-id="bc4dc-118">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bc4dc-119">名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-119">Name</span></span></th>
<th><span data-ttu-id="bc4dc-120">描述</span><span class="sxs-lookup"><span data-stu-id="bc4dc-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><span data-ttu-id="bc4dc-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="bc4dc-123">取得值，指出目前是否已配置基礎資源。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-123">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="bc4dc-124"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bc4dc-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span></span></td>
<td><span data-ttu-id="bc4dc-127">取得此資料表包含的 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-127">Gets the JET_TABLEID that this table contains.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bc4dc-129"><a href="dn351170(v=exchg.10).md">名稱</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-129"><a href="dn351170(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="bc4dc-130">取得此資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-130">Gets the name of this table.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc4dc-131">頁首</span><span class="sxs-lookup"><span data-stu-id="bc4dc-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="bc4dc-132">方法</span><span class="sxs-lookup"><span data-stu-id="bc4dc-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bc4dc-133">名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-133">Name</span></span></th>
<th><span data-ttu-id="bc4dc-134">描述</span><span class="sxs-lookup"><span data-stu-id="bc4dc-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="bc4dc-137">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="bc4dc-138"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-140"><a href="dn351235(v=exchg.10).md">關閉</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-140"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="bc4dc-141">關閉資料表。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-141">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-143"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-143"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="bc4dc-144">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-144">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="bc4dc-145"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-145">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-147"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-147"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="bc4dc-148">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-148">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="bc4dc-149"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-149">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="bc4dc-152"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-154"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="bc4dc-155">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-155">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="bc4dc-156"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-156">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="bc4dc-159"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="bc4dc-162"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="bc4dc-165"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="bc4dc-168">釋放基礎 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-168">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="bc4dc-169"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-169">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="bc4dc-172">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-172">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="bc4dc-173"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-173">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="bc4dc-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="bc4dc-176">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-176">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="bc4dc-177"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-177">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="bc4dc-179"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-179"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="bc4dc-180">傳回表示目前<a href="dn351163(v=exchg.10).md">資料表</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-180">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="bc4dc-181"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-181">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc4dc-182">頁首</span><span class="sxs-lookup"><span data-stu-id="bc4dc-182">Top</span></span>

## <a name="operators"></a><span data-ttu-id="bc4dc-183">運算子</span><span class="sxs-lookup"><span data-stu-id="bc4dc-183">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bc4dc-184">Name</span><span class="sxs-lookup"><span data-stu-id="bc4dc-184">Name</span></span></th>
<th><span data-ttu-id="bc4dc-185">描述</span><span class="sxs-lookup"><span data-stu-id="bc4dc-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="bc4dc-188"><a href="dn351239(v=exchg.10).md">要 JET_TABLEID 的隱含 (資料表) </a></span><span class="sxs-lookup"><span data-stu-id="bc4dc-188"><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="bc4dc-189">從資料表到 JET_TABLEID 的隱含轉換運算子。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-189">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="bc4dc-190">這可讓資料表與預期 JET_TABLEID 的 Api 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-190">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc4dc-191">頁首</span><span class="sxs-lookup"><span data-stu-id="bc4dc-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bc4dc-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc4dc-193">參考</span><span class="sxs-lookup"><span data-stu-id="bc4dc-193">Reference</span></span>

[<span data-ttu-id="bc4dc-194">Table 類別</span><span class="sxs-lookup"><span data-stu-id="bc4dc-194">Table class</span></span>](./table-class.md)

[<span data-ttu-id="bc4dc-195">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bc4dc-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
