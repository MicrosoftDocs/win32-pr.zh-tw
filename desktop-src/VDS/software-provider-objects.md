---
description: 軟體提供者物件
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: 軟體提供者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "103853219"
---
# <a name="software-provider-objects"></a><span data-ttu-id="5ff95-103">軟體提供者物件</span><span class="sxs-lookup"><span data-stu-id="5ff95-103">Software Provider Objects</span></span>

<span data-ttu-id="5ff95-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="5ff95-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5ff95-105">軟體提供者物件會建立實體裝置的模型，例如 IDE 磁片和 CD-ROM，以及套件、磁片區和磁片區 plex 等虛擬元素。</span><span class="sxs-lookup"><span data-stu-id="5ff95-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="5ff95-106">下圖顯示提供者物件與一組軟體提供者物件之間的關聯性，以及各種軟體提供者物件本身之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="5ff95-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![顯示「提供者」與「軟體提供者」物件之間關聯性的圖表，例如「套件」和「磁片區」。](images/vdsswobjects.png)

<span data-ttu-id="5ff95-108">提供者物件可以包含零或多個套件。</span><span class="sxs-lookup"><span data-stu-id="5ff95-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="5ff95-109">套件物件可以包含零或多個磁片與磁片區。</span><span class="sxs-lookup"><span data-stu-id="5ff95-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="5ff95-110">磁片區是由至少一個磁片區 plex 所組成，且每個磁片區 plex 都可以對應至一或多個磁片（視 plex 類型而定）。</span><span class="sxs-lookup"><span data-stu-id="5ff95-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="5ff95-111">VDS 直接管理未配置的磁片，沒有套件容器。</span><span class="sxs-lookup"><span data-stu-id="5ff95-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="5ff95-112">本節的其餘主題描述套件、磁片、磁片區和磁片區 plex 物件。</span><span class="sxs-lookup"><span data-stu-id="5ff95-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff95-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ff95-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff95-114">VDS 物件模型</span><span class="sxs-lookup"><span data-stu-id="5ff95-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
