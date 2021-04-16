---
description: 深入瞭解： JET_OPENTEMPORARYTABLE 成員
title: 'JET_OPENTEMPORARYTABLE 成員 (的) '
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556960"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="f72da-103">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="f72da-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="f72da-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="f72da-104">Include protected members</span></span>  
<span data-ttu-id="f72da-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="f72da-105">Include inherited members</span></span>  

<span data-ttu-id="f72da-106">JetOpenTemporaryTable 方法的參數集合。</span><span class="sxs-lookup"><span data-stu-id="f72da-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="f72da-107">[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="f72da-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="f72da-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="f72da-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f72da-109">名稱</span><span class="sxs-lookup"><span data-stu-id="f72da-109">Name</span></span></th>
<th><span data-ttu-id="f72da-110">描述</span><span class="sxs-lookup"><span data-stu-id="f72da-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="f72da-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="f72da-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f72da-113">頁首</span><span class="sxs-lookup"><span data-stu-id="f72da-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="f72da-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f72da-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f72da-115">名稱</span><span class="sxs-lookup"><span data-stu-id="f72da-115">Name</span></span></th>
<th><span data-ttu-id="f72da-116">描述</span><span class="sxs-lookup"><span data-stu-id="f72da-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="f72da-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="f72da-119">取得或設定表示指定資料列之索引鍵的大小上限。</span><span class="sxs-lookup"><span data-stu-id="f72da-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="f72da-120">您可以設定最大索引鍵大小來控制如何截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="f72da-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="f72da-121">金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。</span><span class="sxs-lookup"><span data-stu-id="f72da-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="f72da-122">如果此參數設定為0或255，則最大的索引鍵大小及其語義將會與 Windows Server 2003 所支援的最大金鑰大小保持一致。</span><span class="sxs-lookup"><span data-stu-id="f72da-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="f72da-123">此參數也可以設定為較大的值，做為實例 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>之資料庫頁面大小的功能。</span><span class="sxs-lookup"><span data-stu-id="f72da-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="f72da-124">如需詳細資訊，請參閱 <a href="dn335292(v=exchg.10).md">KeyMost</a> 。</span><span class="sxs-lookup"><span data-stu-id="f72da-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="f72da-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="f72da-127">取得或設定將從任何變數 lengthcolumn 使用的最大資料量，以針對指定的資料列來建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f72da-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="f72da-128">此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。</span><span class="sxs-lookup"><span data-stu-id="f72da-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="f72da-129">這項限制是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="f72da-129">This limit is in bytes.</span></span> <span data-ttu-id="f72da-130">如果此參數為零或與 <a href="dn335290(v=exchg.10).md">cbKeyMost</a> 屬性相同，則沒有作用中的限制。</span><span class="sxs-lookup"><span data-stu-id="f72da-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="f72da-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="f72da-133">取得或設定 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="f72da-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="f72da-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="f72da-136">取得或設定臨時表的選項。</span><span class="sxs-lookup"><span data-stu-id="f72da-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="f72da-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="f72da-139">取得或設定要用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="f72da-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="f72da-140">當此參數為 null 時，預設的 LCID 將用來比較臨時表中的任何 Unicode 索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="f72da-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="f72da-141">預設的 LCID 是美國英文地區設定。</span><span class="sxs-lookup"><span data-stu-id="f72da-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="f72da-142">當此參數為 null 時，將會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="f72da-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="f72da-143">預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="f72da-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="f72da-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="f72da-146">取得或設定在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="f72da-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="f72da-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="f72da-149">取得或設定輸出緩衝區，此緩衝區會接收建立臨時表時所產生之資料行識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="f72da-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="f72da-150">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="f72da-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="f72da-151">因此，這個緩衝區的大小必須對應到 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>的大小。</span><span class="sxs-lookup"><span data-stu-id="f72da-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="f72da-153"><a href="dn335293(v=exchg.10).md">tableid</a></span><span class="sxs-lookup"><span data-stu-id="f72da-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="f72da-154">取得在成功呼叫 JetOpenTemporaryTable 時所建立之臨時表的資料表控制碼。</span><span class="sxs-lookup"><span data-stu-id="f72da-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f72da-155">頁首</span><span class="sxs-lookup"><span data-stu-id="f72da-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="f72da-156">方法</span><span class="sxs-lookup"><span data-stu-id="f72da-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f72da-157">名稱</span><span class="sxs-lookup"><span data-stu-id="f72da-157">Name</span></span></th>
<th><span data-ttu-id="f72da-158">描述</span><span class="sxs-lookup"><span data-stu-id="f72da-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="f72da-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">等於</a></span><span class="sxs-lookup"><span data-stu-id="f72da-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="f72da-161"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="f72da-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="f72da-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">完成</a></span><span class="sxs-lookup"><span data-stu-id="f72da-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="f72da-164"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="f72da-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="f72da-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="f72da-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="f72da-167"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="f72da-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="f72da-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="f72da-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="f72da-170"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="f72da-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="受保護的方法" alt="Protected method" /></td>
<td><span data-ttu-id="f72da-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="f72da-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="f72da-173"> (繼承自 <a href="/dotnet/api/system.object">Object</a>. ) </span><span class="sxs-lookup"><span data-stu-id="f72da-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /></td>
<td><span data-ttu-id="f72da-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="f72da-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="f72da-176">傳回表示目前<a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>的<a href="/dotnet/api/system.string">字串</a>。</span><span class="sxs-lookup"><span data-stu-id="f72da-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="f72da-177"> (會覆寫 <a href="/dotnet/api/system.object.tostring#System_Object_ToString">物件 ToString () </a>。 ) </span><span class="sxs-lookup"><span data-stu-id="f72da-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f72da-178">頁首</span><span class="sxs-lookup"><span data-stu-id="f72da-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f72da-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f72da-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f72da-180">參考</span><span class="sxs-lookup"><span data-stu-id="f72da-180">Reference</span></span>

[<span data-ttu-id="f72da-181">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="f72da-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="f72da-182">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="f72da-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
