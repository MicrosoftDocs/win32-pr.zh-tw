---
description: 深入瞭解： JET_OPENTEMPORARYTABLE 屬性
title: 'JET_OPENTEMPORARYTABLE (的屬性，請) '
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561222"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="c4c1c-103">JET_OPENTEMPORARYTABLE 屬性</span><span class="sxs-lookup"><span data-stu-id="c4c1c-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="c4c1c-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="c4c1c-104">Include protected members</span></span>  
<span data-ttu-id="c4c1c-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="c4c1c-105">Include inherited members</span></span>  

<span data-ttu-id="c4c1c-106">[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="c4c1c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c4c1c-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="c4c1c-108">名稱</span><span class="sxs-lookup"><span data-stu-id="c4c1c-108">Name</span></span></th>
<th><span data-ttu-id="c4c1c-109">描述</span><span class="sxs-lookup"><span data-stu-id="c4c1c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="c4c1c-112">取得或設定表示指定資料列之索引鍵的大小上限。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="c4c1c-113">您可以設定最大索引鍵大小來控制如何截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="c4c1c-114">金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="c4c1c-115">如果此參數設定為0或255，則最大的索引鍵大小及其語義將會與 Windows Server 2003 所支援的最大金鑰大小保持一致。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="c4c1c-116">此參數也可以設定為較大的值，做為實例 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>之資料庫頁面大小的功能。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="c4c1c-117">如需詳細資訊，請參閱 <a href="dn335292(v=exchg.10).md">KeyMost</a> 。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="c4c1c-120">取得或設定將從任何變數 lengthcolumn 使用的最大資料量，以針對指定的資料列來建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="c4c1c-121">此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="c4c1c-122">這項限制是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-122">This limit is in bytes.</span></span> <span data-ttu-id="c4c1c-123">如果此參數為零或與 <a href="dn335290(v=exchg.10).md">cbKeyMost</a> 屬性相同，則沒有作用中的限制。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="c4c1c-126">取得或設定 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>中的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-128"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="c4c1c-129">取得或設定臨時表的選項。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="c4c1c-132">取得或設定要用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="c4c1c-133">當此參數為 null 時，預設的 LCID 將用來比較臨時表中的任何 Unicode 索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="c4c1c-134">預設的 LCID 是美國英文地區設定。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="c4c1c-135">當此參數為 null 時，將會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="c4c1c-136">預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="c4c1c-139">取得或設定在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="c4c1c-142">取得或設定輸出緩衝區，此緩衝區會接收建立臨時表時所產生之資料行識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="c4c1c-143">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="c4c1c-144">因此，這個緩衝區的大小必須對應到 <a href="dn351228(v=exchg.10).md">prgcolumndef</a>的大小。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="c4c1c-146"><a href="dn335293(v=exchg.10).md">tableid</a></span><span class="sxs-lookup"><span data-stu-id="c4c1c-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="c4c1c-147">取得在成功呼叫 JetOpenTemporaryTable 時所建立之臨時表的資料表控制碼。</span><span class="sxs-lookup"><span data-stu-id="c4c1c-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4c1c-148">頁首</span><span class="sxs-lookup"><span data-stu-id="c4c1c-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="c4c1c-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4c1c-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4c1c-150">參考</span><span class="sxs-lookup"><span data-stu-id="c4c1c-150">Reference</span></span>

[<span data-ttu-id="c4c1c-151">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="c4c1c-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="c4c1c-152">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="c4c1c-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
