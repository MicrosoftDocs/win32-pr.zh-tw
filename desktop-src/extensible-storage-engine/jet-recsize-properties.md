---
description: 深入瞭解： JET_RECSIZE 屬性
title: 'JET_RECSIZE (的屬性，請) '
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852828"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="88e81-103">JET_RECSIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="88e81-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="88e81-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="88e81-104">Include protected members</span></span>  
<span data-ttu-id="88e81-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="88e81-105">Include inherited members</span></span>  

<span data-ttu-id="88e81-106">[JET_RECSIZE](./jet-recsize-structure2.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="88e81-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="88e81-107">屬性</span><span class="sxs-lookup"><span data-stu-id="88e81-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="88e81-108">名稱</span><span class="sxs-lookup"><span data-stu-id="88e81-108">Name</span></span></th>
<th><span data-ttu-id="88e81-109">描述</span><span class="sxs-lookup"><span data-stu-id="88e81-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="88e81-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="88e81-112">取得記錄中的使用者資料集。</span><span class="sxs-lookup"><span data-stu-id="88e81-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="88e81-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="88e81-115">取得記錄中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="88e81-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="88e81-116">如果沒有將內建的 long 值壓縮) ，這就會與 <a href="hh557581(v=exchg.10).md">cbData</a> 相同。</span><span class="sxs-lookup"><span data-stu-id="88e81-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="88e81-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="88e81-119">取得記錄中的使用者資料集，但儲存在長值樹狀目錄中。</span><span class="sxs-lookup"><span data-stu-id="88e81-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="88e81-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="88e81-122">取得完整值樹狀結構中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="88e81-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="88e81-123">如果沒有壓縮分隔的 long 值，就會與 <a href="hh557913(v=exchg.10).md">cbLongValueData</a> 相同。</span><span class="sxs-lookup"><span data-stu-id="88e81-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="88e81-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="88e81-126">取得長數值資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="88e81-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="88e81-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="88e81-129">取得此記錄之 ESENT 記錄結構的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="88e81-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="88e81-130">這包括記錄的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="88e81-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="88e81-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="88e81-133">取得已壓縮記錄中的資料行總數。</span><span class="sxs-lookup"><span data-stu-id="88e81-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="88e81-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="88e81-136">取得儲存在此記錄之完整值樹狀結構中的完整值總數。</span><span class="sxs-lookup"><span data-stu-id="88e81-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="88e81-137">這不包含內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="88e81-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="88e81-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="88e81-140">針對記錄中所有資料行的第一個資料行，取得超過第一個的總值總數。</span><span class="sxs-lookup"><span data-stu-id="88e81-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="88e81-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="88e81-143">取得在此記錄中設定的固定和變數資料行總數。</span><span class="sxs-lookup"><span data-stu-id="88e81-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="88e81-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="88e81-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="88e81-146">取得在此記錄中設定的標記資料行總數。</span><span class="sxs-lookup"><span data-stu-id="88e81-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88e81-147">頁首</span><span class="sxs-lookup"><span data-stu-id="88e81-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="88e81-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88e81-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88e81-149">參考</span><span class="sxs-lookup"><span data-stu-id="88e81-149">Reference</span></span>

[<span data-ttu-id="88e81-150">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="88e81-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="88e81-151">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="88e81-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
