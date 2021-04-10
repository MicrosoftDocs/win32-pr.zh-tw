---
description: 深入瞭解： JET_RETRIEVECOLUMN 屬性
title: JET_RETRIEVECOLUMN 屬性
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694312"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="3d6ec-103">JET_RETRIEVECOLUMN 屬性</span><span class="sxs-lookup"><span data-stu-id="3d6ec-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="3d6ec-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="3d6ec-104">Include protected members</span></span>  
<span data-ttu-id="3d6ec-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="3d6ec-105">Include inherited members</span></span>  

<span data-ttu-id="3d6ec-106">[JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="3d6ec-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3d6ec-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3d6ec-108">名稱</span><span class="sxs-lookup"><span data-stu-id="3d6ec-108">Name</span></span></th>
<th><span data-ttu-id="3d6ec-109">描述</span><span class="sxs-lookup"><span data-stu-id="3d6ec-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="3d6ec-112">取得抓取資料行作業抓取之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="3d6ec-115">取得或設定 <a href="dn351040(v=exchg.10).md">pvData</a> 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="3d6ec-116">抓取資料行作業將不會在 pvData 中儲存比 cbData 更多的資料。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-118"><a href="dn335230(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="3d6ec-119">取得或設定要取得之資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="3d6ec-122">藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-124"><a href="dn335231(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="3d6ec-125">取得從資料行抓取傳回的警告。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="3d6ec-128">取得或設定資料行抓取的選項。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-130"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="3d6ec-131">取得或設定資料將儲存在緩衝區中的位移。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="3d6ec-134">取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="3d6ec-137">取得或設定包含在多值資料行中之值的序號。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="3d6ec-138">如果 itagSequence 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3d6ec-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="3d6ec-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="3d6ec-141">取得或設定將儲存從資料行取出之資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3d6ec-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d6ec-142">頁首</span><span class="sxs-lookup"><span data-stu-id="3d6ec-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3d6ec-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d6ec-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d6ec-144">參考</span><span class="sxs-lookup"><span data-stu-id="3d6ec-144">Reference</span></span>

[<span data-ttu-id="3d6ec-145">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="3d6ec-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="3d6ec-146">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3d6ec-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
