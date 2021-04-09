---
description: 深入瞭解： JET_ENUMCOLUMN 屬性
title: JET_ENUMCOLUMN 屬性
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847998"
---
# <a name="jet_enumcolumn-properties"></a><span data-ttu-id="6507b-103">JET_ENUMCOLUMN 屬性</span><span class="sxs-lookup"><span data-stu-id="6507b-103">JET_ENUMCOLUMN properties</span></span>

<span data-ttu-id="6507b-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="6507b-104">Include protected members</span></span>  
<span data-ttu-id="6507b-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="6507b-105">Include inherited members</span></span>  

<span data-ttu-id="6507b-106">[JET_ENUMCOLUMN](./jet-enumcolumn-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="6507b-106">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="6507b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="6507b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6507b-108">名稱</span><span class="sxs-lookup"><span data-stu-id="6507b-108">Name</span></span></th>
<th><span data-ttu-id="6507b-109">描述</span><span class="sxs-lookup"><span data-stu-id="6507b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-111"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="6507b-111"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="6507b-112">取得為數據行列舉之值的大小。</span><span class="sxs-lookup"><span data-stu-id="6507b-112">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="6507b-113">只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="6507b-113">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-115"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="6507b-115"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="6507b-116">取得針對資料行列舉的資料行值數目。</span><span class="sxs-lookup"><span data-stu-id="6507b-116">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="6507b-117">只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="6507b-117">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-119"><a href="dn335135(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="6507b-119"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="6507b-120">取得已列舉的 columnid 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6507b-120">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-122"><a href="dn335086(v=exchg.10).md">犯 錯</a></span><span class="sxs-lookup"><span data-stu-id="6507b-122"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="6507b-123">取得列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="6507b-123">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-125"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="6507b-125"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="6507b-126">取得為數據行列舉的值。</span><span class="sxs-lookup"><span data-stu-id="6507b-126">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="6507b-127">只有當 <a href="dn335086(v=exchg.10).md">err</a> 等於 <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="6507b-127">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="6507b-128">這會指向傳遞給<a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、[]、int32、[]、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) </a>的<a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a>配置器回呼所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6507b-128">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="6507b-129">請記得在完成時釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="6507b-129">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="6507b-131"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="6507b-131"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="6507b-132">取得資料行的列舉資料行值。</span><span class="sxs-lookup"><span data-stu-id="6507b-132">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="6507b-133">只有在未<a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> <a href="dn335086(v=exchg.10).md">err</a>時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="6507b-133">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6507b-134">頁首</span><span class="sxs-lookup"><span data-stu-id="6507b-134">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6507b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6507b-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6507b-136">參考</span><span class="sxs-lookup"><span data-stu-id="6507b-136">Reference</span></span>

[<span data-ttu-id="6507b-137">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="6507b-137">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="6507b-138">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6507b-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
