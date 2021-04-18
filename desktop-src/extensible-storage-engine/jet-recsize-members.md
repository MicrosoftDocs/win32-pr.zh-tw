---
description: 深入瞭解： JET_RECSIZE 成員
title: 'JET_RECSIZE 成員 (的) '
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556733"
---
# <a name="jet_recsize-members"></a><span data-ttu-id="0d011-103">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="0d011-103">JET_RECSIZE members</span></span>

<span data-ttu-id="0d011-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="0d011-104">Include protected members</span></span>  
<span data-ttu-id="0d011-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="0d011-105">Include inherited members</span></span>  

<span data-ttu-id="0d011-106">[JetGetRecordSize (JET_SESID、JET_TABLEID、JET_RECSIZE、GetRecordSizeGrbit) ](./vistaapi.jetgetrecordsize-method.md)用來傳回有關使用者資料空間中記錄的使用需求、設定的資料行數目、值數目，以及 ESENT 記錄結構額外負荷空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="0d011-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="0d011-107">[JET_RECSIZE](./jet-recsize-structure2.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="0d011-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="0d011-108">屬性</span><span class="sxs-lookup"><span data-stu-id="0d011-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d011-109">名稱</span><span class="sxs-lookup"><span data-stu-id="0d011-109">Name</span></span></th>
<th><span data-ttu-id="0d011-110">描述</span><span class="sxs-lookup"><span data-stu-id="0d011-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="0d011-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="0d011-113">取得記錄中的使用者資料集。</span><span class="sxs-lookup"><span data-stu-id="0d011-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="0d011-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="0d011-116">取得記錄中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="0d011-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="0d011-117">如果沒有將內建的 long 值壓縮) ，這就會與 <a href="hh557581(v=exchg.10).md">cbData</a> 相同。</span><span class="sxs-lookup"><span data-stu-id="0d011-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="0d011-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="0d011-120">取得記錄中的使用者資料集，但儲存在長值樹狀目錄中。</span><span class="sxs-lookup"><span data-stu-id="0d011-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="0d011-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="0d011-123">取得完整值樹狀結構中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="0d011-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="0d011-124">如果沒有壓縮分隔的 long 值，就會與 <a href="hh557913(v=exchg.10).md">cbLongValueData</a> 相同。</span><span class="sxs-lookup"><span data-stu-id="0d011-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="0d011-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="0d011-127">取得長數值資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="0d011-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="0d011-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="0d011-130">取得此記錄之 ESENT 記錄結構的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="0d011-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="0d011-131">這包括記錄的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="0d011-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="0d011-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="0d011-134">取得已壓縮記錄中的資料行總數。</span><span class="sxs-lookup"><span data-stu-id="0d011-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="0d011-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="0d011-137">取得儲存在此記錄之完整值樹狀結構中的完整值總數。</span><span class="sxs-lookup"><span data-stu-id="0d011-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="0d011-138">這不包含內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="0d011-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="0d011-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="0d011-141">針對記錄中所有資料行的第一個資料行，取得超過第一個的總值總數。</span><span class="sxs-lookup"><span data-stu-id="0d011-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="0d011-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="0d011-144">取得在此記錄中設定的固定和變數資料行總數。</span><span class="sxs-lookup"><span data-stu-id="0d011-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="0d011-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="0d011-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="0d011-147">取得在此記錄中設定的標記資料行總數。</span><span class="sxs-lookup"><span data-stu-id="0d011-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d011-148">頁首</span><span class="sxs-lookup"><span data-stu-id="0d011-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="0d011-149">方法</span><span class="sxs-lookup"><span data-stu-id="0d011-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d011-150">名稱</span><span class="sxs-lookup"><span data-stu-id="0d011-150">Name</span></span></th>
<th><span data-ttu-id="0d011-151">描述</span><span class="sxs-lookup"><span data-stu-id="0d011-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-154"><a href="hh538879(v=exchg.10).md">加入</a></span><span class="sxs-lookup"><span data-stu-id="0d011-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="0d011-155">將大小新增至兩個 JET_RECSIZE 結構。</span><span class="sxs-lookup"><span data-stu-id="0d011-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0d011-157"><a href="hh558506(v=exchg.10).md">等於 (物件) </a></span><span class="sxs-lookup"><span data-stu-id="0d011-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="0d011-158">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="0d011-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="0d011-159"> (覆寫 <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (物件) </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="0d011-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0d011-161"><a href="hh577992(v=exchg.10).md">等於 (JET_RECSIZE) </a></span><span class="sxs-lookup"><span data-stu-id="0d011-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="0d011-162">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="0d011-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="0d011-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="0d011-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="0d011-165"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0d011-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0d011-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="0d011-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="0d011-168">傳回這個執行個體的雜湊碼。</span><span class="sxs-lookup"><span data-stu-id="0d011-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="0d011-169"> (覆寫 <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="0d011-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0d011-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="0d011-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="0d011-172"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0d011-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="0d011-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="0d011-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="0d011-175"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0d011-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-178"><a href="hh579561(v=exchg.10).md">減去</a></span><span class="sxs-lookup"><span data-stu-id="0d011-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="0d011-179">計算兩個 JET_RECSIZE 結構之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="0d011-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="0d011-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="0d011-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="0d011-182"> (繼承自 <a href="/dotnet/api/system.valuetype">ValueType</a>. ) </span><span class="sxs-lookup"><span data-stu-id="0d011-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d011-183">頁首</span><span class="sxs-lookup"><span data-stu-id="0d011-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="0d011-184">運算子</span><span class="sxs-lookup"><span data-stu-id="0d011-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0d011-185">Name</span><span class="sxs-lookup"><span data-stu-id="0d011-185">Name</span></span></th>
<th><span data-ttu-id="0d011-186">描述</span><span class="sxs-lookup"><span data-stu-id="0d011-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-189"><a href="hh578675(v=exchg.10).md">除了</a></span><span class="sxs-lookup"><span data-stu-id="0d011-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="0d011-190">將大小新增至兩個 JET_RECSIZE 結構。</span><span class="sxs-lookup"><span data-stu-id="0d011-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-193"><a href="hh596362(v=exchg.10).md">等式</a></span><span class="sxs-lookup"><span data-stu-id="0d011-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="0d011-194">判斷 JET_RECSIZE 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="0d011-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-197"><a href="hh578809(v=exchg.10).md">不等於</a></span><span class="sxs-lookup"><span data-stu-id="0d011-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="0d011-198">判斷 JET_RECSIZE 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="0d011-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="0d011-201"><a href="hh596696(v=exchg.10).md">減法</a></span><span class="sxs-lookup"><span data-stu-id="0d011-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="0d011-202">計算兩個 JET_RECSIZE 結構之間的大小差異。</span><span class="sxs-lookup"><span data-stu-id="0d011-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d011-203">頁首</span><span class="sxs-lookup"><span data-stu-id="0d011-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0d011-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d011-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d011-205">參考</span><span class="sxs-lookup"><span data-stu-id="0d011-205">Reference</span></span>

[<span data-ttu-id="0d011-206">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="0d011-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="0d011-207">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="0d011-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
