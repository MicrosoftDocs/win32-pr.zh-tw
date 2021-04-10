---
description: 深入瞭解： JET_COLUMNDEF 屬性
title: JET_COLUMNDEF 屬性
TOCTitle: JET_COLUMNDEF properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef_properties(v=EXCHG.10)
ms:contentKeyID: 55103489
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e39b0d2f86517c4fb6cab98a0127bc6827977adc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194304"
---
# <a name="jet_columndef-properties"></a><span data-ttu-id="10391-103">JET_COLUMNDEF 屬性</span><span class="sxs-lookup"><span data-stu-id="10391-103">JET_COLUMNDEF properties</span></span>

<span data-ttu-id="10391-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="10391-104">Include protected members</span></span>  
<span data-ttu-id="10391-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="10391-105">Include inherited members</span></span>  

<span data-ttu-id="10391-106">[JET_COLUMNDEF](./jet-columndef-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="10391-106">The [JET_COLUMNDEF](./jet-columndef-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="10391-107">屬性</span><span class="sxs-lookup"><span data-stu-id="10391-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="10391-108">名稱</span><span class="sxs-lookup"><span data-stu-id="10391-108">Name</span></span></th>
<th><span data-ttu-id="10391-109">描述</span><span class="sxs-lookup"><span data-stu-id="10391-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="10391-111"><a href="dn335080(v=exchg.10).md">cbMax</a></span><span class="sxs-lookup"><span data-stu-id="10391-111"><a href="dn335080(v=exchg.10).md">cbMax</a></span></span></td>
<td><span data-ttu-id="10391-112">取得或設定資料行的最大長度。</span><span class="sxs-lookup"><span data-stu-id="10391-112">Gets or sets the maximum length of the column.</span></span> <span data-ttu-id="10391-113">只有 <a href="hh577895(v=exchg.10).md">Text</a>、 <a href="hh577895(v=exchg.10).md">LongText</a>、 <a href="hh577895(v=exchg.10).md">Binary</a> 和 <a href="hh577895(v=exchg.10).md">LongBinary</a>類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="10391-113">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LongText</a>, <a href="hh577895(v=exchg.10).md">Binary</a> and <a href="hh577895(v=exchg.10).md">LongBinary</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="10391-115"><a href="dn335041(v=exchg.10).md">coltyp</a></span><span class="sxs-lookup"><span data-stu-id="10391-115"><a href="dn335041(v=exchg.10).md">coltyp</a></span></span></td>
<td><span data-ttu-id="10391-116">取得或設定資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="10391-116">Gets or sets type of the column.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="10391-118"><a href="dn335079(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="10391-118"><a href="dn335079(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="10391-119">取得資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="10391-119">Gets the columnid of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="10391-121"><a href="dn335044(v=exchg.10).md">cp</a></span><span class="sxs-lookup"><span data-stu-id="10391-121"><a href="dn335044(v=exchg.10).md">cp</a></span></span></td>
<td><span data-ttu-id="10391-122">取得或設定資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="10391-122">Gets or sets code page of the column.</span></span> <span data-ttu-id="10391-123">只有 <a href="hh577895(v=exchg.10).md">Text</a> 和 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="10391-123">This is only meaningful for columns of type <a href="hh577895(v=exchg.10).md">Text</a> and <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="10391-125"><a href="dn335043(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="10391-125"><a href="dn335043(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="10391-126">取得或設定資料行選項。</span><span class="sxs-lookup"><span data-stu-id="10391-126">Gets or sets the column options.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10391-127">頁首</span><span class="sxs-lookup"><span data-stu-id="10391-127">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="10391-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10391-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10391-129">參考</span><span class="sxs-lookup"><span data-stu-id="10391-129">Reference</span></span>

[<span data-ttu-id="10391-130">JET_COLUMNDEF 類別</span><span class="sxs-lookup"><span data-stu-id="10391-130">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="10391-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="10391-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
