---
description: 深入瞭解： JET_INDEXCREATE 成員
title: JET_INDEXCREATE 成員
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194605"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="2ecee-103">JET_INDEXCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="2ecee-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="2ecee-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="2ecee-104">Include protected members</span></span>  
<span data-ttu-id="2ecee-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="2ecee-105">Include inherited members</span></span>  

<span data-ttu-id="2ecee-106">包含在 ESE 資料庫的資料上建立索引所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="2ecee-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="2ecee-107">包含在 ESE 資料庫的資料上建立索引所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="2ecee-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="2ecee-108">[JET_INDEXCREATE](./jet-indexcreate-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="2ecee-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="2ecee-109">建構函式</span><span class="sxs-lookup"><span data-stu-id="2ecee-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ecee-110">名稱</span><span class="sxs-lookup"><span data-stu-id="2ecee-110">Name</span></span></th>
<th><span data-ttu-id="2ecee-111">描述</span><span class="sxs-lookup"><span data-stu-id="2ecee-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ecee-114">頁首</span><span class="sxs-lookup"><span data-stu-id="2ecee-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="2ecee-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2ecee-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ecee-116">名稱</span><span class="sxs-lookup"><span data-stu-id="2ecee-116">Name</span></span></th>
<th><span data-ttu-id="2ecee-117">描述</span><span class="sxs-lookup"><span data-stu-id="2ecee-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="2ecee-120">取得或設定 szKey 的長度（以字元為單位），包括兩個終止的 null。</span><span class="sxs-lookup"><span data-stu-id="2ecee-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="2ecee-123">取得或設定索引中索引鍵允許的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ecee-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="2ecee-124">最小支援的金鑰大小為 JET_cbKeyMostMin (255) 這是舊版的最大金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="2ecee-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="2ecee-125">最大索引鍵大小取決於資料庫頁面大小 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>。</span><span class="sxs-lookup"><span data-stu-id="2ecee-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="2ecee-126">您可以使用 <a href="dn351156(v=exchg.10).md">KeyMost</a>抓取最大的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="2ecee-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="2ecee-127">Windows XP 和 Windows Server 2003 會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="2ecee-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2ecee-128">不同于非受控 API，不需要 <strong>IndexKeyMost () </strong> (JET_bitIndexKeyMost) ，它會自動加入。</span><span class="sxs-lookup"><span data-stu-id="2ecee-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="2ecee-131">取得或設定要儲存在索引中之每個資料行的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ecee-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="2ecee-134">取得或設定條件式資料行的數目。</span><span class="sxs-lookup"><span data-stu-id="2ecee-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-136"><a href="dn335157(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="2ecee-137">取得或設定建立此索引的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2ecee-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="2ecee-140">取得或設定索引建立選項。</span><span class="sxs-lookup"><span data-stu-id="2ecee-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="2ecee-143">取得或設定選擇性的 unicode 比較選項。</span><span class="sxs-lookup"><span data-stu-id="2ecee-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="2ecee-146">取得或設定空間配置、維護和使用方式提示。</span><span class="sxs-lookup"><span data-stu-id="2ecee-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="2ecee-149">取得或設定選擇性的條件式資料行。</span><span class="sxs-lookup"><span data-stu-id="2ecee-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="2ecee-152">取得或設定要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ecee-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-154"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="2ecee-155">取得或設定索引鍵的描述。</span><span class="sxs-lookup"><span data-stu-id="2ecee-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="2ecee-156">這是以 null 分隔之標記的雙 null 結束字串。</span><span class="sxs-lookup"><span data-stu-id="2ecee-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="2ecee-157">每個標記的格式都是 [方向規範] [資料行名稱]，其中的方向規格為 &quot; + &quot; 或 &quot; - &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2ecee-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="2ecee-158">例如， &quot; + abc\0-def\0 + ghi\0 的 szKey 會以 &quot; 遞增順序)  (的三個數據行來編制索引 &quot; &quot; ， &quot; &quot; 而 def (以遞減順序) 和 &quot; ghi &quot; (遞增順序) 。</span><span class="sxs-lookup"><span data-stu-id="2ecee-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="2ecee-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="2ecee-161">取得或設定索引的密度。</span><span class="sxs-lookup"><span data-stu-id="2ecee-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ecee-162">頁首</span><span class="sxs-lookup"><span data-stu-id="2ecee-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="2ecee-163">方法</span><span class="sxs-lookup"><span data-stu-id="2ecee-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ecee-164">名稱</span><span class="sxs-lookup"><span data-stu-id="2ecee-164">Name</span></span></th>
<th><span data-ttu-id="2ecee-165">描述</span><span class="sxs-lookup"><span data-stu-id="2ecee-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="2ecee-168">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="2ecee-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="2ecee-171">傳回物件的深層複本。</span><span class="sxs-lookup"><span data-stu-id="2ecee-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="2ecee-174"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2ecee-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="2ecee-177"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="2ecee-180"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="2ecee-183"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="2ecee-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="2ecee-186"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="2ecee-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="2ecee-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="2ecee-189">產生實例的字串表示。</span><span class="sxs-lookup"><span data-stu-id="2ecee-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="2ecee-190"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="2ecee-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ecee-191">頁首</span><span class="sxs-lookup"><span data-stu-id="2ecee-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2ecee-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ecee-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ecee-193">參考</span><span class="sxs-lookup"><span data-stu-id="2ecee-193">Reference</span></span>

[<span data-ttu-id="2ecee-194">JET_INDEXCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="2ecee-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="2ecee-195">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2ecee-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
