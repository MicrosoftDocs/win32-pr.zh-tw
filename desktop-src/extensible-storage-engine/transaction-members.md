---
description: 深入瞭解：交易成員
title: 交易成員
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555675"
---
# <a name="transaction-members"></a><span data-ttu-id="03b04-103">交易成員</span><span class="sxs-lookup"><span data-stu-id="03b04-103">Transaction members</span></span>

<span data-ttu-id="03b04-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="03b04-104">Include protected members</span></span>  
<span data-ttu-id="03b04-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="03b04-105">Include inherited members</span></span>  

<span data-ttu-id="03b04-106">在 JET_SESID 上封裝交易的類別。</span><span class="sxs-lookup"><span data-stu-id="03b04-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="03b04-107">[交易](./transaction-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="03b04-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="03b04-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="03b04-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="03b04-109">名稱</span><span class="sxs-lookup"><span data-stu-id="03b04-109">Name</span></span></th>
<th><span data-ttu-id="03b04-110">描述</span><span class="sxs-lookup"><span data-stu-id="03b04-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-112"><a href="dn351177(v=exchg.10).md">交易</a></span><span class="sxs-lookup"><span data-stu-id="03b04-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="03b04-113">初始化 Transaction 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="03b04-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="03b04-114">這會自動開始交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-114">This automatically begins a transaction.</span></span> <span data-ttu-id="03b04-115">如果未明確認可，將會回復交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03b04-116">頁首</span><span class="sxs-lookup"><span data-stu-id="03b04-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="03b04-117">屬性</span><span class="sxs-lookup"><span data-stu-id="03b04-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="03b04-118">名稱</span><span class="sxs-lookup"><span data-stu-id="03b04-118">Name</span></span></th>
<th><span data-ttu-id="03b04-119">描述</span><span class="sxs-lookup"><span data-stu-id="03b04-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="受保護的屬性" alt="Protected property" /></td>
<td><span data-ttu-id="03b04-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="03b04-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="03b04-122">取得值，指出目前是否已配置基礎資源。</span><span class="sxs-lookup"><span data-stu-id="03b04-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="03b04-123"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="03b04-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="03b04-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="03b04-126">取得值，指出這個物件目前是否在交易中。</span><span class="sxs-lookup"><span data-stu-id="03b04-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03b04-127">頁首</span><span class="sxs-lookup"><span data-stu-id="03b04-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="03b04-128">方法</span><span class="sxs-lookup"><span data-stu-id="03b04-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="03b04-129">名稱</span><span class="sxs-lookup"><span data-stu-id="03b04-129">Name</span></span></th>
<th><span data-ttu-id="03b04-130">描述</span><span class="sxs-lookup"><span data-stu-id="03b04-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-132"><a href="dn351172(v=exchg.10).md">開始</a></span><span class="sxs-lookup"><span data-stu-id="03b04-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="03b04-133">開始交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-133">Begin a transaction.</span></span> <span data-ttu-id="03b04-134">此物件目前不應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="03b04-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="03b04-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="03b04-137">如果已處置這個物件，則擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="03b04-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="03b04-138"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-140"><a href="dn351179(v=exchg.10).md">認可 (CommitTransactionGrbit) </a></span><span class="sxs-lookup"><span data-stu-id="03b04-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="03b04-141">認可交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-141">Commit a transaction.</span></span> <span data-ttu-id="03b04-142">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="03b04-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-144"><a href="dn351243(v=exchg.10).md">認可 (CommitTransactionGrbit、TimeSpan、JET_COMMIT_ID) </a></span><span class="sxs-lookup"><span data-stu-id="03b04-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="03b04-145">認可交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-145">Commit a transaction.</span></span> <span data-ttu-id="03b04-146">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="03b04-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-148"><a href="dn350553(v=exchg.10).md">Dispose () </a></span><span class="sxs-lookup"><span data-stu-id="03b04-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="03b04-149">處置這個物件，釋放基礎 Esent 資源。</span><span class="sxs-lookup"><span data-stu-id="03b04-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="03b04-150"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-152"><a href="dn350543(v=exchg.10).md">Dispose (布林值) </a></span><span class="sxs-lookup"><span data-stu-id="03b04-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="03b04-153">由 Dispose 和完成項呼叫。</span><span class="sxs-lookup"><span data-stu-id="03b04-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="03b04-154"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="03b04-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="03b04-157"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="03b04-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-159"><a href="dn350552(v=exchg.10).md">完成</a></span><span class="sxs-lookup"><span data-stu-id="03b04-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="03b04-160">完成 EsentResource 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="03b04-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="03b04-161"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="03b04-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="03b04-164"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="03b04-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="03b04-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="03b04-167"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="03b04-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="03b04-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="03b04-170"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="03b04-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="03b04-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="03b04-173">當交易在作用中處置時呼叫。</span><span class="sxs-lookup"><span data-stu-id="03b04-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="03b04-174">這應該會復原交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-174">This should rollback the transaction.</span></span> <span data-ttu-id="03b04-175"> (覆寫 <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="03b04-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="03b04-178">當配置資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="03b04-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="03b04-179"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="03b04-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="03b04-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="03b04-182">釋放資源時由子類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="03b04-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="03b04-183"> (繼承自 <a href="dn319890(v=exchg.10).md">EsentResource</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-185"><a href="dn351244(v=exchg.10).md">復原</a></span><span class="sxs-lookup"><span data-stu-id="03b04-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="03b04-186">復原交易。</span><span class="sxs-lookup"><span data-stu-id="03b04-186">Rollback a transaction.</span></span> <span data-ttu-id="03b04-187">此物件應該在交易中。</span><span class="sxs-lookup"><span data-stu-id="03b04-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="03b04-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="03b04-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="03b04-190">傳回表示目前<a href="dn351174(v=exchg.10).md">交易</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="03b04-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="03b04-191"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="03b04-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03b04-192">頁首</span><span class="sxs-lookup"><span data-stu-id="03b04-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="03b04-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03b04-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03b04-194">參考</span><span class="sxs-lookup"><span data-stu-id="03b04-194">Reference</span></span>

[<span data-ttu-id="03b04-195">Transaction 類別</span><span class="sxs-lookup"><span data-stu-id="03b04-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="03b04-196">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="03b04-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
