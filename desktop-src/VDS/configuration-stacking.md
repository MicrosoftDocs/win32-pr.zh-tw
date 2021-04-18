---
description: 設定堆疊
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: 設定堆疊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567838"
---
# <a name="configuration-stacking"></a><span data-ttu-id="9db27-103">設定堆疊</span><span class="sxs-lookup"><span data-stu-id="9db27-103">Configuration Stacking</span></span>

<span data-ttu-id="9db27-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="9db27-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="9db27-105">堆疊牽涉到一組邏輯區塊對應的串連。</span><span class="sxs-lookup"><span data-stu-id="9db27-105">Stacking involves the concatenating of a set of logical block mappings.</span></span> <span data-ttu-id="9db27-106">您可以從一個 LUN 下的相同子系統堆疊多個 Lun。</span><span class="sxs-lookup"><span data-stu-id="9db27-106">You can stack multiple LUNs from the same subsystem under one LUN.</span></span> <span data-ttu-id="9db27-107">您可以將 LUN 與同一個磁片區中相同套件的磁片區堆疊在一起。</span><span class="sxs-lookup"><span data-stu-id="9db27-107">You can stack a LUN together with volumes from the same pack under one volume.</span></span> <span data-ttu-id="9db27-108">此外，您可以堆疊一個磁片區下的異類子系統所呈現的多個 Lun。</span><span class="sxs-lookup"><span data-stu-id="9db27-108">Further, you can stack multiple LUNs that are surfaced by heterogeneous subsystems under one volume.</span></span>

<span data-ttu-id="9db27-109">如下圖所示，建立磁片區並不會變更參與 LUN 的現有系結。</span><span class="sxs-lookup"><span data-stu-id="9db27-109">As the following illustration shows, the creating of a volume does not change the existing binding of a contributing LUN.</span></span> <span data-ttu-id="9db27-110">同樣地，解除系結也不會解除系結參與的 LUN。</span><span class="sxs-lookup"><span data-stu-id="9db27-110">Similarly, the unbinding of a volume does not unbind a contributing LUN.</span></span> <span data-ttu-id="9db27-111">下圖描述 RAID 0 1 (0 + 1) 設定。</span><span class="sxs-lookup"><span data-stu-id="9db27-111">The illustration depicts the RAID 0 1 (0+1) configuration.</span></span> <span data-ttu-id="9db27-112">這項知名設定結合了分割 (RAID 0) 和鏡像 (RAID 1) ，可將 RAID 0 的快速資料存取與 RAID 1 的可靠性配對在一起。</span><span class="sxs-lookup"><span data-stu-id="9db27-112">This well-known configuration combines striping (RAID 0) and mirroring (RAID 1), which pairs the fast data access of RAID 0 with the reliability of RAID 1.</span></span>

![顯示 RAID 0 1 (0 + 1) 設定的圖表。](images/vdsstacklunvolzeroplusone.png)

<span data-ttu-id="9db27-114">參與 Lun 的系結類型可能不同。</span><span class="sxs-lookup"><span data-stu-id="9db27-114">Contributing LUNs can have different binding types.</span></span> <span data-ttu-id="9db27-115">有許多設定都可以使用 VDS，但很不可能發生，例如下圖。</span><span class="sxs-lookup"><span data-stu-id="9db27-115">Many configurations are possible with VDS but are highly unlikely, such as the next illustration.</span></span> <span data-ttu-id="9db27-116">在此範例中，一個磁片區 plex 是等量 LUN，另一個則是三向鏡像 LUN。</span><span class="sxs-lookup"><span data-stu-id="9db27-116">In this example, one volume plex is a striped LUN and the other is a three-way mirrored LUN.</span></span>

![顯示 VDS 設定的圖表，其中一個磁片區 plex 是等量 LUN，另一個則是三向鏡像 LUN。](images/vdsstacklunvol.png)

<span data-ttu-id="9db27-118">雖然不實用，但此範例說明堆疊的重要層面。</span><span class="sxs-lookup"><span data-stu-id="9db27-118">Although impractical, this example illustrates an important aspect of stacking.</span></span> <span data-ttu-id="9db27-119">由於堆疊串連了 plex，因此 VDS 會將三個 LUN 的 plex 新增至兩個磁片區的 plex，總共有五個 plex。</span><span class="sxs-lookup"><span data-stu-id="9db27-119">Because stacking concatenates plexes, VDS adds the three LUN plexes to the two volume plexes for a total of five plexes.</span></span>

 

 
