---
description: 深入瞭解：轉換成員
title: 轉換成員
TOCTitle: Conversions members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Conversions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions_members(v=EXCHG.10)
ms:contentKeyID: 55107253
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7e192b338c1d19b207b7e7e242289ca7f6782175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114088"
---
# <a name="conversions-members"></a><span data-ttu-id="735a8-103">轉換成員</span><span class="sxs-lookup"><span data-stu-id="735a8-103">Conversions members</span></span>

<span data-ttu-id="735a8-104">包含受保護的成員</span><span class="sxs-lookup"><span data-stu-id="735a8-104">Include protected members</span></span>  
<span data-ttu-id="735a8-105">包含繼承的成員</span><span class="sxs-lookup"><span data-stu-id="735a8-105">Include inherited members</span></span>  

<span data-ttu-id="735a8-106">提供在 Win32 與 .NET Framework 之間轉換資料和旗標的方法。</span><span class="sxs-lookup"><span data-stu-id="735a8-106">Provide methods to convert data and flags between Win32 and the .NET Framework.</span></span>

<span data-ttu-id="735a8-107">[轉換](./conversions-class.md)類型會公開下列成員。</span><span class="sxs-lookup"><span data-stu-id="735a8-107">The [Conversions](./conversions-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="735a8-108">方法</span><span class="sxs-lookup"><span data-stu-id="735a8-108">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="735a8-109">名稱</span><span class="sxs-lookup"><span data-stu-id="735a8-109">Name</span></span></th>
<th><span data-ttu-id="735a8-110">描述</span><span class="sxs-lookup"><span data-stu-id="735a8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="735a8-113"><a href="dn334187(v=exchg.10).md">CompareOptionsFromLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="735a8-113"><a href="dn334187(v=exchg.10).md">CompareOptionsFromLCMapFlags</a></span></span></td>
<td><span data-ttu-id="735a8-114">針對 LCMapFlags 指定旗標，將它們轉換成比較選項。</span><span class="sxs-lookup"><span data-stu-id="735a8-114">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="735a8-115">忽略未知的選項。</span><span class="sxs-lookup"><span data-stu-id="735a8-115">Unknown options are ignored.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="735a8-118"><a href="dn334235(v=exchg.10).md">ConvertDoubleToDateTime</a></span><span class="sxs-lookup"><span data-stu-id="735a8-118"><a href="dn334235(v=exchg.10).md">ConvertDoubleToDateTime</a></span></span></td>
<td><span data-ttu-id="735a8-119">將雙 (的 OA 日期時間格式) 轉換為日期時間。</span><span class="sxs-lookup"><span data-stu-id="735a8-119">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="735a8-120">不同于 DateTime. Date.fromoadate，這不會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="735a8-120">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="公用方法" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><span data-ttu-id="735a8-123"><a href="dn334186(v=exchg.10).md">LCMapFlagsFromCompareOptions</a></span><span class="sxs-lookup"><span data-stu-id="735a8-123"><a href="dn334186(v=exchg.10).md">LCMapFlagsFromCompareOptions</a></span></span></td>
<td><span data-ttu-id="735a8-124">提供 CompareOptions，並將其轉換成 LCMapString 的旗標。</span><span class="sxs-lookup"><span data-stu-id="735a8-124">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="735a8-125">忽略未知的選項。</span><span class="sxs-lookup"><span data-stu-id="735a8-125">Unknown options are ignored.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="735a8-126">頁首</span><span class="sxs-lookup"><span data-stu-id="735a8-126">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="735a8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="735a8-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="735a8-128">參考</span><span class="sxs-lookup"><span data-stu-id="735a8-128">Reference</span></span>

[<span data-ttu-id="735a8-129">轉換類別</span><span class="sxs-lookup"><span data-stu-id="735a8-129">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="735a8-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="735a8-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
