---
description: 深入瞭解：會話成員
title: 工作階段成員
TOCTitle: Session members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Session
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session_members(v=EXCHG.10)
ms:contentKeyID: 55104004
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 05619d765b5a85a7f5330936ceb88266cced3cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945090"
---
# <a name="session-members"></a><span data-ttu-id="a5a66-103">工作階段成員</span><span class="sxs-lookup"><span data-stu-id="a5a66-103">Session members</span></span>

<span data-ttu-id="a5a66-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="a5a66-104">Include protected members</span></span>  
<span data-ttu-id="a5a66-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="a5a66-105">Include inherited members</span></span>  

<span data-ttu-id="a5a66-106">封裝可處置物件中之 JET_SESID 的類別。</span><span class="sxs-lookup"><span data-stu-id="a5a66-106">A class that encapsulates a JET_SESID in a disposable object.</span></span>

<span data-ttu-id="a5a66-107">此 [會話](./session-class.md) 類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="a5a66-107">The [Session](./session-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="a5a66-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="a5a66-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5a66-109">名稱</span><span class="sxs-lookup"><span data-stu-id="a5a66-109">Name</span></span></th>
<th><span data-ttu-id="a5a66-110">描述</span><span class="sxs-lookup"><span data-stu-id="a5a66-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-112"><a href="dn351126(v=exchg.10).md">工作階段</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-112"><a href="dn351126(v=exchg.10).md">Session</a></span></span></td>
<td><span data-ttu-id="a5a66-113">初始化 Session 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="a5a66-113">Initializes a new instance of the Session class.</span></span> <span data-ttu-id="a5a66-114">從指定的實例配置新的 JET_SESSION。</span><span class="sxs-lookup"><span data-stu-id="a5a66-114">A new JET_SESSION is allocated from the given instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5a66-115">頁首</span><span class="sxs-lookup"><span data-stu-id="a5a66-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="a5a66-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a5a66-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5a66-117">名稱</span><span class="sxs-lookup"><span data-stu-id="a5a66-117">Name</span></span></th>
<th><span data-ttu-id="a5a66-118">描述</span><span class="sxs-lookup"><span data-stu-id="a5a66-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><span data-ttu-id="a5a66-120"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-120"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="a5a66-121">取得值，指出目前是否已配置基礎資源。</span><span class="sxs-lookup"><span data-stu-id="a5a66-121">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="a5a66-122"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-122">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="a5a66-124"><a href="dn351175(v=exchg.10).md">JetSesid</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-124"><a href="dn351175(v=exchg.10).md">JetSesid</a></span></span></td>
<td><span data-ttu-id="a5a66-125">取得此會話包含的 JET_SESID。</span><span class="sxs-lookup"><span data-stu-id="a5a66-125">Gets the JET_SESID that this session contains.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5a66-126">頁首</span><span class="sxs-lookup"><span data-stu-id="a5a66-126">Top</span></span>

## <a name="methods"></a><span data-ttu-id="a5a66-127">方法</span><span class="sxs-lookup"><span data-stu-id="a5a66-127">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5a66-128">名稱</span><span class="sxs-lookup"><span data-stu-id="a5a66-128">Name</span></span></th>
<th><span data-ttu-id="a5a66-129">描述</span><span class="sxs-lookup"><span data-stu-id="a5a66-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-131"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-131"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="a5a66-132">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a5a66-132">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="a5a66-133"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-135"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="a5a66-135"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="a5a66-136">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="a5a66-136">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="a5a66-137"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-137">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-139"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="a5a66-139"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="a5a66-140">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="a5a66-140">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="a5a66-141"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-141">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-143"><a href="dn351128(v=exchg.10).md">結束</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-143"><a href="dn351128(v=exchg.10).md">End</a></span></span></td>
<td><span data-ttu-id="a5a66-144">終止會話。</span><span class="sxs-lookup"><span data-stu-id="a5a66-144">Terminate the session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-146"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-146"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="a5a66-147"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-147">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-149"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-149"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="a5a66-150">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a5a66-150">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="a5a66-151"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-151">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-153"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-153"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="a5a66-154"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-154">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-156"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-156"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="a5a66-157"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-159"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-159"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="a5a66-160"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-160">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-162"><a href="dn351165(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-162"><a href="dn351165(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="a5a66-163">釋放基礎 JET_SESID。</span><span class="sxs-lookup"><span data-stu-id="a5a66-163">Free the underlying JET_SESID.</span></span> <span data-ttu-id="a5a66-164"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-164">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-166"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-166"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="a5a66-167">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="a5a66-167">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="a5a66-168"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-168">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="a5a66-170"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-170"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="a5a66-171">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="a5a66-171">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="a5a66-172"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-172">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="a5a66-174"><a href="dn351129(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="a5a66-174"><a href="dn351129(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="a5a66-175">傳回表示目前<a href="dn351164(v=exchg.10).md">會話</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="a5a66-175">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351164(v=exchg.10).md">Session</a>.</span></span> <span data-ttu-id="a5a66-176"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="a5a66-176">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5a66-177">頁首</span><span class="sxs-lookup"><span data-stu-id="a5a66-177">Top</span></span>

## <a name="operators"></a><span data-ttu-id="a5a66-178">運算子</span><span class="sxs-lookup"><span data-stu-id="a5a66-178">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a5a66-179">Name</span><span class="sxs-lookup"><span data-stu-id="a5a66-179">Name</span></span></th>
<th><span data-ttu-id="a5a66-180">描述</span><span class="sxs-lookup"><span data-stu-id="a5a66-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="a5a66-183"><a href="dn351178(v=exchg.10).md">JET_SESID 的隱含 (會話) </a></span><span class="sxs-lookup"><span data-stu-id="a5a66-183"><a href="dn351178(v=exchg.10).md">Implicit(Session to JET_SESID)</a></span></span></td>
<td><span data-ttu-id="a5a66-184">從會話到 JET_SESID 的隱含轉換運算子。</span><span class="sxs-lookup"><span data-stu-id="a5a66-184">Implicit conversion operator from a Session to a JET_SESID.</span></span> <span data-ttu-id="a5a66-185">這可讓會話與預期 JET_SESID 的 Api 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a5a66-185">This allows a Session to be used with APIs which expect a JET_SESID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5a66-186">頁首</span><span class="sxs-lookup"><span data-stu-id="a5a66-186">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a5a66-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5a66-187">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5a66-188">參考</span><span class="sxs-lookup"><span data-stu-id="a5a66-188">Reference</span></span>

[<span data-ttu-id="a5a66-189">工作階段類別</span><span class="sxs-lookup"><span data-stu-id="a5a66-189">Session class</span></span>](./session-class.md)

[<span data-ttu-id="a5a66-190">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a5a66-190">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
