---
description: 深入瞭解： EsentResource 方法
title: EsentResource 方法
TOCTitle: EsentResource methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource_methods(v=EXCHG.10)
ms:contentKeyID: 55102608
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c07cd44075284e4e8fd736102f62f702e055db99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559493"
---
# <a name="esentresource-methods"></a><span data-ttu-id="baa61-103">EsentResource 方法</span><span class="sxs-lookup"><span data-stu-id="baa61-103">EsentResource methods</span></span>

<span data-ttu-id="baa61-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="baa61-104">Include protected members</span></span>  
<span data-ttu-id="baa61-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="baa61-105">Include inherited members</span></span>  

<span data-ttu-id="baa61-106">[EsentResource](./esentresource-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="baa61-106">The [EsentResource](./esentresource-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="baa61-107">方法</span><span class="sxs-lookup"><span data-stu-id="baa61-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="baa61-108">名稱</span><span class="sxs-lookup"><span data-stu-id="baa61-108">Name</span></span></th>
<th><span data-ttu-id="baa61-109">描述</span><span class="sxs-lookup"><span data-stu-id="baa61-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="baa61-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="baa61-112">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="baa61-112">Throw an exception if this object has been disposed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="baa61-114"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="baa61-114"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="baa61-115">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="baa61-115">Dispose of this object, releasing the underlying Esent resource.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-117"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="baa61-117"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="baa61-118">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="baa61-118">Called by Dispose and the finalizer.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="baa61-120"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="baa61-120"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="baa61-121"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="baa61-121">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-123"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="baa61-123"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="baa61-124">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="baa61-124">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="baa61-125"> (覆寫 <a href="/dotnet/api/system.object.finalize#System_Object_Finalize">物件。 Finalize () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="baa61-125">(Overrides <a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Object.Finalize()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="baa61-127"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="baa61-127"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="baa61-128"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="baa61-128">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="baa61-130"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="baa61-130"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="baa61-131"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="baa61-131">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-133"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="baa61-133"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="baa61-134"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="baa61-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-136"><a href="dn350545(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="baa61-136"><a href="dn350545(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="baa61-137">由子類別實作為釋放資源。</span><span class="sxs-lookup"><span data-stu-id="baa61-137">Implemented by the subclass to release a resource.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-139"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="baa61-139"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="baa61-140">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="baa61-140">Called by a subclass when a resource is allocated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="baa61-142"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="baa61-142"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="baa61-143">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="baa61-143">Called by a subclass when a resource is freed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="baa61-145"><a href="/dotnet/api/system.object.tostring#System_Object_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="baa61-145"><a href="/dotnet/api/system.object.tostring#System_Object_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="baa61-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="baa61-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="baa61-147">頁首</span><span class="sxs-lookup"><span data-stu-id="baa61-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="baa61-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baa61-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="baa61-149">參考</span><span class="sxs-lookup"><span data-stu-id="baa61-149">Reference</span></span>

[<span data-ttu-id="baa61-150">EsentResource 類別</span><span class="sxs-lookup"><span data-stu-id="baa61-150">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="baa61-151">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="baa61-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
