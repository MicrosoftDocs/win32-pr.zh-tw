---
description: 深入瞭解：資料表方法
title: 資料表方法
TOCTitle: Table methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_methods(v=EXCHG.10)
ms:contentKeyID: 55104059
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 776224e8c1b72a892ad6600d29adbcc881f6df09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566759"
---
# <a name="table-methods"></a><span data-ttu-id="8dbee-103">資料表方法</span><span class="sxs-lookup"><span data-stu-id="8dbee-103">Table methods</span></span>

<span data-ttu-id="8dbee-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="8dbee-104">Include protected members</span></span>  
<span data-ttu-id="8dbee-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="8dbee-105">Include inherited members</span></span>  

<span data-ttu-id="8dbee-106">[資料表](./table-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="8dbee-106">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="8dbee-107">方法</span><span class="sxs-lookup"><span data-stu-id="8dbee-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8dbee-108">名稱</span><span class="sxs-lookup"><span data-stu-id="8dbee-108">Name</span></span></th>
<th><span data-ttu-id="8dbee-109">描述</span><span class="sxs-lookup"><span data-stu-id="8dbee-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="8dbee-112">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8dbee-112">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="8dbee-113"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-113">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-115"><a href="dn351235(v=exchg.10).md">關閉</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-115"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="8dbee-116">關閉資料表。</span><span class="sxs-lookup"><span data-stu-id="8dbee-116">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-118"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="8dbee-118"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="8dbee-119">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="8dbee-119">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="8dbee-120"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-120">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-122"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="8dbee-122"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="8dbee-123">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="8dbee-123">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="8dbee-124"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="8dbee-127"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-127">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-129"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-129"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="8dbee-130">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8dbee-130">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="8dbee-131"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-131">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="8dbee-134"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="8dbee-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="8dbee-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-142"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-142"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="8dbee-143">釋放基礎 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="8dbee-143">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="8dbee-144"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-144">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="8dbee-147">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="8dbee-147">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="8dbee-148"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-148">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="8dbee-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="8dbee-151">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="8dbee-151">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="8dbee-152"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-152">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="8dbee-154"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="8dbee-154"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="8dbee-155">傳回表示目前<a href="dn351163(v=exchg.10).md">資料表</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="8dbee-155">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="8dbee-156"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="8dbee-156">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8dbee-157">頁首</span><span class="sxs-lookup"><span data-stu-id="8dbee-157">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8dbee-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dbee-158">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dbee-159">參考</span><span class="sxs-lookup"><span data-stu-id="8dbee-159">Reference</span></span>

[<span data-ttu-id="8dbee-160">Table 類別</span><span class="sxs-lookup"><span data-stu-id="8dbee-160">Table class</span></span>](./table-class.md)

[<span data-ttu-id="8dbee-161">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8dbee-161">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
