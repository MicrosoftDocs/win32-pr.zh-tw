---
description: 深入瞭解： DurableCommitCallback 方法
title: Windows8) 的 DurableCommitCallback 方法 (
TOCTitle: DurableCommitCallback methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback_methods(v=EXCHG.10)
ms:contentKeyID: 55104392
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1a337d4e62b0eeeb8c5638430d728da37e8e8dc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695603"
---
# <a name="durablecommitcallback-methods"></a><span data-ttu-id="7d624-103">DurableCommitCallback 方法</span><span class="sxs-lookup"><span data-stu-id="7d624-103">DurableCommitCallback methods</span></span>

<span data-ttu-id="7d624-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="7d624-104">Include protected members</span></span>  
<span data-ttu-id="7d624-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="7d624-105">Include inherited members</span></span>  

<span data-ttu-id="7d624-106">[DurableCommitCallback](./durablecommitcallback-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="7d624-106">The [DurableCommitCallback](./durablecommitcallback-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="7d624-107">方法</span><span class="sxs-lookup"><span data-stu-id="7d624-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7d624-108">名稱</span><span class="sxs-lookup"><span data-stu-id="7d624-108">Name</span></span></th>
<th><span data-ttu-id="7d624-109">描述</span><span class="sxs-lookup"><span data-stu-id="7d624-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="7d624-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="7d624-112">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7d624-112">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="7d624-113"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-113">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-115"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="7d624-115"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="7d624-116">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="7d624-116">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="7d624-117"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-119"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="7d624-119"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="7d624-120">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d624-120">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="7d624-121"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-121">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-123"><a href="dn335442(v=exchg.10).md">結束</a></span><span class="sxs-lookup"><span data-stu-id="7d624-123"><a href="dn335442(v=exchg.10).md">End</a></span></span></td>
<td><span data-ttu-id="7d624-124">終止長期認可會話。</span><span class="sxs-lookup"><span data-stu-id="7d624-124">Terminates the durable commit session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="7d624-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="7d624-127"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7d624-127">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-129"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="7d624-129"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="7d624-130">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7d624-130">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="7d624-131"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-131">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="7d624-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="7d624-134"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7d624-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="7d624-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="7d624-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7d624-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="7d624-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="7d624-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7d624-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-142"><a href="dn335327(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="7d624-142"><a href="dn335327(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="7d624-143">釋出持久的認可會話。</span><span class="sxs-lookup"><span data-stu-id="7d624-143">Frees the durable commit session.</span></span> <span data-ttu-id="7d624-144"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-144">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="7d624-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="7d624-147">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d624-147">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="7d624-148"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-148">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7d624-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="7d624-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="7d624-151">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d624-151">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="7d624-152"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-152">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7d624-154"><a href="dn335445(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="7d624-154"><a href="dn335445(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="7d624-155">產生結構的字串表示。</span><span class="sxs-lookup"><span data-stu-id="7d624-155">Generates a string representation of the structure.</span></span> <span data-ttu-id="7d624-156"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7d624-156">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d624-157">頁首</span><span class="sxs-lookup"><span data-stu-id="7d624-157">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7d624-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d624-158">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d624-159">參考</span><span class="sxs-lookup"><span data-stu-id="7d624-159">Reference</span></span>

[<span data-ttu-id="7d624-160">DurableCommitCallback 類別</span><span class="sxs-lookup"><span data-stu-id="7d624-160">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="7d624-161">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="7d624-161">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
