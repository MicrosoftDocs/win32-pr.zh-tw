---
description: 深入瞭解： JET_SETINFO 成員
title: JET_SETINFO 成員
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689923"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="01901-103">JET_SETINFO 成員</span><span class="sxs-lookup"><span data-stu-id="01901-103">JET_SETINFO members</span></span>

<span data-ttu-id="01901-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="01901-104">Include protected members</span></span>  
<span data-ttu-id="01901-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="01901-105">Include inherited members</span></span>  

<span data-ttu-id="01901-106">JetSetColumn 的設定。</span><span class="sxs-lookup"><span data-stu-id="01901-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="01901-107">[JET_SETINFO](./jet-setinfo-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="01901-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="01901-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="01901-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="01901-109">名稱</span><span class="sxs-lookup"><span data-stu-id="01901-109">Name</span></span></th>
<th><span data-ttu-id="01901-110">描述</span><span class="sxs-lookup"><span data-stu-id="01901-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="01901-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01901-113">頁首</span><span class="sxs-lookup"><span data-stu-id="01901-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="01901-114">屬性</span><span class="sxs-lookup"><span data-stu-id="01901-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="01901-115">名稱</span><span class="sxs-lookup"><span data-stu-id="01901-115">Name</span></span></th>
<th><span data-ttu-id="01901-116">描述</span><span class="sxs-lookup"><span data-stu-id="01901-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="01901-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="01901-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="01901-119">取得或設定要在 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中設定之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="01901-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="01901-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="01901-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="01901-122">取得或設定要設定之多重值資料行中的值順序。</span><span class="sxs-lookup"><span data-stu-id="01901-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="01901-123">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="01901-123">The array of values is one-based.</span></span> <span data-ttu-id="01901-124">第一個值是 sequence 1，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="01901-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="01901-125">如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。</span><span class="sxs-lookup"><span data-stu-id="01901-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="01901-126">值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="01901-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01901-127">頁首</span><span class="sxs-lookup"><span data-stu-id="01901-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="01901-128">方法</span><span class="sxs-lookup"><span data-stu-id="01901-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="01901-129">名稱</span><span class="sxs-lookup"><span data-stu-id="01901-129">Name</span></span></th>
<th><span data-ttu-id="01901-130">描述</span><span class="sxs-lookup"><span data-stu-id="01901-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="01901-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="01901-133">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="01901-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="01901-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="01901-136">傳回物件的深層複本。</span><span class="sxs-lookup"><span data-stu-id="01901-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="01901-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="01901-139"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="01901-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="01901-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="01901-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="01901-142"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="01901-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="01901-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="01901-145"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="01901-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="01901-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="01901-148"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="01901-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="01901-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="01901-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="01901-151"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="01901-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="01901-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="01901-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="01901-154">傳回表示目前<a href="dn351059(v=exchg.10).md">JET_SETINFO</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="01901-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="01901-155"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="01901-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01901-156">頁首</span><span class="sxs-lookup"><span data-stu-id="01901-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="01901-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01901-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01901-158">參考</span><span class="sxs-lookup"><span data-stu-id="01901-158">Reference</span></span>

[<span data-ttu-id="01901-159">JET_SETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="01901-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="01901-160">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="01901-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
