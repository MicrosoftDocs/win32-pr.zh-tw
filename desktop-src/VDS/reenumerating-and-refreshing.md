---
description: Reenumerating 和重新整理
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerating 和重新整理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988848"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="d2e48-103">Reenumerating 和重新整理</span><span class="sxs-lookup"><span data-stu-id="d2e48-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="d2e48-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="d2e48-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d2e48-105">Reenumeration 作業會探索新連線和最近中斷連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="d2e48-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="d2e48-106">重新整理作業會更新現有裝置的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e48-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="d2e48-107">**Reenumerate 軟體提供者物件**</span><span class="sxs-lookup"><span data-stu-id="d2e48-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="d2e48-108">呼叫 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法。</span><span class="sxs-lookup"><span data-stu-id="d2e48-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="d2e48-109">此方法會探索所有新連線和已中斷連線的磁片和 CD-ROM 光碟機，並確保所有磁片都具有適當的擁有者。</span><span class="sxs-lookup"><span data-stu-id="d2e48-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="d2e48-110">VDS 擁有原始磁片或失敗的磁片;基本提供者擁有基本磁碟;而且動態提供者擁有動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="d2e48-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="d2e48-111">這種作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。</span><span class="sxs-lookup"><span data-stu-id="d2e48-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="d2e48-112">**Reenumerate 和重新整理軟體提供者物件**</span><span class="sxs-lookup"><span data-stu-id="d2e48-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="d2e48-113">呼叫 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法，然後呼叫 [**IVdsService：： Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) 方法。</span><span class="sxs-lookup"><span data-stu-id="d2e48-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="d2e48-114">除了探索新連接和中斷連接的磁片和 CD-ROM 光碟機之外，此方法的組合也會針對尚未最近連線或中斷連線的磁片，更新 VDS 快取中的所有磁片、磁片區和 plex 資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e48-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="d2e48-115">單獨呼叫 **refresh** 以重新整理快取中現有物件的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e48-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="d2e48-116">這種作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。</span><span class="sxs-lookup"><span data-stu-id="d2e48-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="d2e48-117">請注意，當觸發通知的變更發生時，VDS 會自動更新快取。</span><span class="sxs-lookup"><span data-stu-id="d2e48-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="d2e48-118">此外 **，呼叫重新** 整理以回應 VDS 通知可能會導致傳送無限迴圈的通知。</span><span class="sxs-lookup"><span data-stu-id="d2e48-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="d2e48-119">基於這些理由，只有在出現快取未正確更新時，才應該呼叫 **Refresh** 。</span><span class="sxs-lookup"><span data-stu-id="d2e48-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="d2e48-120">**Reenumerate 硬體子系統**</span><span class="sxs-lookup"><span data-stu-id="d2e48-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="d2e48-121">呼叫 [**IVdsHwProvider：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) 方法。</span><span class="sxs-lookup"><span data-stu-id="d2e48-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="d2e48-122">視提供者而定，此作業可能牽涉到傳送網路封包，並等候超時時間、重新掃描 SCSI 匯流排，以及等待超時等等。</span><span class="sxs-lookup"><span data-stu-id="d2e48-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="d2e48-123">**Reenumerate 硬體子系統物件**</span><span class="sxs-lookup"><span data-stu-id="d2e48-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="d2e48-124">呼叫 [**IVdsSubSystem：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) 方法來清查物件 (通常會驅動子系統) 。</span><span class="sxs-lookup"><span data-stu-id="d2e48-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="d2e48-125">視子系統而定，此作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。</span><span class="sxs-lookup"><span data-stu-id="d2e48-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="d2e48-126">**重新整理硬體子系統和子系統物件**</span><span class="sxs-lookup"><span data-stu-id="d2e48-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="d2e48-127">呼叫 [**IVdsHwProvider：： refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) 方法，以重新整理 vds 硬體提供者所管理之現有子系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2e48-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="d2e48-128">請注意，當觸發通知的變更發生時，VDS 會自動更新快取。</span><span class="sxs-lookup"><span data-stu-id="d2e48-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="d2e48-129">此外 [**，呼叫重新**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) 整理以回應 VDS 通知可能會導致傳送無限迴圈的通知。</span><span class="sxs-lookup"><span data-stu-id="d2e48-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="d2e48-130">基於這些理由，只有在出現快取未正確更新時，才應該呼叫 **Refresh** 。</span><span class="sxs-lookup"><span data-stu-id="d2e48-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2e48-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2e48-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e48-132">使用 VDS</span><span class="sxs-lookup"><span data-stu-id="d2e48-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="d2e48-133">**IVdsService::Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="d2e48-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="d2e48-134">**IVdsService：： Refresh**</span><span class="sxs-lookup"><span data-stu-id="d2e48-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="d2e48-135">**IVdsHwProvider::Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="d2e48-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="d2e48-136">**IVdsSubSystem::Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="d2e48-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="d2e48-137">**IVdsHwProvider：： Refresh**</span><span class="sxs-lookup"><span data-stu-id="d2e48-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
