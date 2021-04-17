---
description: Pack 物件
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Pack 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b01978747df5ccc273a31ae2f516b35c01df96
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566114"
---
# <a name="pack-object"></a><span data-ttu-id="37f0e-103">Pack 物件</span><span class="sxs-lookup"><span data-stu-id="37f0e-103">Pack Object</span></span>

<span data-ttu-id="37f0e-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="37f0e-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="37f0e-105">套件物件會建立磁片群組的模型，這是由基本或動態軟體提供者所管理的磁片和磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="37f0e-105">A pack object models a disk group, a collection of disks and volumes managed by the basic or dynamic software provider.</span></span> <span data-ttu-id="37f0e-106">提供者可以包含多個套件物件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-106">A provider can contain multiple pack objects.</span></span>

<span data-ttu-id="37f0e-107">使用 API，應用程式可以指示 VDS 將一或多個磁片新增至套件、將磁片系結至磁片區，並選擇性地將磁片移為主機之間的單位。</span><span class="sxs-lookup"><span data-stu-id="37f0e-107">Using the API, applications can direct VDS to add one or more disks to a pack, bind the disks into volumes, and optionally move the disks as a unit between hosts.</span></span> <span data-ttu-id="37f0e-108">您無法將現有的磁片區匯入套件中。</span><span class="sxs-lookup"><span data-stu-id="37f0e-108">You cannot import an existing volume into a pack.</span></span>

> [!Note]  
> <span data-ttu-id="37f0e-109">套件中的成員資格不表示與效能、媒體、互連通訊協定或其他特性相關的磁片之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="37f0e-109">Membership in a pack does not imply consistency among disks with respect to performance, media, interconnection protocol, or other characteristics.</span></span>

 

<span data-ttu-id="37f0e-110">磁片物件為未配置、由 VDS 管理，或只是一個套件的成員。</span><span class="sxs-lookup"><span data-stu-id="37f0e-110">Disk objects are either unallocated, and managed by VDS, or are members of exactly one pack.</span></span> <span data-ttu-id="37f0e-111">基本軟體提供者可以有零或多個套件，每個都包含單一基本磁碟。</span><span class="sxs-lookup"><span data-stu-id="37f0e-111">The basic software provider can have zero or more packs, each containing a single basic disk.</span></span> <span data-ttu-id="37f0e-112">提供者對基本磁碟上的磁片區數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="37f0e-112">The provider imposes no limits to the number of volumes on a basic disk.</span></span> <span data-ttu-id="37f0e-113">動態提供者可以有零或多個套件，且每個套件中都有多個動態磁碟。</span><span class="sxs-lookup"><span data-stu-id="37f0e-113">The dynamic provider can have zero or more packs with multiple dynamic disks in each pack.</span></span> <span data-ttu-id="37f0e-114">此提供者會根據邏輯磁片管理員 (LDM) 資料庫的一 mb 大小，限制磁片上的磁片區數目。</span><span class="sxs-lookup"><span data-stu-id="37f0e-114">This provider limits the number of volumes on a disk, based on the one-megabyte size of the logical disk manager (LDM) database.</span></span> <span data-ttu-id="37f0e-115">由於磁片區至少有一個 plex 和一個磁片區，因此套件的磁片區數目上限大約是1000。</span><span class="sxs-lookup"><span data-stu-id="37f0e-115">Given that a volume has at least one plex and one disk extent, the maximum number of volumes to a pack is approximately 1000.</span></span> <span data-ttu-id="37f0e-116">當磁片數目增加時，最大值會下降。</span><span class="sxs-lookup"><span data-stu-id="37f0e-116">The maximum number goes down as the number of disks goes up.</span></span>

<span data-ttu-id="37f0e-117">除了磁片物件之外，套件還可包含一或多個硬體提供者所執行的一或多個 LUN 物件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-117">In addition to disk objects, a pack can contain one or more LUN objects implemented by one or more hardware providers.</span></span> <span data-ttu-id="37f0e-118">在 Windows 核心中，LUN 只是另一個磁片。</span><span class="sxs-lookup"><span data-stu-id="37f0e-118">To the Windows kernel, a LUN is just another disk.</span></span> <span data-ttu-id="37f0e-119"> (LUN 物件必須在執行提供者程式的電腦上取消遮罩。 ) 當磁片為 LUN 時，LUN 物件會同時公開 [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) 和 [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) 介面。</span><span class="sxs-lookup"><span data-stu-id="37f0e-119">(LUN objects must be unmasked to the computer that is executing the provider program.) When the disk is a LUN, the LUN object exposes both the [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) and [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interfaces.</span></span> <span data-ttu-id="37f0e-120">套件物件會使用 **IVdsDisk**（而不是 **IVdsLun**）來列舉套件中的 lun。</span><span class="sxs-lookup"><span data-stu-id="37f0e-120">A pack object uses **IVdsDisk**, instead of **IVdsLun**, to enumerate the LUNs in a pack.</span></span> <span data-ttu-id="37f0e-121">如需 LUN 的詳細描述，請參閱 [Lun 物件](lun-object.md)。</span><span class="sxs-lookup"><span data-stu-id="37f0e-121">For a more detailed description of a LUN, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="37f0e-122">下圖顯示具有兩個成員的套件：磁片和 LUN。</span><span class="sxs-lookup"><span data-stu-id="37f0e-122">The following illustration shows a pack with two members: a disk and a LUN.</span></span> <span data-ttu-id="37f0e-123">應用程式可以將這些物件新增至線上元件，並從磁片區和磁片區所代表的磁片區建立磁片區。</span><span class="sxs-lookup"><span data-stu-id="37f0e-123">An application can add these objects to an online pack and create a volume from the underlying disk and drive extents represented by spindles.</span></span>

