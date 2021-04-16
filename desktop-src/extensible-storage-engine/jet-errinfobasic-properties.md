---
description: 深入瞭解： JET_ERRINFOBASIC 屬性
title: 'JET_ERRINFOBASIC 的屬性 (Windows8) '
TOCTitle: JET_ERRINFOBASIC properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic_properties(v=EXCHG.10)
ms:contentKeyID: 55104303
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 10e22b582ac26146eae6a7a29b5207a76b17d551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555773"
---
# <a name="jet_errinfobasic-properties"></a><span data-ttu-id="bbb25-103">JET_ERRINFOBASIC 屬性</span><span class="sxs-lookup"><span data-stu-id="bbb25-103">JET_ERRINFOBASIC properties</span></span>

<span data-ttu-id="bbb25-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="bbb25-104">Include protected members</span></span>  
<span data-ttu-id="bbb25-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="bbb25-105">Include inherited members</span></span>  

<span data-ttu-id="bbb25-106">[JET_ERRINFOBASIC](./jet-errinfobasic-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="bbb25-106">The [JET_ERRINFOBASIC](./jet-errinfobasic-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="bbb25-107">屬性</span><span class="sxs-lookup"><span data-stu-id="bbb25-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="bbb25-108">名稱</span><span class="sxs-lookup"><span data-stu-id="bbb25-108">Name</span></span></th>
<th><span data-ttu-id="bbb25-109">描述</span><span class="sxs-lookup"><span data-stu-id="bbb25-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bbb25-111"><a href="dn335340(v=exchg.10).md">errcat</a></span><span class="sxs-lookup"><span data-stu-id="bbb25-111"><a href="dn335340(v=exchg.10).md">errcat</a></span></span></td>
<td><span data-ttu-id="bbb25-112">取得或設定錯誤的類別。</span><span class="sxs-lookup"><span data-stu-id="bbb25-112">Gets or sets the category of the error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bbb25-114"><a href="dn335344(v=exchg.10).md">errValue</a></span><span class="sxs-lookup"><span data-stu-id="bbb25-114"><a href="dn335344(v=exchg.10).md">errValue</a></span></span></td>
<td><span data-ttu-id="bbb25-115">取得或設定要求的資訊層級的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="bbb25-115">Gets or sets the error value for the requested info level.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bbb25-117"><a href="dn335472(v=exchg.10).md">lSourceLine</a></span><span class="sxs-lookup"><span data-stu-id="bbb25-117"><a href="dn335472(v=exchg.10).md">lSourceLine</a></span></span></td>
<td><span data-ttu-id="bbb25-118">取得或設定要求的資訊層級的原始程式檔行。</span><span class="sxs-lookup"><span data-stu-id="bbb25-118">Gets or sets the source file line for the requested info level.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bbb25-120"><a href="dn335345(v=exchg.10).md">rgCategoricalHierarchy</a></span><span class="sxs-lookup"><span data-stu-id="bbb25-120"><a href="dn335345(v=exchg.10).md">rgCategoricalHierarchy</a></span></span></td>
<td><span data-ttu-id="bbb25-121">取得或設定錯誤的階層。</span><span class="sxs-lookup"><span data-stu-id="bbb25-121">Gets or sets the hierarchy of errors.</span></span> <span data-ttu-id="bbb25-122">位置0是階層中最高的層級，而其餘的則是 JET_errcatUnknown。</span><span class="sxs-lookup"><span data-stu-id="bbb25-122">Position 0 is the highest level in the hierarchy, and the rest are JET_errcatUnknown.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="bbb25-124"><a href="dn335474(v=exchg.10).md">rgszSourceFile</a></span><span class="sxs-lookup"><span data-stu-id="bbb25-124"><a href="dn335474(v=exchg.10).md">rgszSourceFile</a></span></span></td>
<td><span data-ttu-id="bbb25-125">取得或設定要求的資訊層級的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="bbb25-125">Gets or sets the source file name for the requested info level.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbb25-126">頁首</span><span class="sxs-lookup"><span data-stu-id="bbb25-126">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="bbb25-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbb25-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bbb25-128">參考</span><span class="sxs-lookup"><span data-stu-id="bbb25-128">Reference</span></span>

[<span data-ttu-id="bbb25-129">JET_ERRINFOBASIC 類別</span><span class="sxs-lookup"><span data-stu-id="bbb25-129">JET_ERRINFOBASIC class</span></span>](./jet-errinfobasic-class.md)

[<span data-ttu-id="bbb25-130">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="bbb25-130">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
