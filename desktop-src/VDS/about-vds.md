---
description: 關於 VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: 關於 VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104553007"
---
# <a name="about-vds"></a><span data-ttu-id="e332f-103">關於 VDS</span><span class="sxs-lookup"><span data-stu-id="e332f-103">About VDS</span></span>

<span data-ttu-id="e332f-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="e332f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e332f-105">虛擬磁碟服務是 Microsoft Windows 服務，它會在要求使用者、腳本和應用程式時執行查詢和設定作業。</span><span class="sxs-lookup"><span data-stu-id="e332f-105">Virtual Disk Service is a Microsoft Windows service that performs query and configuration operations at the request of end users, scripts, and applications.</span></span> <span data-ttu-id="e332f-106">服務會以下列方式擴充 Windows Server 作業系統的現有儲存功能：</span><span class="sxs-lookup"><span data-stu-id="e332f-106">The service extends the existing storage capabilities of Windows Server operating systems in the following ways:</span></span>

-   <span data-ttu-id="e332f-107">提供 API 給 Windows 中現有的磁片區和磁片管理功能。</span><span class="sxs-lookup"><span data-stu-id="e332f-107">Provides an API to the existing volume and disk management features in Windows.</span></span>
-   <span data-ttu-id="e332f-108">整合磁片區管理和獨立磁片的硬體冗餘數組， (RAID) 管理單一 API。</span><span class="sxs-lookup"><span data-stu-id="e332f-108">Unifies volume management and hardware Redundant Array of Independent Disks (RAID) management under a single API.</span></span>

<span data-ttu-id="e332f-109">VDS 不會執行下列儲存管理活動：</span><span class="sxs-lookup"><span data-stu-id="e332f-109">VDS does not perform the following storage-management activities:</span></span>

-   <span data-ttu-id="e332f-110">硬體子系統管理，例如溫度監視或監視磁碟陣列的效能統計資料。</span><span class="sxs-lookup"><span data-stu-id="e332f-110">Hardware subsystem management, such as temperature monitoring or the monitoring of performance statistics for disk arrays.</span></span>
-   <span data-ttu-id="e332f-111">存放區域網路 (SAN) 網狀架構管理，例如 Host-Based Adapter (HBA) 分區和安全性。</span><span class="sxs-lookup"><span data-stu-id="e332f-111">Storage Area Network (SAN) fabric management, such as Host-Based Adapter (HBA) zoning and security.</span></span>

<span data-ttu-id="e332f-112">接下來的各節描述 VDS 的架構、VDS 提供者的角色，以及 API。</span><span class="sxs-lookup"><span data-stu-id="e332f-112">The sections that follow describe the architecture of VDS, the role of VDS providers, and the API.</span></span>

## <a name="service-architecture"></a><span data-ttu-id="e332f-113">服務架構</span><span class="sxs-lookup"><span data-stu-id="e332f-113">Service Architecture</span></span>

<span data-ttu-id="e332f-114">VDS 定義三個介面：應用層和服務之間的單一介面，以及服務與資料層中提供者程式之間的兩個介面。</span><span class="sxs-lookup"><span data-stu-id="e332f-114">VDS defines three interfaces: a single interface between the application layer and the service, and two interfaces between the service and provider programs in the data layer.</span></span> <span data-ttu-id="e332f-115">下圖顯示應用程式與服務的界限，以及服務對提供者的界限。</span><span class="sxs-lookup"><span data-stu-id="e332f-115">The following illustration shows the application-to-service boundary and the service-to-provider boundary.</span></span>

![顯示服務架構分成「應用程式」、「虛擬磁碟服務」和「VDS 提供者」區段的圖表。](images/vdsoverview.png)

<span data-ttu-id="e332f-117">多層式架構可讓 VDS 協調檔案系統功能、同步處理提供者活動，以及在應用程式之間進行仲裁。</span><span class="sxs-lookup"><span data-stu-id="e332f-117">N-tier architecture enables VDS to coordinate with the file-system functions, synchronize provider activities, and arbitrate between applications.</span></span> <span data-ttu-id="e332f-118">在應用程式和提供者之間，VDS 會提供統一的功能給應用程式，即使某些基礎提供者可能缺乏這樣的一致性。</span><span class="sxs-lookup"><span data-stu-id="e332f-118">Being between the application and provider, VDS presents uniform functionality to applications even though some the underlying providers might lack such uniformity.</span></span>

<span data-ttu-id="e332f-119">此服務會執行一般功能：格式化磁片區、新增和移除磁碟機號或掛接的資料夾，以及管理未配置的磁片—沒有磁碟分割資訊的磁片。</span><span class="sxs-lookup"><span data-stu-id="e332f-119">The service implements common functionality: formatting volumes, adding and removing drive letters or mounted folders, as well as managing unallocated disks—disks having no partition information.</span></span> <span data-ttu-id="e332f-120">VDS 也會將事件通知傳回給已註冊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e332f-120">VDS also returns event notifications to registered applications.</span></span> <span data-ttu-id="e332f-121">如需詳細資訊，請參閱 [VDS 通知](vds-notification-model.md)。</span><span class="sxs-lookup"><span data-stu-id="e332f-121">For details, see [VDS Notifications](vds-notification-model.md).</span></span>

