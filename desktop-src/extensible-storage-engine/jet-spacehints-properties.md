---
description: 深入瞭解： JET_SPACEHINTS 屬性
title: JET_SPACEHINTS 屬性
TOCTitle: JET_SPACEHINTS properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints_properties(v=EXCHG.10)
ms:contentKeyID: 55103923
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f361e0a1fbcf8057ae900e57846cce8457489398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565013"
---
# <a name="jet_spacehints-properties"></a><span data-ttu-id="3013b-103">JET_SPACEHINTS 屬性</span><span class="sxs-lookup"><span data-stu-id="3013b-103">JET_SPACEHINTS properties</span></span>

<span data-ttu-id="3013b-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="3013b-104">Include protected members</span></span>  
<span data-ttu-id="3013b-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="3013b-105">Include inherited members</span></span>  

<span data-ttu-id="3013b-106">[JET_SPACEHINTS](./jet-spacehints-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="3013b-106">The [JET_SPACEHINTS](./jet-spacehints-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="3013b-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3013b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="3013b-108">名稱</span><span class="sxs-lookup"><span data-stu-id="3013b-108">Name</span></span></th>
<th><span data-ttu-id="3013b-109">描述</span><span class="sxs-lookup"><span data-stu-id="3013b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span><span class="sxs-lookup"><span data-stu-id="3013b-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span></span></td>
<td><span data-ttu-id="3013b-112">取得或設定初始大小 (（以位元組為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="3013b-112">Gets or sets the initial size (in bytes).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span><span class="sxs-lookup"><span data-stu-id="3013b-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span></span></td>
<td><span data-ttu-id="3013b-115">取得或設定值，這個值會設定 ulGrowth 的上限。</span><span class="sxs-lookup"><span data-stu-id="3013b-115">Gets or sets the value that sets the ceiling of ulGrowth.</span></span> <span data-ttu-id="3013b-116">這個值是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="3013b-116">This value is in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span><span class="sxs-lookup"><span data-stu-id="3013b-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span></span></td>
<td><span data-ttu-id="3013b-119">取得或設定覆寫 ulGrowth （如果太小）的值。</span><span class="sxs-lookup"><span data-stu-id="3013b-119">Gets or sets the value that overrides ulGrowth if too small.</span></span> <span data-ttu-id="3013b-120">這個值是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="3013b-120">This value is in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-122"><a href="dn351068(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="3013b-122"><a href="dn351068(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="3013b-123">取得或設定空間提示選項。</span><span class="sxs-lookup"><span data-stu-id="3013b-123">Gets or sets the space hints options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span><span class="sxs-lookup"><span data-stu-id="3013b-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span></span></td>
<td><span data-ttu-id="3013b-126">取得或設定上一次成長或初始大小 (可能四捨五入為最接近原生 JET 配置大小) 的成長百分比。</span><span class="sxs-lookup"><span data-stu-id="3013b-126">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="3013b-127">有效的值為0，而 [100，50000) 。</span><span class="sxs-lookup"><span data-stu-id="3013b-127">Valid values are 0, and [100, 50000).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span><span class="sxs-lookup"><span data-stu-id="3013b-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span></span></td>
<td><span data-ttu-id="3013b-130">取得或設定 (附加) 版面配置的密度。</span><span class="sxs-lookup"><span data-stu-id="3013b-130">Gets or sets the density at (append) layout.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><span data-ttu-id="3013b-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span><span class="sxs-lookup"><span data-stu-id="3013b-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span></span></td>
<td><span data-ttu-id="3013b-133">取得或設定要維護的密度。</span><span class="sxs-lookup"><span data-stu-id="3013b-133">Gets or sets the density at which to maintain.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3013b-134">頁首</span><span class="sxs-lookup"><span data-stu-id="3013b-134">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="3013b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3013b-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3013b-136">參考</span><span class="sxs-lookup"><span data-stu-id="3013b-136">Reference</span></span>

[<span data-ttu-id="3013b-137">JET_SPACEHINTS 類別</span><span class="sxs-lookup"><span data-stu-id="3013b-137">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="3013b-138">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3013b-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
