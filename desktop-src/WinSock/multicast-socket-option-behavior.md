---
description: 此頁面描述以各種通訊端選項設定狀態為基礎的多播通訊端選項行為。
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: 多播通訊端選項行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026214"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="464f7-103">多播通訊端選項行為</span><span class="sxs-lookup"><span data-stu-id="464f7-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="464f7-104">此頁面描述以各種通訊端選項設定狀態為基礎的多播通訊端選項行為。</span><span class="sxs-lookup"><span data-stu-id="464f7-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="464f7-105">例如，此頁面描述在 \_ \_ \_ \_ \_ \_ 已使用相同網路介面上的指定群組/來源組設定了 ip 新增來源成員資格選項的通訊端上設定 ip 新增來源成員資格通訊端選項時的行為。</span><span class="sxs-lookup"><span data-stu-id="464f7-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="464f7-106">允許在 \_ \_ 不同的網路介面上呼叫 \_ 相同群組的 IP 新增來源成員資格。</span><span class="sxs-lookup"><span data-stu-id="464f7-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="464f7-107">此頁面可協助您正確設計和疑難排解 Windows 通訊端多播應用程式。</span><span class="sxs-lookup"><span data-stu-id="464f7-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="464f7-108">初始通訊端選項</span><span class="sxs-lookup"><span data-stu-id="464f7-108">Initial socket option</span></span></th>
<th><span data-ttu-id="464f7-109">衝突的後續通訊端選項</span><span class="sxs-lookup"><span data-stu-id="464f7-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="464f7-110">傳回的錯誤</span><span class="sxs-lookup"><span data-stu-id="464f7-110">Error returned</span></span></th>
<th><span data-ttu-id="464f7-111">備註</span><span class="sxs-lookup"><span data-stu-id="464f7-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="464f7-112">IP_ADD_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="464f7-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="464f7-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-115">請勿在相同的網路介面上多次呼叫相同群組的 IP_ADD_MEMBERSHIP。</span><span class="sxs-lookup"><span data-stu-id="464f7-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f7-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-118">請勿使用與先前在相同網路介面上 IP_ADD_MEMBERSHIP 呼叫的相同群組來呼叫 IP_ADD_SOURCE_MEMBERSHIP。</span><span class="sxs-lookup"><span data-stu-id="464f7-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="464f7-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-120">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-121">請改用 IP_BLOCK_SOURCE。</span><span class="sxs-lookup"><span data-stu-id="464f7-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="464f7-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-123">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-124">嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="464f7-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-126">對相同群組或群組/來源配對的任何後續呼叫</span><span class="sxs-lookup"><span data-stu-id="464f7-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="464f7-127">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-128">在群組或群組/來源組上進行通訊端選項呼叫，而目前不在包含清單中 (因為卸載成員資格，否則) 會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="464f7-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="464f7-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="464f7-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-132">請勿使用與先前在相同網路介面上 IP_ADD_SOURCE_MEMBERSHIP 呼叫的相同群組來呼叫 IP_ADD_MEMBERSHIP。</span><span class="sxs-lookup"><span data-stu-id="464f7-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="464f7-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-135">請勿使用先前以 IP_ADD_SOURCE_MEMBERSHIP 在相同網路介面上呼叫的相同群組/來源組來呼叫 IP_ADD_SOURCE_MEMBERSHIP。</span><span class="sxs-lookup"><span data-stu-id="464f7-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="464f7-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-137">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-138">嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="464f7-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="464f7-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="464f7-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-141">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-142">嘗試解除封鎖先前未在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f7-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-145">嘗試卸載不在相同網路介面上包含清單中的群組/來源對時，傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="464f7-146">IP_BLOCK_SOURCE $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="464f7-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="464f7-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-149">嘗試封鎖已在相同網路介面上封鎖的群組/來源組時，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f7-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-151">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-152">請改用 IP_UNBLOCK_SOURCE。</span><span class="sxs-lookup"><span data-stu-id="464f7-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="464f7-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="464f7-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="464f7-154">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="464f7-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="464f7-155">請改用 IP_UNBLOCK_SOURCE。</span><span class="sxs-lookup"><span data-stu-id="464f7-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="464f7-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="464f7-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="464f7-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="464f7-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="464f7-159">嘗試解除封鎖不在相同網路介面上封鎖清單中的群組/來源對時，傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="464f7-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



