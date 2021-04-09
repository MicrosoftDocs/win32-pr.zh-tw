---
description: 深入瞭解： EsentVersion 屬性
title: EsentVersion 屬性
TOCTitle: EsentVersion properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.EsentVersion
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion_properties(v=EXCHG.10)
ms:contentKeyID: 55103178
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a9b5d6803be2d59e37024939ebd6c26c94d68d33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853036"
---
# <a name="esentversion-properties"></a><span data-ttu-id="eedcf-103">EsentVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="eedcf-103">EsentVersion properties</span></span>

<span data-ttu-id="eedcf-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="eedcf-104">Include protected members</span></span>  
<span data-ttu-id="eedcf-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="eedcf-105">Include inherited members</span></span>  

<span data-ttu-id="eedcf-106">[EsentVersion](./esentversion-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="eedcf-106">The [EsentVersion](./esentversion-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="eedcf-107">屬性</span><span class="sxs-lookup"><span data-stu-id="eedcf-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="eedcf-108">名稱</span><span class="sxs-lookup"><span data-stu-id="eedcf-108">Name</span></span></th>
<th><span data-ttu-id="eedcf-109">描述</span><span class="sxs-lookup"><span data-stu-id="eedcf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-112"><a href="dn350858(v=exchg.10).md">SupportsLargeKeys</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-112"><a href="dn350858(v=exchg.10).md">SupportsLargeKeys</a></span></span></td>
<td><span data-ttu-id="eedcf-113">取得值，這個值表示是否支援大型 (&gt; 255 位元組) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="eedcf-113">Gets a value that indicates whether large (&gt; 255 byte) keys are supported.</span></span> <span data-ttu-id="eedcf-114">您可以在 <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a> 物件中指定索引的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="eedcf-114">The key size for an index can be specified in the <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a> object.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-117"><a href="dn350871(v=exchg.10).md">SupportsServer2003Features</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-117"><a href="dn350871(v=exchg.10).md">SupportsServer2003Features</a></span></span></td>
<td><span data-ttu-id="eedcf-118">取得值，這個值表示目前的 ESENT 版本是否支援 Windows Server 2003 版 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="eedcf-118">Gets a value that indicates whether the current version of ESENT supports features available in the Windows Server 2003 version of ESENT.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-121"><a href="dn350856(v=exchg.10).md">SupportsUnicodePaths</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-121"><a href="dn350856(v=exchg.10).md">SupportsUnicodePaths</a></span></span></td>
<td><span data-ttu-id="eedcf-122">取得值，這個值表示目前的 ESENT 版本是否可以使用非 ASCII 路徑來存取資料庫。</span><span class="sxs-lookup"><span data-stu-id="eedcf-122">Gets a value that indicates whether the current version of ESENT can use non-ASCII paths to access databases.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-125"><a href="dn350861(v=exchg.10).md">SupportsVistaFeatures</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-125"><a href="dn350861(v=exchg.10).md">SupportsVistaFeatures</a></span></span></td>
<td><span data-ttu-id="eedcf-126">取得值，這個值表示目前的 ESENT 版本是否支援 Windows Vista 版本的 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="eedcf-126">Gets a value that indicates whether the current version of ESENT supports features available in the Windows Vista version of ESENT.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-129"><a href="dn350860(v=exchg.10).md">SupportsWindows7Features</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-129"><a href="dn350860(v=exchg.10).md">SupportsWindows7Features</a></span></span></td>
<td><span data-ttu-id="eedcf-130">取得值，這個值會指出目前版本的 ESENT 是否支援 Windows 7 版 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="eedcf-130">Gets a value that indicates whether the current version of ESENT supports features available in the Windows 7 version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="eedcf-133"><a href="dn350863(v=exchg.10).md">SupportsWindows8Features</a></span><span class="sxs-lookup"><span data-stu-id="eedcf-133"><a href="dn350863(v=exchg.10).md">SupportsWindows8Features</a></span></span></td>
<td><span data-ttu-id="eedcf-134">取得值，這個值會指出目前的 ESENT 版本是否支援 Windows 8 版 ESENT 中可用的功能。</span><span class="sxs-lookup"><span data-stu-id="eedcf-134">Gets a value that indicates whether the current version of ESENT supports features available in the Windows 8 version of ESENT.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eedcf-135">頁首</span><span class="sxs-lookup"><span data-stu-id="eedcf-135">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="eedcf-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eedcf-136">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eedcf-137">參考</span><span class="sxs-lookup"><span data-stu-id="eedcf-137">Reference</span></span>

[<span data-ttu-id="eedcf-138">EsentVersion 類別</span><span class="sxs-lookup"><span data-stu-id="eedcf-138">EsentVersion class</span></span>](./esentversion-class.md)

[<span data-ttu-id="eedcf-139">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="eedcf-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
