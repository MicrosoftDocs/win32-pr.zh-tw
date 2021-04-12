---
description: 磁片區 Plex 物件
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: 磁片區 Plex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a858bc6ce98761bb687e8dca473b1b68879da8
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104321332"
---
# <a name="volume-plex-object"></a><span data-ttu-id="254d4-103">磁片區 Plex 物件</span><span class="sxs-lookup"><span data-stu-id="254d4-103">Volume Plex Object</span></span>

<span data-ttu-id="254d4-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="254d4-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="254d4-105">磁片區 plex 物件會建立磁片區所包含的磁片區 plex 模型。</span><span class="sxs-lookup"><span data-stu-id="254d4-105">A volume plex object models a volume plex that is contained by a volume.</span></span> <span data-ttu-id="254d4-106">只有鏡像磁片區可以有多個 plex;所有其他磁片區類型都有一個 plex。</span><span class="sxs-lookup"><span data-stu-id="254d4-106">Only a mirrored volume can have multiple plexes; all other volume types have one plex.</span></span> <span data-ttu-id="254d4-107">每個 plex 都包含磁片區上的資料複本。</span><span class="sxs-lookup"><span data-stu-id="254d4-107">Each plex contains a copy of the data on the volume.</span></span> <span data-ttu-id="254d4-108">VDS 支援四個磁片區的磁片區 plex 類型：簡單、跨距、等量和同位檢查。</span><span class="sxs-lookup"><span data-stu-id="254d4-108">VDS supports four volume plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="254d4-109">如需這些磁片區類型的說明，請參閱 [磁片區物件](volume-object.md)。</span><span class="sxs-lookup"><span data-stu-id="254d4-109">For a description of each of these volume types, see the [Volume Object](volume-object.md).</span></span>

