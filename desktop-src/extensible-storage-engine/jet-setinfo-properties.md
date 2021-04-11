---
description: 深入瞭解： JET_SETINFO 屬性
title: JET_SETINFO 屬性
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112532"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="e08ad-103">JET_SETINFO 屬性</span><span class="sxs-lookup"><span data-stu-id="e08ad-103">JET_SETINFO properties</span></span>

<span data-ttu-id="e08ad-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="e08ad-104">Include protected members</span></span>  
<span data-ttu-id="e08ad-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="e08ad-105">Include inherited members</span></span>  

<span data-ttu-id="e08ad-106">[JET_SETINFO](./jet-setinfo-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="e08ad-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="e08ad-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e08ad-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e08ad-108">名稱</span><span class="sxs-lookup"><span data-stu-id="e08ad-108">Name</span></span></th>
<th><span data-ttu-id="e08ad-109">描述</span><span class="sxs-lookup"><span data-stu-id="e08ad-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="e08ad-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="e08ad-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="e08ad-112">取得或設定要在 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中設定之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="e08ad-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="e08ad-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="e08ad-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="e08ad-115">取得或設定要設定之多重值資料行中的值順序。</span><span class="sxs-lookup"><span data-stu-id="e08ad-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="e08ad-116">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="e08ad-116">The array of values is one-based.</span></span> <span data-ttu-id="e08ad-117">第一個值是 sequence 1，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="e08ad-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="e08ad-118">如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。</span><span class="sxs-lookup"><span data-stu-id="e08ad-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="e08ad-119">值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="e08ad-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e08ad-120">頁首</span><span class="sxs-lookup"><span data-stu-id="e08ad-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e08ad-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e08ad-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e08ad-122">參考</span><span class="sxs-lookup"><span data-stu-id="e08ad-122">Reference</span></span>

[<span data-ttu-id="e08ad-123">JET_SETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="e08ad-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="e08ad-124">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e08ad-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
