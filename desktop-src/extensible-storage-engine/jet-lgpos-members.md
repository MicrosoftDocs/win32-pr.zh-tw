---
description: 深入瞭解： JET_LGPOS 成員
title: JET_LGPOS 成員
TOCTitle: JET_LGPOS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_LGPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos_members(v=EXCHG.10)
ms:contentKeyID: 39516766
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4031a41fe521f6dceb6bb64b5bc8567afee97e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944699"
---
# <a name="jet_lgpos-members"></a><span data-ttu-id="9cdcb-103">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="9cdcb-103">JET_LGPOS members</span></span>

<span data-ttu-id="9cdcb-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="9cdcb-104">Include protected members</span></span>  
<span data-ttu-id="9cdcb-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="9cdcb-105">Include inherited members</span></span>  

<span data-ttu-id="9cdcb-106">描述記錄順序中的位移。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-106">Describes an offset in the log sequence.</span></span>

<span data-ttu-id="9cdcb-107">[JET_LGPOS](./jet-lgpos-structure2.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-107">The [JET_LGPOS](./jet-lgpos-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9cdcb-108">屬性</span><span class="sxs-lookup"><span data-stu-id="9cdcb-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9cdcb-109">名稱</span><span class="sxs-lookup"><span data-stu-id="9cdcb-109">Name</span></span></th>
<th><span data-ttu-id="9cdcb-110">描述</span><span class="sxs-lookup"><span data-stu-id="9cdcb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9cdcb-112"><a href="hh579511(v=exchg.10).md">601.Hasvalue</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-112"><a href="hh579511(v=exchg.10).md">HasValue</a></span></span></td>
<td><span data-ttu-id="9cdcb-113">取得值，指出此記錄檔的位置是否為 null。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-113">Gets a value indicating whether this log position is null.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9cdcb-115"><a href="hh565113(v=exchg.10).md">Ib</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-115"><a href="hh565113(v=exchg.10).md">ib</a></span></span></td>
<td><span data-ttu-id="9cdcb-116">取得或設定這個記錄位置所表示的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-116">Gets or sets the byte offset represented by this log position.</span></span> <span data-ttu-id="9cdcb-117">此位移是在磁區內。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-117">This offset is inside of the sector.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9cdcb-119"><a href="hh566270(v=exchg.10).md">isec</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-119"><a href="hh566270(v=exchg.10).md">isec</a></span></span></td>
<td><span data-ttu-id="9cdcb-120">取得或設定此記錄位置所表示的磁區編號。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-120">Gets or sets the sector number represented by this log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9cdcb-122"><a href="hh577855(v=exchg.10).md">lGeneration</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-122"><a href="hh577855(v=exchg.10).md">lGeneration</a></span></span></td>
<td><span data-ttu-id="9cdcb-123">取得或設定此記錄位置的產生。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-123">Gets or sets the generation of this log position.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9cdcb-124">頁首</span><span class="sxs-lookup"><span data-stu-id="9cdcb-124">Top</span></span>

## <a name="methods"></a><span data-ttu-id="9cdcb-125">方法</span><span class="sxs-lookup"><span data-stu-id="9cdcb-125">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9cdcb-126">名稱</span><span class="sxs-lookup"><span data-stu-id="9cdcb-126">Name</span></span></th>
<th><span data-ttu-id="9cdcb-127">描述</span><span class="sxs-lookup"><span data-stu-id="9cdcb-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-129"><a href="hh579485(v=exchg.10).md">CompareTo</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-129"><a href="hh579485(v=exchg.10).md">CompareTo</a></span></span></td>
<td><span data-ttu-id="9cdcb-130">將這個記錄檔位置與另一個記錄位置進行比較，並判斷這個實例是否在另一個實例之前、相同的或之後。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-130">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-132"><a href="hh565006(v=exchg.10).md">等於 (物件) </a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-132"><a href="hh565006(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="9cdcb-133">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-133">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="9cdcb-134"> (覆寫 <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (物件) </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-134">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-136"><a href="hh558574(v=exchg.10).md">等於 (JET_LGPOS) </a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-136"><a href="hh558574(v=exchg.10).md">Equals(JET_LGPOS)</a></span></span></td>
<td><span data-ttu-id="9cdcb-137">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-137">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="9cdcb-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="9cdcb-140"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-142"><a href="hh578422(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-142"><a href="hh578422(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="9cdcb-143">傳回這個執行個體的雜湊碼。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-143">Returns the hash code for this instance.</span></span> <span data-ttu-id="9cdcb-144"> (覆寫 <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-144">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-146"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-146"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="9cdcb-147"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-147">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="9cdcb-149"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-149"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="9cdcb-150"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-150">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="9cdcb-152"><a href="hh558225(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-152"><a href="hh558225(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="9cdcb-153">產生結構的字串表示。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-153">Generate a string representation of the structure.</span></span> <span data-ttu-id="9cdcb-154"> (覆寫 <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString"> () 的 ValueType。 </a>) </span><span class="sxs-lookup"><span data-stu-id="9cdcb-154">(Overrides <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9cdcb-155">頁首</span><span class="sxs-lookup"><span data-stu-id="9cdcb-155">Top</span></span>

## <a name="operators"></a><span data-ttu-id="9cdcb-156">運算子</span><span class="sxs-lookup"><span data-stu-id="9cdcb-156">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9cdcb-157">Name</span><span class="sxs-lookup"><span data-stu-id="9cdcb-157">Name</span></span></th>
<th><span data-ttu-id="9cdcb-158">描述</span><span class="sxs-lookup"><span data-stu-id="9cdcb-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-161"><a href="hh557134(v=exchg.10).md">等式</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-161"><a href="hh557134(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="9cdcb-162">判斷 JET_LGPOS 的兩個指定實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-162">Determines whether two specified instances of JET_LGPOS are equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-165"><a href="hh557121(v=exchg.10).md">GreaterThan</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-165"><a href="hh557121(v=exchg.10).md">GreaterThan</a></span></span></td>
<td><span data-ttu-id="9cdcb-166">判斷一個記錄檔位置是否位於另一個記錄檔位置之後。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-166">Determine whether one log position is after another log position.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-169"><a href="hh557469(v=exchg.10).md">GreaterThanOrEqual</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-169"><a href="hh557469(v=exchg.10).md">GreaterThanOrEqual</a></span></span></td>
<td><span data-ttu-id="9cdcb-170">判斷一個記錄檔位置是否位於或等於另一個記錄位置。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-170">Determine whether one log position is after or equal to another log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-173"><a href="hh564795(v=exchg.10).md">不等於</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-173"><a href="hh564795(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="9cdcb-174">判斷 JET_LGPOS 的兩個指定實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-174">Determines whether two specified instances of JET_LGPOS are not equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-177"><a href="hh577466(v=exchg.10).md">LessThan</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-177"><a href="hh577466(v=exchg.10).md">LessThan</a></span></span></td>
<td><span data-ttu-id="9cdcb-178">判斷一個記錄檔位置是否在另一個記錄位置之前。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-178">Determine whether one log position is before another log position.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="公用運算子" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9cdcb-181"><a href="hh557093(v=exchg.10).md">LessThanOrEqual</a></span><span class="sxs-lookup"><span data-stu-id="9cdcb-181"><a href="hh557093(v=exchg.10).md">LessThanOrEqual</a></span></span></td>
<td><span data-ttu-id="9cdcb-182">判斷一個記錄檔位置是否早于或等於另一個記錄位置。</span><span class="sxs-lookup"><span data-stu-id="9cdcb-182">Determine whether one log position is before or equal to another log position.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9cdcb-183">頁首</span><span class="sxs-lookup"><span data-stu-id="9cdcb-183">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9cdcb-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cdcb-184">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9cdcb-185">參考</span><span class="sxs-lookup"><span data-stu-id="9cdcb-185">Reference</span></span>

[<span data-ttu-id="9cdcb-186">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="9cdcb-186">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="9cdcb-187">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9cdcb-187">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