<span data-ttu-id="254d4-110">有兩種方式可以建立具有多個 plex 的磁片區。</span><span class="sxs-lookup"><span data-stu-id="254d4-110">There are two ways to create a volume with multiple plexes.</span></span> <span data-ttu-id="254d4-111">您可以使用 [**IVdsPack：： CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) 方法直接建立鏡像磁片區，或使用 [**IVdsVolume：： AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) 方法將一個磁片區新增到另一個磁片區。</span><span class="sxs-lookup"><span data-stu-id="254d4-111">You can use the [**IVdsPack::CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) method to create the mirrored volume directly, or use the [**IVdsVolume::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) method to add one volume to another volume.</span></span> <span data-ttu-id="254d4-112">磁片區 (以及基礎磁片) 必須位於相同的套件中。</span><span class="sxs-lookup"><span data-stu-id="254d4-112">The volumes (and the underlying disks) must be in the same pack.</span></span> <span data-ttu-id="254d4-113">下圖顯示一個範例，說明如何將一個磁片區 (B) 做為) 的另一個 (磁片區，以及產生的多工磁片區 () 。</span><span class="sxs-lookup"><span data-stu-id="254d4-113">The following illustration shows an example of adding one volume (B) as a plex to another volume (A), and the resulting multiplexed volume (A).</span></span> <span data-ttu-id="254d4-114">磁片區 A 上的資料會保持不變，而磁片區 B 上的資料會變成磁片區 A 上的鏡像資料複本。</span><span class="sxs-lookup"><span data-stu-id="254d4-114">The data on volume A remains intact, while the data on volume B becomes a mirrored copy of the data on volume A.</span></span>

![顯示兩個單一 plex 的圖表，一個具有簡單磁片區 A，另一個具有簡單磁片區 B，等於具有鏡像磁片區 A 的多重 plex。](images/vdsplex.png)

<span data-ttu-id="254d4-116">您可以藉由叫用 [**IVdsVolume：： QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) 方法來查詢磁片區的 plex。</span><span class="sxs-lookup"><span data-stu-id="254d4-116">You can query for volume plexes by invoking the [**IVdsVolume::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) method.</span></span> <span data-ttu-id="254d4-117">您可以從 **QueryPlexes** 傳回的列舉中選取所需的 plex 物件，以取得特定磁片區 plex 的指標。</span><span class="sxs-lookup"><span data-stu-id="254d4-117">You can get a pointer to a specific volume plex by selecting the desired plex object from the enumeration that is returned by **QueryPlexes**.</span></span> <span data-ttu-id="254d4-118">除了最後一個 plex 之外，現有的 plex 也可以中斷或移除。</span><span class="sxs-lookup"><span data-stu-id="254d4-118">With the exception of the last plex, existing plexes can be broken or removed.</span></span> <span data-ttu-id="254d4-119">使用 [**IVdsVolume：： BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) 從磁片區分割一個 plex，然後將中斷的 plex 物件轉換成磁片區物件。</span><span class="sxs-lookup"><span data-stu-id="254d4-119">Use the [**IVdsVolume::BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) to split a plex from a volume and convert the broken plex object into a volume object.</span></span> <span data-ttu-id="254d4-120">使用 [**IVdsVolume：： RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) 可完全刪除該 plex。</span><span class="sxs-lookup"><span data-stu-id="254d4-120">Use the [**IVdsVolume::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) to delete the plex altogether.</span></span> <span data-ttu-id="254d4-121">您可以藉由呼叫 [**IVdsVolumePlex：： repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) 方法，將錯誤的成員移至良好的磁片，藉以嘗試修復容錯叢。</span><span class="sxs-lookup"><span data-stu-id="254d4-121">You can attempt to repair a fault-tolerant plex by calling the [**IVdsVolumePlex::Repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) method, which moves bad members to good disks.</span></span>

<span data-ttu-id="254d4-122">除了物件識別碼和 plex 類型之外，磁片區 plex 物件屬性還包括 plex 的狀態、健全狀況和轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="254d4-122">In addition to an object identifier and plex type, volume plex object properties include the status, health, and transition state of the plex.</span></span> <span data-ttu-id="254d4-123">此物件沒有旗標。</span><span class="sxs-lookup"><span data-stu-id="254d4-123">This object has no flags.</span></span>

<span data-ttu-id="254d4-124">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="254d4-124">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="254d4-125">類型</span><span class="sxs-lookup"><span data-stu-id="254d4-125">Type</span></span>                                              | <span data-ttu-id="254d4-126">元素</span><span class="sxs-lookup"><span data-stu-id="254d4-126">Element</span></span>                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="254d4-127">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="254d4-127">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="254d4-128">[**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex)。</span><span class="sxs-lookup"><span data-stu-id="254d4-128">[**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).</span></span>                                                                                                                                          |
| <span data-ttu-id="254d4-129">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="254d4-129">Associated enumerations</span></span>                           | <span data-ttu-id="254d4-130">[**VDS \_磁片區 \_ PLEX \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status)、vds 磁片區 [**\_ \_ plex \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)，以及 [**VDS \_ 磁片 \_ 區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)。</span><span class="sxs-lookup"><span data-stu-id="254d4-130">[**VDS\_VOLUME\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**VDS\_VOLUME\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type), and [**VDS\_DISK\_EXTENT\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).</span></span> |
| <span data-ttu-id="254d4-131">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="254d4-131">Associated structures</span></span>                             | <span data-ttu-id="254d4-132">[**VDS \_磁片 \_ 區 \_ PLEX**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop)的大小。</span><span class="sxs-lookup"><span data-stu-id="254d4-132">[**VDS\_VOLUME\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).</span></span>                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="254d4-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="254d4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="254d4-134">軟體提供者物件</span><span class="sxs-lookup"><span data-stu-id="254d4-134">Software Provider Objects</span></span>](software-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="254d4-135">磁片區物件</span><span class="sxs-lookup"><span data-stu-id="254d4-135">Volume Object</span></span>](volume-object.md)
</dt> </dl>

 

 
