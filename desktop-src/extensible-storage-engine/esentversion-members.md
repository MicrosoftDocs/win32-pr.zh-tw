---
description: 深入瞭解： EsentVersion 成員
title: EsentVersion 成員
TOCTitle: EsentVersion members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentVersion
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion_members(v=EXCHG.10)
ms:contentKeyID: 55103183
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d16c54ec9efb7d332a5e4ca56e13a96fd595daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695683"
---
# <a name="esentversion-members"></a><span data-ttu-id="e8491-103">EsentVersion 成員</span><span class="sxs-lookup"><span data-stu-id="e8491-103">EsentVersion members</span></span>

<span data-ttu-id="e8491-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="e8491-104">Include protected members</span></span>  
<span data-ttu-id="e8491-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="e8491-105">Include inherited members</span></span>  

<span data-ttu-id="e8491-106">提供所使用之 ESENT 版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8491-106">Gives information about the version of ESENT being used.</span></span>

<span data-ttu-id="e8491-107">[EsentVersion](./esentversion-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="e8491-107">The [EsentVersion](./esentversion-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="e8491-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e8491-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e8491-109">名稱</span><span class="sxs-lookup"><span data-stu-id="e8491-109">Name</span></span></th>
<th><span data-ttu-id="e8491-110">描述</span><span class="sxs-lookup"><span data-stu-id="e8491-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-113"><a href="dn350858(v=exchg.10).md">SupportsLargeKeys</a></span><span class="sxs-lookup"><span data-stu-id="e8491-113"><a href="dn350858(v=exchg.10).md">SupportsLargeKeys</a></span></span></td>
<td><span data-ttu-id="e8491-114">取得值，這個值表示是否支援大型 (&gt; 255 位元組) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8491-114">Gets a value that indicates whether large (&gt; 255 byte) keys are supported.</span></span> <span data-ttu-id="e8491-115">您可以在 <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a> 物件中指定索引的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="e8491-115">The key size for an index can be specified in the <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a> object.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-118"><a href="dn350871(v=exchg.10).md">SupportsServer2003Features</a></span><span class="sxs-lookup"><span data-stu-id="e8491-118"><a href="dn350871(v=exchg.10).md">SupportsServer2003Features</a></span></span></td>
<td><span data-ttu-id="e8491-119">取得值，這個值表示目前的 ESENT 版本是否支援 Windows Server 2003 版 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e8491-119">Gets a value that indicates whether the current version of ESENT supports features available in the Windows Server 2003 version of ESENT.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-122"><a href="dn350856(v=exchg.10).md">SupportsUnicodePaths</a></span><span class="sxs-lookup"><span data-stu-id="e8491-122"><a href="dn350856(v=exchg.10).md">SupportsUnicodePaths</a></span></span></td>
<td><span data-ttu-id="e8491-123">取得值，這個值表示目前的 ESENT 版本是否可以使用非 ASCII 路徑來存取資料庫。</span><span class="sxs-lookup"><span data-stu-id="e8491-123">Gets a value that indicates whether the current version of ESENT can use non-ASCII paths to access databases.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-126"><a href="dn350861(v=exchg.10).md">SupportsVistaFeatures</a></span><span class="sxs-lookup"><span data-stu-id="e8491-126"><a href="dn350861(v=exchg.10).md">SupportsVistaFeatures</a></span></span></td>
<td><span data-ttu-id="e8491-127">取得值，這個值表示目前的 ESENT 版本是否支援 Windows Vista 版本的 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e8491-127">Gets a value that indicates whether the current version of ESENT supports features available in the Windows Vista version of ESENT.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-130"><a href="dn350860(v=exchg.10).md">SupportsWindows7Features</a></span><span class="sxs-lookup"><span data-stu-id="e8491-130"><a href="dn350860(v=exchg.10).md">SupportsWindows7Features</a></span></span></td>
<td><span data-ttu-id="e8491-131">取得值，這個值會指出目前版本的 ESENT 是否支援 Windows 7 版 ESENT 中提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e8491-131">Gets a value that indicates whether the current version of ESENT supports features available in the Windows 7 version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="e8491-134"><a href="dn350863(v=exchg.10).md">SupportsWindows8Features</a></span><span class="sxs-lookup"><span data-stu-id="e8491-134"><a href="dn350863(v=exchg.10).md">SupportsWindows8Features</a></span></span></td>
<td><span data-ttu-id="e8491-135">取得值，這個值會指出目前的 ESENT 版本是否支援 Windows 8 版 ESENT 中可用的功能。</span><span class="sxs-lookup"><span data-stu-id="e8491-135">Gets a value that indicates whether the current version of ESENT supports features available in the Windows 8 version of ESENT.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8491-136">頁首</span><span class="sxs-lookup"><span data-stu-id="e8491-136">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e8491-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8491-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8491-138">參考</span><span class="sxs-lookup"><span data-stu-id="e8491-138">Reference</span></span>

[<span data-ttu-id="e8491-139">EsentVersion 類別</span><span class="sxs-lookup"><span data-stu-id="e8491-139">EsentVersion class</span></span>](./esentversion-class.md)

[<span data-ttu-id="e8491-140">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e8491-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