## <a name="role-of-providers"></a><span data-ttu-id="e332f-122">提供者的角色</span><span class="sxs-lookup"><span data-stu-id="e332f-122">Role of Providers</span></span>

<span data-ttu-id="e332f-123">VDS 定義了兩個提供者介面，一個用於軟體提供者，另一個用於硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="e332f-123">VDS defines two provider interfaces, one for a software provider and one for a hardware provider.</span></span> <span data-ttu-id="e332f-124">每個提供者都會執行 VDS 所定義之 API 的不同部分：</span><span class="sxs-lookup"><span data-stu-id="e332f-124">Each provider implements a different portion of the API defined by VDS:</span></span>

-   <span data-ttu-id="e332f-125">*軟體提供者* 是以主機為基礎的程式，由存放裝置 i/o 堆疊中的核心模式驅動程式支援。</span><span class="sxs-lookup"><span data-stu-id="e332f-125">A *software provider* is a host-based program that is supported by a kernel-mode driver in the storage I/O stack.</span></span> <span data-ttu-id="e332f-126">提供者核心執行時間會在開機時與裝載管理員進行互動，或在探索期間隨插即用 (PnP) 管理員來索取每個磁片。</span><span class="sxs-lookup"><span data-stu-id="e332f-126">The provider-kernel runtime interacts with the Mount Manager at boot time or the Plug and Play (PnP) Manager at discovery time to claim each disk.</span></span> <span data-ttu-id="e332f-127">軟體提供者會在磁片區、磁片和磁碟分割上運作。</span><span class="sxs-lookup"><span data-stu-id="e332f-127">Software providers operate on volumes, disks, and disk partitions.</span></span>

    <span data-ttu-id="e332f-128">VDS 包含兩種提供者類型。</span><span class="sxs-lookup"><span data-stu-id="e332f-128">VDS includes two provider types.</span></span> <span data-ttu-id="e332f-129">基本軟體提供者會管理基本磁碟，而不提供容錯系結。</span><span class="sxs-lookup"><span data-stu-id="e332f-129">The basic software provider manages basic disks and offers no fault-tolerant binding.</span></span> <span data-ttu-id="e332f-130">動態軟體提供者會管理動態磁碟，並在適用時提供錯誤管理。</span><span class="sxs-lookup"><span data-stu-id="e332f-130">The dynamic software provider manages dynamic disks and offers fault management where applicable.</span></span> <span data-ttu-id="e332f-131">軟體提供者行為與主機上的基本和動態磁碟的行為一致。</span><span class="sxs-lookup"><span data-stu-id="e332f-131">Software-provider behavior is consistent with the behavior of basic and dynamic disks on the host.</span></span> <span data-ttu-id="e332f-132">例如，如果指定主機的作業系統支援容錯動態磁碟，則 VDS 也支援主機上的這項行為。</span><span class="sxs-lookup"><span data-stu-id="e332f-132">For example, if the operating system of a given host supports fault-tolerant dynamic disks, VDS also supports this behavior on the host.</span></span>

