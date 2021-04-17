---
description: 深入瞭解： JET_RETINFO 屬性
title: JET_RETINFO 屬性
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565416"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="9ea3b-103">JET_RETINFO 屬性</span><span class="sxs-lookup"><span data-stu-id="9ea3b-103">JET_RETINFO properties</span></span>

<span data-ttu-id="9ea3b-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="9ea3b-104">Include protected members</span></span>  
<span data-ttu-id="9ea3b-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="9ea3b-105">Include inherited members</span></span>  

<span data-ttu-id="9ea3b-106">[JET_RETINFO](./jet-retinfo-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9ea3b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="9ea3b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9ea3b-108">名稱</span><span class="sxs-lookup"><span data-stu-id="9ea3b-108">Name</span></span></th>
<th><span data-ttu-id="9ea3b-109">描述</span><span class="sxs-lookup"><span data-stu-id="9ea3b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9ea3b-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="9ea3b-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="9ea3b-112">藉由將0傳遞為 JetRetrieveColumn 的 columnid，來取得所有標記的資料行時，取得已標記、多重值或稀疏資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9ea3b-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="9ea3b-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="9ea3b-115">取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a>或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="9ea3b-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="9ea3b-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="9ea3b-118">取得或設定多重值資料行中值的序號。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="9ea3b-119">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-119">The array of values is one-based.</span></span> <span data-ttu-id="9ea3b-120">第一個值是 sequence 1，不是0。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="9ea3b-121">如果 [記錄] 資料行只有一個值，則應該以 itagSequence 的形式傳遞1。</span><span class="sxs-lookup"><span data-stu-id="9ea3b-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ea3b-122">頁首</span><span class="sxs-lookup"><span data-stu-id="9ea3b-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9ea3b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ea3b-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ea3b-124">參考</span><span class="sxs-lookup"><span data-stu-id="9ea3b-124">Reference</span></span>

[<span data-ttu-id="9ea3b-125">JET_RETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="9ea3b-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="9ea3b-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9ea3b-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
