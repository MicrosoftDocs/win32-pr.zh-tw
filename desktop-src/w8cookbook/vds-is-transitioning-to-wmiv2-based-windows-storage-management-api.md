---
title: 虛擬磁碟服務正在轉換至 Windows 儲存體管理 API
description: 虛擬磁碟服務正在轉換至 Windows 儲存體管理 API
ms.assetid: AB2A7D08-03B2-4595-A8EC-805D111A0E89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceea3ffe82358737ca8f39e9ef6db0bdb1f116ef
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383037"
---
# <a name="virtual-disk-service-is-transitioning-to-windows-storage-management-api"></a><span data-ttu-id="d7c73-103">虛擬磁碟服務正在轉換至 Windows 儲存體管理 API</span><span class="sxs-lookup"><span data-stu-id="d7c73-103">Virtual Disk Service is transitioning to Windows Storage Management API</span></span>

## <a name="platforms"></a><span data-ttu-id="d7c73-104">平台</span><span class="sxs-lookup"><span data-stu-id="d7c73-104">Platforms</span></span>

<span data-ttu-id="d7c73-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="d7c73-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="d7c73-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7c73-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="d7c73-107">Description</span><span class="sxs-lookup"><span data-stu-id="d7c73-107">Description</span></span>

<span data-ttu-id="d7c73-108">從 Windows 8 和 Windows Server 2012 開始，虛擬磁碟服務 COM 介面會由儲存體管理 API （以 WMI 為基礎的程式設計介面）取代。</span><span class="sxs-lookup"><span data-stu-id="d7c73-108">Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="d7c73-109">若要管理儲存子系統、 (Windows) 磁片、磁碟分割和磁片區，強烈建議使用存放裝置管理 API。</span><span class="sxs-lookup"><span data-stu-id="d7c73-109">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="d7c73-110">如需詳細資訊，請參閱 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)。</span><span class="sxs-lookup"><span data-stu-id="d7c73-110">For more info, see [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="d7c73-111">針對鏡像開機磁碟區以外的所有使用方式 (使用鏡像磁片區來裝載作業系統) ，動態磁碟已淘汰。</span><span class="sxs-lookup"><span data-stu-id="d7c73-111">For all usages except mirror boot volumes (using a mirror volume to host the operating system), dynamic disks are deprecated.</span></span> <span data-ttu-id="d7c73-112">對於需要針對磁片磁碟機失敗進行復原的資料，請使用儲存空間，這是一個彈性的儲存體虛擬化解決方案。</span><span class="sxs-lookup"><span data-stu-id="d7c73-112">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="d7c73-113">如需詳細資訊，請參閱 [儲存空間技術預覽](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="d7c73-113">For more info, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="d7c73-114">您可以在淘汰期間繼續使用 DiskPart、DiskRAID 和磁片管理，但是這些工具將無法搭配儲存空間使用，也不適用於任何其他新的 Windows Management Instrumentation (WMI) 架構的 Windows 儲存管理 Api 或內建的存放裝置管理公用程式或用戶端。</span><span class="sxs-lookup"><span data-stu-id="d7c73-114">You can continue to use DiskPart, DiskRAID, and Disk Management during the deprecation period, but these tools will not work with Storage Spaces or with any other new Windows Management Instrumentation (WMI)-based Windows Storage Management APIs or in-box storage management utilities or clients.</span></span>


| <span data-ttu-id="d7c73-115">API</span><span class="sxs-lookup"><span data-stu-id="d7c73-115">APIs</span></span> | <span data-ttu-id="d7c73-116">儲存子系統</span><span class="sxs-lookup"><span data-stu-id="d7c73-116">Storage Subsystems</span></span> | <span data-ttu-id="d7c73-117">基本磁碟</span><span class="sxs-lookup"><span data-stu-id="d7c73-117">Basic Disks</span></span> | <span data-ttu-id="d7c73-118">動態磁碟</span><span class="sxs-lookup"><span data-stu-id="d7c73-118">Dynamic Disks</span></span> | <span data-ttu-id="d7c73-119">儲存空間</span><span class="sxs-lookup"><span data-stu-id="d7c73-119">Storage Spaces</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="d7c73-120">Vds</span><span class="sxs-lookup"><span data-stu-id="d7c73-120">VDS</span></span> | <span data-ttu-id="d7c73-121">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-121">Yes</span></span> | <span data-ttu-id="d7c73-122">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-122">Yes</span></span> | <span data-ttu-id="d7c73-123">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-123">Yes</span></span> | <span data-ttu-id="d7c73-124">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-124">No</span></span> |
| <span data-ttu-id="d7c73-125">WMI</span><span class="sxs-lookup"><span data-stu-id="d7c73-125">WMI</span></span> | <span data-ttu-id="d7c73-126">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-126">Yes</span></span> | <span data-ttu-id="d7c73-127">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-127">Yes</span></span> | <span data-ttu-id="d7c73-128">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-128">No</span></span> | <span data-ttu-id="d7c73-129">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-129">Yes</span></span> |
| <span data-ttu-id="d7c73-130">DiskPart</span><span class="sxs-lookup"><span data-stu-id="d7c73-130">DiskPart</span></span> | <span data-ttu-id="d7c73-131">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-131">n/a</span></span> | <span data-ttu-id="d7c73-132">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-132">Yes</span></span> | <span data-ttu-id="d7c73-133">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-133">Yes</span></span> | <span data-ttu-id="d7c73-134">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-134">No</span></span> |
| <span data-ttu-id="d7c73-135">DiskRAID</span><span class="sxs-lookup"><span data-stu-id="d7c73-135">DiskRAID</span></span> |  <span data-ttu-id="d7c73-136">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-136">Yes</span></span> | <span data-ttu-id="d7c73-137">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-137">n/a</span></span> | <span data-ttu-id="d7c73-138">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-138">n/a</span></span> | <span data-ttu-id="d7c73-139">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-139">n/a</span></span> |
| <span data-ttu-id="d7c73-140">磁片管理 GUI</span><span class="sxs-lookup"><span data-stu-id="d7c73-140">Disk Mgmt GUI</span></span> | <span data-ttu-id="d7c73-141">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-141">n/a</span></span> | <span data-ttu-id="d7c73-142">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-142">Yes</span></span> | <span data-ttu-id="d7c73-143">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-143">Yes</span></span> | <span data-ttu-id="d7c73-144">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-144">No</span></span> |
| <span data-ttu-id="d7c73-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7c73-145">PowerShell</span></span> | <span data-ttu-id="d7c73-146">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-146">Yes</span></span> | <span data-ttu-id="d7c73-147">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-147">Yes</span></span> | <span data-ttu-id="d7c73-148">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-148">No</span></span> | <span data-ttu-id="d7c73-149">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-149">Yes</span></span> |
| <span data-ttu-id="d7c73-150">儲存空間主控台</span><span class="sxs-lookup"><span data-stu-id="d7c73-150">Storage Spaces Control Panel</span></span> | <span data-ttu-id="d7c73-151">n/a</span><span class="sxs-lookup"><span data-stu-id="d7c73-151">n/a</span></span> | <span data-ttu-id="d7c73-152">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-152">No</span></span> | <span data-ttu-id="d7c73-153">否</span><span class="sxs-lookup"><span data-stu-id="d7c73-153">No</span></span> | <span data-ttu-id="d7c73-154">是</span><span class="sxs-lookup"><span data-stu-id="d7c73-154">Yes</span></span> |


<span data-ttu-id="d7c73-155">這項轉換的結果將會提高儲存體復原能力、可用性和擴充性;統一的腳本和程式設計語言、降低存放裝置管理成本，以及更輕鬆的遠端存放裝置管理。</span><span class="sxs-lookup"><span data-stu-id="d7c73-155">The result of this transition will be increased storage resiliency, availability, and scalability; a unified scripting and programming language, reduced storage management costs, and easier remote storage management.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d7c73-156">表現</span><span class="sxs-lookup"><span data-stu-id="d7c73-156">Manifestation</span></span>

<span data-ttu-id="d7c73-157">VDS 環境中使用的 DiskPart 和 DiskRAID 公用程式不支援新的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="d7c73-157">The DiskPart and DiskRAID utilities used in the VDS environment do not support the new Storage Spaces.</span></span> <span data-ttu-id="d7c73-158">同樣地，新的儲存體 PowerShell 公用程式不支援已被取代的動態磁碟</span><span class="sxs-lookup"><span data-stu-id="d7c73-158">Similarly, the new Storage PowerShell utility does not support the deprecated Dynamic Disks</span></span>

## <a name="mitigation"></a><span data-ttu-id="d7c73-159">降低</span><span class="sxs-lookup"><span data-stu-id="d7c73-159">Mitigation</span></span>

<span data-ttu-id="d7c73-160">Microsoft 強烈建議您將任何新的儲存體管理應用程式放在 Windows 儲存體管理 API，並規劃在標準更新週期期間，將以 VDS 基礎結構為基礎的現有應用程式轉換成 Windows 儲存體管理 API。</span><span class="sxs-lookup"><span data-stu-id="d7c73-160">Microsoft strongly recommends that you base any new storage management apps on the Windows Storage Management API, and that you plan to transition existing apps that are based on the VDS infrastructure to the Windows Storage Management API during your standard updating cycles.</span></span>

## <a name="resources"></a><span data-ttu-id="d7c73-161">資源</span><span class="sxs-lookup"><span data-stu-id="d7c73-161">Resources</span></span>

-   [<span data-ttu-id="d7c73-162">Windows 儲存裝置管理 API</span><span class="sxs-lookup"><span data-stu-id="d7c73-162">Windows Storage Management API</span></span>](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   [<span data-ttu-id="d7c73-163">Windows PowerShell 中的儲存體 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d7c73-163">Storage Cmdlets in Windows PowerShell</span></span>](/powershell/module/storage/?view=win10-ps)
-   [<span data-ttu-id="d7c73-164">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="d7c73-164">Windows Management Instrumentation</span></span>](../wmisdk/wmi-start-page.md)
-   <span data-ttu-id="d7c73-165">[Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d7c73-165">[Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=VS.85).aspx)</span></span>

 

 