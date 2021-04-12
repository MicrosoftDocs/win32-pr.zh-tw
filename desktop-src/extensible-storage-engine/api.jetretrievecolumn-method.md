---
description: 深入瞭解： JetRetrieveColumn 方法
title: JetRetrieveColumn 方法
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195213"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="9aafe-103">JetRetrieveColumn 方法</span><span class="sxs-lookup"><span data-stu-id="9aafe-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="9aafe-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="9aafe-104">Include protected members</span></span>  
<span data-ttu-id="9aafe-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="9aafe-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="9aafe-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="9aafe-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9aafe-107">Name</span><span class="sxs-lookup"><span data-stu-id="9aafe-107">Name</span></span></th>
<th><span data-ttu-id="9aafe-108">描述</span><span class="sxs-lookup"><span data-stu-id="9aafe-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9aafe-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、[]、Int32、Int32、RetrieveColumnGrbit、JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="9aafe-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="9aafe-112">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="9aafe-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="9aafe-113">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="9aafe-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="9aafe-114">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="9aafe-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="9aafe-115">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="9aafe-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="9aafe-116">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="9aafe-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="9aafe-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID，JET_TABLEID，JET_COLUMNID，[]，Int32，Int32，Int32，RetrieveColumnGrbit，JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="9aafe-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="9aafe-120">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="9aafe-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="9aafe-121">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="9aafe-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="9aafe-122">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="9aafe-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="9aafe-123">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="9aafe-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="9aafe-124">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="9aafe-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9aafe-125">頁首</span><span class="sxs-lookup"><span data-stu-id="9aafe-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9aafe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aafe-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9aafe-127">參考</span><span class="sxs-lookup"><span data-stu-id="9aafe-127">Reference</span></span>

[<span data-ttu-id="9aafe-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="9aafe-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9aafe-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="9aafe-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9aafe-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9aafe-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
