---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: 伺服器 Hyper-v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981058"
---
# <a name="server-hyper-v"></a><span data-ttu-id="a1f40-103">伺服器 Hyper-v</span><span class="sxs-lookup"><span data-stu-id="a1f40-103">Server Hyper-V</span></span>

## <a name="platforms"></a><span data-ttu-id="a1f40-104">平台</span><span class="sxs-lookup"><span data-stu-id="a1f40-104">Platforms</span></span>

 <span data-ttu-id="a1f40-105">**客戶** 端-windows XP \| windows Vista \| windows 7</span><span class="sxs-lookup"><span data-stu-id="a1f40-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="a1f40-106">**伺服器** -windows server 2008 \| Windows server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1f40-106">**Servers** - Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="a1f40-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="a1f40-107">Feature Impact</span></span>

 <span data-ttu-id="a1f40-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="a1f40-108">**Severity** - Low</span></span>  
<span data-ttu-id="a1f40-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="a1f40-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="a1f40-110">Description</span><span class="sxs-lookup"><span data-stu-id="a1f40-110">Description</span></span>

<span data-ttu-id="a1f40-111">伺服器虛擬化可讓您在單一實體電腦上執行多個作業系統，作為虛擬機器 (Vm) ，可讓您將使用量過低之伺服器機器的工作負載合併到較少的充分利用電腦上。</span><span class="sxs-lookup"><span data-stu-id="a1f40-111">Server virtualization enables multiple operating systems to run on a single physical machine as virtual machines (VMs), allowing you to consolidate workloads of underutilized server machines onto a smaller number of fully utilized machines.</span></span> <span data-ttu-id="a1f40-112">Windows 7 包含 Windows Server 2008 版的幾項增強功能：</span><span class="sxs-lookup"><span data-stu-id="a1f40-112">Windows 7 includes several enhancements to the Windows Server 2008 version:</span></span>

-   <span data-ttu-id="a1f40-113">**即時移轉：** 在 Windows Server 2008 中，我們有快速的遷移。</span><span class="sxs-lookup"><span data-stu-id="a1f40-113">**Live Migration:** In Windows Server 2008, we had Quick Migration.</span></span> <span data-ttu-id="a1f40-114">透過即時移轉，我們改善了遷移速度和儲存彈性。</span><span class="sxs-lookup"><span data-stu-id="a1f40-114">With Live Migration, we improved migration speed and storage flexibility.</span></span>
-   <span data-ttu-id="a1f40-115">**邏輯處理器支援：** 我們已將邏輯主機處理器從16LP 增加至64LP。</span><span class="sxs-lookup"><span data-stu-id="a1f40-115">**Logical Processor Support:** We increased logical host processors from 16LP to 64LP.</span></span>
-   <span data-ttu-id="a1f40-116">**儲存體熱新增：** 現在您可以將額外的 VHD 或傳遞磁片新增至執行中的虛擬機器，而不需要關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a1f40-116">**Storage Hot Add:** Now you can add additional VHD or Pass-through disks to a running virtual machine without turning off the virtual machine.</span></span>
-   <span data-ttu-id="a1f40-117">**新硬體支援：** 我們已新增新處理器所包含的技術支援，以及即將上市的網路卡，包括第二層轉譯 (SLAT) 、TCP 卸載 (煙囪) 和 VMdQ。</span><span class="sxs-lookup"><span data-stu-id="a1f40-117">**New Hardware Support:** We have added support for the technologies included in new processors and network cards coming to market, including Second Level Translation (SLAT), TCP Offload (Chimney), and VMdQ.</span></span>
-   <span data-ttu-id="a1f40-118">**終端機服務虛擬化 (TSv) ：** 適用于 Hyper-v 的集中式桌面解決方案。</span><span class="sxs-lookup"><span data-stu-id="a1f40-118">**Terminal Services virtualization (TSv):** We centralized desktop solution for Hyper-V.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a1f40-119">影響的表現</span><span class="sxs-lookup"><span data-stu-id="a1f40-119">Manifestation of Impact</span></span>

