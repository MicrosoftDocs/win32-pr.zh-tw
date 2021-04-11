---
description: 深入瞭解： JET_CONDITIONALCOLUMN 成員
title: JET_CONDITIONALCOLUMN 成員
TOCTitle: JET_CONDITIONALCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103431
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ecb132cd3fa3a313889c0a9a92fe6761da3b1cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944702"
---
# <a name="jet_conditionalcolumn-members"></a><span data-ttu-id="70f90-103">JET_CONDITIONALCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="70f90-103">JET_CONDITIONALCOLUMN members</span></span>

<span data-ttu-id="70f90-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="70f90-104">Include protected members</span></span>  
<span data-ttu-id="70f90-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="70f90-105">Include inherited members</span></span>  

<span data-ttu-id="70f90-106">定義如何針對指定的索引執行條件式索引編制。</span><span class="sxs-lookup"><span data-stu-id="70f90-106">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="70f90-107">條件式索引僅包含符合指定條件之資料列的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="70f90-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="70f90-108">不過，條件資料行不是索引索引鍵的一部分，而只會控制索引項目是否存在。</span><span class="sxs-lookup"><span data-stu-id="70f90-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

<span data-ttu-id="70f90-109">[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="70f90-109">The [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="70f90-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="70f90-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="70f90-111">名稱</span><span class="sxs-lookup"><span data-stu-id="70f90-111">Name</span></span></th>
<th><span data-ttu-id="70f90-112">描述</span><span class="sxs-lookup"><span data-stu-id="70f90-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-114"><a href="dn335106(v=exchg.10).md">JET_CONDITIONALCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="70f90-114"><a href="dn335106(v=exchg.10).md">JET_CONDITIONALCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70f90-115">頁首</span><span class="sxs-lookup"><span data-stu-id="70f90-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="70f90-116">屬性</span><span class="sxs-lookup"><span data-stu-id="70f90-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="70f90-117">名稱</span><span class="sxs-lookup"><span data-stu-id="70f90-117">Name</span></span></th>
<th><span data-ttu-id="70f90-118">描述</span><span class="sxs-lookup"><span data-stu-id="70f90-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="70f90-120"><a href="dn335060(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="70f90-120"><a href="dn335060(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="70f90-121">取得或設定條件式索引的選項。</span><span class="sxs-lookup"><span data-stu-id="70f90-121">Gets or sets the options for the conditional index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="70f90-123"><a href="dn335113(v=exchg.10).md">szColumnName</a></span><span class="sxs-lookup"><span data-stu-id="70f90-123"><a href="dn335113(v=exchg.10).md">szColumnName</a></span></span></td>
<td><span data-ttu-id="70f90-124">取得或設定條件式資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="70f90-124">Gets or sets the name of the conditional column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70f90-125">頁首</span><span class="sxs-lookup"><span data-stu-id="70f90-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="70f90-126">方法</span><span class="sxs-lookup"><span data-stu-id="70f90-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="70f90-127">名稱</span><span class="sxs-lookup"><span data-stu-id="70f90-127">Name</span></span></th>
<th><span data-ttu-id="70f90-128">描述</span><span class="sxs-lookup"><span data-stu-id="70f90-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-130"><a href="dn335109(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="70f90-130"><a href="dn335109(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="70f90-131">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="70f90-131">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-133"><a href="dn335108(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="70f90-133"><a href="dn335108(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="70f90-134">傳回物件的深層複本。</span><span class="sxs-lookup"><span data-stu-id="70f90-134">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="70f90-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="70f90-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="70f90-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="70f90-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="70f90-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="70f90-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="70f90-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="70f90-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="70f90-143"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="70f90-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="70f90-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="70f90-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="70f90-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="70f90-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="70f90-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="70f90-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="70f90-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="70f90-151"><a href="dn335058(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="70f90-151"><a href="dn335058(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="70f90-152">產生實例的字串表示。</span><span class="sxs-lookup"><span data-stu-id="70f90-152">Generate a string representation of the instance.</span></span> <span data-ttu-id="70f90-153"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="70f90-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70f90-154">頁首</span><span class="sxs-lookup"><span data-stu-id="70f90-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="70f90-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70f90-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70f90-156">參考</span><span class="sxs-lookup"><span data-stu-id="70f90-156">Reference</span></span>

[<span data-ttu-id="70f90-157">JET_CONDITIONALCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="70f90-157">JET_CONDITIONALCOLUMN class</span></span>](./jet-conditionalcolumn-class.md)

[<span data-ttu-id="70f90-158">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="70f90-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
