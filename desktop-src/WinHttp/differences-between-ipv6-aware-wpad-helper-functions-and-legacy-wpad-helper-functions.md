---
title: IPv6-Aware 和舊版 WPAD helper 函數
description: IPv6-Aware WPAD Helper 函式和舊版 WPAD Helper 函數之間的差異
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975214"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="259ff-103">IPv6-Aware 和舊版 WPAD helper 函數</span><span class="sxs-lookup"><span data-stu-id="259ff-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="259ff-104">下表說明新的 WPAD helper 函式和舊版 WPAD helper 函數之間的差異。</span><span class="sxs-lookup"><span data-stu-id="259ff-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="259ff-105">新的函式會以星號標記。</span><span class="sxs-lookup"><span data-stu-id="259ff-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="259ff-106">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-106">Functions</span></span></th>
<th><span data-ttu-id="259ff-107">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-107">Input</span></span></th>
<th><span data-ttu-id="259ff-108">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-108">Output</span></span></th>
<th><span data-ttu-id="259ff-109">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="259ff-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="259ff-110">dnsResolve</span></span></td>
<td><span data-ttu-id="259ff-111">主機</span><span class="sxs-lookup"><span data-stu-id="259ff-111">Host</span></span></td>
<td><span data-ttu-id="259ff-112">IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="259ff-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="259ff-113">Ex 函數會傳回 IPv6/IPv4 的清單。</span><span class="sxs-lookup"><span data-stu-id="259ff-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="259ff-114">因為 IPv6 或 IPv4 位址可以針對單一介面擁有多個單播位址，所以需要此項。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="259ff-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="259ff-115">dnsResolveEx\*</span><span class="sxs-lookup"><span data-stu-id="259ff-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="259ff-116">主機</span><span class="sxs-lookup"><span data-stu-id="259ff-116">Host</span></span></td>
<td><span data-ttu-id="259ff-117">IPv6/IPv4 地址清單</span><span class="sxs-lookup"><span data-stu-id="259ff-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="259ff-118">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-118">Functions</span></span></th>
<th><span data-ttu-id="259ff-119">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-119">Input</span></span></th>
<th><span data-ttu-id="259ff-120">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-120">Output</span></span></th>
<th><span data-ttu-id="259ff-121">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="259ff-122">isResolveable</span><span class="sxs-lookup"><span data-stu-id="259ff-122">isResolveable</span></span></td>
<td><span data-ttu-id="259ff-123">IPv4 主機</span><span class="sxs-lookup"><span data-stu-id="259ff-123">IPv4 host</span></span></td>
<td><span data-ttu-id="259ff-124">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="259ff-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="259ff-125">如果主機可以解析成 IPv6 或 IPv4 位址，則 Ex 函數會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="259ff-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="259ff-126">如果主機解析成 IPv4 位址，則舊版函式只會傳回 TRUE。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="259ff-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="259ff-127">isResolveableEx\*</span><span class="sxs-lookup"><span data-stu-id="259ff-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="259ff-128">IPv6/IPv4 主機</span><span class="sxs-lookup"><span data-stu-id="259ff-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="259ff-129">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="259ff-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="259ff-130">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-130">Functions</span></span></th>
<th><span data-ttu-id="259ff-131">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-131">Input</span></span></th>
<th><span data-ttu-id="259ff-132">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-132">Output</span></span></th>
<th><span data-ttu-id="259ff-133">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="259ff-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="259ff-134">myIPAddress</span></span></td>
<td><span data-ttu-id="259ff-135">無</span><span class="sxs-lookup"><span data-stu-id="259ff-135">none</span></span></td>
<td><span data-ttu-id="259ff-136">IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="259ff-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="259ff-137">Ex 函數會傳回 IPv6/IPv4 的清單。</span><span class="sxs-lookup"><span data-stu-id="259ff-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="259ff-138">需要的原因是 IPv6 或 IPv4 位址可以有單一介面 $ {REMOVE} $ 的多重單播位址</span><span class="sxs-lookup"><span data-stu-id="259ff-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="259ff-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="259ff-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="259ff-140">無</span><span class="sxs-lookup"><span data-stu-id="259ff-140">none</span></span></td>
<td><span data-ttu-id="259ff-141">IPv6/IPv4 地址清單</span><span class="sxs-lookup"><span data-stu-id="259ff-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="259ff-142">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-142">Functions</span></span></th>
<th><span data-ttu-id="259ff-143">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-143">Input</span></span></th>
<th><span data-ttu-id="259ff-144">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-144">Output</span></span></th>
<th><span data-ttu-id="259ff-145">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="259ff-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="259ff-146">isInNet</span></span></td>
<td><span data-ttu-id="259ff-147">主機、點分隔 IP 位址模式、IP 位址遮罩</span><span class="sxs-lookup"><span data-stu-id="259ff-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="259ff-148">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="259ff-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="259ff-149">提供 IP 版本中立的方式，以找出 IP 位址是否在指定的子網中。</span><span class="sxs-lookup"><span data-stu-id="259ff-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="259ff-150">此外，IPv4 中的遮罩標記法已淘汰。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="259ff-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="259ff-151">isInNetEx\*</span><span class="sxs-lookup"><span data-stu-id="259ff-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="259ff-152">IP 位址 IP 首碼</span><span class="sxs-lookup"><span data-stu-id="259ff-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="259ff-153">TRUE/FALSE</span><span class="sxs-lookup"><span data-stu-id="259ff-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="259ff-154">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-154">Functions</span></span>           | <span data-ttu-id="259ff-155">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-155">Input</span></span>                       | <span data-ttu-id="259ff-156">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-156">Output</span></span>                             | <span data-ttu-id="259ff-157">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259ff-158">sortIPAddressList\*</span><span class="sxs-lookup"><span data-stu-id="259ff-158">sortIPAddressList\*</span></span> | <span data-ttu-id="259ff-159">IPv6/IPv4 地址清單</span><span class="sxs-lookup"><span data-stu-id="259ff-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="259ff-160">IPv6/IPv4 位址的排序清單</span><span class="sxs-lookup"><span data-stu-id="259ff-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="259ff-161">沒有對應的舊版函式，因為舊版函式只會傳回單一的 IPv4 位址，因此不需要排序。</span><span class="sxs-lookup"><span data-stu-id="259ff-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="259ff-162">函式</span><span class="sxs-lookup"><span data-stu-id="259ff-162">Functions</span></span>          | <span data-ttu-id="259ff-163">輸入</span><span class="sxs-lookup"><span data-stu-id="259ff-163">Input</span></span> | <span data-ttu-id="259ff-164">輸出</span><span class="sxs-lookup"><span data-stu-id="259ff-164">Output</span></span>                     | <span data-ttu-id="259ff-165">變更的原因</span><span class="sxs-lookup"><span data-stu-id="259ff-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259ff-166">getClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="259ff-166">getClientVersion\*</span></span> | <span data-ttu-id="259ff-167">無</span><span class="sxs-lookup"><span data-stu-id="259ff-167">none</span></span>  | <span data-ttu-id="259ff-168">WPAD 引擎版本號碼</span><span class="sxs-lookup"><span data-stu-id="259ff-168">WPAD engine version number</span></span> | <span data-ttu-id="259ff-169">此函數目前會傳回1.0 版。</span><span class="sxs-lookup"><span data-stu-id="259ff-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="259ff-170">我們新增了此函式，可讓 IT 系統管理員更新其 WPAD 以使用不同版本的 WPAD 引擎，而不會導致其存在的部署中斷。</span><span class="sxs-lookup"><span data-stu-id="259ff-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="259ff-171">這種功能需要 Windows Internet Explorer 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="259ff-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