![顯示「套件」的圖表，其中包含由應用程式新增的磁片和 LUN，以建立由「磁片磁碟機」和「主軸」表示的磁片區。](images/vdsdisksareluns.png)

<span data-ttu-id="37f0e-125">使用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法來建立新的套件物件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-125">Use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new pack object.</span></span> <span data-ttu-id="37f0e-126">呼叫端可以從 [**IVdsSwProvider：： QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) 方法所傳回的列舉中選取所需的套件物件，以取得特定套件的指標。</span><span class="sxs-lookup"><span data-stu-id="37f0e-126">Callers can get a pointer to a specific pack by selecting the desired pack object from the enumeration that is returned by the [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method.</span></span> <span data-ttu-id="37f0e-127">您可以使用 pack 物件來加入、移除或取代套件的成員。</span><span class="sxs-lookup"><span data-stu-id="37f0e-127">With a pack object, you can add, remove, or replace the members of a pack.</span></span> <span data-ttu-id="37f0e-128">當您將磁片物件新增至套件時，VDS 會初始化磁片來解除所有現有磁片區的系結。</span><span class="sxs-lookup"><span data-stu-id="37f0e-128">When you add a disk object to a pack, VDS initializes a disk to unbind all existing volumes.</span></span> <span data-ttu-id="37f0e-129">相反地，在將所有系結詳細資料加入套件時，LUN 都會保留所有的系結詳細資料。</span><span class="sxs-lookup"><span data-stu-id="37f0e-129">In contrast, a LUN retains all binding details when it is added to a pack.</span></span> <span data-ttu-id="37f0e-130">如果您從套件中移除最後一個磁片，當呼叫端釋出物件的最後一個參考時，VDS 會刪除套件物件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-130">If you remove the last disk from a pack, VDS deletes the pack object when the caller releases the last reference to the object.</span></span>

<span data-ttu-id="37f0e-131">物件屬性包括物件識別碼、名稱、套件狀態和旗標。</span><span class="sxs-lookup"><span data-stu-id="37f0e-131">Object properties include an object identifier, a name, pack status, and flags.</span></span> <span data-ttu-id="37f0e-132">線上套件適用于設定和使用，無法使用離線套件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-132">An online pack is available for configuration and use, an offline pack is unavailable.</span></span> <span data-ttu-id="37f0e-133">VDS 支援任意數量的線上與離線套件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-133">VDS supports any number of online and offline packs.</span></span>

<span data-ttu-id="37f0e-134">**Windows Server 2003：** 一次只支援一個線上套件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-134">**Windows Server 2003:** Supports only one online pack at a time.</span></span>

<span data-ttu-id="37f0e-135">VDS 會強制執行套件內的線上磁碟仲裁。</span><span class="sxs-lookup"><span data-stu-id="37f0e-135">VDS enforces a quorum of online disks within a pack.</span></span> <span data-ttu-id="37f0e-136">仲裁會判斷套件是否可具有線上狀態，並防止多部主機將線上狀態授與相同的套件。</span><span class="sxs-lookup"><span data-stu-id="37f0e-136">The quorum determines whether a pack can have an online status, and prevents multiple hosts from granting an online status to the same pack.</span></span> <span data-ttu-id="37f0e-137">如果套件中的線上磁片數目落在仲裁 (n/2 + 1) ，則 VDS 會讓線上套件離線。</span><span class="sxs-lookup"><span data-stu-id="37f0e-137">If the number of online disks in a pack falls below the quorum (n/2 + 1), VDS takes the online pack offline.</span></span>

<span data-ttu-id="37f0e-138">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="37f0e-138">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="37f0e-139">類型</span><span class="sxs-lookup"><span data-stu-id="37f0e-139">Type</span></span>                                              | <span data-ttu-id="37f0e-140">元素</span><span class="sxs-lookup"><span data-stu-id="37f0e-140">Element</span></span>                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f0e-141">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="37f0e-141">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="37f0e-142">[**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack)和 [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* 。</span><span class="sxs-lookup"><span data-stu-id="37f0e-142">[**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) and [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2)\*.</span></span>                                     |
| <span data-ttu-id="37f0e-143">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="37f0e-143">Associated enumerations</span></span>                           | <span data-ttu-id="37f0e-144">[**VDS \_套件 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) 標和 [**VDS \_ PACK \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_pack_status)。</span><span class="sxs-lookup"><span data-stu-id="37f0e-144">[**VDS\_PACK\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) and [**VDS\_PACK\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).</span></span>             |
| <span data-ttu-id="37f0e-145">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="37f0e-145">Associated structures</span></span>                             | <span data-ttu-id="37f0e-146">[**VDS \_套件 \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) 的元件和 [**VDS \_ 套件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)。</span><span class="sxs-lookup"><span data-stu-id="37f0e-146">[**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) and [**VDS\_PACK\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification).</span></span> |



 

<span data-ttu-id="37f0e-147">**\* Windows Server 2003：** 在 windows Vista 之前，不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="37f0e-147">**\*Windows Server 2003:** This interface is not supported until Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37f0e-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="37f0e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f0e-149">軟體提供者物件</span><span class="sxs-lookup"><span data-stu-id="37f0e-149">Software Provider Objects</span></span>](software-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="37f0e-150">LUN 物件</span><span class="sxs-lookup"><span data-stu-id="37f0e-150">LUN Object</span></span>](lun-object.md)
</dt> <dt>

[<span data-ttu-id="37f0e-151">**IVdsLun**</span><span class="sxs-lookup"><span data-stu-id="37f0e-151">**IVdsLun**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[<span data-ttu-id="37f0e-152">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="37f0e-152">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
