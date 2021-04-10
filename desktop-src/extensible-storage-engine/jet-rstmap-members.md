---
description: 深入瞭解： JET_RSTMAP 成員
title: JET_RSTMAP 成員
TOCTitle: JET_RSTMAP members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RSTMAP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstmap_members(v=EXCHG.10)
ms:contentKeyID: 55103832
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c12fa62a00fce9afe50f0c0408de4e5637b004a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847838"
---
# <a name="jet_rstmap-members"></a><span data-ttu-id="74104-103">JET_RSTMAP 成員</span><span class="sxs-lookup"><span data-stu-id="74104-103">JET_RSTMAP members</span></span>

<span data-ttu-id="74104-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="74104-104">Include protected members</span></span>  
<span data-ttu-id="74104-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="74104-105">Include inherited members</span></span>  

<span data-ttu-id="74104-106">在復原期間啟用儲存在交易記錄中的資料庫檔案路徑的對應。</span><span class="sxs-lookup"><span data-stu-id="74104-106">Enables the remapping of database file paths that are stored in the transaction logs during recovery.</span></span>

<span data-ttu-id="74104-107">[JET_RSTMAP](./jet-rstmap-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="74104-107">The [JET_RSTMAP](./jet-rstmap-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="74104-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="74104-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="74104-109">名稱</span><span class="sxs-lookup"><span data-stu-id="74104-109">Name</span></span></th>
<th><span data-ttu-id="74104-110">描述</span><span class="sxs-lookup"><span data-stu-id="74104-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-112"><a href="dn335250(v=exchg.10).md">JET_RSTMAP</a></span><span class="sxs-lookup"><span data-stu-id="74104-112"><a href="dn335250(v=exchg.10).md">JET_RSTMAP</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74104-113">頁首</span><span class="sxs-lookup"><span data-stu-id="74104-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="74104-114">屬性</span><span class="sxs-lookup"><span data-stu-id="74104-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="74104-115">名稱</span><span class="sxs-lookup"><span data-stu-id="74104-115">Name</span></span></th>
<th><span data-ttu-id="74104-116">描述</span><span class="sxs-lookup"><span data-stu-id="74104-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="74104-118"><a href="dn351049(v=exchg.10).md">szDatabaseName</a></span><span class="sxs-lookup"><span data-stu-id="74104-118"><a href="dn351049(v=exchg.10).md">szDatabaseName</a></span></span></td>
<td><span data-ttu-id="74104-119">取得或設定資料庫的舊名稱/路徑。</span><span class="sxs-lookup"><span data-stu-id="74104-119">Gets or sets the old name/path of the database.</span></span> <span data-ttu-id="74104-120">如果未變更，則可以是 null。</span><span class="sxs-lookup"><span data-stu-id="74104-120">Can be null if it is unchanged.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="74104-122"><a href="dn335254(v=exchg.10).md">szNewDatabaseName</a></span><span class="sxs-lookup"><span data-stu-id="74104-122"><a href="dn335254(v=exchg.10).md">szNewDatabaseName</a></span></span></td>
<td><span data-ttu-id="74104-123">取得或設定資料庫的目前名稱/路徑。</span><span class="sxs-lookup"><span data-stu-id="74104-123">Gets or sets the current name/path of the database.</span></span> <span data-ttu-id="74104-124">不得為 null。</span><span class="sxs-lookup"><span data-stu-id="74104-124">Must not be null.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74104-125">頁首</span><span class="sxs-lookup"><span data-stu-id="74104-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="74104-126">方法</span><span class="sxs-lookup"><span data-stu-id="74104-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="74104-127">名稱</span><span class="sxs-lookup"><span data-stu-id="74104-127">Name</span></span></th>
<th><span data-ttu-id="74104-128">描述</span><span class="sxs-lookup"><span data-stu-id="74104-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-130"><a href="dn335251(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="74104-130"><a href="dn335251(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="74104-131">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="74104-131">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-133"><a href="dn351047(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="74104-133"><a href="dn351047(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="74104-134">傳回物件的深層複本。</span><span class="sxs-lookup"><span data-stu-id="74104-134">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="74104-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="74104-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="74104-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="74104-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="74104-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="74104-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="74104-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="74104-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="74104-143"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="74104-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="74104-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="74104-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="74104-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="74104-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="74104-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="74104-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="74104-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="74104-151"><a href="dn351050(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="74104-151"><a href="dn351050(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="74104-152">傳回表示目前<a href="dn351048(v=exchg.10).md">JET_RSTMAP</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="74104-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351048(v=exchg.10).md">JET_RSTMAP</a>.</span></span> <span data-ttu-id="74104-153"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="74104-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74104-154">頁首</span><span class="sxs-lookup"><span data-stu-id="74104-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="74104-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74104-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74104-156">參考</span><span class="sxs-lookup"><span data-stu-id="74104-156">Reference</span></span>

[<span data-ttu-id="74104-157">JET_RSTMAP 類別</span><span class="sxs-lookup"><span data-stu-id="74104-157">JET_RSTMAP class</span></span>](./jet-rstmap-class.md)

[<span data-ttu-id="74104-158">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="74104-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
