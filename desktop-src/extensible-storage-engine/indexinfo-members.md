---
description: 深入瞭解： IndexInfo 成員
title: IndexInfo 成員
TOCTitle: IndexInfo members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.IndexInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103271
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: abda2eab4a258c5bdc32c77132ac749af31be450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850740"
---
# <a name="indexinfo-members"></a><span data-ttu-id="32a51-103">IndexInfo 成員</span><span class="sxs-lookup"><span data-stu-id="32a51-103">IndexInfo members</span></span>

<span data-ttu-id="32a51-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="32a51-104">Include protected members</span></span>  
<span data-ttu-id="32a51-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="32a51-105">Include inherited members</span></span>  

<span data-ttu-id="32a51-106">一個 esent 索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="32a51-106">Information about one esent index.</span></span> <span data-ttu-id="32a51-107">這不是 interop 類別，而是由中繼資料 helper 方法所使用。</span><span class="sxs-lookup"><span data-stu-id="32a51-107">This is not an interop class, but is used by the meta-data helper methods.</span></span>

<span data-ttu-id="32a51-108">[IndexInfo](./indexinfo-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="32a51-108">The [IndexInfo](./indexinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="32a51-109">屬性</span><span class="sxs-lookup"><span data-stu-id="32a51-109">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="32a51-110">名稱</span><span class="sxs-lookup"><span data-stu-id="32a51-110">Name</span></span></th>
<th><span data-ttu-id="32a51-111">描述</span><span class="sxs-lookup"><span data-stu-id="32a51-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-113"><a href="dn350908(v=exchg.10).md">CompareOptions</a></span><span class="sxs-lookup"><span data-stu-id="32a51-113"><a href="dn350908(v=exchg.10).md">CompareOptions</a></span></span></td>
<td><span data-ttu-id="32a51-114">取得索引的 CompareOptions。</span><span class="sxs-lookup"><span data-stu-id="32a51-114">Gets the CompareOptions for the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-116"><a href="dn350921(v=exchg.10).md">CultureInfo</a></span><span class="sxs-lookup"><span data-stu-id="32a51-116"><a href="dn350921(v=exchg.10).md">CultureInfo</a></span></span></td>
<td><span data-ttu-id="32a51-117">取得索引排序依據的 CultureInfo。</span><span class="sxs-lookup"><span data-stu-id="32a51-117">Gets the CultureInfo the index is sorted by.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-119"><a href="dn350907(v=exchg.10).md">項目</a></span><span class="sxs-lookup"><span data-stu-id="32a51-119"><a href="dn350907(v=exchg.10).md">Entries</a></span></span></td>
<td><span data-ttu-id="32a51-120">取得索引中的專案數。</span><span class="sxs-lookup"><span data-stu-id="32a51-120">Gets the number of entries in the index.</span></span> <span data-ttu-id="32a51-121">此值不是最新值，而且只會由 JetComputeStats 更新。</span><span class="sxs-lookup"><span data-stu-id="32a51-121">This value is not current and is only is updated by Api.JetComputeStats.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-123"><a href="dn350925(v=exchg.10).md">Grbit</a></span><span class="sxs-lookup"><span data-stu-id="32a51-123"><a href="dn350925(v=exchg.10).md">Grbit</a></span></span></td>
<td><span data-ttu-id="32a51-124">取得索引選項。</span><span class="sxs-lookup"><span data-stu-id="32a51-124">Gets the index options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-126"><a href="dn350910(v=exchg.10).md">IndexSegments</a></span><span class="sxs-lookup"><span data-stu-id="32a51-126"><a href="dn350910(v=exchg.10).md">IndexSegments</a></span></span></td>
<td><span data-ttu-id="32a51-127">取得索引的區段。</span><span class="sxs-lookup"><span data-stu-id="32a51-127">Gets the segments of the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-129"><a href="dn350926(v=exchg.10).md">[索引鍵]</a></span><span class="sxs-lookup"><span data-stu-id="32a51-129"><a href="dn350926(v=exchg.10).md">Keys</a></span></span></td>
<td><span data-ttu-id="32a51-130">取得索引中的唯一索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="32a51-130">Gets the number of unique keys in the index.</span></span> <span data-ttu-id="32a51-131">此值不是最新值，而且只會由 JetComputeStats 更新。</span><span class="sxs-lookup"><span data-stu-id="32a51-131">This value is not current and is only is updated by Api.JetComputeStats.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-133"><a href="dn350911(v=exchg.10).md">名稱</a></span><span class="sxs-lookup"><span data-stu-id="32a51-133"><a href="dn350911(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="32a51-134">取得索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a51-134">Gets the name of the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="32a51-136"><a href="dn350928(v=exchg.10).md">頁面</a></span><span class="sxs-lookup"><span data-stu-id="32a51-136"><a href="dn350928(v=exchg.10).md">Pages</a></span></span></td>
<td><span data-ttu-id="32a51-137">取得索引中的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="32a51-137">Gets the number of pages in the index.</span></span> <span data-ttu-id="32a51-138">此值不是最新值，而且只會由 JetComputeStats 更新。</span><span class="sxs-lookup"><span data-stu-id="32a51-138">This value is not current and is only is updated by Api.JetComputeStats.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32a51-139">頁首</span><span class="sxs-lookup"><span data-stu-id="32a51-139">Top</span></span>

## <a name="methods"></a><span data-ttu-id="32a51-140">方法</span><span class="sxs-lookup"><span data-stu-id="32a51-140">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="32a51-141">名稱</span><span class="sxs-lookup"><span data-stu-id="32a51-141">Name</span></span></th>
<th><span data-ttu-id="32a51-142">描述</span><span class="sxs-lookup"><span data-stu-id="32a51-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="32a51-144"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="32a51-144"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="32a51-145"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="32a51-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="32a51-147"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="32a51-147"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="32a51-148"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="32a51-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="32a51-150"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="32a51-150"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="32a51-151"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="32a51-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="32a51-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="32a51-153"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="32a51-154"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="32a51-154">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="32a51-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="32a51-156"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="32a51-157"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="32a51-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="32a51-159"><a href="dn350905(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="32a51-159"><a href="dn350905(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="32a51-160">傳回表示目前<a href="dn350919(v=exchg.10).md">IndexInfo</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="32a51-160">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350919(v=exchg.10).md">IndexInfo</a>.</span></span> <span data-ttu-id="32a51-161"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="32a51-161">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32a51-162">頁首</span><span class="sxs-lookup"><span data-stu-id="32a51-162">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="32a51-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32a51-163">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32a51-164">參考</span><span class="sxs-lookup"><span data-stu-id="32a51-164">Reference</span></span>

[<span data-ttu-id="32a51-165">IndexInfo 類別</span><span class="sxs-lookup"><span data-stu-id="32a51-165">IndexInfo class</span></span>](./indexinfo-class.md)

[<span data-ttu-id="32a51-166">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="32a51-166">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