-   <span data-ttu-id="e332f-133">*硬體提供者* 會執行用來管理儲存子系統的方法，這是硬體磁碟陣列或介面卡，可讓您建立邏輯磁片以增強效能、資料可用性或資料復原。</span><span class="sxs-lookup"><span data-stu-id="e332f-133">A *hardware provider* implements the methods that are used to manage a storage subsystem—a hardware disk array or adapter card that enables the creation of logical disks configured to enhance performance, data availability, or data recovery.</span></span> <span data-ttu-id="e332f-134">許多主要的 RAID 封包製造商都產生了專為與 VDS 搭配使用而設計的硬體提供者。</span><span class="sxs-lookup"><span data-stu-id="e332f-134">Many major RAID cabinet manufacturers have produced a hardware provider that is designed for use with VDS.</span></span> <span data-ttu-id="e332f-135">服務取用者必須從製造商取得硬體提供者和相關聯的硬體。</span><span class="sxs-lookup"><span data-stu-id="e332f-135">Service consumers must obtain a hardware provider and associated hardware from the manufacturer.</span></span>

    <span data-ttu-id="e332f-136">硬體提供者的功能取決於基礎硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="e332f-136">The capabilities of a hardware provider depend on the capabilities of the underlying hardware.</span></span> <span data-ttu-id="e332f-137">因此，每個製造商實施 API 的程度可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="e332f-137">Consequently, the degree to which each manufacturer implements the API can vary.</span></span> <span data-ttu-id="e332f-138">例如，製造商可以包含其他方法來優化設定、監視及動態調整效能、將錯誤管理自動化，或提供其他有用的功能。</span><span class="sxs-lookup"><span data-stu-id="e332f-138">For example, manufacturers can include additional methods to optimize configurations, monitor and dynamically tune performance, automate fault management, or provide other beneficial functionality.</span></span>

    <span data-ttu-id="e332f-139">硬體提供者提供數個無法供軟體提供者使用的設定選項。</span><span class="sxs-lookup"><span data-stu-id="e332f-139">Hardware providers offer several configuration options that are not available to the software providers.</span></span> <span data-ttu-id="e332f-140">最值得注意的是 automagic 設定模型，它會針對每個應用程式呈現以屬性為基礎的儲存體觀點。</span><span class="sxs-lookup"><span data-stu-id="e332f-140">Most notable is the automagic configuration model, which presents an attribute-based view of storage to each application.</span></span> <span data-ttu-id="e332f-141">系結提示（例如「大部分讀取」或「快速損毀復原」）取代將實體儲存體系結至虛擬儲存體的複雜性。</span><span class="sxs-lookup"><span data-stu-id="e332f-141">Binding hints, such as "mostly reads" or "fast crash recovery required" replace the complexity of binding physical storage into virtual storage.</span></span> <span data-ttu-id="e332f-142">每個硬體提供者會根據應用程式所提交的提示，執行範圍對應、空間配置以及系結類型選取專案。</span><span class="sxs-lookup"><span data-stu-id="e332f-142">Each hardware provider performs extent mapping, space allocation, and binding-type selection based on the hints that are submitted by an application.</span></span> <span data-ttu-id="e332f-143">如需完整的硬體提供者描述，包括設定選項，請參閱子系統製造商提供的檔。</span><span class="sxs-lookup"><span data-stu-id="e332f-143">For the complete hardware provider description, including the configuration options, see the documentation that is supplied by the subsystem manufacturer.</span></span>

## <a name="application-programming-interface"></a><span data-ttu-id="e332f-144">應用程式設計介面</span><span class="sxs-lookup"><span data-stu-id="e332f-144">Application Programming Interface</span></span>

<span data-ttu-id="e332f-145">應用程式可以叫用 VDS 方法來查詢及設定主機型磁片、RAID 存放裝置或兩者。</span><span class="sxs-lookup"><span data-stu-id="e332f-145">Applications can invoke VDS methods to query and configure host-based disks, RAID storage, or both.</span></span> <span data-ttu-id="e332f-146">如需 API 的總覽，請參閱 [VDS 物件模型](vds-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="e332f-146">For an overview of the API, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="e332f-147">適用于 VDS 的一般應用程式可解決設定管理和監視問題，並將專用儲存體管理系統的範圍從專用的儲存管理系統移至後端應用程式，以更妥善掌控設定或錯誤管理。</span><span class="sxs-lookup"><span data-stu-id="e332f-147">Typical applications for VDS solve configuration management and monitoring problems, and range from dedicated storage-management systems to back-office applications seeking better control over configuration or fault management.</span></span> <span data-ttu-id="e332f-148">下列應用程式現在會使用 VDS：</span><span class="sxs-lookup"><span data-stu-id="e332f-148">The following applications use VDS today:</span></span>

-   <span data-ttu-id="e332f-149">磁片管理嵌入式管理單元會設定及管理主機電腦所控制的磁片。</span><span class="sxs-lookup"><span data-stu-id="e332f-149">The Disk Management snap-in configures and manages disks controlled by a host computer.</span></span> <span data-ttu-id="e332f-150">系統管理員和終端使用者可以使用此使用者介面 (UI) 工具來查詢及設定本機 (或遠端) 磁片和磁片區。</span><span class="sxs-lookup"><span data-stu-id="e332f-150">System administrators and end users can query and configure local (or remote) disks and volumes with this user interface (UI) tool.</span></span>
-   <span data-ttu-id="e332f-151">Diskpart.exe 是一種命令列公用程式，可設定及管理磁片、磁片區和磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="e332f-151">Diskpart.exe is a command-line utility that configures and manages disks, volumes, and partitions.</span></span>
-   <span data-ttu-id="e332f-152">Diskraid.exe 是一種命令列公用程式，可設定和管理硬體 RAID 子系統。</span><span class="sxs-lookup"><span data-stu-id="e332f-152">Diskraid.exe is a command-line utility that configures and manages hardware RAID subsystems.</span></span> <span data-ttu-id="e332f-153">此公用程式可以與任何隨附于 VDS 硬體提供者的存放裝置硬體互動。</span><span class="sxs-lookup"><span data-stu-id="e332f-153">This utility can interact with any storage hardware that is accompanied by a VDS hardware provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e332f-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="e332f-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e332f-155">虛擬磁碟服務</span><span class="sxs-lookup"><span data-stu-id="e332f-155">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="e332f-156">VDS 通知</span><span class="sxs-lookup"><span data-stu-id="e332f-156">VDS Notifications</span></span>](vds-notification-model.md)
</dt> <dt>

[<span data-ttu-id="e332f-157">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="e332f-157">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
