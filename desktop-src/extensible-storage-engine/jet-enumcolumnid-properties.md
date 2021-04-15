---
description: 深入瞭解： JET_ENUMCOLUMNID 屬性
title: JET_ENUMCOLUMNID 屬性
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510938"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="02733-103">JET_ENUMCOLUMNID 屬性</span><span class="sxs-lookup"><span data-stu-id="02733-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="02733-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="02733-104">Include protected members</span></span>  
<span data-ttu-id="02733-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="02733-105">Include inherited members</span></span>  

<span data-ttu-id="02733-106">[JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="02733-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="02733-107">屬性</span><span class="sxs-lookup"><span data-stu-id="02733-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="02733-108">名稱</span><span class="sxs-lookup"><span data-stu-id="02733-108">Name</span></span></th>
<th><span data-ttu-id="02733-109">描述</span><span class="sxs-lookup"><span data-stu-id="02733-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="02733-111"><a href="dn335141(v=exchg.10).md">columnid</a></span><span class="sxs-lookup"><span data-stu-id="02733-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="02733-112">取得或設定要列舉的 columnid 識別碼。</span><span class="sxs-lookup"><span data-stu-id="02733-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="02733-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="02733-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="02733-115">取得或設定以一為基礎的索引) 所 (的資料行值計數，以列舉指定的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="02733-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="02733-116">如果 ctagSequence 為 0 (零) 則會忽略 rgtagSequence，並且會列舉指定之資料行識別碼的所有資料行值。</span><span class="sxs-lookup"><span data-stu-id="02733-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="02733-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="02733-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="02733-119">取得或設定指定資料行的資料行值陣列中，以一個為基底的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="02733-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="02733-120">單一元素是 JET_RETRIEVECOLUMN 中定義的 itagSequence。</span><span class="sxs-lookup"><span data-stu-id="02733-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="02733-121">ItagSequence 0 (零) 表示 &quot; skip &quot; 。</span><span class="sxs-lookup"><span data-stu-id="02733-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="02733-122">1的 itagSequence 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="02733-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02733-123">頁首</span><span class="sxs-lookup"><span data-stu-id="02733-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="02733-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02733-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02733-125">參考</span><span class="sxs-lookup"><span data-stu-id="02733-125">Reference</span></span>

[<span data-ttu-id="02733-126">JET_ENUMCOLUMNID 類別</span><span class="sxs-lookup"><span data-stu-id="02733-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="02733-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="02733-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
