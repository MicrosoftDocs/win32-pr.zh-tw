---
description: 深入瞭解： RetrieveColumn 方法
title: RetrieveColumn 方法
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694627"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="56a54-103">RetrieveColumn 方法</span><span class="sxs-lookup"><span data-stu-id="56a54-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="56a54-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="56a54-104">Include protected members</span></span>  
<span data-ttu-id="56a54-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="56a54-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="56a54-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="56a54-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="56a54-107">Name</span><span class="sxs-lookup"><span data-stu-id="56a54-107">Name</span></span></th>
<th><span data-ttu-id="56a54-108">描述</span><span class="sxs-lookup"><span data-stu-id="56a54-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="56a54-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID) </a></span><span class="sxs-lookup"><span data-stu-id="56a54-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="56a54-112">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="56a54-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="56a54-113">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="56a54-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="56a54-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit、JET_RETINFO) </a></span><span class="sxs-lookup"><span data-stu-id="56a54-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="56a54-117">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="56a54-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="56a54-118">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="56a54-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="56a54-119">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="56a54-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="56a54-120">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="56a54-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="56a54-121">除了取得實際的資料行值之外，JetRetrieveColumn 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。</span><span class="sxs-lookup"><span data-stu-id="56a54-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56a54-122">頁首</span><span class="sxs-lookup"><span data-stu-id="56a54-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="56a54-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56a54-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56a54-124">參考</span><span class="sxs-lookup"><span data-stu-id="56a54-124">Reference</span></span>

[<span data-ttu-id="56a54-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="56a54-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="56a54-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="56a54-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="56a54-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="56a54-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
