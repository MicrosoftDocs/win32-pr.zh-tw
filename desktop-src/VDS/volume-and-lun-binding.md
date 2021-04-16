---
description: 磁片區和 LUN 系結
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: 磁片區和 LUN 系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195652"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="4ecd7-103">磁片區和 LUN 系結</span><span class="sxs-lookup"><span data-stu-id="4ecd7-103">Volume and LUN Binding</span></span>

<span data-ttu-id="4ecd7-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="4ecd7-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4ecd7-105">系結是指建立磁片區或 Lun。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="4ecd7-106">磁片區是由磁片區和 Lun 組成，由磁片區所組成。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="4ecd7-107">系結會針對實體資源的一組對應進行選取，並且在子系統內、在元件內或同時發生。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="4ecd7-108">所有提供者程式都支援部分導向的系結模型，在此模型中，呼叫端僅指定特定興趣的系結屬性，並允許提供者選擇其餘部分。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="4ecd7-109">在 VDS 中系結磁片區和 Lun 的作業很類似，但不完全相同。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="4ecd7-110">例如，硬體提供者可以提供其他的系結選項。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="4ecd7-111">VDS 針對部分導向的設定支援下列五種磁片區和 LUN 系結類型。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="4ecd7-112"> (硬體提供者可以和支援許多其他系結。 ) </span><span class="sxs-lookup"><span data-stu-id="4ecd7-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="4ecd7-113">詞彙</span><span class="sxs-lookup"><span data-stu-id="4ecd7-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="4ecd7-114">描述</span><span class="sxs-lookup"><span data-stu-id="4ecd7-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecd7-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>簡單</span><span class="sxs-lookup"><span data-stu-id="4ecd7-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="4ecd7-116">只有一個連續範圍的線性對應。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="4ecd7-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>跨越</span><span class="sxs-lookup"><span data-stu-id="4ecd7-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="4ecd7-118">在多個磁片或磁片磁碟機上具有多個非連續範圍的線性對應。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="4ecd7-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>條紋</span><span class="sxs-lookup"><span data-stu-id="4ecd7-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="4ecd7-120">跨多個磁片或磁片磁碟機交錯連續磁片區範圍的對應。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="4ecd7-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>鏡像</span><span class="sxs-lookup"><span data-stu-id="4ecd7-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="4ecd7-122">維護兩個以上相同資料複本的對應。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="4ecd7-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>以同位等量分割</span><span class="sxs-lookup"><span data-stu-id="4ecd7-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="4ecd7-124">在多個磁片或磁片磁碟機之間分散同位檢查資訊的對應。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="4ecd7-125">VDS 會使用來自多個成員的同位系結來建立鏡像、等量和等量分割。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="4ecd7-126">例如，雙向鏡像有兩個成員。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="4ecd7-127">每個成員都可以佔用多個磁片或磁片磁碟機上的範圍。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="4ecd7-128">VDS 會串連範圍來形成成員，然後在成員上系結磁片區或 LUN。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="4ecd7-129">提供者可支援所有系結類型或任何子集。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="4ecd7-130">在 VDS 物件模型中，鏡像的每個成員都是一個稱為 plex 的獨立物件。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="4ecd7-131">同樣地，磁片區和 LUN 類型都很類似，但並非完全相同。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="4ecd7-132">如需磁片區類型的描述，請參閱 [磁片區物件](volume-object.md)。針對 LUN 類型，請參閱 [Lun 物件](lun-object.md)。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="4ecd7-133">系結類型不是容錯或容錯。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="4ecd7-134">不可容錯的系結</span><span class="sxs-lookup"><span data-stu-id="4ecd7-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="4ecd7-135">非容錯磁片區和 Lun 不提供嚴重損壞修復。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="4ecd7-136">如果有一個磁片區對不容錯磁片區或 LUN 造成故障，則整個磁片區或 LUN 會失敗。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="4ecd7-137">在交換中，對於資料的風險，非容錯磁片區和 Lun 提供的輸入/輸出效能通常會優於容錯磁片區和 Lun 的效能。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="4ecd7-138">VDS 支援下列三種不可容錯的類型：簡單、跨距和等量。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="4ecd7-139">簡單</span><span class="sxs-lookup"><span data-stu-id="4ecd7-139">Simple</span></span>

![此圖顯示具有2個元件和2個子系統的簡單非容錯型別。](images/vdssimplelunvol.png)

<span data-ttu-id="4ecd7-141">合併</span><span class="sxs-lookup"><span data-stu-id="4ecd7-141">Spanned</span></span>

![顯示具有1個套件和1個子系統的跨距非容錯類型圖表。](images/vdsspanlunvol.png)

<span data-ttu-id="4ecd7-143">等量</span><span class="sxs-lookup"><span data-stu-id="4ecd7-143">Striped</span></span>

![顯示具有1個套件和1個子系統之等量非容錯類型的圖表。](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="4ecd7-145">容錯系結</span><span class="sxs-lookup"><span data-stu-id="4ecd7-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="4ecd7-146">下列容錯磁片區和 Lun 提供嚴重損壞修復。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="4ecd7-147">如果其中一個磁片區對容錯磁片區或 LUN 失敗，則可以復原資料。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="4ecd7-148">在資料安全性的 exchange 中，容錯磁片區和 Lun 的輸入/輸出效能通常會與非容錯磁片區和 Lun 的輸入/輸出效能很差。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="4ecd7-149">VDS 支援兩種容錯類型：使用同位鏡像和等量分割。</span><span class="sxs-lookup"><span data-stu-id="4ecd7-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="4ecd7-150">鏡像 (三向鏡像) </span><span class="sxs-lookup"><span data-stu-id="4ecd7-150">Mirrored (three-way mirror)</span></span>

![顯示鏡像 (三向鏡像) 容錯類型的圖表。](images/vdsmirrorlunvol.png)

<span data-ttu-id="4ecd7-152">以同位等量分割</span><span class="sxs-lookup"><span data-stu-id="4ecd7-152">Striped with parity</span></span>

![顯示具有同位容錯類型之等量的圖表。](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="4ecd7-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ecd7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ecd7-155">設定總覽</span><span class="sxs-lookup"><span data-stu-id="4ecd7-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="4ecd7-156">磁片區物件</span><span class="sxs-lookup"><span data-stu-id="4ecd7-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="4ecd7-157">LUN 物件</span><span class="sxs-lookup"><span data-stu-id="4ecd7-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

