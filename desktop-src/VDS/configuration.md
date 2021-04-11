---
description: 設定總覽
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: 設定總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943356"
---
# <a name="configuration-overview"></a><span data-ttu-id="5a9ca-103">設定總覽</span><span class="sxs-lookup"><span data-stu-id="5a9ca-103">Configuration Overview</span></span>

<span data-ttu-id="5a9ca-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="5a9ca-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5a9ca-105">如果您不熟悉 VDS 所定義的物件，請參閱 [Vds 物件模型](vds-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="5a9ca-106">虛擬磁片的設定複雜度可能從非常簡單到微調的範圍。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="5a9ca-107">不在意、無人在意和企業虛擬磁片會定義三種一般設定的觀點。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="5a9ca-108">每個觀點都呈現不同的需求：</span><span class="sxs-lookup"><span data-stu-id="5a9ca-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="5a9ca-109">不需要小心設定的虛擬磁片，或許只是為了將新磁片的磁碟分割和格式設定自動化，或暫時建立鏡像磁片區以將資料從一個磁片遷移到另一個磁片，而不需要停機。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="5a9ca-110">這種磁片適用于具有一或多個磁片的筆記本電腦和其他系統。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="5a9ca-111">免費的虛擬磁片提供可自行設定、自我修復和可用的儲存體;使用等量磁片區和 Lun 來達到更佳的效能;使用鏡像磁片區和 Lun 來達成更高的可用性;並使用套件使失敗模式變成乾淨且包含。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="5a9ca-112">以新的大型快速磁片來取代舊的小型系統磁片時，此設定層級很理想。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="5a9ca-113">它也適用于使用自動熱備份的鏡像資料—單一備用主軸可以保護許多磁片主軸。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="5a9ca-114">如需詳細資訊，請參閱 [熱備份](hot-sparing.md)。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="5a9ca-115">小規模 San 取決於此設定層級所提供的彈性和自動化，與網路連接儲存 (NAS) 設備一樣。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="5a9ca-116">免費的虛擬磁片可簡化合並應用程式儲存體的工作（例如，SQL 和 Exchange 的儲存體），而不需要合併伺服器。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="5a9ca-117">企業虛擬磁片包含非常大型或複雜的企業設定，具有額外的網站特定或應用程式特定需求。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="5a9ca-118">系統管理員會針對可能只執行的單一應用程式調整儲存子系統，例如訂單交易系統上的每月批次報告作業。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="5a9ca-119">企業虛擬磁片必須調整規模、顯示儲存子系統的即時活動，以及滿足實際操作管理員的需求。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="5a9ca-120">如需有關在 VDS 中鏡像、條紋和其他設定選項的詳細資訊，請參閱 [磁片區和 LUN](volume-and-lun-binding.md)系結。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="5a9ca-121">先進的設定技術稱為「堆疊」，可讓您結合與現有磁片區和 Lun 相關聯的設定。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="5a9ca-122">如需詳細資訊，請參閱設定 [堆疊](configuration-stacking.md)。</span><span class="sxs-lookup"><span data-stu-id="5a9ca-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a9ca-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a9ca-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9ca-124">虛擬磁碟服務</span><span class="sxs-lookup"><span data-stu-id="5a9ca-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="5a9ca-125">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="5a9ca-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="5a9ca-126">熱備份</span><span class="sxs-lookup"><span data-stu-id="5a9ca-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="5a9ca-127">磁片區和 LUN 系結</span><span class="sxs-lookup"><span data-stu-id="5a9ca-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="5a9ca-128">設定堆疊</span><span class="sxs-lookup"><span data-stu-id="5a9ca-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
