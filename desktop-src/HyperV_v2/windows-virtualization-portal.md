---
description: Microsoft Hyper-V server 提供可調整、可靠且高可用性的虛擬機器管理環境。 Hyper-v 虛擬機器軟體會合並伺服器和開發與測試環境。
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: 'Hyper-v WMI 提供者 (V2) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555fd3cd1e8420c59bb5f1b8ef16480b3ddfcf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973447"
---
# <a name="hyper-v-wmi-provider-v2"></a><span data-ttu-id="4e397-104">Hyper-v WMI 提供者 (V2) </span><span class="sxs-lookup"><span data-stu-id="4e397-104">Hyper-V WMI provider (V2)</span></span>

## <a name="purpose"></a><span data-ttu-id="4e397-105">目的</span><span class="sxs-lookup"><span data-stu-id="4e397-105">Purpose</span></span>

<span data-ttu-id="4e397-106">Hyper-v 提供可調整、可靠且高度可用的虛擬化伺服器運算環境。</span><span class="sxs-lookup"><span data-stu-id="4e397-106">Hyper-V provides a scalable, reliable, and highly available virtualized server computing environment.</span></span> <span data-ttu-id="4e397-107">它可讓一或多個客體作業系統同時在單一實體電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="4e397-107">It enables one or more guest operating systems to run concurrently on a single physical computer.</span></span> <span data-ttu-id="4e397-108">虛擬機器技術的主要用途包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="4e397-108">Key uses for virtual machine technology include the following:</span></span>

-   <span data-ttu-id="4e397-109">伺服器合併</span><span class="sxs-lookup"><span data-stu-id="4e397-109">Server consolidation</span></span>
-   <span data-ttu-id="4e397-110">合併開發與測試環境</span><span class="sxs-lookup"><span data-stu-id="4e397-110">Consolidation of development and testing environments</span></span>
-   <span data-ttu-id="4e397-111">簡化嚴重損壞修復</span><span class="sxs-lookup"><span data-stu-id="4e397-111">Simplified disaster recovery</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4e397-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="4e397-112">In this section</span></span>



