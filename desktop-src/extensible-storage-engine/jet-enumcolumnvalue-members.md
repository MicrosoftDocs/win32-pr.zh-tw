---
description: 深入瞭解： JET_ENUMCOLUMNVALUE 成員
title: JET_ENUMCOLUMNVALUE 成員
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559603"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="7a2c5-103">JET_ENUMCOLUMNVALUE 成員</span><span class="sxs-lookup"><span data-stu-id="7a2c5-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="7a2c5-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="7a2c5-104">Include protected members</span></span>  
<span data-ttu-id="7a2c5-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="7a2c5-105">Include inherited members</span></span>  

<span data-ttu-id="7a2c5-106">使用 JetEnumerateColumns 函數來列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="7a2c5-107">[JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、 \[ \] 、int32、 \[ \] 、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) ](./api.jetenumeratecolumns-method.md)會傳回 JET_ENUMCOLUMNVALUE 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="7a2c5-108">陣列會在使用提供給該函式之回呼配置的記憶體中傳回。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="7a2c5-109">[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="7a2c5-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="7a2c5-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7a2c5-111">名稱</span><span class="sxs-lookup"><span data-stu-id="7a2c5-111">Name</span></span></th>
<th><span data-ttu-id="7a2c5-112">描述</span><span class="sxs-lookup"><span data-stu-id="7a2c5-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7a2c5-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a2c5-115">頁首</span><span class="sxs-lookup"><span data-stu-id="7a2c5-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="7a2c5-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7a2c5-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7a2c5-117">名稱</span><span class="sxs-lookup"><span data-stu-id="7a2c5-117">Name</span></span></th>
<th><span data-ttu-id="7a2c5-118">描述</span><span class="sxs-lookup"><span data-stu-id="7a2c5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="7a2c5-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="7a2c5-121">取得資料行的資料行值大小。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="7a2c5-123"><a href="dn335144(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="7a2c5-124">取得資料行值的列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="7a2c5-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="7a2c5-127">取得已列舉之以一為基) 的索引 (的資料行值。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="7a2c5-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="7a2c5-130">取得為數據行列舉的值。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a2c5-131">頁首</span><span class="sxs-lookup"><span data-stu-id="7a2c5-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="7a2c5-132">方法</span><span class="sxs-lookup"><span data-stu-id="7a2c5-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="7a2c5-133">名稱</span><span class="sxs-lookup"><span data-stu-id="7a2c5-133">Name</span></span></th>
<th><span data-ttu-id="7a2c5-134">描述</span><span class="sxs-lookup"><span data-stu-id="7a2c5-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7a2c5-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="7a2c5-137"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7a2c5-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="7a2c5-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7a2c5-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="7a2c5-143"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7a2c5-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="7a2c5-146"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="7a2c5-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="7a2c5-149"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="7a2c5-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="7a2c5-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="7a2c5-152">傳回表示目前<a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="7a2c5-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="7a2c5-153"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="7a2c5-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a2c5-154">頁首</span><span class="sxs-lookup"><span data-stu-id="7a2c5-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="7a2c5-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a2c5-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a2c5-156">參考</span><span class="sxs-lookup"><span data-stu-id="7a2c5-156">Reference</span></span>

[<span data-ttu-id="7a2c5-157">JET_ENUMCOLUMNVALUE 類別</span><span class="sxs-lookup"><span data-stu-id="7a2c5-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="7a2c5-158">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7a2c5-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
