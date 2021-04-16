---
description: 控制器物件
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: 控制器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104558854"
---
# <a name="controller-object"></a><span data-ttu-id="e40f4-103">控制器物件</span><span class="sxs-lookup"><span data-stu-id="e40f4-103">Controller Object</span></span>

<span data-ttu-id="e40f4-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="e40f4-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e40f4-105">控制器物件會在子系統中建立控制器的模型。</span><span class="sxs-lookup"><span data-stu-id="e40f4-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="e40f4-106">控制器是由子系統所包含，而每個控制器都有一或多個控制器埠，可供主機電腦用來寫入和讀取 Lun。</span><span class="sxs-lookup"><span data-stu-id="e40f4-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="e40f4-107">單一控制器可同時設為作用中的一個 LUN，而其他則為非使用中。</span><span class="sxs-lookup"><span data-stu-id="e40f4-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="e40f4-108">作用中的指定 LUN 的控制器，負責處理 LUN 的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="e40f4-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="e40f4-109">下圖說明這個概念。</span><span class="sxs-lookup"><span data-stu-id="e40f4-109">The following figure illustrates this idea.</span></span>

![此圖顯示左邊有作用中 LUN 的「控制器」，以及右邊的兩個作用中 Lun。](images/vdscontroller.png)

<span data-ttu-id="e40f4-111">**VDS 1.0：** 子系統的每個控制器都會設定為 [作用中] 或 [非使用中]，而不是與子系統所呈現的每個 Lun 相關。</span><span class="sxs-lookup"><span data-stu-id="e40f4-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="e40f4-112">VDS 應用程式會使用 [**IVdsSubSystem：： QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) 方法來判斷特定子系統所包含的控制器。</span><span class="sxs-lookup"><span data-stu-id="e40f4-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="e40f4-113">呼叫端可以從 **QueryControllers** 方法所傳回的列舉中選取所需的控制器物件，以取得特定控制器的指標。</span><span class="sxs-lookup"><span data-stu-id="e40f4-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="e40f4-114">使用控制器物件時，呼叫端可以設定控制器狀態、查詢其相關聯的 Lun、查詢其控制器埠，以及排清和使快取失效。</span><span class="sxs-lookup"><span data-stu-id="e40f4-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="e40f4-115">除了物件識別碼、名稱和序號之外，控制器物件屬性還包括控制器狀態和健全狀況，以及埠的計數。</span><span class="sxs-lookup"><span data-stu-id="e40f4-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="e40f4-116">下表列出相關的介面、列舉和結構。</span><span class="sxs-lookup"><span data-stu-id="e40f4-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="e40f4-117">類型</span><span class="sxs-lookup"><span data-stu-id="e40f4-117">Type</span></span>                                                                                              | <span data-ttu-id="e40f4-118">元素</span><span class="sxs-lookup"><span data-stu-id="e40f4-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e40f4-119">一律由這個物件公開的介面</span><span class="sxs-lookup"><span data-stu-id="e40f4-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="e40f4-120">**IVdsController**</span><span class="sxs-lookup"><span data-stu-id="e40f4-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="e40f4-121">只有在 VDS 1.1 和2.0 光纖通道提供者中，此物件一律公開的介面</span><span class="sxs-lookup"><span data-stu-id="e40f4-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="e40f4-122">**IVdsControllerControllerPort**</span><span class="sxs-lookup"><span data-stu-id="e40f4-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="e40f4-123">此物件可能公開的介面</span><span class="sxs-lookup"><span data-stu-id="e40f4-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="e40f4-124">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="e40f4-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="e40f4-125">相關聯的列舉</span><span class="sxs-lookup"><span data-stu-id="e40f4-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="e40f4-126">[**VDS \_控制器 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_controller_status)。</span><span class="sxs-lookup"><span data-stu-id="e40f4-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="e40f4-127">相關聯的結構</span><span class="sxs-lookup"><span data-stu-id="e40f4-127">Associated structures</span></span>                                                                             | <span data-ttu-id="e40f4-128">[**VDS \_控制器 \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) 的和 [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)。</span><span class="sxs-lookup"><span data-stu-id="e40f4-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e40f4-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e40f4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40f4-130">硬體提供者物件</span><span class="sxs-lookup"><span data-stu-id="e40f4-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="e40f4-131">**IVdsSubSystem::QueryControllers**</span><span class="sxs-lookup"><span data-stu-id="e40f4-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