-   <span data-ttu-id="a1f40-120">**即時移轉：** 您可能需要變更您的儲存系統架構，才能充分利用此技術。</span><span class="sxs-lookup"><span data-stu-id="a1f40-120">**Live Migration:** You may need to change the way you have architected your storage systems in order to fully leverage this technology.</span></span> <span data-ttu-id="a1f40-121">雖然可能不需要這些變更，但您可以選擇執行這些變更，以充分利用這些優勢。</span><span class="sxs-lookup"><span data-stu-id="a1f40-121">Though these changes may not be required, you may choose to implement them in order to fully leverage the benefits.</span></span> <span data-ttu-id="a1f40-122">您可能需要一個管理應用程式來協調即時移轉。</span><span class="sxs-lookup"><span data-stu-id="a1f40-122">You may need a management application to orchestrate Live Migration.</span></span>
-   <span data-ttu-id="a1f40-123">**邏輯處理器支援：** 從 Windows Server 2008 遷移至 Windows Server 2008 R2 時，這項功能不會影響客戶或 Isv。</span><span class="sxs-lookup"><span data-stu-id="a1f40-123">**Logical Processor Support:** This feature will have no impact on customers or ISVs when migrating from Windows Server 2008 to Windows Server 2008 R2.</span></span>
-   <span data-ttu-id="a1f40-124">**儲存體熱新增：** 從 Windows Server 2008 遷移至 Windows Server 2008 R2 時，此功能不會影響客戶或 Isv。</span><span class="sxs-lookup"><span data-stu-id="a1f40-124">**Storage Hot Add:** This feature will have no impact to customers or ISVs when migrating from Windows Server 2008 to Windows Server 2008 R2.</span></span> <span data-ttu-id="a1f40-125">設定虛擬機器設定的管理應用程式可能需要更新，才能管理這項新功能。</span><span class="sxs-lookup"><span data-stu-id="a1f40-125">Management applications that configure the settings of a virtual machine may require updating in order to manage this new feature.</span></span>
-   <span data-ttu-id="a1f40-126">**新硬體支援：** 這些功能僅適用于推出到市場的新硬體。</span><span class="sxs-lookup"><span data-stu-id="a1f40-126">**New Hardware Support:** These features apply only to new hardware that is being introduced to the market.</span></span> <span data-ttu-id="a1f40-127">因為它不支援這些功能的內建支援，所以從 Windows Server 2008 遷移至 Windows Server 2008 R2 的實體伺服器不太可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="a1f40-127">Because it will not have build-in support for these features, it is not likely that a physical server that is being migrated from Windows Server 2008 to Windows Server 2008 R2 will be impacted.</span></span> <span data-ttu-id="a1f40-128">如果要遷移的伺服器上有這些功能，則不會預期直接變更。</span><span class="sxs-lookup"><span data-stu-id="a1f40-128">If these features are available on the server that is being migrated, no direct changes are anticipated.</span></span>
-   <span data-ttu-id="a1f40-129">**終端機服務虛擬化：** 從 Windows Server 2008 遷移至 Windows Server 2008 R2 時，此功能不會影響客戶或 Isv。</span><span class="sxs-lookup"><span data-stu-id="a1f40-129">**Terminal Services virtualization:** This feature will have no impact to customers or ISVs when migrating from Windows Server 2008 to Windows Server 2008 R2.</span></span> <span data-ttu-id="a1f40-130">利用終端機服務 (TS) 的應用程式可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="a1f40-130">Applications that leverage Terminal Services (TS) may be impacted.</span></span> <span data-ttu-id="a1f40-131">這項功能會直接與 TS 整合，因此設定 TS 的應用程式可能需要更新，才能管理這項新功能。</span><span class="sxs-lookup"><span data-stu-id="a1f40-131">This feature directly integrates with TS and therefore applications that configure TS may require updating in order to manage this new feature.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a1f40-132">降低</span><span class="sxs-lookup"><span data-stu-id="a1f40-132">Mitigation</span></span>

-   <span data-ttu-id="a1f40-133">**即時移轉：** 針對具有儲存體系統設計的最佳作法和建議，為終端使用者提供規範性指導方針。</span><span class="sxs-lookup"><span data-stu-id="a1f40-133">**Live Migration:** Provide prescriptive Guidance to end users with best practices and recommendations for storage system design.</span></span> <span data-ttu-id="a1f40-134">您必須通知終端使用者關於選項和建議。</span><span class="sxs-lookup"><span data-stu-id="a1f40-134">You must inform the end user about the options and recommendations.</span></span>

## <a name="leveraging-capabilitities"></a><span data-ttu-id="a1f40-135">利用 Capabilitities</span><span class="sxs-lookup"><span data-stu-id="a1f40-135">Leveraging Capabilitities</span></span>

-   <span data-ttu-id="a1f40-136">**即時移轉：** 這項功能可啟用動態 IT 環境。</span><span class="sxs-lookup"><span data-stu-id="a1f40-136">**Live Migration:** This feature enables the Dynamic IT environment.</span></span> <span data-ttu-id="a1f40-137">虛擬化管理應用程式開發人員必須修改其應用程式，以利用這項新功能。</span><span class="sxs-lookup"><span data-stu-id="a1f40-137">Virtualization Management Application Developers must modify their application to leverage this new feature.</span></span> <span data-ttu-id="a1f40-138">Microsoft 會公開提供 WMI 介面，讓開發人員能夠整合應用程式與這項功能。</span><span class="sxs-lookup"><span data-stu-id="a1f40-138">Microsoft will make WMI interfaces publically available to allow a developer to integrate applications with this feature.</span></span>
-   <span data-ttu-id="a1f40-139">**終端機服務虛擬化：** 這項功能可提供新的虛擬化案例。</span><span class="sxs-lookup"><span data-stu-id="a1f40-139">**Terminal Services virtualization:** This feature enables a new virtualization scenario.</span></span> <span data-ttu-id="a1f40-140">利用終端機服務 (TS) 的應用程式可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="a1f40-140">Applications that leverage Terminal Services (TS) may be impacted.</span></span> <span data-ttu-id="a1f40-141">這項功能會直接與 TS 整合，因此設定 TS 的應用程式可能需要更新，才能管理這項新功能。</span><span class="sxs-lookup"><span data-stu-id="a1f40-141">This feature directly integrates with TS and therefore applications that configure TS may require updating in order to manage this new feature.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a1f40-142">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="a1f40-142">Links to Other Resources</span></span>

<span data-ttu-id="a1f40-143">[Hyper-v v1 的 WMI 管理介面](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)。</span><span class="sxs-lookup"><span data-stu-id="a1f40-143">[WMI management interfaces for Hyper-V v1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal).</span></span> <span data-ttu-id="a1f40-144">雖然此內容大多適用于 Hyper-v 的 v2，但是具有 v2 特定資訊的更新版本應可在更接近 Windows 7 啟動時使用。</span><span class="sxs-lookup"><span data-stu-id="a1f40-144">While most of this content will apply to v2 of Hyper-V, an updated version with v2-specific information should be available closer to the Windows 7 launch.</span></span>

 

 