| <span data-ttu-id="4e397-113">主題</span><span class="sxs-lookup"><span data-stu-id="4e397-113">Topic</span></span>                                                                                                 | <span data-ttu-id="4e397-114">描述</span><span class="sxs-lookup"><span data-stu-id="4e397-114">Description</span></span>                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e397-115">關於 Hyper-v WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="4e397-115">About the Hyper-V WMI provider</span></span>](about-the-virtualization-wmi-provider.md)<br/>                | <span data-ttu-id="4e397-116">Hyper-v 的 WMI 提供者可讓開發人員和腳本撰寫人員快速建立虛擬化平臺的自訂工具、公用程式和增強功能。</span><span class="sxs-lookup"><span data-stu-id="4e397-116">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="4e397-117">WMI 介面可以管理 Hyper-v 服務的所有層面。</span><span class="sxs-lookup"><span data-stu-id="4e397-117">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span><br/> |
| [<span data-ttu-id="4e397-118">使用 Hyper-v WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="4e397-118">Using the Hyper-V WMI provider</span></span>](using-the-virtualization-wmi-provider.md)<br/>                | <span data-ttu-id="4e397-119">下列主題說明如何使用 Hyper-v WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="4e397-119">The following topics describe how to use the Hyper-V WMI provider.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="4e397-120">Hyper-v WMI 類別</span><span class="sxs-lookup"><span data-stu-id="4e397-120">Hyper-V WMI classes</span></span>](hyper-v-wmi-classes.md)<br/>                                             | <span data-ttu-id="4e397-121">以下是 Hyper-v WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="4e397-121">The following are the Hyper-V WMI classes.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="4e397-122">Hyper-v 應用程式健康情況監視 API</span><span class="sxs-lookup"><span data-stu-id="4e397-122">Hyper-V application health monitoring API</span></span>](hyper-v-application-health-monitoring-api.md)<br/> | <span data-ttu-id="4e397-123">Hyper-v 應用程式健康情況監視 API 可用來監視虛擬機器中執行之應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="4e397-123">The Hyper-V application health monitoring API is used to monitor the health state of applications running in a virtual machine.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4e397-124">Hyper-v 複寫 API</span><span class="sxs-lookup"><span data-stu-id="4e397-124">Hyper-V replication API</span></span>](hyper-v-replication-api.md)<br/>                                     | <span data-ttu-id="4e397-125">Hyper-v 複寫 API 用來控制虛擬機器複寫和容錯移轉復原。</span><span class="sxs-lookup"><span data-stu-id="4e397-125">The Hyper-V replication API is used to control virtual machine replication and failover recovery.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="4e397-126">Hyper-v 計量 API</span><span class="sxs-lookup"><span data-stu-id="4e397-126">Hyper-V metrics API</span></span>](hyper-v-metrics-api.md)<br/>                                             | <span data-ttu-id="4e397-127">Hyper-v 計量 API 可用來監視虛擬機器中執行之應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="4e397-127">The Hyper-V metrics API is used to monitor the health state of applications running in a virtual machine.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="4e397-128">Hyper-v 網路 API</span><span class="sxs-lookup"><span data-stu-id="4e397-128">Hyper-V networking API</span></span>](hyper-v-networking-api.md)<br/>                                       | <span data-ttu-id="4e397-129">Hyper-v 網路 API 是用來控制 Hyper-v 中的網路功能。</span><span class="sxs-lookup"><span data-stu-id="4e397-129">The Hyper-V networking API is used to control networking in Hyper-V.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="4e397-130">Hyper-v 遷移 API</span><span class="sxs-lookup"><span data-stu-id="4e397-130">Hyper-V migration API</span></span>](hyper-v-storage-migration-api.md)<br/>                                 | <span data-ttu-id="4e397-131">Hyper-v 遷移 API 是用來控制 Hyper-v 的儲存和即時移轉。</span><span class="sxs-lookup"><span data-stu-id="4e397-131">The Hyper-V migration API is used to control storage and live migration in Hyper-V.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="4e397-132">Hyper-v 虛擬光纖通道 API</span><span class="sxs-lookup"><span data-stu-id="4e397-132">Hyper-V virtual Fibre Channel API</span></span>](hyper-v-virtual-fiber-channels-api.md)<br/>                | <span data-ttu-id="4e397-133">Hyper-v 虛擬光纖通道 API 是用來控制 Hyper-v 中的虛擬光纖通道介面卡。</span><span class="sxs-lookup"><span data-stu-id="4e397-133">The Hyper-V virtual Fibre Channel API is used to control virtual Fibre Channel adapters in Hyper-V.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="4e397-134">Hyper-v VM 放置 API</span><span class="sxs-lookup"><span data-stu-id="4e397-134">Hyper-V VM placement API</span></span>](hyper-v-vm-placement-api.md)<br/>                                   | <span data-ttu-id="4e397-135">Hyper-v 虛擬機器 (VM) 放置 API 包含 Vm 或主控電腦系統的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="4e397-135">The Hyper-V virtual machine (VM) placement API contains the compatibility info for the VMs or hosting computer system.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="4e397-136">閾值類別</span><span class="sxs-lookup"><span data-stu-id="4e397-136">Threshold classes</span></span>](threshold-classes.md)<br/>                                                 | <span data-ttu-id="4e397-137">包含 Windows 10 中引進的類別。</span><span class="sxs-lookup"><span data-stu-id="4e397-137">Contains the classes introduced in Windows 10.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="4e397-138">RS2 類別</span><span class="sxs-lookup"><span data-stu-id="4e397-138">RS2 Classes</span></span>](redstone-classes.md)<br/>                                                        | <span data-ttu-id="4e397-139">包含 Windows 10 1703 版的新類別。</span><span class="sxs-lookup"><span data-stu-id="4e397-139">Contains the new classes for Windows 10, version 1703.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="4e397-140">RS3 類別</span><span class="sxs-lookup"><span data-stu-id="4e397-140">RS3 Classes</span></span>](rs3-classes.md)<br/>                                                             | <span data-ttu-id="4e397-141">包含 Windows 10 1709 版的新類別。</span><span class="sxs-lookup"><span data-stu-id="4e397-141">Contains the new classes for Windows 10, version 1709.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="4e397-142">Hyper-v 詞彙</span><span class="sxs-lookup"><span data-stu-id="4e397-142">Hyper-V glossary</span></span>](virtualization-glossary.md)<br/>                                            | <span data-ttu-id="4e397-143">Windows 虛擬化 SDK 檔中使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="4e397-143">Glossary of terms used in the Windows Virtualization SDK documentation.</span></span><br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a><span data-ttu-id="4e397-144">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="4e397-144">Run-time requirements</span></span>

<span data-ttu-id="4e397-145">Hyper-v 服務需要支援執行 Hyper-v 硬體輔助虛擬化的 x64 型系統。</span><span class="sxs-lookup"><span data-stu-id="4e397-145">Hyper-V services require an x64-based system that supports hardware-assisted virtualization running Hyper-V.</span></span> <span data-ttu-id="4e397-146">不過，與 Hyper-v WMI 介面互動的程式可以在任何支援 WMI 的系統上遠端執行。</span><span class="sxs-lookup"><span data-stu-id="4e397-146">Programs that interact with the Hyper-V WMI interfaces however, can run remotely on any system that supports WMI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e397-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e397-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4e397-148">[Hyper-v (Windows Server 2008 R2 技術文件庫) ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4e397-148">[Hyper-V (Windows Server 2008 R2 Technical Library)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="4e397-149">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="4e397-149">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[<span data-ttu-id="4e397-150">Windows Server Virtualization</span><span class="sxs-lookup"><span data-stu-id="4e397-150">Windows Server Virtualization</span></span>](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

