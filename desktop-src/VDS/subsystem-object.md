---
description: 子系統物件
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: 子系統物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104560629"
---
# <a name="subsystem-object"></a><span data-ttu-id="859fb-103">子系統物件</span><span class="sxs-lookup"><span data-stu-id="859fb-103">Subsystem Object</span></span>

<span data-ttu-id="859fb-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="859fb-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="859fb-105">子系統物件會建立儲存子系統的模型。</span><span class="sxs-lookup"><span data-stu-id="859fb-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="859fb-106">子系統可以是 RAID 主機殼或 PCI RAID 卡。</span><span class="sxs-lookup"><span data-stu-id="859fb-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="859fb-107">單一主機電腦可以連接至任意數目的子系統。</span><span class="sxs-lookup"><span data-stu-id="859fb-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="859fb-108">每個子系統只會由一個硬體提供者管理。</span><span class="sxs-lookup"><span data-stu-id="859fb-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="859fb-109">在 SAN 設定中，子系統類別代表 SAN 存放裝置主機殼。</span><span class="sxs-lookup"><span data-stu-id="859fb-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="859fb-110">子系統可以包含任意數目的控制器和磁片磁碟機，而且可以 (遮罩，) 任意數量的 Lun 寫入執行硬體提供者的電腦。</span><span class="sxs-lookup"><span data-stu-id="859fb-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="859fb-111">較高階的子系統可以取消遮罩 Lun 給網路上的其他電腦。</span><span class="sxs-lookup"><span data-stu-id="859fb-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="859fb-112">子系統內的每個磁片磁碟機都會連接至匯流排，並佔用匯流排中的插槽。</span><span class="sxs-lookup"><span data-stu-id="859fb-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="859fb-113">子系統內的每個控制器都有一或多個控制器埠。</span><span class="sxs-lookup"><span data-stu-id="859fb-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="859fb-114">下圖顯示子系統中包含的實體裝置 (Lun 不會顯示) 和它們之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="859fb-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![此圖表會顯示從左側的「埠」開始、移至「控制器」，然後將「插槽」指向個別「磁片磁碟機」的「匯流排」。](images/vdssubsystem.png)

<span data-ttu-id="859fb-116">VDS 應用程式使用 [**IVdsHwProvider：： QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) 方法來查詢屬於特定硬體提供者的子系統。</span><span class="sxs-lookup"><span data-stu-id="859fb-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="859fb-117">呼叫端可以從 **QuerySubSystems** 方法所傳回的列舉中選取所需的子系統物件，以取得特定子系統的指標。</span><span class="sxs-lookup"><span data-stu-id="859fb-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="859fb-118">使用子系統物件，您可以設定子系統狀態、建立 Lun、更換磁片磁碟機，以及查詢控制器、磁片磁碟機和 Lun。</span><span class="sxs-lookup"><span data-stu-id="859fb-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="859fb-119">除了物件識別碼、名稱和序號之外，子系統物件屬性還包括子系統狀態、健全狀況和旗標;控制器、插槽和匯流排的計數;以及重建優先權設定。</span><span class="sxs-lookup"><span data-stu-id="859fb-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="859fb-120">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="859fb-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="859fb-121">類型</span><span class="sxs-lookup"><span data-stu-id="859fb-121">Type</span></span>                                                                                      | <span data-ttu-id="859fb-122">元素</span><span class="sxs-lookup"><span data-stu-id="859fb-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="859fb-123">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="859fb-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="859fb-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)。</span><span class="sxs-lookup"><span data-stu-id="859fb-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="859fb-125">只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="859fb-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="859fb-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) 和 [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget)。</span><span class="sxs-lookup"><span data-stu-id="859fb-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="859fb-127">此物件可能公開的介面</span><span class="sxs-lookup"><span data-stu-id="859fb-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="859fb-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) 和 [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)。</span><span class="sxs-lookup"><span data-stu-id="859fb-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="859fb-129">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="859fb-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="859fb-130">[**VDS \_SUB \_ system \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) 標和 [**VDS \_ sub \_ system \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status)。</span><span class="sxs-lookup"><span data-stu-id="859fb-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="859fb-131">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="859fb-131">Associated structures</span></span>                                                                     | <span data-ttu-id="859fb-132">[**VDS \_子 \_ 系統的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) 和 [**VDS \_ 子 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification)。</span><span class="sxs-lookup"><span data-stu-id="859fb-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="859fb-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="859fb-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="859fb-134">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="859fb-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="859fb-135">**IVdsHwProvider::QuerySubSystems**</span><span class="sxs-lookup"><span data-stu-id="859fb-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
