---
description: 深入瞭解：交易方法
title: 交易方法
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556271"
---
# <a name="transaction-methods"></a><span data-ttu-id="5b777-103">交易方法</span><span class="sxs-lookup"><span data-stu-id="5b777-103">Transaction methods</span></span>

<span data-ttu-id="5b777-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="5b777-104">Include protected members</span></span>  
<span data-ttu-id="5b777-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="5b777-105">Include inherited members</span></span>  

<span data-ttu-id="5b777-106">[交易](./transaction-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="5b777-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="5b777-107">方法</span><span class="sxs-lookup"><span data-stu-id="5b777-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5b777-108">名稱</span><span class="sxs-lookup"><span data-stu-id="5b777-108">Name</span></span></th>
<th><span data-ttu-id="5b777-109">描述</span><span class="sxs-lookup"><span data-stu-id="5b777-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-111"><a href="dn351172(v=exchg.10).md">開始</a></span><span class="sxs-lookup"><span data-stu-id="5b777-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="5b777-112">開始交易。</span><span class="sxs-lookup"><span data-stu-id="5b777-112">Begin a transaction.</span></span> <span data-ttu-id="5b777-113">此物件目前不應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="5b777-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="5b777-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="5b777-116">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5b777-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="5b777-117"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-119"><a href="dn351179(v=exchg.10).md">認可 (CommitTransactionGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="5b777-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="5b777-120">認可交易。</span><span class="sxs-lookup"><span data-stu-id="5b777-120">Commit a transaction.</span></span> <span data-ttu-id="5b777-121">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="5b777-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-123"><a href="dn351243(v=exchg.10).md">認可 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) </a></span><span class="sxs-lookup"><span data-stu-id="5b777-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="5b777-124">認可交易。</span><span class="sxs-lookup"><span data-stu-id="5b777-124">Commit a transaction.</span></span> <span data-ttu-id="5b777-125">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="5b777-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-127"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="5b777-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="5b777-128">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="5b777-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="5b777-129"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-131"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="5b777-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="5b777-132">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="5b777-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="5b777-133"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="5b777-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="5b777-136"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="5b777-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-138"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="5b777-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="5b777-139">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5b777-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="5b777-140"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="5b777-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="5b777-143"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="5b777-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="5b777-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="5b777-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="5b777-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="5b777-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="5b777-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="5b777-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="5b777-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="5b777-152">當交易在作用中處置時呼叫。</span><span class="sxs-lookup"><span data-stu-id="5b777-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="5b777-153">這應該會復原交易。</span><span class="sxs-lookup"><span data-stu-id="5b777-153">This should rollback the transaction.</span></span> <span data-ttu-id="5b777-154"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="5b777-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="5b777-157">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="5b777-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="5b777-158"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="5b777-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="5b777-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="5b777-161">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="5b777-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="5b777-162"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-164"><a href="dn351244(v=exchg.10).md">復原</a></span><span class="sxs-lookup"><span data-stu-id="5b777-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="5b777-165">復原交易。</span><span class="sxs-lookup"><span data-stu-id="5b777-165">Rollback a transaction.</span></span> <span data-ttu-id="5b777-166">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="5b777-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="5b777-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="5b777-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="5b777-169">傳回表示目前<a href="dn351174(v=exchg.10).md">交易</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="5b777-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="5b777-170"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5b777-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5b777-171">頁首</span><span class="sxs-lookup"><span data-stu-id="5b777-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5b777-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b777-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b777-173">參考</span><span class="sxs-lookup"><span data-stu-id="5b777-173">Reference</span></span>

[<span data-ttu-id="5b777-174">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="5b777-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="5b777-175">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5b777-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
